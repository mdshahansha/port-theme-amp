# Component contracts

This inventory defines observed presentation/behavior and provisional future implementation boundaries. **No components are implemented.** Evidence IDs resolve through [evidence-index.md](evidence-index.md). Data/props and architecture choices below are **RECOMMENDATIONS**, not claims about the reference source API. Root should reconcile contract names with [component-inventory.md](component-inventory.md) and add other observed reusable structures.

## CONTRACT-GRID-001 — Responsive layout foundation

- **Class/purpose:** Primitive; reproduce measured spatial composition and aligned section structure.
- **Usage/anatomy:** Observed homepage grid. Exact section spans/children belong to [page-specs/](page-specs/), not one presumed universal layout.
- **Observed default/variants:** One column below 768 px; three columns at 768–1023; five fractional columns at 1024+ with ratio 560:560:373:373:373. `--lens-cell-padding: clamp(.75rem, 1.5vw, 1.5rem)`. At 1440: section padding 56 px vertically and 59.0112 px horizontally; child cell adds 21.6 px, yielding content anchor 80.6016 px. Grid/subgrid class indicators exist; confirm actual nested computed subgrid before declaring it exact.
- **Proposed inputs:** Section content, measured span map, validated spacing/container tokens. Avoid arbitrary span variants unsupported by reference.
- **Responsive:** Discrete track changes at confirmed boundaries; individual ordering/spans/overflow require section evidence.
- **States/motion:** Control states **NOT APPLICABLE**. Layout itself does not prove a scroll or entrance animation; integrate only linked measured section motion.
- **Accessibility recommendation:** Preserve logical DOM reading order across visual rearrangement; avoid making critical content inaccessible through clipping/overflow.
- **Relationships:** Title, media, carousel, installer and content sections depend on the grid's dimensions.
- **Risks/open questions:** Different spans between sections; subgrid semantics; accumulated page-height drift; unsampled section-specific gaps/spans. This measured nested grid must not be replaced by one generic centered container.
- **Evidence:** HOME-CSS-001, RESP-MATRIX-001, RESP-BOUNDARY-001.

## CONTRACT-TITLE-001 — Observed animated title

- **Class/purpose:** Composite, local to the observed title until reuse is proven; preserve typographic emphasis and measured word motion.
- **Usage/anatomy:** Homepage H1 has invisible aria-hidden phrase measurement layers, a changing screen-reader-only current phrase, and aria-hidden animated word spans. Eight phrases cycle. Line breaks and clipping still depend on section/responsive evidence.
- **Observed default/variants:** Hero uses Sagittaire Display, weight 400, line-height 0.9 and tracking −0.06em with italic emphasis. Exact title scale is `clamp(2.07rem, 1.07rem + 2.5 * min(1vi, calc(1920px / 100)), 7rem)`, measured at rem base 16 px; floor 33.12 px and sample 65.12 px at 1920. CSSOM confirms Sagittaire face/weight/style mappings and TX-02→Berkeley Mono; all declare swap. Actual loaded subsets, TX-02 variable axes/range and licensing remain unknown.
- **Proposed inputs:** Observed title content/segments, measured typography, resolved sequence data and reduced-motion policy. Do not invent a generic word-rotation API as reference fact.
- **Responsive:** Preserve recorded wraps and clipping; grid change and fluid type scaling are different mechanisms. Reflow during active animation must be investigated.
- **Motion:** Entrance opacity 0→1/Y 26→0, origin 0% 100%, 560 ms cubic-bezier(0.16, 1, 0.3, 1), sampled delays 280/340/400/460 ms. Exit opacity 1→0/Y 0→−18 px, center origin, computed 300 ms ease and sampled delays 0/40/80/120 ms. New/old emphasis skew 14→0/0→−14 degrees with fades over 560 ms. Timed DOM supports approximately four-second insertions and old/new coexistence; exact scheduler/full eight-phrase cycle/offscreen/interruption remain **UNKNOWN**. Reduced CSS disables entrance/emphasis and hides exits; runtime scheduling/activation is untested. See animation-timelines.md.
- **Interactive states:** Hover/focus/pressed/disabled/loading/error **NOT APPLICABLE** unless the title contains a separately documented control. Dynamic lifecycle states still require observed initial/active/settled transitions.
- **Accessibility recommendation:** Keep meaningful text available in a stable reading order; avoid announcing every decorative word transition. Implement the confirmed reduced-motion declarations, then test runtime scheduler/reading behavior; CSS configuration alone is not a passed preference test.
- **Relationships:** Tight coupling to typography metrics, line wrapping, grid, clipping and section height; develop these together.
- **Risks/open questions:** A matching settled screenshot hides wrong sequence; inaccessible or duplicated text nodes; exit/entrance conflation.
- **Evidence:** HOME-CSS-001, HOME-CSSOM-001, HOME-MOTION-001, HOME-TIMED-DOM-001, HOME-WRAP-001, RESP-MATRIX-001, RESP-BOUNDARY-001.

