# Full-Stack: Data, Access Rules, Edge Cases, Deploy

> Module 5 · Full-Stack. Add data schemas, access rules, and edge cases; stress-test and deploy.

## Deployed link

_The working, shareable link that survives real users._

https://vanshikasarin92-spec.github.io/my-vibe-coding-project-website/#role

## Data schema

| Entity | Key fields | Notes |
|---|---|---|
| invites | id, sender_id, sender_email, recipient_email, status (pending / accepted / cancelled), created_at, responded_at | The database sets the sender, sender email, status and time from the session. Recipient emails are lowercased and checked by a regex. Each sender can have only one active invite per recipient. The dashboard figures come from invite_metrics(). |
| profiles + checklist_ticks | id / user_id (= auth.uid()), role, lang, item_id, done, client_updated_at | A profile is created automatically at sign-up. Last-write-wins: a trigger keeps whichever edit was made latest and limits future-dated clocks to now + 5 min. |

## Access rules

_Who can see / do what? Where are the auth boundaries?_

Content tables (news, resources, roles, checklists) are read-only for everyone, signed in or not; there are no write policies, so the browser can’t edit them. Everything a person creates (profile, checklist ticks, completed actions, visits, events) has row-level security: (select auth.uid()) = user_id, so people can only read and write their own rows. Invites: the sender sees the ones they sent; the recipient sees the ones addressed to their signed-in email. Nobody can update or delete an invite directly; it can only be cancelled through cancel_invite() (sender, pending only) or accepted through accept_my_invites() (recipient, on sign-in). The functions run as security definer with an empty search path, and anonymous users can’t call them. The dashboard returns hub-wide totals with no names or emails, plus the caller’s own counts. The auth boundary is Supabase Auth email sign-up and login; the browser only ever holds the publishable key, never the service-role key.

## Edge cases hardened

| Case | Before | After |
|---|---|---|
| Empty / first-run state | Lists rendered blank with no guidance. A new person saw an empty Checklists or Invites area and a blank gap while sign-in loaded. | Skeletons while loading. Empty states explain what goes there and have a “Get Started” button: pick a role, open the checklist, or jump to the invite email field. Signed-out pages point to Sign in. |
| Bad / malicious input | Checks were only in the browser and data was hardcoded, so a crafted request could fake a sender, invite themselves, send duplicates or push a future timestamp. | The server enforces the rules. An email regex check constraint, a trigger that overwrites the sender from the session, a self-invite block, and a unique index stop duplicates. Clocks are capped at now + 5 min. RLS rejects any other person’s rows, and status changes only happen through guarded functions. |
| Failure / offline | A slow or failed request hung on a spinner or left a blank screen. Simultaneous edits overwrote each other at random. | 8-second timeout, then an inline error with a Retry button that returns focus to the section heading. Progress stays saved on the device and syncs on return. Last-write-wins for simultaneous edits, and first-change-wins for invite cancel versus accept. |

## Stress test results

_What you threw at it, and what held / broke._

Tested: Claude used deliberately failed and hung requests in automated browser tests. I also tested by hand in Chrome DevTools, with Offline and a custom Hang profile (20-second delay).
Result: Pass after fixes. The hub now acknowledges every disconnection with an inline error and a Retry button.
What broke: A hung connection froze the screen. Going fully Offline already showed an error straight away, because offline requests fail instantly. But a request that never answered left “Sending…” stuck forever. That affected sending invites, logging in and saving progress.
Checking a saved sign-in could load forever, if the network hung while the session was being refreshed.
Failed saves offered no way to retry. Your role and Checklists said “Couldn’t save” but had no Retry button.
A slow reply looked like a failure. You found this one with the Hang profile. The invite had actually been saved, but the reply came after the hub stopped waiting. So Retry said “You have already invited this address.”

How we fixed it:

One shared timeout: every request now goes through it. After 8 seconds the request is cancelled and you get an inline error with Retry. This covers loading pages, the sign-in check, logging in, sending and cancelling invites, and saving progress.
Retry buttons on every save that can fail, and the email you typed stays in the field.
A retry that finds the invite already saved now says “Invite saved… your first try got through”, not the “already invited” error.

Retest:
Claude Automated: 22/22 browser checks pass. My manual Hang test: “Couldn’t reach the server…” with Retry appeared after about 8 seconds 
2. Spam Click (and Ghost User)
Spam Click: does 5× submit create duplicates?
Result:  It held the line. Claude checked by counting rows in the live database.
What broke: double-clicking Cancel sent two requests. The second wrongly showed “Couldn’t cancel. It may already be accepted,” even though the cancel had worked.

How we fixed it: every submit and cancel button now accepts one click at a time while its request is in flight. Behind that, the database refuses a second active invite to the same address, and ticks and completed actions are stored one row per item. Even a request that slipped past the button lock couldn’t create a duplicate.
Ghost User: does a brand-new account hit a dead end?
Result:  The pages pass; sign-up was blocked, and that’s now fixed.
What broke:

Sign-up was blocked. Supabase’s built-in email sender only emails members of your Supabase team, about 2 an hour, so real new users couldn’t sign up.
The error was vague. The hub showed “Something went wrong.”
How we fixed it:

Specific messages: sign-up errors now say why, such as an address refused, the email not sent, or too many attempts.
Settings: I turned off Confirm email to unblock sign-up. I set up a Gmail sender so Confirm email can go back on.

