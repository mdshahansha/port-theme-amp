# Future high-fidelity verification plan

This document defines **future implementation tests**, not completed tests. No app has been built. Root findings are traceable through [evidence-index.md](evidence-index.md); pass/fail cases are in [acceptance-criteria.md](acceptance-criteria.md).

## Current evidence limitations

Screenshots were viewed but not persisted, asset download was refused, reduced-motion emulation/frame recording were unsupported, and exact title scheduler/full cycle/scroll mechanisms remain unknown. Loaded CSSOM confirms paths, font mappings and alternative selectors; timed DOM confirms sampled exit metadata and approximate cadence. Those methods improve the specification but do not replace visual frames or actual preference/input tests. Recover missing sources or explicitly accept the corresponding verification limits before sign-off.

## Baseline capture protocol

1. Use a fresh browser session and record investigation/capture timestamp in Asia/Calcutta, browser/version, OS, viewport, DPR, zoom, color scheme, reduced-motion setting, locale, authentication, hardware/network conditions and unsupported capabilities.
2. Load reference and future implementation at identical routes/content/conditions. Capture the unscrolled/unhovered first view before testing controls.
3. Record font/media readiness and animation state. Compare first-frame and settled-state captures separately; do not wait a convenient arbitrary delay and assume it is the reference's settled state.
4. Record CSS-pixel scroll position and key anchor bounds. Preserve viewport/section context and raw evidence, not only crops.
5. Capture all required viewports: 1920×1080, 1440×900, 1280×800, 1024×768, 768×1024, 390×844, 360×800. Add 767/768 and 1023/1024 px widths to bracket confirmed grid transitions, retaining recorded heights.
6. Name captures by route, viewport, input/state, scroll position and frame time when applicable. Connect results to stable page/section/animation/interaction IDs.

Never treat an image resize as viewport emulation or an inaccessible file as captured evidence.

## Visual verification

Compare section boundaries, container/grid geometry, alignment, spacing, text wrap, measured font values, color/surface/borders, media aspect/crop, overlay positions and document overflow.

- Exact computed tokens must agree when source measurements are exact. Approximate/inferred tokens retain their uncertainty until better evidence is captured.
- **Proposed project tolerance:** major geometry within 2 CSS px at matching browser/DPR. This is a future acceptance recommendation, not a discovered reference value; calibrate before use, especially accumulated page drift.
- Heading line breaks and ordering must match at each measured width; a close overall image score cannot excuse wrong wrapping.
- Generate difference images and region measurements if supported. Calibrate thresholds against font rasterization, anti-aliasing, dynamic media and timing variance. Do not assign an arbitrary global pixel percentage and call the site correct.
- Review every material structural difference manually, including those in a small area of an otherwise matching page.

## Motion verification

For each important effect, bind the test to [animation-spec.md](animation-spec.md) and [animation-timelines.md](animation-timelines.md), including trigger, initial/intermediate/final states, travel/opacity/clip values, timing/overlap, reversal/reset, repeat and interruption.

- The observed title entrance is per-word, 560 ms, `cubic-bezier(0.16, 1, 0.3, 1)` (HOME-CSS-001). The four-word sample has 280/340/400/460 ms entrance delays (HOME-MOTION-001). Verify these computed values plus actual intermediate frames; do not generalize delays to every phrase or verify only the final heading.
- Loaded CSSOM confirms entrance opacity 0→1/translateY 26→0 and exit opacity 1→0/translateY 0→−18 px. Timed DOM confirms exit 300 ms, ease, center origin and four-word delays 0/40/80/120 ms; entrance origin is 0% 100%. Test these distinct paths/origins and both emphasis skew paths.
- 495 caller-clock-bracketed DOM reads over 12,014 ms support approximately four-second new-phrase cadence and coexistence of old/new nodes. This is not page T0, an exact configured 4000 ms timer or a recorded full cycle. Compare approximate cadence under matched conditions; exact scheduler/full-period/pause/offscreen lifecycle remains unresolved.
- Storm entrance/exit, Puck travel/bob, testimonial −100% endpoint/masks and declared hover/focus/reduced alternatives are now specified from CSSOM. Verify configuration and runtime activation separately; unknown generation/seams/lifecycle cannot pass from declarations alone.
- **Proposed timing tolerance:** ±50 ms or ±5% of measured duration, whichever is larger, after timestamped capture calibration. This is a project proposal, not a reference observation.
- Observe representative frame checkpoints relative to actual trigger, including 0/150/300/500/750/1000/1500 ms when useful. These checkpoints do not establish the effect's duration.
- For scroll effects, record position/progress and element bounds instead of describing them only as “fade” or “parallax.” Test slow/medium/fast/reverse scroll, repeated entry, mid-page reload, resize and back navigation.
- Test reduced-motion once supported. Confirmed CSS disables title entrance/emphasis and hides exits; storm keeps timing with opacity-only paths; proof becomes manual horizontal scroll without drifters/duplicates/mask, bob/caret animations disabled. Current inspection confirms these rules but not runtime rendering or phrase scheduling.