## CONTRACT-NAV-001 — Navigation with mobile overlay

- **Class/purpose:** Composite; expose recorded public navigation and its mobile presentation.
- **Usage/anatomy:** Homepage navigation and observed mobile overlay. Item labels, ordering, URLs and shared-page reuse must come from [website-map.md](website-map.md), not conventional guessed navigation.
- **Observed states:** Trigger aria-expanded=false→click→true, repeated opening, outside-page click and Escape closure are confirmed. Tab reaches Home with a visible 1 px foreground ring. At 768 px resize the trigger is hidden while aria-expanded stays true. Full focus cycle/trapping/restoration, scroll lock, return-to-mobile behavior, hover/pressed/loading/error states remain **UNKNOWN**.
- **Proposed inputs:** Recorded nav entries/destinations, measured desktop/mobile presentation, controlled open state and resolved dismissal/focus policy.
- **Responsive:** The menu boundary was separately confirmed: below 768 px, trigger is 48×48 px and nav links have zero rectangles; at 768 px links appear and trigger has zero rectangle. Overlay items include Home, Chronicle, Docs, Using Amp, Models, Pricing, About, Sign In, Start and More. More closed the menu but no further visible outcome was captured.
- **Motion:** Overlay entrance/exit timing/easing is **UNKNOWN** unless measured in [animation-spec.md](animation-spec.md).
- **Accessibility recommendation:** Semantic links and trigger button with clear accessible name/state; logical keyboard path; visible focus; agreed overlay dismissal/restoration and background interaction policy. These are future usability requirements, not untested reference findings.
- **Relationships:** Navigation graph, shared route shells, responsive layout and document scroll state.
- **Risks/open questions:** Overlay open during resize/navigation; repeated toggles; keyboard focus behind overlay; unconfirmed history behavior.
- **Evidence:** HOME-STRUCT-001, INT-MENU-001, RESP-MATRIX-001, RESP-BOUNDARY-001.

## CONTRACT-MEDIA-001 — Synchronized screen/camera media

- **Class/purpose:** Composite; retain the observed product demonstration with two synchronized media surfaces.
- **Usage/anatomy:** Screen media plus camera media and observed control surfaces. Display dimensions/crop/layering and control labels belong to page/asset/interaction specs.
- **Observed states:** Initial paused 00:00/26:05 and 1×; clicking chapter 0:16 seeks/starts both streams; sampled times 16.311/16.316 s. Choosing 1.5× changes both rates. Both streams have loop/autoplay/native-controls=false; screen muted=false, camera=true. Captions/Sidebar false→true update labels; sidebar becomes 272 px+967.797 px at 1440. Mobile transcript expands to 70 timestamp buttons; Chapters false→true. Later pause near 32.65 s has unknown cause. Mute/fullscreen/webcam/seek-scrubber success, buffering/end/error, complete keyboard paths and drift correction remain **UNKNOWN**.
- **Proposed inputs:** Approved screen/camera assets, measured composition and explicit shared control/synchronization contract. Internal shared time/control state is a candidate design, not a source-code finding.
- **Responsive:** Composite stage uses screen width 78.2143% and camera width 20.7662%, with camera beginning at 79.2338%; stage aspect is 4909.587/2002. Mobile player measured 319 px wide and one column, with Chapters and collapsed Transcript. Desktop caption/rate controls are absent in the narrow observed state; alternative Settings behavior is unresolved. Preserve both streams rather than cropping to one video.
- **Motion:** Video playback is native media, not proof of GSAP/CSS animation. Approximately 5 ms drift is one sample, not a guaranteed tolerance. Caption/sidebar/rate/transcript states are independent axes rather than playback prerequisites.
- **Accessibility recommendation:** Label controls, keep keyboard access, communicate actual play/pause state; supply appropriate accessible alternatives/captions according to final content and rights decisions. Do not fabricate reference captions.
- **Relationships:** Asset loading and dimensions, page geometry, platform media support, interaction state machine.
- **Risks/open questions:** One stream buffers or ends first; rapid seek/pause; autoplay restrictions; decode workload; inaccessible custom controls.
- **Evidence:** INT-VIDEO-001, ASSET-VIDEO-FLAGS-002; asset-inventory.md and interaction-spec.md for sources/control details.

