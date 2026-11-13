# Living PRD

> Module 4 · Production Specs. Refactor for readability; extract a living PRD that stays true as the build evolves.

## Problem

_What user problem does this solve? Tie to the validated hypothesis._

The hub sorts accessibility content by source (standards, news, checklists), not by the job people come to do. So practitioners skim it once, leave, and accessibility gets checked late, at QA or audit, instead of in the story.Hypothesis under test (role-first): if the hub opens on "what's your role?" and answers with the requirements that apply to that role, the deadline, and one action to do this sprint, then more people will act on it and come back.
Status: designed, not yet validated. The clickable prototype (control vs role-first treatment) and the moderated test plan exist. No sessions have run. Every baseline below is a placeholder from the brief, to be replaced with measured numbers.
Measure
Baseline (placeholder)
Target (placeholder)
Bounce on first visit
[80%]
Lower than control
Participants who pick a role and click the recommended action
—
[70%]
Return within 14 days
[2%]
[5%]
Time to find the requirement for their role
[90 seconds]
Under [15] seconds
Clicks before reaching a requirement
[7]
Fewer than control
Stories with accessibility criteria by [Q3]
[50%]
Higher (not measured in the test)
Accessibility defects found late per release
[10]
Lower (not measured in the test)
Kill switch: if fewer than [X%] of participants pick a role and click the action, or time to requirement doesn't beat the control, drop role-first and test task-based entry next. The [X%] threshold is still to be set.
Why now: the Accessible Canada Regulations' digital amendments (registered 5 Dec 2025) set dates of 5 Dec 2027 and 5 Dec 2028, and the Canada Post Accessibility Plan 2026–2028 commits to moving from 67% to 97% of products tested with people with disabilities.

## Users & jobs

- **Primary user:** Primary user: practitioners on Design & Engineering product teams, meaning developers, product designers and product owners. They are mid-sprint, on a story or component, and have minutes, not an afternoon. Secondary users: QA testers, procurement, and team leads. Each has a role card in the picker, but in the prototype their views are stubs.Role What they need from the hub View in prototype View in hub Developer Criteria for the component, code pattern, test to run Full Full Product designer Criteria for the screen, annotation pattern, contrast and target size Full (EN/FR) Full Product owner Acceptance criteria to paste into the story, deadline Full Full QA tester Test steps and tools per criterion Stub Full Procurement Contract and conformance-report language (EN 301 549) Stub Full Team lead Deadlines and what the team must do by when Stub Full
- **Job to be done:** Job to be done: "When I'm working on a story or component, show me which accessibility requirements apply to my role, by when, and one concrete thing I can do this sprint, so I can build it in now and not fix it after audit."

## Scope

- **In:** In scope
• Role picker as the hub's default route (#role): six Mercury cards, one per role, in English and French
• A role view per role: applicable criteria tagged with WCAG 2.2 and EN 301 549 references, ACA deadlines with live day counts
• "Do this now" (one action, copyable text, mark as done) and "Do this next"
• Return visit ("Welcome back"): last action, what's new for the role since the last visit, with loading, empty and error states
• EN/FR switch on the role page, change role, link through to full requirements
• Resource library opens filtered to the chosen role
• The existing hub sections (Overview, News, Standards, Platforms, Checklists, Testing, Research, Trends, Resources), unchanged in content
- **Out (explicitly):** Out of scope (this release)
• Sign-in, and a profile that follows the user across devices or browsers
• An analytics pipeline; no event leaves the browser
• A live "what's new" feed; items come from the static news file
• Native-speaker review of the French copy
• WCAG 3, and task-based entry (the fallback if role-first fails)
• Hosting inside SharePoint pages; the build is a static site linked from SharePoint

## Requirements

