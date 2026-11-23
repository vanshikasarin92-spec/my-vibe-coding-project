# My Vibe-Coded Product

_Product School · Vibe Coding Certification · Final Project Showcase_

**Live product:** https://vanshikasarin92-spec.github.io/my-vibe-coding-project-website/#role

## The Problem & Hypothesis

**Problem.** The hub sorts accessibility content by source (standards, news, checklists), not by the job people come to do. So practitioners skim it once, leave, and accessibility gets checked late, at QA or audit, instead of in the story.Hypothesis under test (role-first): if the hub opens on "what's your role?" and answers with the requirements that apply to that role, the deadline, and one action to do this sprint, then more people will act on it and come back.
Status: designed, not yet validated. The clickable prototype (control vs role-first treatment) and the moderated test plan exist. No sessions have run. Every baseline below is a placeholder from the brief, to be replaced with measured numbers.

Kill switch: if fewer than [X%] of participants pick a role and click the action, or time to requirement doesn't beat the control, drop role-first and test task-based entry next. The [X%] threshold is still to be set.
Why now: the Accessible Canada Regulations' digital amendments (registered 5 Dec 2025) set dates of 5 Dec 2027 and 5 Dec 2028, and the Canada Post Accessibility Plan 2026–2028 commits to moving from 67% to 97% of products tested with people with disabilities.

**Hypothesis.** > We believe **a first screen that asks "What's your role?" and answers with three things — what applies to you, by when, and one thing to do this sprint —** will cause **people to use the hub while they're doing the work (pick a role, act on "Do this now", come back) instead of reading it once** for **designers, developers, product owners, QA analysts and procurement in Design & Engineering**. We'll know we're right when **[70%] of first visits end with a role picked and "Do this now" clicked, 14-day return rises from [0% as is new metric] to [5%], and time to find the requirement for a task drops from [90 seconds] to under [15] seconds.**

## The Evidence

Module 6 · Evals & Iteration. Read the analytics, run an iteration sprint, present with evidence.

## Data Signal → The One Fix

| Change | Hypothesis | Result |
| Copy as ticket, a checklist for each role, live "What's new" | Putting "Do this now" into tickets and pull requests gives a reason to return (14-day return from 0% to 5%) | Shipped 19 Nov and verified live. No users yet, so the result is unknown |

## The Recommendation

**Verdict: ITERATE, keep refining.**

**Decision:** ☐ Go ☑ Iterate ☐ Kill

Track the three criteria, and exclude the team's own visits.
Run a timed task test with 2–3 people from each of the 5 roles, on the old hub and on this one.
Ask each person whether they already knew the requirement. That tests your riskiest assumption: prioritization, not findability.
Decide Go or Kill on 4 December, when the first 14-day window closes.

## My Story, Friction · Learning · Aha

- **Demo link:** https://vanshikasarin92-spec.github.io/my-vibe-coding-project-website/
- **The one-sentence story:** Accessibility guidance was organized by standard, so teams read it once and went back to guessing. Accessible by Default asks "What's your role?" and answers with what applies, by when, and one thing to do this sprint, in a form you can paste straight into your ticket.
- **Where it landed on the Confidence Line (M2 → now):** "can we build it?" has moved up a lot; "will people use it?" hasn't moved. M2 rested on the problem framing alone. Now the solution is built, stress-tested and instrumented, so confidence that it works and can be measured is high. Confidence that it changes behaviour is unchanged, because no real users have tried it yet.

---
_Built across six modules with an AI build tool, then iterated from live product data. Hosted on GitHub Pages._