## CONTRACT-CAROUSEL-001 — Bounded episode carousel

- **Class/purpose:** Composite; preserve observed horizontally scrollable content presentation.
- **Usage/anatomy:** Homepage episode section: introduction/Start Watching/Previous/Next and four ordered linked cards with thumbnail, duration, heading and summary. At 1440, desktop card width is 326.89 px; its thumbnail is 283.70×159.58 px (16:9). This thumbnail measurement is not a mobile card width; exact mobile item width remains unknown. This is distinct from looping testimonial tracks.
- **Observed default/states:** Initially Previous disabled and Next enabled; Next moves scrollLeft 0→327 px and enables Previous. Sample track client width 1039 px and total width 1367 px. Previous action was performed but its exact reverse endpoint was not recorded. Final disabled rules, drag/wheel/key/touch, snapping/timing, rapid repeat and hover/focus states remain unknown.
- **Proposed inputs:** Recorded item sequence, dimensions, bounds and measured input/control behavior.
- **Responsive:** Below 768 px the introduction sits above the horizontal cards; preserve measured widths/visible portion and input behavior rather than replacing the strip with a generic stacked list.
- **Motion:** Native scroll versus custom mechanism is unresolved unless technical evidence specifies it. Do not presume momentum/snap/auto-advance.
- **Accessibility recommendation:** Reach meaningful content and controls with keyboard; clear control labels where controls exist; avoid trapping document scrolling.
- **Relationships:** Grid/container overflow, repeated item component, assets/content order and input-mode contract.
- **Risks/open questions:** Horizontal document overflow; inaccessible off-screen content; generic carousel defaults replacing reference behavior.
- **Evidence:** HOME-STRUCT-001, INT-EPISODES-001, RESP-MATRIX-001.

## CONTRACT-INSTALL-001 — Platform installation command

- **Class/purpose:** Composite; present the observed installation command for the selected platform.
- **Usage/anatomy:** Platform selection and command display, plus only those additional controls observed. Exact labels, commands, defaults and copy feedback belong to [interaction-spec.md](interaction-spec.md).
- **Observed states:** Mac/Linux/WSL default; Windows/Homebrew change the command. Native select appears in the homepage narrow grid column, with button variants elsewhere; this is not solely a viewport rule. Later Windows command click shows Copied to clipboard toast, Dismiss and adjacent icon replacement. Clipboard accessor returned previous documentation content rather than the command, so payload success/tool-site mismatch cause remain **UNKNOWN**. Icon details/reset, dismissal activation, denied/error/repeat states, detection/persistence/full keyboard remain untested. No command was executed.
- **Proposed inputs:** Observed platform/command records, selected styling, separate command-copy action and observed feedback state. Do not invent commands or equate a success toast with verified clipboard payload.
- **Responsive:** Command wrapping/scrolling and selector presentation should match viewport evidence; preserve full command usability.
- **Motion:** Command inner text declares transform transition 0.5 s linear; actual hover/autoscroll trigger and travel remain unknown. Selection/copy-feedback timing/easing is unresolved.
- **Accessibility recommendation:** Semantic selectable controls with clear current state; selectable/copyable command text as agreed; readable labels and keyboard operation. Feedback announcement is a future recommendation when copy exists, not a reference claim.
- **Relationships:** Typography (monospace role only where measured), installer route/anchors, state machine and platform data.
- **Risks/open questions:** Wrong shell/platform command, truncated text, rapid changes, unconfirmed detection/persistence/copy feedback.
- **Evidence:** INT-INSTALL-001, INT-INSTALL-COPY-002.

