# Engineering Handoff Note

> Module 4 · Production Specs. Open the black box, make the build legible to an engineer.

## What this is

_One paragraph an engineer can read in 60 seconds._

Accessible by Default is a static React 18 + Vite 5 site that tells Design & Engineering practitioners which accessibility requirements apply to their role, by when, and one thing to do this sprint. There is no backend: all content ships as JavaScript modules in each feature's data/ folder, and the only state is a per-browser profile in localStorage. The code is grouped by feature (src/features/your-role, news, resource-library, and so on), with data, pure logic, React state and display kept in separate folders, and 11 unit tests cover the logic. It builds and behaves correctly, but it is a working prototype, not a product: no analytics, no sign-in, no CI, no deploy target chosen, and the role-first hypothesis it serves has not been tested with users yet. Start by running it (last section), then read src/features/your-role/YourRole.jsx, which wires the main flow; the Living PRD has the requirements and what is mocked.

## Architecture (plain language)

- **Frontend:** Frontend • React 18.3.1, Vite 5.4.11, no router library. src/App.jsx maps the URL hash (#role, #news, #resources, …) to a feature page; #role is the default. On a page change, focus moves to the new page's heading. • Ten features under src/features/, one per menu item: your-role, overview, news, standards, platforms, checklists, testing, research, trends, resource-library. • Layers in each feature: data/ (content only, no imports) → logic/ (pure functions, unit-tested) → hooks/ (React state and storage) → screens/, components/ and the page file (JSX only). • Shared code in src/shared/: page frame (Layout, Footer), RichText (renders a small inline markup in data strings: backticks, bold, links), date and routing logic, storage and clipboard helpers, and the Mercury styles (tokens.css, app.css). • Your role is the only stateful feature. YourRole.jsx holds which screen is showing; each PRD screen is a component in screens/: RolePicker, RoleView, DoThisNow, DoThisNext, ActionDone, WelcomeBack.
- **Backend / data:** Backend and data • There is no backend, API or database. Content is JavaScript in each feature's data/ folder (largest: your-role/data/roles.js, about 1,100 lines of English and French). Changing content means editing a file and redeploying. • The only user data is in the browser, read and written through src/shared/lib/storage.js, which never throws: Key Storage Holds abd-profile localStorage Role, language, when each action was done, lastVisit, prevVisit abd-visit sessionStorage Marks the current browser session so a visit is counted once abd-role localStorage Resource library role filter abd-checks localStorage Checklist ticks abd-tab localStorage Last platform tab • No data leaves the browser. No analytics, no cookies, no network calls apart from Google Fonts (Roboto).
- **Key flows:** Key flows
1.  First visit. No profile → Role picker. Picking a role saves the profile, sets the library filter to that role, and opens Role view.
2.  Act. Role view's card offers "Do this now" → steps and text to copy → mark done (saved with a timestamp) → Action done. Next time the card offers "Do this next", then "all done".
3.  Return visit. A new browser session moves lastVisit to prevVisit (logic/profile.js). A prevVisit opens Welcome back, which shows what was done, What's new (news items dated after prevVisit whose topic maps to the role, from features/news/data/news.js), and the next action.
4.  Language. The EN/FR switch re-renders every Your role string from roles.js and saves the choice. The other nine pages are English only.
5.  Library. Resource library reads abd-role, so it opens filtered to the role picked in Your role.

## What's solid vs. what's duct tape

| Area | State | Notes |
|---|---|---|
| Layer separation | solid | A script checks every code file's imports: 60 of 60 pass (data imports nothing, logic has no React or storage, display touches no storage or dates). It was tested against injected violations and catches them. |
| Content updates | rough | Hand-edited JS files; "Updated 3 Nov 2026" typed in shared/data/site.js.A CMS or SharePoint list feeding the data/ shape, with a real last-updated date |

## Risks & assumptions for the team

The biggest risk is product, not code: the role-first design is untested with users, so the next build decision should wait for the moderated sessions.

## How to run it

```
You need Node 21 or later (tested on Node 22) and npm. Unzip accessible-by-default-react.zip, then from the a11y-hub folder:
npm install        # React 18.3.1, Vite 5.4.11, @vitejs/plugin-react 4.3.4
npm run dev        # local dev server at http://localhost:5173
npm test           # 11 unit tests across every logic/ folder
npm run build      # static site in dist/
npm run preview    # serve dist/ at http://localhost:4173
To see a return visit: pick a role and mark an action done. Then open a new browser window (a new session), or in DevTools set lastVisit in abd-profile to an earlier date and clear sessionStorage, and reload. To reset: clear the site's storage in DevTools.
To deploy: copy dist/ to any static web server; asset paths are relative, so any folder works. Serve it over HTTPS so copy-to-clipboard works, and link to it from SharePoint until hosting is decided (see Risks).
To check the code: the source inspector shows every file, its imports and its layer check. The project README maps each PRD screen to its component.
```
