# Technical decision records

All records are **PROPOSED FOR FUTURE IMPLEMENTATION**. No stack, dependency, code, or animation has been installed or implemented. Observed constraints are in [architecture-analysis.md](architecture-analysis.md); evidence is in [evidence-index.md](evidence-index.md).

## ADR-001 — Stack and rendering

- **Problem:** Establish a public site architecture without an existing application stack.
- **Constraints:** REPO-001 confirms an initially empty folder. Svelte/SvelteKit is inferred from reference indicators, not selected for the replacement. Public routes/templates and hosting constraints govern the choice.
- **Options/tradeoffs:** Static multipage generation minimizes runtime but may complicate interactive shared state; SSR/prerendered framework supports routes and content with client islands/components; client-only routing simplifies some state but increases loading and deep-link obligations.
- **Recommendation:** Select an SSR/prerender-capable approach after route scope and hosting are settled; retain the inferred reference family as an option. Do not choose a framework solely from source signatures.
- **Dependencies:** Final route/template map; hosting and browser support; approved asset strategy.
- **Risks:** Invented routes, broken direct entry/history, excess client runtime.
- **Verification:** Every scoped route loads by direct URL and refresh; browser history and scroll restoration follow measured contracts.

## ADR-002 — Animation orchestration

- **Problem:** Reproduce title motion precisely while avoiding invented sequence details.
- **Constraints:** Entrance 560 ms cubic-bezier(0.16, 1, 0.3, 1), sampled delays 280/340/400/460 ms, opacity 0→1/Y 26→0, origin 0% 100%. Exit computed 300 ms ease, sample delays0/40/80/120 ms, opacity 1→0/Y 0→−18 px, center origin. Emphasis skew/fades are 560 ms. Timed DOM measures approximately four-second phrase insertion, not exact timer/full-cycle. CSSOM alternatives are known; runtime preference/interruption/scheduler remain unknown (HOME-CSSOM-001, HOME-TIMED-DOM-001).
- **Options/tradeoffs:** CSS transitions/keyframes are compact for isolated transitions; Web Animations adds programmatic control; an orchestration library can coordinate complex sequences but adds dependency/runtime and lifecycle cost.
- **Recommendation:** Preserve confirmed CSS keyframes and separate entrance cubic-bezier from measured exit ease. Use observed insertion cadence as a measured behavioral constraint while investigating exact scheduler/lifecycle; do not present a candidate 4000 ms timer as a source fact. Select an orchestration library only if resolved coupling requires one.
- **Dependencies:** Animation timeline evidence, responsive wrapping, reduced-motion behavior, teardown rules.
- **Risks:** Converting approximate cadence into an exact source timer; applying entrance origin to centered exit nodes; clipping on reflow; duplicate/hidden-route timers.
- **Verification:** Initial/intermediate/final word states, sequence overlap, responsive reflow, rapid interruption and lifecycle cleanup.

## ADR-003 — Scroll architecture

- **Problem:** Preserve horizontal carousel and any confirmed scroll choreography.
- **Constraints:** Episode Next moves scrollLeft 0→327 px and enables Previous (INT-EPISODES-001). Homepage navigation is static in a measured scroll sample; supporting Orb navigation/media and docs sidebar have recorded sticky positions (HOME-SCROLL-001). Exact scroll mechanisms and trajectories are not established; pinning/scrubbing cannot be presumed.
- **Options/tradeoffs:** Native scroll preserves platform input and accessibility; observers provide discrete visibility triggers; controlled scroll timelines/libraries handle linked effects but create mobile/overflow/history obligations.
- **Recommendation:** Native document/carousel scroll as default; add measured effects only. Do not install a global smooth-scroll system during discovery or merely to create a familiar aesthetic.
- **Dependencies:** Scroll thresholds, snap/end behavior, reverse/re-entry/fast scroll evidence, touch/keyboard contracts.
- **Risks:** Trapped scrolling, invalid scroll restoration, unnecessary pin space or horizontal overflow.
- **Verification:** Fixed scroll positions/progress; reverse/fast scroll; history restoration; viewport resize and mobile input.

## ADR-004 — Component boundaries

- **Problem:** Reuse actual structure without over-abstracting unique motion.
- **Constraints:** Observed grid, title, overlay navigation, synchronized media, carousel, installer. Font inventory alone does not prove every text style is a reusable component.
- **Options/tradeoffs:** Whole-page markup duplicates changes; excessive primitives obscure section choreography; a small primitive/composite/template system balances reuse and local behavior.
- **Recommendation:** Share measured layout/type/control foundations and observed repeated templates. Keep section-specific motion local until real reuse is demonstrated.
- **Dependencies:** Component inventory and usage evidence; resolved interactions.
- **Risks:** Global state coupling; generalized carousel/menu behavior that differs from the reference.
- **Verification:** Shared-foundation regression across all affected routes and boundary widths; section contracts pass independently.

## ADR-005 — Responsive system

- **Problem:** Reproduce grid and title transformations as a system.
- **Constraints:** One column below 768 px; three at 768–1023; five at 1024+, ratio 560:560:373:373:373. Exact title variable is `clamp(2.07rem, 1.07rem + 2.5 * min(1vi, calc(1920px / 100)), 7rem)`, measured at rem base 16 px (HOME-CSS-001, RESP-MATRIX-001, RESP-BOUNDARY-001).
- **Options/tradeoffs:** Fluid rules prevent abrupt sizing; discrete queries encode actual layout changes; container queries can localize behavior but should not alter observed page-wide transitions.
- **Recommendation:** Model confirmed discrete grid/nav transitions separately from the exact fluid title rule. Reproduce individual section spans from page specs; do not derive a competing formula from sample sizes.
- **Dependencies:** Full seven-view matrix, boundary evidence, exact hero wrapping, overflow/cropping measurements.
- **Risks:** Assuming all sections share identical spans; scaling screenshots instead of actual viewports; hover-dependent touch behavior.
- **Verification:** Required viewports plus 767/768 and 1023/1024 px boundary checks; line breaks, content order and overflow.

