# Validation Brief

> Module 2 · Validation. Frame the riskiest assumption, then build to test it. **This locks your scenario, no switching after M2.**

## Scenario

Digital Accessibility Hub for Design & Engineering (own product)

## Riskiest assumption

_The one belief that, if false, sinks the idea._

The data is all there, but users can't find the insight, so they bounce.

People don't use the hub because it's organized by source (WCAG, EN 301 549, ACA, guides), not by job. They can't tell what applies to their role and their current task, so they read it once and go back to guessing, and accessibility gets checked at the end of a release instead of built in. If they already know what applies and just don't prioritize it, reorganizing the hub won't change anything.

## Hypothesis

> > We believe **a first screen that asks "What's your role?" and answers with three things — what applies to you, by when, and one thing to do this sprint —** will cause **people to use the hub while they're doing the work (pick a role, act on "Do this now", come back) instead of reading it once** for **designers, developers, product owners, QA analysts and procurement in Design & Engineering**. We'll know we're right when **[70%] of first visits end with a role picked and "Do this now" clicked, 14-day return rises from [0% as is new metric] to [5%], and time to find the requirement for a task drops from [90 seconds] to under [15] seconds.**


## Risk type

- [x] Value (do they want it?)
- [x] Usability (can they use it?)
- [ ] Feasibility (can we build it?)
- [ ] Viability (should we?)

## Kill switch

_The result that would make you stop or pivot._

- If people pick a role but fewer than [10%] click "Do this now", or finding the requirement isn't faster than on the current home page, role isn't the right way in. Pivot to task-based entry ("I'm building a form", "I'm buying a vendor tool").

- If people pick roles inconsistently or say "I'm two of these", the roles don't match how teams work. Pivot to task-based entry.

- If role + action works in moderated sessions but 14-day return stays at [lower than 5%] in the live pilot, the hub helps once but isn't a working tool. Pivot to putting the guidance where the work happens: Jira story templates, PR templates and CI checks, with the hub as the reference behind them.

## The three ingredients

- **Real data (domain metrics):** - *Our measurements (placeholders until measured)*
    - [80%] bounce rate on the hub home: sessions under 15s with no click (SharePoint analytics)
    - [7] clicks to reach the checklist for your role from the home page
    - [50%] of user stories in [Q3] with accessibility acceptance criteria (Jira)
    - [10] open accessibility defects found after release vs. before (last [YEAR])
- **User voice (verbatim quotes):**  -
- "[I don't know which WCAG criteria apply to a component]", Developer
  - "[I am finding out about accessibility issues only at QA]", Product designer
  - "[I don't know what "done" means for accessibility in a story]", Product owner
  - "[I don't know the test method
- **Hypothesis (above):** ✓
