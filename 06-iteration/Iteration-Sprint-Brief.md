# Iteration Sprint Brief: Template (Module 6)

> **What this is:** the seven-section structure your `Iteration-Sprint-Brief.md` follows in Module 6. It captures one full loop, **data → AI → one fix → redeploy**: and feeds your `06-iteration/iteration.md` deliverable. Every change in M6 starts with *"based on the data showing…"*.

**Product:** [name]
**Live URL (before):** [link]
**Owner:** [your name]
**Date:** [date]

---

## 1 · Problem & Hypothesis
Pulled straight from your Living PRD, the anchor for everything below.
- **Problem statement:** [the problem this product solves]
- **M2 hypothesis:** *I was testing whether* [X].

## 2 · The Metrics (from your product analytics)
Your live numbers, as **text** (so they paste into the LLM). Narrow to the 3 to 5 signals that map to your problem.
| Metric | Your number | Read |
|---|---|---|
| Visitors / sessions | [#] | [context] |
| Activation (key action) | [%] | [vs. expectation] |
| Retention / return | [%] | … |
| Bounce rate | [%] | [honesty metric] |
| [problem-specific] | [#] | … |

## 3 · Peer Feedback
The structured comments you collected on your live product (qualitative *why* behind the numbers).
- "[verbatim peer comment]", what it points to: [theme]
- "[verbatim peer comment]", what it points to: [theme]
- Recurring theme: [the thing two or more people independently flagged]

## 4 · AI Analysis (ranked backlog)
Output of the strategic prompt (problem + hypothesis + metrics + peer feedback → top 3, ranked by impact).
1. **[Finding 1]**: likely impact: [high/med], rationale: […]
2. **[Finding 2]**: likely impact: [med], rationale: […]
3. **[Finding 3]**: likely impact: [low], rationale: […]

## 5 · The One Finding
The single highest-impact recommendation you chose to act on. Not three. Not the safest.
- **Chosen finding:** [#1 above, restated]
- **Why this one:** [it moves the needle on the problem statement because …]
- **Move type:** [ Persona (rewrite voice) · Branching (swap the mental model) · Guardrail (hard IF/THEN rule) ]

## 6 · Implementation Prompt
The surgical change, exactly as pasted into your build tool.
```
Based on the user data showing [finding], update [specific part] to [specific change]. Keep all existing functionality working.
```
- Tested? [yes/no] · Anything break? [no / re-prompted to fix [regression]]

## 7 · Result & Redeployed URL
What changed and where it now lives.
- **Before → after:** [metric or behaviour you expect to move]
- **Redeployed live URL:** [link]
- **Folded into:** `06-iteration/iteration.md` + redeployed URL in `README.md`

---
*Module 6 · Vibe Coding Certification, the AI provides the synthesis; you provide the conviction. One finding, one change.*