## ADR-006 — Asset and font management

- **Problem:** Supply correct visual media with traceable provenance and loading behavior.
- **Constraints:** Asset download refused. Public availability is not reuse authorization. Loaded CSSOM maps TX-02-Variable to Berkeley Mono normal/italic (woff2-variations, swap, no declared axes/weight range), Sagittaire Display faces at 100/200/400/700 as recorded in architecture-analysis.md, and Sagittaire Text Light 300/Medium 500/Medium Italic 500, all swap. Three preload leads are confirmed; actual network-loaded subsets, TX-02 axes/range, readiness and licensing remain unknown.
- **Options/tradeoffs:** Authorized originals maximize fidelity; approved replacements reduce rights/dependency uncertainty but require renewed visual comparison; dynamic reconstruction can reproduce simple decoration but must not silently replace complex media.
- **Recommendation:** Maintain a manifest of approved sources/replacements, variants, dimensions, crop, loading priority, routes, declared video flags and permission classification. Resolve font rights before claiming exact typographic readiness. CLI loop=true is confirmed independently of its unknown playback trigger; both demo streams have loop=false.
- **Dependencies:** Asset inventory, declared font-face map, source permissions, actual loading/network subset evidence and media variants.
- **Risks:** Wrong font metrics alter every wrap; unsupported media format; broken remote dependency; copyrighted asset reuse assumption.
- **Verification:** Route asset checks, font readiness, intrinsic/display aspect ratios, media synchronization and loading captures.

## ADR-007 — Accessibility

- **Problem:** Preserve essential behavior with usable keyboard, focus, touch and motion alternatives.
- **Constraints:** Mobile overlay Escape/outside closure and Tab-to-Home with a visible 1 px ring are tested. Loaded CSSOM declares reduced-motion alternatives and testimonial hover/focus scrolling modes. Their runtime activation, complete menu trap/cycle/restoration/scroll lock and most keyboard behaviors remain unknown. Reference accessibility is not automatically compliant.
- **Options/tradeoffs:** Native semantics reduce custom behavior burden; custom controls allow visual precision but require full keyboard/state contracts.
- **Recommendation:** Use semantic controls/visible focus and implement confirmed reduced-motion/focus-scroll declarations with a tested runtime contract. Keep overlay lifecycle gaps separate. Document any accessibility improvement that diverges from reference behavior as a deliberate decision.
- **Dependencies:** Accessibility review and interaction contracts.
- **Risks:** Focus behind overlay, hidden scroll content inaccessible, unlabeled media controls, motion continuing despite user preference.
- **Verification:** Preserve the tested menu focus/dismissal subset, then manually test the remaining keyboard sequence, labels/landmarks/heading order, touch interaction, applicable automated checks and real reduced-motion behavior once supported. Viewport clicks are not proof of real touch equivalence.

Installer copy feedback requires a separate UI-versus-payload decision: a toast/icon confirms feedback, while the clipboard accessor mismatch leaves payload success unknown (INT-INSTALL-COPY-002). Future verification must assert the exact command copied and independently test toast/icon/reset/dismissal, rather than treating a success label as payload proof.

## ADR-008 — Performance

- **Problem:** Keep large type/media and continuous behavior responsive without fabricated targets.
- **Constraints:** No measured Core Web Vitals or frame baseline supplied. Dual media and font loading are potential workloads, not proven performance defects.
- **Options/tradeoffs:** Lazy loading saves work below fold but can delay observed entrances; priority loading aids above-fold content but increases contention; composited transforms can help motion but extra layers cost memory.
- **Recommendation:** Measure a reproducible reference baseline before setting numeric budgets. Prioritize actual first-view content, reserve media dimensions, and stop unneeded work when the component lifecycle requires it.
- **Dependencies:** Loading trace, device/network profile, animation lifecycle, font and media strategy.
- **Risks:** Layout shift, decode contention, synchronization drift, timers after unmount, excessive compositing.
- **Verification:** Comparable loading filmstrip/trace, layout-shift measurements where supported, frame consistency and media drift checks.

## ADR-009 — Test automation and fidelity

- **Problem:** Turn discovery into objective future acceptance tests.
- **Constraints:** No local test stack. Screenshot persistence, frame recording and reduced-motion emulation were unavailable in current discovery.
- **Options/tradeoffs:** Automated screenshot/state suites are reproducible but sensitive to rasterization/timing; manual behavioral review detects nuances but needs disciplined conditions; combined approach is stronger.
- **Recommendation:** Select tooling with the eventual stack. Map one case to every important interaction and motion contract; run screenshots at identical conditions and calibrated dynamic-content masks.
- **Dependencies:** Stable evidence/contract IDs, missing captures recovered, accepted tolerances, browser/device support.
- **Risks:** A matching final frame conceals wrong motion; uncalibrated pixel score hides structural drift; tests mirror guessed implementation.
- **Verification:** [verification-plan.md](verification-plan.md) and [acceptance-criteria.md](acceptance-criteria.md), with evidence requirements enforced.
