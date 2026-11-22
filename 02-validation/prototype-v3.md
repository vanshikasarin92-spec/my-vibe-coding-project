# Prototype (v3): The Build That Tests the Hypothesis

> Module 2 · Validation. The prototype is a hypothesis test, not a demo.

## Link

https://claude.ai/artifact/KNoqZf2bQTk1Zc5F42M7Fw#page-b07d61496073

## What it tests

_Tie it back to the validation brief: which assumption does this prototype put in front of a user?_

The riskiest assumption from the validation brief: people don't use the hub because they can't tell what applies to their role and task, not because they don't prioritize accessibility.

How the prototype tests it: it puts the current hub home (A · Control, organized by source) side by side with "What's your role?" (B · Treatment). Each participant gets a real sprint task for their role, and the moderator measures:
whether they pick a role and click "Do this now" (target 70%)
time to name the right requirement (baseline 90s, target under 15s)
whether they click "Do this next" on a simulated return visit, two weeks later (a stand-in for 14-day return)

Kill signals, stated in the test plan:
They pick a role but don't act.
B isn't faster than A.
People say "I'm two of these roles".
_____

## Context injected (no placeholders)

- **Real user quotes on screen:**

Each role card shows a quote, but they're bracketed placeholders, and the screen says "Placeholder quote: replace with a verbatim interview quote." The current text:

Developer: "[I don't know which WCAG criteria apply to a component]"
Product designer: "[I am finding out about accessibility issues only at QA]"
Product owner: "[I don't know what 'done' means for accessibility in a story]"
QA analyst: "[I don't know test method across web, iOS and Android]"
Procurement: "[I don't know what to ask vendors for]"
Lead: "[Add a quote from a leadership interview]"
- **Domain metrics on screen:**

Real and sourced:
ACA deadlines: 5 Dec 2027 for federal public-sector web pages, and 5 Dec 2028 for apps, documents and procurement. The countdown is worked out live from today's date. (Sources: Accessible Canada Regulations, amended Dec 2025; the government's summary of them.)
67% → 97%: digital products usability-tested with people with disabilities, today and by 2028. (Canada Post Accessibility Plan 2026–2028.)
WCAG 2.1 AA is required by CAN/ASC-EN 301 549:2024; the team builds to 2.2 AA.
Control screen only: 95.9% of the top 1 million home pages had WCAG failures, averaging 56.1 errors per page. (WebAIM Million, Feb 2026.)

Still placeholders, shown in dashed yellow in the test plan:
[80%] bounce rate
[7] clicks to reach your role's checklist
[90 seconds] to find a requirement
[2%] 14-day return
[50%] of [Q3] stories with accessibility acceptance criteria

## Iteration log (v1 → v3)

| Version | Change | Why |
|---|---|---|
| v1 | _____ | _____ |
| v2 | _____ | _____ |
| v3 | _____ | _____ |
Version	Change	Why
v1a: Deadline test [(link)](https://claude.ai/artifact/KNoqZf2bQTk1Zc5F42M7Fw#page-deadline)	
Change: First screen leads with one metric (days to 5 Dec 2027), one takeaway and one action ("confirm our deadline"), against the current "Start here" screen with nine possible first clicks.	
why: To test whether one clear action stops decision-makers from bouncing.
v1b: Role-first test [(link)](https://claude.ai/artifact/KNoqZf2bQTk1Zc5F42M7Fw#page-role)	
Change: "What's your role?" → what applies, by when, one "Do this now", against the current hub home organized by source. Includes a moderator log, a simulated return visit and a role-specific test plan.	
Why: The deadline test only reached leads. The real gap was individual contributors not knowing what applies to their role, so the hypothesis moved to role-first.
v2 / v3: Hub build [(link)](https://vanshikasarin92-spec.github.io/my-vibe-coding-project-website/)	
Change: The role-first idea built as a working product: Mercury design system, all six roles in English and French, sign-in with saved progress, Copy as ticket, checklists for each role, and analytics.	
Why: Partner feedback: empty links and a visible log made v1 feel like a test, not a product. The role-first flow needed real content on every path, and a way to be measured with real users.
