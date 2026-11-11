# PROMPTS.md: Living Prompt Pack

> Module 3 · Prompt Chaining. Re-architect the build with prompt chains; capture the reusable ones here.

## How to use this pack

_Each prompt is a reusable step. Chain them: the output of one becomes the input to the next._

## Prompt chain: [name your flow]

### Step 1: Expand: add the two missing screens
```
Create a screen with a full Product designer view, in English and French. It follows the developer and product owner pattern, with its own “Do this now” action and confirmation.
Create a  returning-visit screen. It opens straight on the person’s role and shows last time’s action, the next action, and what’s changed. A moderator can trigger it from the log once a role is picked, or a session can start on it from the board’s settings.
```

### Step 2: Behavior: handle loading, empty and error states
```
Apply the following logic constraints to the Return-visit screen ("Welcome back"): the screen a person sees when they open the hub again after picking a role. It carries the return metric (14-day return, [2%] → [5%]). flow:
- Use skeleton screens for the "New in the hub for your role": the requirements, guidance and deadlines added or changed for this person's role since their last visit, loaded for each person along with their last action. loading state.
- If no data is present, show the empty state: ""Nothing new for product designers since your last visit on 27 Oct. Your next step is below." FR : « Rien de nouveau pour le design de produits depuis votre dernière visite le 27 oct. Votre prochaine étape est ci-dessous. » (The section heading stays visible. The role name and date fill in automatically. "Do this next" and the countdown still show.)".
- On fetch failure, trigger the error state: ""We couldn't load what's new for your role. Your requirements and next step are still below." [Try again] FR : « Impossible de charger les nouveautés pour votre rôle. Vos exigences et votre prochaine étape sont toujours ci-dessous. » [Réessayer] (Shown where the list would be. The rest of the page stays usable. Screen readers announce it politely. Logged as load_failed in the moderator log.)".

Maintain the same design language throughout and tether all behavior strictly to these rules.
```

### Step 3: Refine: polish one thing on one screen
```
The Role picker: the first screen of the treatment ("What's your role?"). It decides the primary metric: role picked, then "Do this now" clicked. needs a professional Mercury (Canada Post's design system), as used across the hub: white background, red #CA261A for the brand strip and primary actions, blue #0467C6 for links and selection, greys #111111–#F0F0F0, Roboto, 4px spacing steps, 4px corners. Take the layout pattern, not the brand: no logo or corporate name. polish.
1. Start by listing the 3 biggest gaps in typography and spacing compared to Mercury design system home page: https://design.canadapost-postescanada.ca/en/mercury/home.page Compare its card grid: short title, one supporting line, a clear arrow, equal card heights and plenty of white space..
2. Once you've identified those, resize the headers and update the The six role cards. - Today each card stacks a name, a blurb, a placeholder quote, the label "Placeholder quote: replace with a verbatim interview quote", and "See what applies to you →". That's five lines per card, 30 across the grid, and the repeated placeholder label is the loudest text on the screen. - Update to match the Mercury card pattern:   · Role name (19px bold) and a one-line blurb, then a right-aligned arrow   · The quote moves to a single quiet line under the blurb; the placeholder label shows once above the grid, not on every card   · Equal card heights in a 3 × 2 grid (one column on phones), a blue border and tint on hover, and a visible 2px blue focus ring   · The whole card stays one button with a 44px minimum height, so keyboard and screen reader users hear "Developer, Web, iOS and Android code" and nothing more to match.

Don't change anything else in the project or touch the underlying logic.
```

## Reusable techniques learned

- Build only the screens that prove or break the hypothesis: control, treatment, the action's end screen and a test plan.
- Keep each earlier version on its own canvas page instead of overwriting it, so the hypotheses can be compared.
- Put a moderator log in the prototype so bounce, first click, time to requirement and action clicks are visible as they happen.
- Keep a whole flow in one artboard when its log has to follow the person across screens.
- Fact-check every published figure against its primary source before it goes on screen.
- Show unmeasured numbers and unconfirmed quotes as visible [placeholders], never as invented values.
- Calculate time-sensitive values live (the deadline countdown) instead of hard-coding them.
- Give every section that loads data a loading, empty and error state, and keep the rest of the page usable when it fails.
- Make an empty or error message's promises true in the layout ("your next step is below" means it is below).
- Store bilingual text as data, mark quoted text with its own language, and handle French spacing and punctuation.

## What broke (and the fix)

_Where a single mega-prompt failed and chaining fixed it._

Leaving via "Back to SharePoint" counted as a first click, so a bounce looked like engagement → excluded bounce, exit and load_failed from first-click timing.
The placeholder label was the loudest text on the role picker, repeated on all six cards → showed it once above the grid.
The grid's column count varied with screen width and could leave orphan cards → fixed 3 × 2 grid, one column on phones.
The return screen offered "Finish it now" and "Do this next" for the same action → one "Do this next" card.
The error message said "still below" while the requirements link sat in the side column → moved the link under "Do this next".
The return-visit test didn't actually reload the page (only the hash changed) → reran it with a real reload.
The first prompt had no screenshot and an empty content list → built with real published data and said what was missing.

