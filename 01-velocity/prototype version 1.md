[Skip to content](#main)

Design & Engineering · Digital accessibility hub

# Accessible by Default

Team baseline: WCAG 2.2 AA Web · iOS · Android Updated 3 Nov 2026

- [Start here 01](#start)
- [Latest news 02](#news)
- [Standards & law 03](#standards)
- [Web & mobile guides 04](#platforms)
- [Checklists 05](#checklists)
- [Testing & tools 06](#testing)
- [Research & data 07](#research)
- [Trends 08](#trends)
- [Resource library 09](#resources)

Not legal advice. For questions about whether a law applies to a product, talk to Legal.

## Everything Design and Engineering need to ship accessible products

Standards, laws, platform guidance, checklists, tools and research for websites, iOS and Android apps, kept in one place and dated so you know how current it is.

What we build to

Every new feature meets WCAG 2.2 Level AA on web, iOS and Android before release.

WCAG 2.2 AA is a superset of 2.1 AA, which US law (ADA Title II) and most court settlements reference. Europe's harmonised standard, EN 301 549 V4.1.1, moved to WCAG 2.2 AA in September 2026. Building to 2.2 AA covers both.

The four principles (POUR)

**Perceivable**Text alternatives, captions, contrast, content that adapts to text size.

**Operable**Keyboard, switch and voice access, enough time, no seizure triggers, big enough targets.

**Understandable**Readable language, predictable behaviour, clear errors and help.

**Robust**Correct names, roles and states for assistive technology.

### The state of things, 2026

95.9%of the top 1M home pages had detectable WCAG failuresWebAIM Million, Feb 2026 (up from 94.8%)

56.1average detectable errors per home page, up 10.1%WebAIM Million, Feb 2026

\~6,176US digital accessibility lawsuits projected for 2026UsableNet midyear report, Jul 2026

2major regimes now actively enforced: the EU's EAA and US ADA litigationEAA enforceable since 28 Jun 2025

### Jump to

[**Platform guides**Design and build must-haves for web, iOS (UIKit, SwiftUI) and Android (Views, Compose).Web & mobile guides →](#platforms) [**Release checklists**Designer, engineer and pre-release QA checklists you can tick off per feature.Checklists →](#checklists) [**Which rules apply**WCAG, EN 301 549, EAA, ADA, Section 508, AODA and app store requirements.Standards & law →](#standards) [**What changed recently**Dated news with a line on what each item means for our team.Latest news →](#news) [**How to test**Automated scanners, screen readers and the manual passes they can't replace.Testing & tools →](#testing) [**Evidence for the roadmap**Studies and data to cite when prioritising accessibility work.Research & data →](#research)

## Latest news

The developments from the past year that change how we design, build or test. Newest first.

1. 2 Sep 2026

   Standards

   ### EN 301 549 V4.1.1 published: Europe moves to WCAG 2.2 AA

   ETSI, CEN and CENELEC published the new version of Europe's ICT accessibility standard. Web content, documents and software clauses now reference WCAG 2.2 AA instead of 2.1, real-time communication requirements were rewritten, and new annexes map the standard directly to the European Accessibility Act. Deque reports it is on track to be cited in the EU Official Journal around 30 November 2026, which is when it gives a presumption of conformity.

   **For us:** anything shipping into the EU next year should be built and tested against 2.2 AA plus the non-WCAG EN clauses (user preferences, real-time text).

   Sources: [National Disability Authority](https://nda.ie/news/en301549-published) · [Deque](https://www.deque.com/blog/en-301-549-v4-1-1-is-final-what-changed-what-it-means-and-what-you-should-do/) · [Davis Wright Tremaine](https://www.dwt.com/insights/2026/09/european-accessibility-act-ict-standards-update)
2. Sep 2026

   Standards

   ### New WCAG 3 Working Draft opens for review

   W3C published another WCAG 3 Working Draft in September, following the March 2026 draft. WCAG 3 is still a draft: it replaces pass/fail success criteria with more granular requirements and a Bronze/Silver/Gold conformance model, and broadens scope beyond web content. W3C says WCAG 2 will not be deprecated for several years after WCAG 3 is final.

   **For us:** read it, don't build to it. No law or procurement rule references WCAG 3 yet.

   Sources: [W3C WAI announcement](https://lists.w3.org/Archives/Public/public-wai-announce/2026JulSep/0001.html) · [WCAG 3 Introduction](https://www.w3.org/WAI/standards-guidelines/wcag/wcag3-intro/)
3. 16 Sep 2026

   Research

   ### AI speeds up building faster than it speeds up accessibility testing

   Level Access's eighth State of Digital Accessibility report found about 80% of accessibility professionals now use AI, but only around 30% say it has helped their QA and testing. Applause's 2026 report similarly found 78% of organisations use AI for accessibility work, with 90% combining it with manual testing.

   **For us:** AI-generated UI still needs the same manual keyboard and screen reader passes. Treat AI output like a new contributor's PR.

   Sources: [Level Access](https://www.levelaccess.com/news/press-releases-news/level-access-research-finds-broad-ai-adoption-isnt-closing-the-accessibility-gap/) · [Applause report coverage](https://digiworld.news/news/72472/enhancing-digital-accessibility-through-ai-insights-from-applauses-2026-report)
4. 8 Jul 2026

   Law & enforcement

   ### US digital accessibility lawsuits on pace for a record year

   UsableNet's midyear report projects about 6,176 website and app lawsuits in 2026, nearly 20% above 2025, and its highest first-half volume on record. About two in three website suits target companies under $50M in revenue. Seyfarth Shaw separately counted 5,006 federal ADA Title III filings (physical and digital) in H1 2026, up 9%. App lawsuits are a growing share.

   **For us:** native apps are in scope for plaintiffs, not just websites. Checkout, sign-in and account flows are the usual targets.

   Sources: [Stacker (UsableNet and Seyfarth data)](https://stacker.com/stories/small-business/website-accessibility-lawsuits-are-rising-and-smaller-businesses-are) · [UsableNet blog](https://blog.usablenet.com/)
5. 28 Jun 2026

   Law & enforcement

   ### European Accessibility Act turns one; enforcement is ramping up

   The EAA has been enforceable since 28 June 2025. Year one was mostly awareness and soft enforcement, but national authorities are building audit capacity: Italy's AGID introduced a two-stage model in May 2026 (cooperative remediation, then sanctions), and the first enforcement actions were injunctions filed against retailers in France in November 2025. Organisations that ignored early inquiries are reported to be prioritised for audits in the second half of 2026.

   **For us:** EU-facing e-commerce flows and apps need a current accessibility statement and a documented remediation plan.

   Sources: [Taylor Wessing](https://www.taylorwessing.com/en/insights-and-events/insights/2026/06/the-eaa-and-bfsg-recap-and-update) · [Level Access](https://www.levelaccess.com/blog/eaa-compliance-in-2026-how-enforcement-has-evolved-and-what-to-expect-next/) · [Accesstive](https://accesstive.com/eaa-compliance/)
6. 16 Jun 2026

   Mobile platforms

   ### Android 17 ships with accessibility API restrictions and large-screen changes

   Android 17 (API level 37) is rolling out. Under Advanced Protection Mode it blocks apps that aren't genuine accessibility tools from using the Accessibility API, to curb malware. Apps targeting API 37 can no longer lock orientation or disable resizing on large screens. Google's I/O 2026 session covered TalkBack, Voice Access, expanded dark theme and accessibility API changes.

   **For us:** test layouts in landscape and on tablets/foldables at large font sizes; we can no longer rely on portrait lock.

   Sources: [Google I/O 2026: Android accessibility updates](https://io.google/2026/explore/technical-session-5) · [Techlomedia](https://techlomedia.in/2026/06/google-rolls-out-android-17-focusing-on-ai-productivity-and-privacy-124732/)
7. 19 May 2026

   Mobile platforms

   ### Apple previews AI-powered accessibility features for its 27 releases

   Ahead of Global Accessibility Awareness Day, Apple announced Apple Intelligence upgrades to VoiceOver, Magnifier, Voice Control (including natural-language commands) and Accessibility Reader, generated subtitles across its platforms, and power wheelchair control with Apple Vision Pro.

   **For us:** AI image descriptions don't replace our own labels. Natural-language Voice Control works best when visible labels match accessible names.

   Sources: [Apple Newsroom](https://www.apple.com/newsroom/2026/05/apple-unveils-new-accessibility-features-and-updates-with-apple-intelligence/) · [MacRumors](https://macrumors.com/2026/05/19/new-accessibility-features-with-apple-intelligence/)
8. May 2026

   Mobile platforms

   ### Apple pushes developers to prepare Accessibility Nutrition Labels

   App Store product pages now show which accessibility features an app supports (VoiceOver, Voice Control, Larger Text, Sufficient Contrast, Dark Interface, Differentiate Without Color Alone, Reduced Motion, Captions, Audio Descriptions). A feature can only be claimed if users can complete all of the app's common tasks with it. Labels are optional today; Apple says they will become required for new apps and updates.

   **For us:** audit each common task per feature now so our labels are accurate when they become mandatory. Users can filter App Store search by these features.

   Sources: [App Store Connect Help](https://developer.apple.com/help/app-store-connect/manage-app-accessibility/overview-of-accessibility-nutrition-labels) · [Hello Developer, May 2026](https://developer.apple.com/hello/may26)
9. 20 Apr 2026

   Law & enforcement

   ### DOJ extends ADA Title II web and app deadlines by one year

   An Interim Final Rule moved compliance dates for state and local governments to 26 April 2027 (population 50,000+) and 26 April 2028 (smaller entities and special districts). The technical standard, WCAG 2.1 AA for web content and mobile apps, did not change.

   **For us:** if we sell to schools, libraries or government customers, they will ask for conformance reports (VPATs/ACRs) against WCAG 2.1 AA.

   Sources: [Federal Register](https://www.federalregister.gov/documents/2026/04/20/2026-07663/extension-of-compliance-dates-for-nondiscrimination-on-the-basis-of-disability-accessibility-of-web) · [Vispero](https://vispero.com/resources/ada-title-ii-deadline-extension-2026/)
10. Feb 2026

    Research

    ### WebAIM Million 2026: the web got less accessible

    For the first time in years, detectable failures rose: 95.9% of the top million home pages failed, averaging 56.1 errors per page. Pages grew to an average of 1,437 elements, up 22.5% in a year. The most common failures were low-contrast text (83.9% of pages), missing alt text (53.1%), missing form labels (51%), empty links (46.3%) and empty buttons (30.6%). Pages with ARIA averaged 59.1 errors versus 42 without.

    **For us:** the top five failures are all catchable in design review and automated CI. More ARIA is not better ARIA.

    Source: [WebAIM Million](https://webaim.org/projects/million/)

## Standards, laws and requirements

Technical standards say *how* to make something accessible. Laws and platform policies say *who must*. Most laws point back to a version of WCAG.

Status as of November 2026

| Requirement | What it is | Status | Technical bar | Applies to |
| --- | --- | --- | --- | --- |
| [WCAG 2.2](https://www.w3.org/TR/WCAG22/) | W3C Web Content Accessibility Guidelines; also ISO/IEC 40500:2025. | Current standard | Level AA (our baseline) | Web, and via W3C guidance, mobile apps and non-web software |
| [WCAG 3](https://www.w3.org/WAI/standards-guidelines/wcag/wcag3-intro/) | Next-generation guidelines with Bronze/Silver/Gold conformance. | Working Draft | Not yet usable for conformance | Planning only |
| [EN 301 549 V4.1.1](https://www.etsi.org/deliver/etsi_en/301500_301599/301549/04.01.01_60/en_301549v040101p.pdf) | EU harmonised ICT accessibility standard. | Published Sep 2026; OJ citation pending | WCAG 2.2 AA plus extra clauses (user preferences, real-time text, hardware) | Products and services under the EAA; EU public procurement |
| [European Accessibility Act](https://eur-lex.europa.eu/eli/dir/2019/882/oj) | EU Directive 2019/882, transposed into each member state's law. | Enforced since 28 Jun 2025 | Presumption of conformity via EN 301 549 | Consumer e-commerce, apps, e-books, banking, transport, devices sold in the EU (microenterprise carve-out) |
| [ADA Title II rule](https://www.ada.gov/resources/2024-03-08-web-rule/) | US DOJ rule for state and local government web content and apps. | Deadlines Apr 2027 / Apr 2028 | WCAG 2.1 AA | Public entities, and vendors whose products they use |
| ADA Title III | US law covering businesses open to the public. | Actively litigated | No regulation; settlements and courts usually cite WCAG 2.1 AA | Private businesses' websites and apps |
| [Section 508](https://www.section508.gov/) | US federal procurement standard (Revised 508, 2018). | In force | WCAG 2.0 AA, applied to web, documents and software | Products sold to US federal agencies |
| [AODA (Ontario)](https://www.ontario.ca/page/how-make-websites-accessible) | Integrated Accessibility Standards, information and communications. | In force | WCAG 2.0 AA (large organisations) | Organisations with 50+ employees in Ontario |
| [Accessible Canada Act](https://accessible.canada.ca/) | Federal Canadian law; adopted EN 301 549 as CAN/ASC-EN 301 549:2024. | In force | EN 301 549 (WCAG 2.1 AA in the 2024 adoption) | Federally regulated sectors |
| [Apple Accessibility Nutrition Labels](https://developer.apple.com/help/app-store-connect/manage-app-accessibility/overview-of-accessibility-nutrition-labels) | App Store disclosure of supported accessibility features. | Optional; will become required | Apple's per-feature criteria: all common tasks completable | Every App Store app, per device type |

This table is orientation, not legal advice. Coverage depends on where we sell, who our customers are and company size. Confirm applicability with Legal before making conformance claims.

### What WCAG 2.2 added over 2.1

Six new Level A and AA success criteria (2.2 also removed 4.1.1 Parsing). These are the ones teams most often miss because older checklists don't include them.

2.4.11 · AA**Focus Not Obscured (Minimum)**

A focused element isn't entirely hidden by sticky headers, cookie banners or chat widgets.

2.5.7 · AA**Dragging Movements**

Anything done by dragging (sliders, reorder, canvas moves) has a single-pointer alternative such as tap or buttons.

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

Our rule: design to the platform guidance (44 pt / 48 dp, 44 px on touch web) and treat 24 px as the floor that must never be broken.

## Web and mobile guides

The same WCAG outcomes, implemented with each platform's own APIs and assistive technology.

### Design

- Text contrast 4.5:1 (3:1 for 18.66 px bold / 24 px regular and up); UI component and focus indicator contrast 3:1.
- Design a visible focus state for every interactive component, not just links.
- Layouts reflow at 320 CSS px wide (400% zoom) without two-direction scrolling.
- Never use colour alone to show state, errors or chart series.
- Annotate heading levels, landmarks, reading order and accessible names in handoff files.
- Provide a non-drag alternative for any drag interaction.

### Build

- Native HTML first: `<button>`, `<a href>`, `<label>`, `<fieldset>`. Add ARIA only when no native element exists, and follow the ARIA Authoring Practices patterns when you do.
- Every input has a programmatic label; errors are linked with `aria-describedby` and announced.
- Manage focus on route changes, modals and deleted items. Trap focus only inside modal dialogs.
- Set `lang` on `<html>`; use one `h1` and a logical heading outline.
- Respect `prefers-reduced-motion` and `prefers-contrast`; don't disable zoom in the viewport meta.
- Status messages (toasts, cart updates) use a polite live region.

#### Key APIs and references

`aria-label / aria-labelledby``aria-describedby``aria-live``aria-expanded``inert``<dialog>``:focus-visible``prefers-reduced-motion`

[ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/) · [MDN Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility) · [How to Meet WCAG (Quick Reference)](https://www.w3.org/WAI/WCAG22/quickref/)

#### Test with

axe or Lighthouse in CI · keyboard only · NVDA + Firefox or Chrome · JAWS + Chrome · VoiceOver + Safari (macOS and iOS) · 200% text and 400% zoom

### Design

- Support Dynamic Type through the accessibility sizes; layouts must stack or scroll, not truncate.
- 44 × 44 pt minimum hit areas, even when the visible icon is smaller.
- Check designs in Dark Mode, Increase Contrast, Bold Text and Reduce Transparency.
- Provide alternatives to custom gestures (long-press, swipe actions) and avoid gestures that conflict with VoiceOver.
- Specify VoiceOver labels, hints and grouping in specs (for example, a product card reads as one element).

### Build

- Set `accessibilityLabel`, `accessibilityValue` and traits for custom controls; standard controls get these for free.
- SwiftUI: use `.accessibilityElement(children: .combine)`, `.accessibilityAction`, `.accessibilityHeading`.
- Use text styles (`.font(.body)`, `UIFont.preferredFont`) so Dynamic Type works; adapt layout with `dynamicTypeSize.isAccessibilitySize`.
- Honour Reduce Motion (`accessibilityReduceMotion`) and post announcements with `AccessibilityNotification`.
- Add custom rotor entries and actions where lists have secondary actions.
- Match visible text and accessible names so Voice Control commands work.

#### Key APIs and references

`accessibilityLabel``accessibilityTraits``accessibilityCustomActions``accessibilityRotor``UIAccessibility.post``performAccessibilityAudit()`

[Apple Developer: Accessibility](https://developer.apple.com/accessibility/) · [Human Interface Guidelines: Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) · [Accessibility Nutrition Labels criteria](https://developer.apple.com/help/app-store-connect/manage-app-accessibility/overview-of-accessibility-nutrition-labels)

#### Test with

Xcode Accessibility Inspector · XCUITest `performAccessibilityAudit()` in CI · VoiceOver on device · Voice Control · Switch Control · largest Dynamic Type size · Full Keyboard Access on iPad

### Design

- 48 × 48 dp minimum touch targets with at least 8 dp between them.
- Specify text in sp and design for 200% font scale; Android uses non-linear scaling so large text grows less than small text.
- Design for landscape, tablets and foldables: apps targeting API 37 can't lock orientation on large screens.
- Check designs with dark theme, high-contrast text and colour correction.
- Specify TalkBack labels, grouping and custom actions in handoff.

### Build

- Views: set `contentDescription`; mark decorative images `importantForAccessibility="no"`; use `labelFor` on form labels.
- Compose: use `Modifier.semantics`, `mergeDescendants = true` for cards, `heading()`, `stateDescription` and `role`.
- Add `customActions` instead of relying on swipe or long-press alone.
- Announce changes with `liveRegion` (Compose `LiveRegionMode.Polite`).
- Support keyboard, D-pad and Switch Access focus order; use `traversalIndex` only when the natural order is wrong.
- Don't use the Accessibility Service API for non-accessibility features; Android 17 Advanced Protection blocks it.

#### Key APIs and references

`contentDescription``Modifier.semantics``mergeDescendants``stateDescription``CustomAccessibilityAction``AccessibilityChecks.enable()`

[Android Developers: Accessibility](https://developer.android.com/guide/topics/ui/accessibility) · [Compose accessibility](https://developer.android.com/develop/ui/compose/accessibility) · [Material 3: Accessible design](https://m3.material.io/foundations/designing/overview)

#### Test with

Accessibility Scanner · Espresso `AccessibilityChecks` and Compose UI tests in CI · TalkBack on device · Voice Access · Switch Access · Display size and font size at maximum

## Checklists

Use one pass per feature. Ticks are saved only in your browser, so each person keeps their own progress.

### Designer

- [ ] Text and icon contrast checked in light and dark themes 1.4.3 · 1.4.11
- [ ] Focus state designed for every interactive component 2.4.7 · 2.4.11
- [ ] Targets meet 44 pt / 48 dp; never under 24 px 2.5.8
- [ ] Colour isn't the only way state or meaning is shown 1.4.1
- [ ] Layouts tested at 200% text and 320 px width 1.4.4 · 1.4.10
- [ ] Headings, landmarks and reading order annotated 1.3.1 · 2.4.6
- [ ] Accessible names written for icon-only controls 4.1.2
- [ ] Error messages say what went wrong and how to fix it 3.3.1 · 3.3.3
- [ ] Drag interactions have a tap or button alternative 2.5.7
- [ ] Motion is optional and respects reduced-motion settings 2.3.3

### Engineer

- [ ] Native elements and platform controls used before custom ones 4.1.2
- [ ] Every control has a correct name, role, value and state 4.1.2
- [ ] Full task completable with keyboard / switch, in logical order 2.1.1 · 2.4.3
- [ ] Focus moved and restored on dialogs, navigation and deletes 2.4.3
- [ ] Form inputs labelled; errors linked and announced 1.3.1 · 3.3.1
- [ ] Status updates use live regions / announcements 4.1.3
- [ ] Text scales with Dynamic Type / sp / browser zoom 1.4.4
- [ ] Images have alt text or are marked decorative 1.1.1
- [ ] Sign-in allows paste and password managers 3.3.8
- [ ] Automated accessibility checks pass in CI axe · XCTest · Espresso

### Before release

- [ ] Core tasks completed with a screen reader on each platform
- [ ] Core tasks completed with keyboard only (web, iPad, ChromeOS)
- [ ] Core tasks completed with Voice Control / Voice Access
- [ ] Checked at the largest text size and in landscape
- [ ] Videos have captions; audio-only has a transcript
- [ ] Third-party components (chat, consent, payments) tested too
- [ ] Known issues logged with WCAG reference and severity
- [ ] App Store Nutrition Labels and accessibility statement still accurate

## Testing and tools

Automated scanners find a portion of issues quickly and cheaply. Keyboard, screen reader and zoom passes find the rest. Usability testing with disabled people finds what neither catches.

Recommended toolkit

| Tool | Platform | Used by | Best for |
| --- | --- | --- | --- |
| [Stark](https://www.getstark.co/) | Figma | Design | Contrast, colour-blindness simulation, focus order and annotations in design files |
| [Colour Contrast Analyser](https://www.tpgi.com/color-contrast-checker/) | Desktop | Design, QA | Sampling real rendered colours from any screen |
| [axe-core / axe DevTools](https://www.deque.com/axe/) | Web | Engineering, QA | Browser extension and CI integration (Playwright, Cypress, Jest) |
| [Accessibility Insights](https://accessibilityinsights.io/) | Web, Windows | Engineering, QA | Guided manual assessment with tab-stop visualisation |
| [WAVE](https://wave.webaim.org/) | Web | Everyone | Visual, in-page view of errors and structure |
| [Lighthouse](https://developer.chrome.com/docs/lighthouse/) | Web | Engineering | Quick score in DevTools and performance budgets |
| [Accessibility Inspector + XCUITest audits](https://developer.apple.com/accessibility/) | iOS, macOS | Engineering | Inspecting labels and traits; automated audits in UI tests |
| [Accessibility Scanner](https://play.google.com/store/apps/details?id=com.google.android.apps.accessibility.auditor) | Android | QA, Design | On-device suggestions for targets, contrast and labels |
| [Espresso Accessibility Checks](https://developer.android.com/training/testing/espresso/accessibility-checking) | Android | Engineering | Failing UI tests on accessibility violations in CI |
| [NVDA](https://www.nvaccess.org/) · JAWS · VoiceOver · TalkBack | All | Engineering, QA | Real screen reader behaviour; free options: NVDA, VoiceOver, TalkBack |

### Shift left

Accessibility annotations in Figma, linting in the IDE, automated checks on every pull request. Fixing a missing label in design takes minutes; after launch it's a ticket, a release and sometimes a demand letter.

### Five-minute manual pass

Tab through the feature. Turn on the screen reader and complete the main task without looking. Zoom to 200% or set the largest text. Toggle reduced motion and dark mode. Most blocking bugs show up here.

### Test with disabled users

Include screen reader, magnification, voice control and cognitive-disability participants in research rounds for major flows. Budget for recruiting and compensation through specialist panels.

### Avoid overlays

Overlay widgets don't fix source code. The FTC ordered accessiBe to pay $1 million in 2025 over its compliance marketing claims, more than 1,000 practitioners have signed the Overlay Fact Sheet, and sites with widgets are still regularly sued.

[Overlay Fact Sheet](https://overlayfactsheet.com/) · [FTC action summary](https://www.hudsoncook.com/article/ftc-targets-accessibility-overlays/)

## Research and data

Studies and datasets to cite in roadmaps, design reviews and business cases. Check the date on each before quoting it.

Web · Feb 2026

### [The WebAIM Million 2026](https://webaim.org/projects/million/)

95.9% of home pages failing

Annual automated scan of the top million home pages. First regression in years: average errors per page rose to 56.1 and page complexity grew 22.5%. Low contrast appears on 83.9% of pages.

Industry · Sep 2026

### [Level Access: State of Digital Accessibility (8th)](https://www.levelaccess.com/news/press-releases-news/level-access-research-finds-broad-ai-adoption-isnt-closing-the-accessibility-gap/)

\~80% of practitioners use AI

Survey of accessibility and digital teams. AI adoption is broad, but only about 30% say it has helped QA and testing, so build speed is outpacing verification.

Apps & web · 2026

### [Applause: State of Digital Quality in Accessibility](https://digiworld.news/news/72472/enhancing-digital-accessibility-through-ai-insights-from-applauses-2026-report)

78% use AI; 90% pair it with manual tests

Sixth annual report. Only 10% of organisations rely exclusively on AI for accessibility testing, and assistive technology users still frequently hit inaccessible apps.

Litigation · Jul & Sep 2026

### [UsableNet and Seyfarth Shaw midyear reports](https://blog.usablenet.com/)

\~6,176 suits projected in 2026

Website, app and video lawsuits in US federal and NY/CA state courts, around 20% above 2025. E-commerce is the most-sued sector; app lawsuits are growing.

Population · WHO

### [WHO: Disability and health](https://www.who.int/news-room/fact-sheets/detail/disability-and-health)

1.3 billion people, about 1 in 6

Global estimate of people living with significant disability. Add temporary and situational limitations (a broken arm, bright sunlight, a noisy room) and the audience is everyone.

Users · WebAIM

### [WebAIM Screen Reader User Survey](https://webaim.org/projects/screenreadersurvey10/)

How screen reader users actually navigate

Long-running survey on screen reader and browser combinations, mobile vs desktop use, and how people find content (headings remain the most common way to navigate a page).

Personas · W3C WAI

### [How People with Disabilities Use the Web](https://www.w3.org/WAI/people-use-web/)

Stories, tools and barriers

User stories and the assistive technologies people use. Good material for personas, research plans and onboarding new designers.

Design method · Microsoft

### [Microsoft Inclusive Design toolkit](https://inclusive.microsoft.design/)

Permanent, temporary, situational

The persona spectrum and activity cards for designing with exclusion in mind. Useful for workshops and design critiques.

## Trends to plan for

What's shifting in 2026 and 2027, and what each shift asks of Design and Engineering.

### AI builds UI faster than teams can verify it

Signal

WebAIM linked rising page complexity and errors to faster, AI-assisted building. Level Access found AI is widely used but rarely improves QA.

Our response

Put accessibility rules in coding-assistant instructions, component libraries and CI gates so generated code inherits them. Keep human screen reader passes.

### Enforcement replaces deadlines

Signal

The EAA is in its second enforcement year with national audits starting; US suits are at record pace, with apps increasingly named.

Our response

Keep accessibility statements, conformance reports (ACR/VPAT) and remediation backlogs current. Documented progress is what regulators ask for first.

### WCAG 2.2 becomes the global baseline

Signal

EN 301 549 V4.1.1 adopts WCAG 2.2 AA; WCAG 2.2 is also an ISO standard. US rules still cite 2.1, which 2.2 contains.

Our response

Retire 2.1-only checklists. Add the six new criteria to design reviews and test plans.

### App stores make accessibility visible to buyers

Signal

Apple's Accessibility Nutrition Labels appear on product pages, can be filtered in search, and will become mandatory.

Our response

Define our app's common tasks and audit each one per feature (VoiceOver, Larger Text, Voice Control and so on) before claiming support.

### Assistive technology gets AI built in

Signal

Apple Intelligence now powers VoiceOver image exploration and natural-language Voice Control; Android 17 adds Gemini at OS level.

Our response

Good semantics matter more, not less: AI assistants read the same accessibility tree. Keep visible labels and accessible names aligned.

### WCAG 3 and cognitive accessibility

Signal

WCAG 3 drafts broaden scope beyond content and put more weight on cognitive and learning needs, plain language and predictable UI.

Our response

No conformance work yet. Start practising now: plain-language copy reviews, consistent navigation, fewer steps in key flows.

## Resource library

Primary sources first, then the best practitioner guides. Filter by any word.

Filter resources

Maintained for the Design & Engineering teams. Content current to 3 November 2026; every news item links its source. This hub is guidance, not legal advice.

Body text on page background: above 14:1 Secondary text: above 7:1 Links: above 6:1