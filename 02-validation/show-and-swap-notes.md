# Show & Swap Notes

> Module 2 · Validation. Put the prototype in front of a peer. Their reaction is the data.

## What I showed
https://claude.ai/artifact/KNoqZf2bQTk1Zc5F42M7Fw#page-54f6c066aea5


## What my partner understood (in their words)
I think you are testing whether the start screen gets me to do one clear next thing. The log on the right tracks my first click, how long it took, and whether I acted or just wandered. The page itself says it has no single recommended action, so the test looks like: if most people just wander or leave, the current start screen is not working as a front door.


## Where they got confused / pushed back

On the first click. Every link I tried opened the same page saying there is no content in this section yet. After that it felt like a test, not a product. The moderator log stays on screen the whole time, so I am watching myself being measured. One more thing: the top says WCAG 2.2 AA, but the text below says the 2024 standard uses WCAG 2.1 AA. Those two do not match.

## What I'll change as a result

"Every link opened the same 'no content yet' page" → every path now leads to real content. The control screens in the canvas are deliberately thin, since they stand in for the current hub. But the built hub (https://vanshikasarin92-spec.github.io/my-vibe-coding-project-website/) has real content behind all 12 sections, and each role → "Do this now" path ends in a real action: steps, a snippet or criteria to copy, and a ticket to paste into Jira. No click ends on an empty page.

"The moderator log stays on screen, so I'm watching myself being measured" → measuring moved out of sight.
In the test canvas: the log can now be hidden with the showLog setting, so participants run sessions without it. The moderator watches it separately.
In the built hub: no log at all. Usage is recorded in the background and shown on a separate Analytics page that participants never see.
Lesson: a visible test turns a product test into a usability lab, and people act differently.

"The page says it has no single recommended action" gave away the hypothesis → test framing stays off participant screens. My partner described the hypothesis almost word for word, because the screen said what was being tested. Test plans and kill criteria now live in the moderator's materials only, so participants react to the product, not the experiment.