## Interaction and navigation verification

Each important interaction must receive at least one future case mapped to its interaction ID, plus applicable state variants. Case fields: source evidence, route/component, conditions, start state, action, expected state/destination, timing/tolerance, reversal, input mode, recorded result and evidence.

- Menu: repeat open/close, outside click, Escape and Tab-to-Home with a 1 px foreground ring are confirmed. Preserve this subset. Separately test the unresolved complete keyboard sequence, focus restoration/trapping, scroll lock, resize back to mobile and input equivalence. At 768 px resize the reference hides the trigger while aria-expanded remains true; any usability correction must be a documented decision.
- Installer: platform selection, exact command and selected state; later Windows copy produces toast/Dismiss/icon replacement (INT-INSTALL-COPY-002). Test UI feedback separately from exact copied payload. Current clipboard accessor returned earlier docs content, so payload success and mismatch cause are unknown. Feedback lifetime/dismissal/repeat/error/persistence remain untested.
- Dual media: observed screen/camera seek/rate synchronization and custom controls; confirm both loop/autoplay/native-controls=false, screen muted=false/camera=true. CLI miniatures separately have loop/muted=true and autoplay/controls=false; their viewport playback trigger remains unconfirmed. Test loading/end/pause lifecycle only against resolved evidence.
- Carousel: initial position, observed horizontal input/controls, bounds, responsive behavior, keyboard/touch equivalents and repeated changes. Snap or drag behavior is not presumed.
- Navigation: internal routes, CTA destinations, anchors, external/authenticated boundaries, direct entry, refresh, back/forward and recorded scroll restoration. Documentation `/docs`→`/docs/the-dial`→Browser Back `/docs` is confirmed; scroll restoration and routing mechanism are not. An `href` alone does not prove other redirect/history behavior.
- Stay within publicly observable non-destructive behavior. No real purchases, registrations or authenticated bypasses.

## Responsive and accessibility verification

At every viewport and boundary, check grid track count/ratio, spans/order, title size/wrap, spacing/crop, overlay/media/carousel/installer composition, touch targets and unintended overflow. The title's measured declaration is `clamp(2.07rem, 1.07rem + 2.5 * min(1vi, calc(1920px / 100)), 7rem)` with measured rem base 16 px. Verify actual viewport dimensions and separate that fluid rule from discrete grid/nav transitions. Current viewport clicks are not real touch/gesture evidence.

Use semantic/label/landmark/heading inspection and automated checks where supported, plus manual keyboard/focus/touch/reduced-motion tests. Native control semantics and accessible focus behavior are future implementation recommendations; untested reference focus behavior must not be presented as a confirmed contract. Record intentional accessibility improvements separately from fidelity differences.

## Performance verification

No reference performance score/baseline has been measured here. First capture comparable loading and main-thread/frame/media traces on an agreed device/network profile; then set budgets.

Check content stability during fonts/media loading, largest visible content readiness, media decode/synchronization, scroll/frame responsiveness, continuous title work and navigation cleanup. Do not fabricate Core Web Vitals, FPS, CPU or GPU measurements. Require no agreed regression against the measured baseline, with exact thresholds selected only after instrumentation is reliable.

## Shared-foundation regression policy

| Changed area | Required affected checks |
|---|---|
| Fonts/typography | All headline wraps, section heights and content templates at required widths |
| Navigation/overlay | All entry points, route destinations, focus/keyboard states, mobile widths and open-menu resize |
| Global color/CSS | Every template and component state; diff review for unintended inherited changes |
| Motion lifecycle/utilities | Every dependent animation's trigger, intermediate frames, interruption, reverse/reset and reduced-motion |
| Grid/container/spacing | Section boundaries/spans, full-page accumulated drift, carousel/media overflow |
| Breakpoints | Required samples, exact boundary brackets, visible order/input behavior and resize during active state |
| Asset source/loading | Aspect/crop/typography readiness, loading stability, synchronization and all routes using the asset |

## Result and sign-off rules

Store expected/measured values, pass/fail criteria, result captures/logs, discrepancy severity and unresolved questions per requirement. Fail critical cases when evidence is missing; do not turn UNKNOWN into PASS. An implementation can only be accepted within explicitly stated evidence and rights limitations. [acceptance-criteria.md](acceptance-criteria.md) contains explicit mappings for every current motion/interaction inventory ID; any newly discovered ID must be mapped before handoff.

Discovery quality gates are evaluated separately in [README.md](README.md)/[progress.json](progress.json). This plan alone does not pass the discovery or implementation gates.
