# PAGE-HOME-001 — Observed homepage anatomy

Reference: https://ampcode.com/. Page title: Amp: Coding agent and dev environment built for the frontier. Priority: P0. Entry points include direct navigation and marketing logo/home links. The page has eight scrollable sections plus a footer.

Core measurements are in [home-sections.json](../evidence/measurements/home-sections.json). Unless noted otherwise, coordinates use the ordinary 1440 × 900 viewport, with a 1425 px layout width and DPR 1. Dynamic control states can change document height. All sections were visually inspected; durable captures do not cover every lifecycle state or viewport. See [design-system.md](../design-system.md), [interaction-spec.md](../interaction-spec.md), and [animation-spec.md](../animation-spec.md) for shared values and behavioral contracts.

## SECTION-HERO-001 — Distributed work proposition

**Purpose — INFERRED:** communicate that agents can continue independently of the user's machine and reduce perceived coordination overhead.

**Visual and semantic structure:** a dark atmospheric section spans the page width. It contains grid navigation, an isolated 560 px stage, a central H1 with supporting copy and CTA, and an explanatory strip across the width. The single H1 includes invisible phrase-measurement layers marked aria-hidden, a changing screen-reader-only current phrase, and animated word spans marked aria-hidden. Inline italic words provide emphasis. Absolute, rounded prompt bubbles appear behind and around the text, varying in scale, depth, blur and position. Typography, colors and glow values are recorded in the design system.

**Geometry:** section extent y = 0–702 px; header height 80 px. Heading rectangle: x = 426.13, y = 276.03, width = 572.73, height = 47.80 px. Supporting copy: maximum width 672 px; x = 376.5, y = 339.84, height = 50.13 px. The centered orange Start CTA measures 78.75 × 38 px. The navigation logo has SVG viewBox="0 0 281 144" and displays at 62.44 × 32 px. Sign In uses an outline; Start uses a fill. Header links include Chronicle, Docs, Models, Pricing, About, Sign In and Start. The logo links home. The proposition strip has a border under the stage, with horizontal padding 24 px and vertical padding 20 px according to classes.

**Actions:** Start leads to /auth/sign-up. The orb explanation word and proposition strip expose a popover. Mobile navigation uses an overlay.

**Motion:** ANIM-HERO-001 and ANIM-STORM-001. The heading rotates through eight phrases; it is not split into individually animated characters. Loaded CSSOM confirms an entrance from translateY(26 px) to 0 with opacity 0→1, and an exit from 0 to −18 px with opacity 1→0. Emphasis declarations use skewX(+14°)→0 for new text and 0→skewX(−14°) for old text. HOME-TIMED-DOM-001 additionally confirms sampled outgoing animations of 300 ms with ease and 0/40/80/120 ms delays for four outgoing words; a two-word sample uses 0/40 ms. Exit origins were consistent with node centers, distinct from the entrance origin of 0 px 100%. Phrase insertions were approximately four seconds apart within the sampled window; an exact scheduler or full-cycle duration is not established. These are declarations and timed DOM reads, not captured intermediate frames; configuration and runtime limits are in the animation specification and HOME-CSSOM-001.

**Responsive behavior:** the header menu replaces desktop links below 768 px. The mobile hero reserves two heading lines. Background particles were present at 390 px during a later runtime phase; a sparse first screenshot does not justify hiding them on mobile.

**Evidence and confidence:** HOME-STRUCT, HOME-CSS, HOME-CSSOM-001, HOME-TIMED-DOM-001, HOME-WRAP, INT-POPOVER, INT-MENU and RESP. Measured structure, inspected declarations and sampled computed timings have high confidence; complete choreography is partial. Open questions: full-cycle scheduling and exit-node removal timing, transient clipping, offscreen lifecycle, font readiness and runtime reduced-motion behavior.

## SECTION-DEMO-001 — Long-form product proof

**Purpose — INFERRED:** substantiate the opening proposition with a real workflow.

**Structure:** eyebrow, H2 linking to /docs/using-amp/a-day-in-amp, six chapter-shortcut buttons, a custom screencast stage, chapters, controls and transcript. The authenticated product shown inside the media is a recorded demonstration.

**Geometry:** y = 702 px; height = 942.85 px. Heading and copy are centered; the outer section grid has five tracks. Default player rectangle: x = 80.60, y = 941.52, width = 1263.80, height = 647.34 px. Within the stage, the screen and camera panes use 78.2143% and 20.7662% widths; the camera starts at 79.2338%. Stage aspect ratio is 4909.587 / 2002; corner radius is .6110cqw. These values describe the measured inline composition, not the videos' intrinsic resolutions.

**Typography and assets:** type-xl Sagittaire heading and monospace eyebrow. Two distinct MP4s and posters are recorded in the asset inventory.

