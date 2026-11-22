# Iteration: Analytics, Sprint, Final Recommendation

> Module 6 · Evals & Iteration. Read the analytics, run an iteration sprint, present with evidence.

## What the evidence says

_What real usage showed: numbers if your tool has analytics, counted behaviour if it does not. Put the signal that matters on screen._

- **Primary signal:** Primary metric: % of first visits that end with a role picked and "Do this now" clicked. Target 70%. Not yet measurable. It needs actions tracked, not page views, and the only traffic so far is one internal test session.
- **What moved:** Every role flow completes end to end. The internal walkthrough picked a role and finished "Do this now" in all 3 test accounts (procurement, designer, QA).
People land on the role page. "Your role" is the most-viewed page (10 of 37 views), at about 17 seconds per view, which suggests a requirement can be found well under the 90-second baseline. That's a signal from one tester, not proof.
Reliability: the hub now holds up under failure. There are no frozen screens offline or on a hung connection, rapid clicks create no duplicate records, and new users get a clear first step on every screen.
- **What didn't:** No real users. 1 visitor, 1 visit, 37 page views, 0% bounce. That's the builder touring every page on 19 November (evening, Toronto time). Nobody has visited since.
14-day return: not measurable yet. The first 14-day window closes on 4 December.
Time to find a requirement: no timed task test yet, against the old hub or the new one.
Sign-up was blocked for new users until the email setting was fixed. The full email-confirmation path is still untested.

_Analytics snapshot: visitors 1; page views 36; views per visit 36; duration 9m 44 s; bounce 0%._

## Iteration sprint

| Change | Hypothesis | Result |
|---|---|---|
| Copy as ticket, a checklist for each role, live "What's new" | Putting "Do this now" into tickets and pull requests gives a reason to return (14-day return from 0% to 5%) | Shipped 19 Nov and verified live. No users yet, so the result is unknown |

## Peer feedback

1. The colour scheme can be better- remove red colour, 2.  the chips- ACA standard, build target etc. on the header seems interactive but aren't so better to remove them, 3. the sign in flow should be a separate landing screen.

## The recommendation

**Decision:** ☐ Go  ☑ Iterate  ☐ Kill

_The evidence that justifies the call:_

Track the three criteria, and exclude the team's own visits.
Run a timed task test with 2–3 people from each of the 5 roles, on the old hub and on this one.
Ask each person whether they already knew the requirement. That tests your riskiest assumption: prioritization, not findability.
Decide Go or Kill on 4 December, when the first 14-day window closes.

## Final showcase

- **Demo link:** https://vanshikasarin92-spec.github.io/my-vibe-coding-project-website/
- **The one-sentence story:** Accessibility guidance was organized by standard, so teams read it once and went back to guessing. Accessible by Default asks "What's your role?" and answers with what applies, by when, and one thing to do this sprint, in a form you can paste straight into your ticket.
- **Where it landed on the Confidence Line (M2 → now):** "can we build it?" has moved up a lot; "will people use it?" hasn't moved. M2 rested on the problem framing alone. Now the solution is built, stress-tested and instrumented, so confidence that it works and can be measured is high. Confidence that it changes behaviour is unchanged, because no real users have tried it yet.
