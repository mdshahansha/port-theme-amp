# Responsive contracts

The measured matrix and adjacent-width tests are CONFIRMED by RESP-MATRIX-001 and RESP-BOUNDARY-001. Tests used viewport resizing with DPR 1; they did not emulate a real device or touch input. See [responsive-matrix.md](responsive-matrix.md).

## Measured transition points

At 767 px, marketing navigation links have zero rectangles and the menu measures 48 × 48 px. At 768 px, navigation links appear, the menu has a zero rectangle, and the section grid changes from one column to three equal tracks. At 1023 px the grid still has three equal tracks; at 1024 px it changes to five tracks with proportions 560:560:373:373:373. The 639/640 px samples do not change this composition. Other component-specific boundaries remain UNKNOWN.

Hero font size changes fluidly: 36.295 px at 767 px → 36.32 px at 768 px. It does not jump at the navigation breakpoint.

## Hero composition and wrapping

The hero stays centered. Mobile uses 24 px inner gutters and 16 px supporting copy; desktop copy has a maximum width of 672 px. Invisible grid layers reserve space for the longest H1 phrase, preventing shorter current phrases from collapsing the heading height.

At 1440 px, all eight phrases occupy one line. At 390 px, five remain on one line: Juggle less; Ship more; Agents that keep going; Share with teammates; Forget worktrees. The other three wrap as follows; / denotes a measured line break:

- Send prompt, / close laptop
- Continue from / your phone
- Continue / while you sleep

At 360 px, the reserved H1 height is 59.61 px; individual phrase wrapping was not separately recorded. Italic emphasis and word segmentation must survive reflow. Mobile bubbles were present during a later runtime phase; a sparse first snapshot does not establish hidden motion.

## Homepage section transformations

The feature bento collapses into DOM order: introduction, portal, review, event, multiplayer and terminal. The baseline mobile document is approximately 9600 px high, versus 6578 px at 1440 px; heights depend on interaction/media state. Main testimonials stack while three compact tracks remain horizontal and clipped within the section. Episodes retain a horizontal strip, with the header above it on mobile. CLI cards stack. News dates and headings stack. Footer groups restack, but complete column-span measurements remain unavailable.

The desktop episode card is 326.89 px wide. Its thumbnail measured 283.70 × 159.58 px at the actual 1440 px viewport. That thumbnail measurement was previously associated with a mobile viewport request that applied to a different selected tab; it must not be used as a mobile width.

## Homepage player

At 390 px, the player showed a 319 px single-column layout. Desktop starts with a single column and closed sidebar; opening the sidebar at 1440 px produces tracks of 272 px + 967.797 px. Mobile uses a Chapters button and collapsed Transcript. Desktop captions/rate controls were not visible in the narrow state; the alternative Settings behavior remains unresolved. Screen and camera retain a composite stage aspect ratio; a cropped single video would change the observed composition.

## Supporting pages and documentation

Supporting marketing pages use cream/black surfaces independently of the homepage's dark palette. Pricing changes from four desktop cards to one column at 390 px. Its initially measured H1 was 96 px at 1280 × 720, versus 72 px on mobile; no 1440 px pricing-heading measurement is asserted. The initial 1280 px viewport had a 1265 px layout width. Pricing's Gigawatt selection changed the displayed monthly price from 20 to 200, and its FAQ showed one open item at a time; these are state changes, not breakpoint evidence.

App's H1 was 72 px at 1440 px and wrapped across lines on mobile; the exact mobile font size was not recorded. The Orbs marketing H1 measured 60 px at 1440 px and 40 px at 390 px. Its sticky-sidebar/media transformation was not fully measured.

Documentation has a near-white body and a sticky 280 px sidebar at 1440 px. At 390 px, it hides that sidebar and exposes a 320 × 844 px drawer plus a header search button. The search panel measured 374 × 412 px. The Next link to The Dial and browser Back were tested; complete focus containment and scroll-lock behavior remain unresolved.

## Remaining unknowns

Loaded CSSOM partially establishes declared reduced-motion alternatives: title entrance/emphasis animations are disabled and exiting words hidden; storm transitions become opacity-only; drifters are hidden and bob/caret motion disabled; testimonial tracks use manual horizontal scrolling with masks/duplicates removed. A focused mini-card selector declares the same track arrangement, while hover declares animation pause. HOME-CSSOM-001 and the animation specification record these declarations. Actual preference/hover/focus activation and title-scheduler behavior were not tested.

Reduced-motion runtime behavior could not be emulated with the available capability. Real touch/hover equivalence, mobile decorative-cycle policy, landscape phones, high DPR, orientation changes, most supporting-page breakpoints, scroll locking, full focus containment and overflow across all open states remain UNKNOWN. Proposed responsive checks in the verification plan are future work, not passed tests.