**Actions and states:** shortcuts at 0:16, 4:07, 8:14, 11:46, 16:24 and 22:52 seek and play. The timeline has 15 chapters. Controls include play, mute, speed, captions, sidebar, webcam and fullscreen. Initial duration is 26:05 with a 1× rate. The desktop sidebar starts closed; opening it produces grid tracks of 272 px + 967.797 px. Mobile exposes a Chapters control and a collapsed Transcript; expansion revealed 70 visible timestamp buttons.

**Motion:** media playback is synchronized. Playback was verified at 16.31 s and at 1.5×. This is moving media, not a decorative image. A later snapshot showed a pause at 32.65 s; its cause remains unresolved.

**Evidence and confidence:** INT-VIDEO-001. Tested states have high confidence. Errors, fullscreen, mute, recovery and drift correction remain unknown.

## SECTION-ORBS-001 — Capability bento

**Purpose — INFERRED:** answer practical questions about previews, review, events, teamwork and terminal access.

**Structure:** an introduction with linked H2, two paragraphs and two learning links precedes five whole-card anchors. Cards combine captions with layered HTML/SVG illustrations. All five contain zero image/video nodes; their SVG-node counts are 11, 26, 7, 7 and 6. Product miniatures are compositions rather than fetched screenshots.

**Geometry:** y = 1644.85 px; height = 946.58 px. The introduction occupies the first track at x = 59.01 with width 326.89 px. Cards occupy the four tracks to its right.

| Card | x / y, px | Width / height, px | Grid span |
|---|---|---|---|
| Portal | 385.90 / 1701.85 | 544.63 / 303.79 | 2 × 2 |
| Review | 930.52 / 1701.85 | 435.47 / 416.29 | 2 × 3 |
| Event | 385.90 / 2006.64 | 544.63 / 224 | 2 × 2 |
| Multiplayer | 930.52 / 2119.14 | 435.47 / 416.29 | 2 × 3 |
| Terminal | 385.90 / 2231.64 | 544.63 / 303.79 | 2 × 2 |

**Typography and states:** tight type-2xl H2. Feature H3s use type-lg, weight 500 and Sagittaire Text, with a short tick and muted supporting copy. Classes declare hover/focus primary-heading treatment and a 2 px focus outline; actual hover-animation timing was not tested. Exact card destinations are in the navigation map.

**Responsive behavior:** one-column stack below 768 px; three tracks on tablet; asymmetric desktop bento.

**Motion and evidence:** terminal caret uses a 1 s linear loop. Other illustration motion and lifecycle remain incomplete. HOME-STRUCT, HOME-CSS, ASSET-DOM and RESP support high confidence in structure/geometry and partial confidence in animation.

## SECTION-PROOF-001 — Orbservations

**Purpose — INFERRED:** provide social proof of changed work habits.

**Structure:** #orbservations; decorative stars and drifting Pucks; eyebrow; large balanced H2; introduction; nine prominent testimonial anchors; and three continuous rows of compact linked cards with duplicated track groups. Links lead to external X, Reddit and blog destinations. Compact-row links have target="_blank" and rel="noopener". Preserve attribution and distinguish decorative repetitions from unique records.

**Geometry and surfaces:** y = 2591.43 px; height = 1491.77 px; background #05100f. Introduction classes specify max-w-6xl, horizontal padding 24 px and top padding 112 px on desktop / 80 px on mobile. The large heading uses type-3xl, −.05em tracking and cream text. Main quotes use three columns on desktop and stack on mobile, as visually observed. Compact-card classes specify 320 px width, 20 px padding, rounded-md, a cream border at 15% opacity and surface at 3% opacity. Row gap is 20 px; top margin is 64 px.

**Motion:** ANIM-PROOF-001 and ANIM-PROOF-002; exact loops are in the motion specification. The mobile section-height sample was 2213.53 px in an altered media state. Compact rows remain horizontal and extend beyond the visible section; this is not document-level overflow. HOME-CSSOM-001 confirms declarations that pause groups on hover and, with a focused mini-card selector or reduced-motion preference, disable animation, expose manual horizontal scrolling, remove the mask, hide duplicates and remove right padding. Runtime activation of these selectors was not tested.

**Evidence and open questions:** structure and CSS-declaration confidence is high; runtime lifecycle coverage is partial. Actual hover/focus activation, interruption, keyboard exposure of duplicated links and star movement remain unresolved. No exact parallax relationship is asserted.

## SECTION-TOKENS-001 — Subscription bridge

**Purpose — INFERRED:** address cost by offering an existing-subscription connection.

**Structure:** the wrapper includes a hidden heading variant with a zero rectangle. The visible dark row has a left eyebrow/H3/copy with Link ChatGPT and See Amp Tiers actions; the right side contains a four-item usage list and footnote. The hidden wrapper heading is not a second visible section. A decorative blurred orb band sits behind the grid.