## CONTRACT-POPOVER-001 — Explanatory popovers

- **Class/purpose:** Composite; expose the observed orb-term and proposition explanations without navigation.
- **Usage/anatomy/default:** Two distinct content variants. Orb popover measured x611/y216/w288/h120 at 1440; proposition popup 288×122 px. Orb trigger uses cursor-help/dotted underline; proposition anchor has role=button and no href. Layer/shadow values are in design-system.md.
- **Observed transitions:** Click opens; Escape closes. Settled computed animation is none, which does not establish an instantaneous transition. Hover initiation/delay, outside dismissal, repeated/double click, mobile placement, focus trapping/restoration and announcement remain unknown.
- **Proposed inputs:** Recorded trigger/content variants and measured bounds; resolved dismissal/focus policy. A semantic button is an implementation recommendation if the trigger is an action.
- **Responsive/motion:** Preserve recorded variant content/geometry; mobile placement and exact entrance/exit behavior require further measurement.
- **Accessibility recommendation/relations:** Keyboard-reachable labeled trigger and agreed focus/dismissal policy; relates to hero wording, section overlay/layering and INT-POPOVER-001.
- **Risks/evidence:** Do not infer hover from dotted underline. Evidence: INT-POPOVER-001, HOME-CSS-001; ACC-POPOVER-001.

## CONTRACT-CARD-001 — Linked content cards and rows

- **Class/purpose:** Reusable linked-card primitive with distinct observed feature, episode, testimonial and news compositions. This does not imply all variants have identical markup.
- **Usage/anatomy:** Features are whole-card anchors with heading/caption and layered HTML/SVG product miniature; five feature cards contain zero img/video nodes, with 11/26/7/7/6 SVG nodes. Episodes have thumbnails/duration/summary; news has date/headline/summary and selective AVIF art; testimonial links retain attribution. Exact destinations and visual variants are in page specs and website-map.md.
- **Observed styling/states:** Feature heading uses Sagittaire Text, type-lg, weight 500, tracking −0.04em. Class indicators declare a 2 px primary focus outline with negative offset. Compact testimonial links use target=_blank/rel=noopener. Actual hover/pressed/keyboard activation are not exhaustively tested.
- **Proposed inputs:** Recorded href/content/attribution/media or miniature composition; limited variant definition reflecting actual templates. Product miniatures are visual demonstrations, not interactive private-product controls.
- **Responsive/motion:** Feature bento becomes DOM-order stack below 768; episode/testimonial horizontal strips remain distinct. Terminal caret has its own ANIM-TERMINAL-001 contract. News transition-colors is a class indicator, not measured hover timing.
- **Accessibility recommendation/relations:** Native anchor semantics, visible agreed focus, intelligible destination labels and duplicate-link policy; relate to grid, assets, carousel and content templates.
- **Risks/evidence:** Replacing HTML/SVG miniatures with screenshots loses anatomy; generic hover transforms are unsupported. Evidence: HOME-STRUCT-001, HOME-CSS-001, ASSET-DOM-001, INT-CARD-001.

## CONTRACT-PROOF-001 — Testimonial section and continuous tracks

- **Class/purpose:** Section/composition; combine nine prominent testimonial links, three compact tracks and decorative drifting Pucks/stars.
- **Anatomy/default:** Dark #05100f surface, cream large heading, prominent quotes in three columns desktop/stacked mobile; compact cards 320 px wide with 20 px padding. Duplicated track groups enable loops and must be distinct from unique testimonial records.
- **Proposed inputs:** Approved attributed testimonial records and observed decorative/track data. Track duplication is presentation state rather than duplicate content inventory.
- **Responsive/motion:** Mobile compact rows remain horizontal. Pucks start at left=−size−40 px and travel X0→100vw+size+80 px; bob Y−10→10/rotation face±10 degrees, face 90 normal/−90 reverse. Three testimonial loops end at translateX(−100%) with 1.25 rem gap/trailing padding. Horizontal mask transparent at ends/solid 6–94%; parent mask fades last 24 px vertically. Durations/delays are in animation-spec.md.
- **Declared alternatives/accessibility:** CSS hover pauses groups. Descendant focus-visible selector disables animation, enables overflow-x:auto, removes mask, hides duplicates and right padding. Reduced CSS uses that manual-scroll layout and hides drifters/disables bob/caret. These are confirmed declarations; actual hover/focus/preference activation and complete keyboard reachability remain untested.
- **Relations/risks/evidence:** Grid/title/cards/assets and clocks interact. Seam/clock/offscreen lifecycle remains unresolved despite known configured paths. Evidence: HOME-STRUCT-001, HOME-CSSOM-001, HOME-MOTION-001, ANIM-PROOF-001 and ANIM-PROOF-002; ACC-PROOF-001.

