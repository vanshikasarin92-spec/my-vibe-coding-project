[Skip to content](#main)

Design & Engineering · Digital accessibility hub

# Accessible by Default

ACA standard: CAN/ASC-EN 301 549:2024 Build target: WCAG 2.2 AA Web · iOS · Android Updated 3 Nov 2026

- [Start here 01](#start)
- [Latest news 02](#news)
- [Standards & law 03](#standards)
- [Web & mobile guides 04](#platforms)
- [Checklists 05](#checklists)
- [Testing & tools 06](#testing)
- [Research & data 07](#research)
- [Trends 08](#trends)
- [Resource library 09](#resources)

Not legal advice. Confirm which obligations apply to a product with Legal and the Accessibility office.

## Everything Design and Engineering need to ship accessible products

Standards, the Accessible Canada Act, platform guidance, checklists, tools and research for websites, iOS and Android apps, kept in one place and dated so you know how current it is.

What we build to

Every new feature conforms to CAN/ASC-EN 301 549, with web and app content built to WCAG 2.2 AA.

The Accessible Canada Act's digital regulations require conformance with CAN/ASC-EN 301 549:2024. That edition uses WCAG 2.1 AA for web content and adds requirements for software, video players, documentation and support. WCAG 2.2 AA contains all of 2.1 AA plus six newer criteria, so building to 2.2 AA meets the WCAG part of the Canadian standard and keeps us ready for its next edition.

The four principles (POUR)

**Perceivable**Text alternatives, captions, contrast, content that adapts to text size.

**Operable**Keyboard, switch and voice access, enough time, no seizure triggers, big enough targets.

**Understandable**Readable language, predictable behaviour, clear errors and help.

**Robust**Correct names, roles and states for assistive technology.

### The state of things, 2026

5 Dec 2027First Accessible Canada Act digital deadline: new and updated web pages for the federal public sectorAccessible Canada Regulations, amended Dec 2025

5 Dec 2028Mobile apps, documents and procurement checks for the public sector and large businessesESDC summary of the amendments

95.9%of the top 1M home pages had detectable WCAG failuresWebAIM Million, Feb 2026

56.1average detectable errors per home page, up 10.1%WebAIM Million, Feb 2026

### Jump to

[**Accessible Canada Act**What the 2025 digital regulations require, by when, and how they relate to WCAG 2.2.Standards & law →](#standards) [**Resources for your role**Filter the library for designers, product managers, product owners, developers, QA or procurement.Resource library →](#resources) [**Platform guides**Design and build must-haves for web, iOS (UIKit, SwiftUI) and Android (Views, Compose).Web & mobile guides →](#platforms) [**Release checklists**Designer, engineer and pre-release checklists, including the EN 301 549 items WCAG doesn't cover.Checklists →](#checklists) [**What changed recently**Dated news with a line on what each item means for our team.Latest news →](#news) [**How to test**Automated scanners, screen readers and the manual passes they can't replace.Testing & tools →](#testing)

## Latest news

The developments from the past year that change how we design, build or test. Newest first.

1. 2 Sep 2026

   Standards

   ### EN 301 549 V4.1.1 published: Europe moves to WCAG 2.2 AA

   ETSI, CEN and CENELEC published the new version of Europe's ICT accessibility standard. Web content, documents and software clauses now reference WCAG 2.2 AA instead of 2.1, real-time communication requirements were rewritten, and new annexes map the standard to the European Accessibility Act. Deque reports it is on track to be cited in the EU Official Journal around 30 November 2026.

   **For us:** Canada's adopted edition is still CAN/ASC-EN 301 549:2024, based on EN 301 549:2021 (V3.2.1) and WCAG 2.1. Accessibility Standards Canada says it follows the international review cycle but hasn't announced a date to adopt V4.1.1. Building to WCAG 2.2 AA now avoids rework when it does.

   Sources: [National Disability Authority](https://nda.ie/news/en301549-published) · [Deque](https://www.deque.com/blog/en-301-549-v4-1-1-is-final-what-changed-what-it-means-and-what-you-should-do/) · [Accessibility Standards Canada](https://accessible.canada.ca/en-301-549-accessibility-requirements-ict-products-and-services-1)
2. Sep 2026

   Standards

   ### New WCAG 3 Working Draft opens for review

   W3C published another WCAG 3 Working Draft in September, following the March 2026 draft. WCAG 3 is still a draft: it replaces pass/fail success criteria with more granular requirements and a Bronze/Silver/Gold conformance model. W3C says WCAG 2 will not be deprecated for several years after WCAG 3 is final.

   **For us:** read it, don't build to it. No law or procurement rule, including the ACA's, references WCAG 3.

   Sources: [W3C WAI announcement](https://lists.w3.org/Archives/Public/public-wai-announce/2026JulSep/0001.html) · [WCAG 3 Introduction](https://www.w3.org/WAI/standards-guidelines/wcag/wcag3-intro/)
3. 16 Sep 2026

   Research

   ### AI speeds up building faster than it speeds up accessibility testing

   Level Access's eighth State of Digital Accessibility report found about 80% of accessibility professionals now use AI, but only around 30% say it has helped their QA and testing. Applause's 2026 report found 78% of organisations use AI for accessibility work, with 90% combining it with manual testing.

   **For us:** AI-generated UI still needs manual keyboard and screen reader passes. Treat AI output like a new contributor's pull request.

   Sources: [Level Access](https://www.levelaccess.com/news/press-releases-news/level-access-research-finds-broad-ai-adoption-isnt-closing-the-accessibility-gap/) · [Applause report coverage](https://digiworld.news/news/72472/enhancing-digital-accessibility-through-ai-insights-from-applauses-2026-report)
4. 8 Jul 2026

   Other law & enforcement

   ### US digital accessibility lawsuits on pace for a record year

   UsableNet's midyear report projects about 6,176 website and app lawsuits in the US in 2026, nearly 20% above 2025. About two in three website suits target companies under $50M in revenue, and app lawsuits are a growing share.

   **For us:** relevant for any product sold into the US. Checkout, sign-in and account flows are the usual targets.

   Sources: [Stacker (UsableNet and Seyfarth data)](https://stacker.com/stories/small-business/website-accessibility-lawsuits-are-rising-and-smaller-businesses-are)
5. 28 Jun 2026

   Other law & enforcement

   ### European Accessibility Act turns one; enforcement is ramping up

   The EAA has been enforceable since 28 June 2025. National authorities are building audit capacity: Italy's AGID introduced a two-stage model in May 2026, and the first enforcement actions were injunctions filed against retailers in France in November 2025.

   **For us:** applies only to products and services offered to consumers in the EU.

   Sources: [Taylor Wessing](https://www.taylorwessing.com/en/insights-and-events/insights/2026/06/the-eaa-and-bfsg-recap-and-update) · [Level Access](https://www.levelaccess.com/blog/eaa-compliance-in-2026-how-enforcement-has-evolved-and-what-to-expect-next/)
6. 16 Jun 2026

   Mobile platforms

   ### Android 17 ships with accessibility API restrictions and large-screen changes

   Android 17 (API level 37) blocks apps that aren't genuine accessibility tools from using the Accessibility API under Advanced Protection Mode. Apps targeting API 37 can no longer lock orientation or disable resizing on large screens.

   **For us:** test layouts in landscape and on tablets and foldables at large font sizes.

   Sources: [Google I/O 2026](https://io.google/2026/explore/technical-session-5) · [Techlomedia](https://techlomedia.in/2026/06/google-rolls-out-android-17-focusing-on-ai-productivity-and-privacy-124732/)
7. 19 May 2026

   Mobile platforms

   ### Apple previews AI-powered accessibility features for its 27 releases

   Apple announced Apple Intelligence upgrades to VoiceOver, Magnifier, Voice Control (including natural-language commands) and Accessibility Reader, plus generated subtitles and power wheelchair control with Apple Vision Pro.

   **For us:** AI image descriptions don't replace our own labels. Voice Control works best when visible labels match accessible names.

   Sources: [Apple Newsroom](https://www.apple.com/newsroom/2026/05/apple-unveils-new-accessibility-features-and-updates-with-apple-intelligence/)
8. May 2026

   Mobile platforms

   ### Apple pushes developers to prepare Accessibility Nutrition Labels

   App Store product pages show which accessibility features an app supports. A feature can only be claimed if users can complete all of the app's common tasks with it. Labels are optional today; Apple says they will become required for new apps and updates.

   **For us:** the same common-task audit feeds the ACA mobile app conformity assessment due in December 2028.

   Sources: [App Store Connect Help](https://developer.apple.com/help/app-store-connect/manage-app-accessibility/overview-of-accessibility-nutrition-labels)
9. 20 Apr 2026

   Other law & enforcement

   ### US DOJ extends ADA Title II web and app deadlines by one year

   US state and local governments now have until 26 April 2027 (population 50,000+) or 26 April 2028 to meet WCAG 2.1 AA for web content and mobile apps.

   **For us:** relevant only to products sold to US public entities.

   Sources: [Federal Register](https://www.federalregister.gov/documents/2026/04/20/2026-07663/extension-of-compliance-dates-for-nondiscrimination-on-the-basis-of-disability-accessibility-of-web)
10. Feb 2026

    Research

    ### WebAIM Million 2026: the web got less accessible

    95.9% of the top million home pages failed, averaging 56.1 errors per page. The most common failures were low-contrast text (83.9% of pages), missing alt text (53.1%), missing form labels (51%), empty links (46.3%) and empty buttons (30.6%). Pages with ARIA averaged 59.1 errors versus 42 without.

    **For us:** the top five failures are all catchable in design review and automated CI. More ARIA is not better ARIA.

    Source: [WebAIM Million](https://webaim.org/projects/million/)
11. 5 Dec 2025

    Canada

    ### Digital accessibility rules added to the Accessible Canada Regulations

    The federal government registered amendments to the Accessible Canada Regulations covering web pages, mobile apps, digital documents, procurement and training. They require conformance with CAN/ASC-EN 301 549, phased in from 5 December 2027 for the federal public sector and 5 December 2028 for federally regulated businesses with 100 or more employees. Organisations must also publish accessibility statements, update them annually and keep records for four years.

    **For us:** this is the rule that turns CAN/ASC-EN 301 549 from a voluntary standard into a requirement. See the Accessible Canada Act panel in Standards & law for the full timeline.

    Sources: [ESDC summary](https://www.canada.ca/en/employment-social-development/programs/accessible-canada/regulations-summary-act/amendment.html) · [Blakes](https://www.blakes.com/insights/federal-government-finalizes-new-digital-technologies-accessibility-regulations/) · [Deque](https://www.deque.com/blog/the-accessible-canada-act-deadlines-are-closer-than-you-think)

## Standards, laws and requirements

Technical standards say *how* to make something accessible. Laws and regulations say *who must*. In Canada, the federal law points to CAN/ASC-EN 301 549, which in turn points to WCAG.

Canada

### Accessible Canada Act: what applies to digital products

Checked against the ESDC summary of the regulations, Accessibility Standards Canada and legal commentary on 3 November 2026.

The law**Accessible Canada Act (2019)**

Covers federally regulated entities, including federal Crown corporations. Requires an accessibility plan updated every three years, a public feedback process and annual progress reports.

The digital rules**Accessible Canada Regulations, amended Dec 2025**

Registered 5 December 2025. Require web pages, mobile apps and digital documents to conform to CAN/ASC-EN 301 549, plus accessibility statements, procurement checks and staff training.

The standard**CAN/ASC-EN 301 549:2024**

Published May 2024 by Accessibility Standards Canada. An identical adoption of EN 301 549:2021 (V3.2.1), which uses WCAG 2.1 Level A and AA for web, documents and software, plus non-WCAG clauses.

#### Fact check: is WCAG 2.2 the ACA standard? No.

- The standard the regulations reference is CAN/ASC-EN 301 549. Its current edition reflects **WCAG 2.1**, not 2.2.
- WCAG 2.2 AA is our **build target**. It includes every WCAG 2.1 AA criterion, so meeting it satisfies the WCAG portion of the Canadian standard.
- Meeting WCAG 2.2 AA alone does **not** satisfy CAN/ASC-EN 301 549. The standard also covers software and user preferences (clause 11), video caption and audio description controls (clause 7), two-way voice and real-time text (clause 6), and documentation and support services (clause 12).
- Europe's EN 301 549 V4.1.1 (September 2026) moved to WCAG 2.2. Accessibility Standards Canada has not announced when, or whether, it will adopt that edition.

#### Digital compliance timeline

| Deadline | Requirement | Federal public sector | Large business (500+) | Medium business (100–499) |
| --- | --- | --- | --- | --- |
| 5 Dec 2027 | New and updated web pages conform; website accessibility statement | Yes | — | — |
| 5 Dec 2027 | Digital accessibility training for relevant employees | Yes | Yes | Yes |
| 5 Dec 2028 | New and updated web pages conform | Already due | Yes | Yes |
| 5 Dec 2028 | New mobile apps conform; existing public-facing apps assessed | Yes | Yes | — |
| 5 Dec 2028 | New and updated digital documents (such as PDFs) conform | Yes | Yes | — |
| 5 Dec 2028 | Checks on purchased apps and web pages | Yes | Yes | — |
| 5 Dec 2028 | Accessibility statement covers websites, apps and documents | Yes | Yes | — |

Ongoing: update accessibility statements annually, refresh training every 3 years, keep records for 4 years. Exempt: heritage content, user-generated content and internal collaboration platforms. Where conformance isn't feasible, provide alternative access. ESDC classes these violations as minor, with penalties of $250 to $75,000. Businesses with 99 or fewer employees are not covered.

#### Canada Post's Accessibility Plan 2026–2028

- New public-facing digital products must meet WCAG 2.1 Level AA; a strategy for the additional WCAG 2.2 requirements is in development.
- Usability testing with people with disabilities covers 67% of digital products, with a target of 97% by 2028.
- Accessible procurement guidelines were due to be finalised in early 2026. Internal software that doesn't meet WCAG 2.1 AA must be fixed within 24 months of contract signature.
- More than 170 employees and contractors have been trained in digital accessibility testing.

Source: [Accessibility Plan 2026 (PDF)](https://www.canadapost-postescanada.ca/cpc/doc/en/aboutus/corporate-responsibility/accessibility-plan-2026.pdf) · [Plans and progress reports](https://www.canadapost-postescanada.ca/cpc/en/our-company/accessibility/accessibility-plan-and-annual-progress-reports.page)

#### Which deadline applies?

Canada Post describes itself as a federal Crown corporation. The regulations include certain Crown corporations in the federal public sector, whose web deadline is December 2027, a year ahead of businesses. Canada Post published its first plan on 16 December 2022, which matches the government-entity timeline. Confirm the applicable category with the Accessibility office before planning to the 2028 date.

Accessibility feedback: accessibility@canadapost.ca · accessibilite@postescanada.ca

All standards and requirements, status as of November 2026

| Requirement | What it is | Status | Technical bar | Applies to |
| --- | --- | --- | --- | --- |
| [Accessible Canada Act](https://laws-lois.justice.gc.ca/eng/acts/A-0.6/) | Federal law for barrier-free federal jurisdiction. | In force since 2019 | Plans, feedback process, progress reports | Federal public sector, Crown corporations, federally regulated businesses |
| [Accessible Canada Regulations (digital)](https://www.canada.ca/en/employment-social-development/programs/accessible-canada/regulations-summary-act/amendment.html) | Digital technologies amendments registered 5 Dec 2025. | Deadlines Dec 2027 / Dec 2028 | CAN/ASC-EN 301 549 | Web, mobile apps, documents, procurement, training |
| [CAN/ASC-EN 301 549:2024](https://accessible.canada.ca/en-301-549-accessibility-requirements-ict-products-and-services-1) | National Standard of Canada; identical to EN 301 549:2021 (V3.2.1). | Current edition | WCAG 2.1 A and AA plus non-web clauses | Required through the regulations above; voluntary on its own |
| [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | W3C guidelines; also ISO/IEC 40500:2025. | Current W3C standard | Level AA (our build target) | Exceeds the WCAG 2.1 baseline in the Canadian standard |
| [WCAG 3](https://www.w3.org/WAI/standards-guidelines/wcag/wcag3-intro/) | Next-generation guidelines with Bronze/Silver/Gold conformance. | Working Draft | Not usable for conformance | Planning only |
| [EN 301 549 V4.1.1](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/04.01.01_60/en_301549v040101p.pdf) | European edition published Sep 2026. | Not adopted in Canada | WCAG 2.2 AA plus extra clauses | EU (EAA, public procurement) |
| [AODA (Ontario)](https://www.ontario.ca/page/how-make-websites-accessible) | Provincial Integrated Accessibility Standards. | In force | WCAG 2.0 AA (large organisations) | Provincially regulated organisations in Ontario; federal entities fall under the ACA |
| [European Accessibility Act](https://eur-lex.europa.eu/eli/dir/2019/882/oj) | EU Directive 2019/882. | Enforced since 28 Jun 2025 | EN 301 549 | Products and services offered to EU consumers |
| [ADA Title II rule (US)](https://www.ada.gov/resources/2024-03-08-web-rule/) | DOJ rule for US state and local governments. | Deadlines Apr 2027 / Apr 2028 | WCAG 2.1 AA | US public entities and their vendors |
| [Section 508 (US)](https://www.section508.gov/) | US federal procurement standard. | In force | WCAG 2.0 AA | Products sold to US federal agencies |
| [Apple Accessibility Nutrition Labels](https://developer.apple.com/help/app-store-connect/manage-app-accessibility/overview-of-accessibility-nutrition-labels) | App Store disclosure of supported features. | Optional; will become required | All common tasks completable per feature | Every App Store app |

Orientation, not legal advice. Coverage depends on the organisation's category under the ACA, where products are sold and to whom. Confirm with Legal and the Accessibility office before making conformance claims.

### What WCAG 2.2 added over 2.1

These six criteria are in our build target but not yet in the WCAG 2.1 baseline of CAN/ASC-EN 301 549:2024. Canada Post's 2026–2028 plan lists a WCAG 2.2 strategy as in progress.

2.4.11 · AA**Focus Not Obscured (Minimum)**

A focused element isn't entirely hidden by sticky headers, cookie banners or chat widgets.

2.5.7 · AA**Dragging Movements**

Anything done by dragging has a single-pointer alternative such as tap or buttons.

2.5.8 · AA**Target Size (Minimum)**

Pointer targets are at least 24 × 24 CSS px, or spaced so a 24 px circle doesn't overlap a neighbour.

3.2.6 · A**Consistent Help**

Help options (contact, chat, FAQ) appear in the same relative place across pages.

3.3.7 · A**Redundant Entry**

Don't ask for the same information twice in one process; auto-fill it or let users select it.

3.3.8 · AA**Accessible Authentication (Minimum)**

No memory or puzzle tests to sign in unless there's an alternative. Allow paste and password managers.

### Minimum touch target sizes across platforms

| Source | Minimum | Unit | Type |
| --- | --- | --- | --- |
| WCAG 2.2 · 2.5.8 (AA) | 24 × 24 | CSS px | Requirement |
| WCAG 2.2 · 2.5.5 (AAA) | 44 × 44 | CSS px | Enhanced requirement |
| Apple Human Interface Guidelines | 44 × 44 | pt | Platform guidance |
| Android / Material Design | 48 × 48 | dp | Platform guidance |

Our rule: design to the platform guidance (44 pt / 48 dp, 44 px on touch web) and treat 24 px as the floor.

## Web and mobile guides

The same WCAG outcomes, implemented with each platform's own APIs and assistive technology. Test in both English and French wherever the product ships in both.

### Design

- Text contrast 4.5:1 (3:1 for large text); UI component and focus indicator contrast 3:1.
- Design a visible focus state for every interactive component, not just links.
- Layouts reflow at 320 CSS px wide (400% zoom) without two-direction scrolling.
- Never use colour alone to show state, errors or chart series.
- Annotate heading levels, landmarks, reading order and accessible names in handoff files.
- Allow for French text running about a third longer than English in buttons and labels.

### Build

- Native HTML first: `<button>`, `<a href>`, `<label>`, `<fieldset>`. Add ARIA only when no native element exists.
- Every input has a programmatic label; errors are linked with `aria-describedby` and announced.
- Manage focus on route changes, modals and deleted items.
- Set `lang="en"` or `lang="fr"` on `<html>`, and on any passage in the other language.
- Respect `prefers-reduced-motion` and `prefers-contrast`; don't disable zoom.
- Status messages use a polite live region.

#### Key APIs and references

`aria-label``aria-describedby``aria-live``aria-expanded``inert``<dialog>``:focus-visible``lang`

[ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/) · [MDN Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility) · [How to Meet WCAG](https://www.w3.org/WAI/WCAG22/quickref/) · [Mercury design system](https://design.canadapost-postescanada.ca/en/mercury/home.page)

#### Test with

axe or Lighthouse in CI · keyboard only · NVDA + Firefox or Chrome · JAWS + Chrome · VoiceOver + Safari · 200% text and 400% zoom · screen reader set to French for French pages

### Design

- Support Dynamic Type through the accessibility sizes; layouts must stack or scroll, not truncate.
- 44 × 44 pt minimum hit areas, even when the visible icon is smaller.
- Check designs in Dark Mode, Increase Contrast, Bold Text and Reduce Transparency.
- Provide alternatives to custom gestures and avoid gestures that conflict with VoiceOver.
- Specify VoiceOver labels, hints and grouping in specs, in both languages.

### Build

- Set `accessibilityLabel`, `accessibilityValue` and traits for custom controls.
- SwiftUI: `.accessibilityElement(children: .combine)`, `.accessibilityAction`, `.accessibilityHeading`.
- Use text styles so Dynamic Type works; adapt layout at accessibility sizes.
- Honour Reduce Motion and post announcements with `AccessibilityNotification`.
- Localise accessibility labels and hints along with visible strings.
- Match visible text and accessible names so Voice Control commands work.

#### Key APIs and references

`accessibilityLabel``accessibilityTraits``accessibilityCustomActions``accessibilityRotor``performAccessibilityAudit()`

[Apple Developer: Accessibility](https://developer.apple.com/accessibility/) · [HIG: Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) · [Accessibility Nutrition Labels](https://developer.apple.com/help/app-store-connect/manage-app-accessibility/overview-of-accessibility-nutrition-labels)

#### Test with

Accessibility Inspector · XCUITest `performAccessibilityAudit()` in CI · VoiceOver in English and French · Voice Control · Switch Control · largest Dynamic Type size · Full Keyboard Access on iPad

### Design

- 48 × 48 dp minimum touch targets with at least 8 dp between them.
- Specify text in sp and design for 200% font scale.
- Design for landscape, tablets and foldables: apps targeting API 37 can't lock orientation on large screens.
- Check designs with dark theme, high-contrast text and colour correction.
- Specify TalkBack labels, grouping and custom actions in handoff, in both languages.

### Build

- Views: set `contentDescription`; mark decorative images `importantForAccessibility="no"`.
- Compose: `Modifier.semantics`, `mergeDescendants = true`, `heading()`, `stateDescription`.
- Add `customActions` instead of relying on swipe or long-press alone.
- Announce changes with `liveRegion`.
- Support keyboard, D-pad and Switch Access focus order.
- Don't use the Accessibility Service API for non-accessibility features.

#### Key APIs and references

`contentDescription``Modifier.semantics``mergeDescendants``stateDescription``AccessibilityChecks.enable()`

[Android Developers: Accessibility](https://developer.android.com/guide/topics/ui/accessibility) · [Compose accessibility](https://developer.android.com/develop/ui/compose/accessibility) · [Material 3](https://m3.material.io/foundations/designing/overview)

#### Test with

Accessibility Scanner · Espresso `AccessibilityChecks` in CI · TalkBack in English and French · Voice Access · Switch Access · maximum display and font size

## Checklists

One pass per feature. Ticks are saved only in your browser.

References in grey are **WCAG 2.2** success criteria, our build target. References in red are **CAN/ASC-EN 301 549** clauses that go beyond WCAG; the ACA regulations require these too.

### Designer

- [ ] Text and icon contrast checked 1.4.3 · 1.4.11
- [ ] Focus state designed for every interactive component 2.4.7 · 2.4.11
- [ ] Targets meet 44 pt / 48 dp; never under 24 px 2.5.8
- [ ] Colour isn't the only way state or meaning is shown 1.4.1
- [ ] Layouts tested at 200% text and 320 px width 1.4.4 · 1.4.10
- [ ] Headings, landmarks and reading order annotated 1.3.1 · 2.4.6
- [ ] Accessible names written for icon-only controls, in both languages 4.1.2
- [ ] Error messages say what went wrong and how to fix it 3.3.1 · 3.3.3
- [ ] Drag interactions have a tap or button alternative 2.5.7
- [ ] Motion is optional and respects reduced-motion settings 2.3.3

### Engineer

- [ ] Native elements and platform controls used first 4.1.2
- [ ] Every control has a correct name, role, value and state 4.1.2
- [ ] Full task works with keyboard or switch, in logical order 2.1.1 · 2.4.3
- [ ] Focus moved and restored on dialogs, navigation and deletes 2.4.3
- [ ] Form inputs labelled; errors linked and announced 1.3.1 · 3.3.1
- [ ] Status updates use live regions or announcements 4.1.3
- [ ] Text scales with Dynamic Type, sp or browser zoom 1.4.4
- [ ] Page and passage language set correctly 3.1.1 · 3.1.2
- [ ] Sign-in allows paste and password managers 3.3.8
- [ ] Software honours platform accessibility settings EN 11.7

### Before release

- [ ] Core tasks completed with a screen reader on each platform
- [ ] Core tasks completed with keyboard only
- [ ] Core tasks completed with Voice Control or Voice Access
- [ ] Checked at the largest text size and in landscape
- [ ] Tested in English and French where the product ships in both
- [ ] Videos captioned; players expose caption and audio description controls 1.2.2 · EN 7.3
- [ ] Help, documentation and support channels are accessible EN 12
- [ ] PDFs and other documents checked EN 10
- [ ] Known issues logged with WCAG or EN clause and severity
- [ ] Accessibility statement and App Store labels still accurate

## Testing and tools

Automated scanners find a portion of issues quickly. Keyboard, screen reader and zoom passes find the rest. Usability testing with disabled people finds what neither catches.

Recommended toolkit

| Tool | Platform | Used by | Best for |
| --- | --- | --- | --- |
| [Stark](https://www.getstark.co/) | Figma | Design | Contrast, colour-blindness simulation, focus order and annotations |
| [Colour Contrast Analyser](https://www.tpgi.com/color-contrast-checker/) | Desktop | Design, QA | Sampling real rendered colours from any screen |
| [axe-core / axe DevTools](https://www.deque.com/axe/) | Web | Engineering, QA | Browser extension and CI integration |
| [Accessibility Insights](https://accessibilityinsights.io/) | Web, Windows | Engineering, QA | Guided manual assessment with tab-stop visualisation |
| [WAVE](https://wave.webaim.org/) | Web | Everyone | Visual, in-page view of errors and structure |
| [Lighthouse](https://developer.chrome.com/docs/lighthouse/) | Web | Engineering | Quick checks in DevTools |
| [Accessibility Inspector + XCUITest audits](https://developer.apple.com/accessibility/) | iOS, macOS | Engineering | Inspecting labels and traits; automated audits in UI tests |
| [Accessibility Scanner](https://play.google.com/store/apps/details?id=com.google.android.apps.accessibility.auditor) | Android | QA, Design | On-device suggestions for targets, contrast and labels |
| [Espresso Accessibility Checks](https://developer.android.com/training/testing/espresso/accessibility-checking) | Android | Engineering | Failing UI tests on violations in CI |
| [NVDA](https://www.nvaccess.org/) · JAWS · VoiceOver · TalkBack | All | Engineering, QA | Real screen reader behaviour, in English and French |

### Shift left

Accessibility annotations in Figma, linting in the IDE, automated checks on every pull request. Fixing a missing label in design takes minutes; after launch it's a ticket and a release.

### Five-minute manual pass

Tab through the feature. Turn on the screen reader and complete the main task without looking. Zoom to 200% or set the largest text. Toggle reduced motion and dark mode.

### Test with disabled users

Canada Post's plan targets usability testing with people with disabilities on 97% of digital products by 2028. Include screen reader, magnification, voice control and cognitive-disability participants.

### Avoid overlays

Overlay widgets don't fix source code. The US FTC ordered accessiBe to pay $1 million in 2025 over its compliance marketing claims, and more than 1,000 practitioners have signed the Overlay Fact Sheet.

[Overlay Fact Sheet](https://overlayfactsheet.com/)

## Research and data

Studies and datasets to cite in roadmaps, design reviews and business cases. Check the date on each before quoting it.

Web · Feb 2026

### [The WebAIM Million 2026](https://webaim.org/projects/million/)

95.9% of home pages failing

Annual automated scan of the top million home pages. First regression in years: average errors per page rose to 56.1.

Industry · Sep 2026

### [Level Access: State of Digital Accessibility](https://www.levelaccess.com/news/press-releases-news/level-access-research-finds-broad-ai-adoption-isnt-closing-the-accessibility-gap/)

\~80% of practitioners use AI

Only about 30% say AI has helped QA and testing, so build speed is outpacing verification.

Canada · 2026–2028

### [Canada Post Accessibility Plan](https://www.canadapost-postescanada.ca/cpc/doc/en/aboutus/corporate-responsibility/accessibility-plan-2026.pdf)

67% → 97% tested with disabled users

Commitments on digital products, procurement and training, with a reported digital accessibility score of 93.3%.

Apps & web · 2026

### [Applause: State of Digital Quality in Accessibility](https://digiworld.news/news/72472/enhancing-digital-accessibility-through-ai-insights-from-applauses-2026-report)

78% use AI; 90% pair it with manual tests

Only 10% of organisations rely exclusively on AI for accessibility testing.

Population · WHO

### [WHO: Disability and health](https://www.who.int/news-room/fact-sheets/detail/disability-and-health)

1.3 billion people, about 1 in 6

Global estimate of people living with significant disability.

Users · WebAIM

### [WebAIM Screen Reader User Survey](https://webaim.org/projects/screenreadersurvey10/)

How screen reader users navigate

Screen reader and browser combinations, mobile vs desktop use, and how people find content.

## Trends to plan for

What's shifting in 2026 and 2027, and what each shift asks of Design and Engineering.

### Canada's digital rules now have dates

Signal

The December 2025 amendments set deadlines in December 2027 and 2028 for web pages, apps, documents, procurement, training and accessibility statements.

Our response

Build a conformity assessment and statement process now, and plan legacy app assessments well before 2028.

### WCAG 2.2 leads, Canada's standard follows

Signal

Europe's EN 301 549 V4.1.1 moved to WCAG 2.2 in September 2026. Canada's edition still uses WCAG 2.1, with no adoption date announced for the update.

Our response

Keep building to WCAG 2.2 AA and track the six new criteria separately, so reports can show both the ACA baseline and our target.

### AI builds UI faster than teams can verify it

Signal

WebAIM linked rising errors to faster building; Level Access found AI rarely improves QA.

Our response

Put accessibility rules in coding-assistant instructions, component libraries and CI gates. Keep human screen reader passes.

### Procurement becomes an accessibility gate

Signal

From December 2028 the public sector and large businesses must check purchased apps and web pages; Canada Post's plan adds accessible procurement guidelines.

Our response

Ask vendors for conformance reports against EN 301 549, not WCAG alone, and write remediation timelines into contracts.

### App stores make accessibility visible

Signal

Apple's Accessibility Nutrition Labels appear on product pages and will become mandatory.

Our response

Audit each common task per feature; reuse the evidence for ACA app assessments.

### WCAG 3 and cognitive accessibility

Signal

WCAG 3 drafts put more weight on cognitive needs, plain language and predictable UI.

Our response

No conformance work yet. Start with plain-language reviews in both official languages and fewer steps in key flows.

## Resource library

Primary sources first, then practitioner guides. Pick your role to see what's most useful for your work, then narrow by keyword.

Show resources for

Filter by keyword

Maintained for the Design & Engineering teams. Content current to 3 November 2026; every news item links its source. This hub is guidance, not legal advice.

Body text #333333 on white: 12.6:1 Secondary text #666666: 5.7:1 Links #0467C6: 5.6:1 Red #CA261A with white: 5.5:1