**Geometry:** y = 4083.20 px; height = 456.59 px. Dark palette, left/right division and multiple decorative vertical rails.

**Actions:** /settings/model-routing?add=chatgpt is an authentication boundary; other destinations are /pricing and /docs/the-dial.

**Motion:** band movement is not established. A computed transform: none sample does not prove that it stays static.

**Responsive behavior:** left copy/actions precede the stacked usage list on mobile.

**Evidence and confidence:** HOME-STRUCT, HOME-CSS and P3 web results. Visible content has high confidence; the decorative lifecycle remains unknown.

## SECTION-EPISODES-001 — Orbs from Zero

**Purpose — INFERRED:** teach setup through a staged sequence.

**Structure:** left header with linked H2, summary, Start Watching and previous/next controls; right track with four ordered episode links, each containing a thumbnail, duration, H3 and summary. The track scrolls horizontally.

**Geometry:** y = 4539.78 px; height = 427.45 px; bottom padding 0. The header occupies the first track on the left. Desktop episode-card width is 326.89 px. The thumbnail measured 283.70 × 159.58 px at the actual 1440 px viewport and has a 16:9 ratio. The 283.70 px thumbnail width is not a mobile-card measurement; an earlier viewport request had applied to another selected tab.

**Actions:** Next moved the track by one card, approximately 327 px in the sample, and activated Previous. Each episode link has a documented destination.

**Responsive behavior:** below 768 px, the introduction sits above the horizontal cards. This is not an infinite carousel.

**Motion and evidence:** scroll timing and snapping remain unknown. INT-EPISODES and ASSET-DOM support high confidence in the measured scroll action; dragging and end conditions have partial coverage.

## SECTION-CLI-001 — Local and remote terminal continuation

**Purpose — INFERRED:** retain terminal users and show other work surfaces.

**Structure:** left label/H2/platform selector/command-copy control; right pair of feature cards with screen media and captions. The default command is for Mac/Linux/WSL; Windows and Homebrew alternatives exist. A native select appears in the narrow header track at 1440 px despite hidden platform-button copies. The wider documentation CLI row shows button variants. Selector variation cannot be attributed to viewport width alone.

**Geometry:** y = 4967.23 px; height = 539.20 px. The introduction occupies the first track, with two illustrations to the right; cards stack on mobile.

**Assets and actions:** two MP4 miniatures were inspected after scrolling. Root's 1440 px DOM inspection confirms loop=true, muted=true, autoplay=false and native controls=false for both. Those attributes do not establish the runtime visibility/playback trigger or uninterrupted looping. Article links lead to /docs/cli and /docs/cli/remote-control. See INT-INSTALL-001. A newer Windows-command click at 1440 px produced a Copied to clipboard toast with Dismiss and replacement of the adjacent icon (INT-INSTALL-COPY-002). The copied payload remains unverified. Installer commands were inspected as content and were never executed. The long command's inner element declares a .5s linear transform transition; a hover-driven scrolling trigger was not confirmed.

**Evidence and confidence:** HOME, INT, ASSET and INT-INSTALL-COPY-002 observations. Selection behavior and the tested copy toast/icon state have high confidence. Clipboard payload, icon reset/feedback lifetime and copy errors remain unknown.

## SECTION-NEWS-001 — Announcements

**Purpose — INFERRED:** signal continuing product development and encourage return visits.

**Structure:** left label/H2; six article anchors to the right, with short titles/summaries and dates. Selected rows have background art; a final link opens more news.

**Geometry:** y = 5506.42 px; height = 777.34 px; section vertical padding 0. Classes specify 24 px vertical row padding and border separators. Desktop uses a date column alongside title/copy; these stack on mobile.

**Assets and actions:** three AVIF backgrounds are in the asset inventory; the other rows use flat surfaces. Links cover six news routes and /chronicle.

**Motion and evidence:** transition-colors classes are confirmed; actual hover state and timing remain unknown. HOME-STRUCT and ASSET support high confidence in structure and partial coverage of state visuals.

## SECTION-FOOTER-001 — Directory and trust

**Structure and purpose:** large Amp wordmark, operational-status label, legal links, and Product, Resources, Guides and Community groups.

**Geometry:** y = 6283.76 px; height = 294.50 px; padding 56 px vertically / 59.01 px horizontally. The sampled grid includes an extra 0 px track. Wordmark dimensions are 120 × 61.49 px.

**Responsive behavior:** groups restack; exact transition widths were not measured.

**Actions and motion:** canonical routes are in the route ledger. Status, social and YouTube links are external P3 entries. No footer motion was confirmed; this does not prove that none exists.

**Evidence and confidence:** HOME-STRUCT and HOME-CSS. Href inventory confidence is high; responsive geometry coverage is partial.