## CONTRACT-DOCS-001 — Documentation template and navigation/search

- **Class/purpose:** Template with navigation/search composites; reproduce the representative public reading experience and tested history.
- **Anatomy/default:** Near-white body rgb(250,250,248), system-ui article text; desktop H1 40/40 px and article width 704 px. Desktop sidebar is 280 px, sticky top 48 px, viewport-minus-48 height with overflow-y:auto. Mobile replaces sidebar with a 320 px full-height drawer and header search button.
- **Observed transitions:** Drawer opens and Escape closes. Search Docs opens a dialog/active combobox/listbox; query Orbs filters results; Escape closes. Next The Dial navigates `/docs`→`/docs/the-dial`; Back returns `/docs`. Copy Page click leaves the captured textual label unchanged; clipboard payload/icon/reset are unverified. Ctrl+K is a displayed hint, not an executed shortcut.
- **Proposed inputs:** Approved scoped content/navigation index, actual article links and search data contract. Public website reconstruction does not require independently recreating an unobserved search backend.
- **States/responsive/motion:** Search selection, empty/error/debounce, full focus cycle, More Markdown actions, scroll restoration and route mechanism are unknown. Drawer/search animation timing was not established.
- **Accessibility recommendation/relations:** Semantic article/headings/nav, labeled search and keyboard/focus contract once tested; relates to content templates, website-map.md and history tests.
- **Risks/evidence:** Do not generalize measured docs behavior to all routes; text rights and dynamic backend remain scoped. Evidence: PAGE-CONTENT-BROWSER-001, INT-DOCS-001, INT-DOCS-NAV-001, INT-DOCS-COPY-001, INT-DOCS-HISTORY-001.

## CONTRACT-FOOTER-001 — Marketing footer directory

- **Class/purpose:** Composite; provide observed Product, Resources, Guides and Community groups plus legal/status/social entries.
- **Anatomy/default:** Homepage footer measured y6283.76/h294.50 at baseline 1440; padding 56/59.01 px; Amp wordmark 120×61.49 px. Destination ledger is in website-map.md.
- **Proposed inputs:** Recorded group labels/links and approved wordmark; maintain explicit internal/external boundaries.
- **Responsive/states/motion:** Groups restack on mobile; exact spans/boundaries remain unknown. Link interaction follows native navigation; no motion is confirmed, which does not prove absence. Actual hover/focus styles require remaining inspection.
- **Accessibility recommendation/relations:** Semantic footer/navigation grouping, accessible wordmark/link names and clear focus; shared route graph and asset dependencies.
- **Risks/evidence:** A sampled extra zero-width grid track is not a new visible group. Evidence: HOME-STRUCT-001, HOME-CSS-001, RESP-MATRIX-001.

## Supporting-page control boundaries

Pricing tier tabs, single-open FAQ and Models payment context are observed distinct composites, not one generic selector component. Proposed data/state APIs should remain local until actual reuse is established. Contracts and measured state changes are INT-PRICING-001, INT-FAQ-001 and INT-MODES-001 in interaction-spec.md. Full reverse/keyboard/persistence/timing behavior is unresolved; related future cases are ACC-PRICING-001 and ACC-MODES-001. Pricing geometry and supporting-page breakpoint coverage remain partial.

## Shared acceptance and unresolved boundaries

All contracts require evidence-linked future tests in [acceptance-criteria.md](acceptance-criteria.md). Unknown control/motion/focus variants must be resolved or explicitly accepted as a fidelity limitation before implementation sign-off. Media/font download and permission limits remain in [asset-inventory.md](asset-inventory.md). Component boundaries above derive from observed structure; provisional input APIs remain recommendations. Any further structure requires actual route/template evidence.