| # | Requirement | Priority | Acceptance criteria |
|---|---|---|---|
| 1 | Role picker is the first screen for anyone without a saved role | MUST | Opening the hub with no profile lands on #role. Six cards show in a 3×2 grid, or one column on narrow screens. Each card's accessible name is the role name plus its one-line description. |
| 2 | Picking a role opens that role's view | MUST | One click or Enter or Space opens the view. Focus moves to the view's heading. The role is saved to the profile. role_picked is logged. |
| 3 | Role view lists only the criteria that apply to the role | MUST | Each criterion shows its WCAG number and is tagged "WCAG 2.1 · required", "WCAG 2.2 · our target" or "EN 301 549 · required". Opening a criterion logs requirement_opened. |
| 4 | Deadlines are shown with a live day count | MUST | 5 Dec 2027 and 5 Dec 2028 show with days left, counted from today. No date or figure appears without a source. |
| 5 | "Do this now" offers exactly one action with text to copy | MUST | One primary button. Copy puts the role's text (test, acceptance criteria, annotations, contract clause) on the clipboard and confirms in a polite live region. Mark as done saves to the profile. do_now_click, copied and action_done are logged. |
| 6 | "Do this next" appears after the first action | P1 | Shown under "Do this now" with a link to full requirements. Done state saves separately. do_next_click and next_action_done are logged. |
| 7 | Return visit opens "Welcome back" | MUST | A new browser session with a saved role shows the welcome screen. It shows the last action as done (with date) or not finished, and "Not your role? Change it". |
| 8 | What's new for the role, since the last visit | P1 | Lists news items dated after prevVisit whose topic matches the role. Newest first. |
| 9 | Loading, empty and error states on What's new | MUST | Loading: skeleton rows, announced politely. Empty: "Nothing new for {role plural} since your last visit on {date}. Your next step is below." Error: "We couldn't load what's new for your role. Your requirements and next step are still below." with a Try again button. The error is announced politely and logs load_failed. Retry logs retry. |
| 10 | English and French | MUST | The switch changes every string on the role page with no reload. Lang attribute updates. Choice is saved. French dates don't end in a double full stop. language_switch is logged. |
| 11 | Meets WCAG 2.2 AA (EN 301 549 for WCAG 2.1 AA) | MUST | Text contrast at least 4.5:1, UI at least 3:1. Targets at least 44 px. Visible focus on every control. Works by keyboard only. Skip link moves focus without changing the route. Screen reader check in English and French. |
| 12 | Mercury look | P1 | TMercury colours, Roboto, 4 px spacing scale, 4 px corners, Mercury card pattern on the picker. Light theme only. |
| 13 | Resource library opens filtered to the user's role | P1 | After a role is picked, Resources opens on that role's filter. Counts per role are correct. |
| 14 | Storage never breaks the page | MUST | If localStorage or sessionStorage is blocked, the page still renders as a first visit and nothing throws. |
| 15 | Usage events reach a real analytics store | P2 | The events in Data & events are sent to the chosen analytics tool with role and language, and no personal data. Not built. |
| 16 | Profile follows the user across devices | P2 | Role and actions come back after signing in on another device. Not built. |

## Data & events

_What gets stored, what gets tracked._

Today, events exist only in the prototype's on-screen moderator log, for one session. The hub collects nothing. Every metric in Problem needs an analytics source before it can be measured outside moderated sessions.Events (prototype)
Event
Fires when
Feeds
screen_view
Any screen shows
Time to requirement, funnel
role_picked
A role card is chosen
Role + action rate
requirement_opened / requirement_closed
A criterion is expanded or collapsed
Time to requirement
do_now_click
The "Do this now" button is used
Role + action rate (primary)
copied
Action text is copied
Action depth
action_done
"Do this now" is marked done
Action completion
do_next_click / next_action_done
"Do this next" is used or marked done
Action completion
view_requirements
"See everything that applies to you" is used
Depth
language_switch
EN/FR is changed
FR usage
change_role / back
Role is changed, or user goes back to the picker
Picker clarity
resume_last_action
An unfinished action is resumed on return
Return value
load_failed / retry
What's new fails to load, or Try again is used
Reliability
bounce / exit
User leaves without a click, or leaves after clicks
Bounce
nav_click, tile_click, checklist_opened
Control board only: menu, tile or checklist used
Control comparison
bounce and load_failed are passive. They never count as the first click.
Metric definitions
• Role + action rate: sessions with role_picked and then do_now_click, divided by all sessions.
• Time to requirement: time from the first screen_view to the first requirement_opened.
• Clicks to requirement: clicks before the first requirement_opened.
• Bounce: sessions whose only event is the first screen_view, then bounce.
• 14-day return: profiles with a second session within 14 days of the first. Needs a real analytics source; local storage can't report it.
Stored data (hub, per browser, no personal data)
Key
Where
Holds
abd-profile
localStorage
role, lang, actions {do, next} with done dates, lastVisit, prevVisit
abd-visit
sessionStorage
Marks the current session, so a new one moves lastVisit to prevVisit
abd-role
localStorage
Resource library role filter
abd-checks
localStorage
Checklist ticks
abd-tab
localStorage
Last platform tab
Content sources: role content and copy in src/data/roles.js. What's new comes from src/data/news.js, matched by RA_TOPIC. Both are static files edited by hand.

## Open questions

Open questions
[ ] Which ACA date applies to Canada Post's web products: 5 Dec 2027 or 5 Dec 2028? Confirm with Legal and the Accessibility office.
[ ] What are the real baselines for bounce, clicks, time to requirement, return rate, stories with criteria and late defects?
[ ] What is the [X%] kill threshold for the role + action rate?
[ ] Which analytics source will measure bounce and 14-day return (SharePoint usage analytics, or a tool on the static host)?
[ ] Who are the moderated test participants, and how many per role? We need real quotes to replace the bracketed placeholders.
[ ] Who will review the French copy, and by when?
[ ] Where will the hub be hosted: an internal static host linked from SharePoint, or an SPFx web part?
[ ] Is a cross-device profile (sign-in) worth building, or is a per-browser profile enough?
[ ] Who owns "what's new", and should it become a live feed instead of a hand-edited news file?
[ ] Which stub roles (QA, Procurement, Team lead) should get full prototype views before testing, if any?
