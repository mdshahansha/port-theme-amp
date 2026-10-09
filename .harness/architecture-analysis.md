# Architecture analysis

## Status and evidence boundary

Discovery documentation only. No application implementation or package installation has begun. This analysis distinguishes observed reference behavior, inferred technology, replacement requirements, and provisional implementation recommendations. It does not declare discovery complete.

Evidence IDs refer to [evidence-index.md](evidence-index.md). Browser-derived facts below were supplied by the root investigator. The local repository was inspected read-only before harness creation.

## Existing project assessment

**CONFIRMED — REPO-001:** `C:\Users\mdsha\Desktop\amp-port` initially existed as an empty directory, including hidden entries. `.harness/` was subsequently created for authorized discovery output. No application manifest, framework, language, dependencies, routing conventions, styling system, build tooling, testing infrastructure, or Git metadata was available in the initial snapshot.

**CONFIRMED — REPO-002:** At the final read-only review, `.git` was present and Git listed discovery harness files. No application files existed outside `.harness` and Git metadata. Git creation/checkpointing was not performed by the documented discovery commands; its provenance is not established here. This later metadata does not supply an application stack.

**UNKNOWN:** The future implementation stack, hosting environment, target browser support policy, and authorized asset sources. A stack must not be silently selected during discovery.

## Reference mechanisms

| Area | Finding | Classification and evidence | What remains unknown |
|---|---|---|---|
| Framework | DOM asset paths containing `_app/immutable` and `svelte-*` class signatures | **INFERRED:** Svelte/SvelteKit; HOME-STRUCT-001. Indicators support the family but do not prove exact version or build configuration. | Version, rendering mode, hydration boundaries, routing lifecycle |
| Layout | CSS grid layout; one column below 768 px, three columns at 768–1023 px, five fractional columns at 1024 px and above with ratio 560:560:373:373:373 | **CONFIRMED:** HOME-CSS-001, RESP-MATRIX-001, RESP-BOUNDARY-001 | Detailed per-section spans, intrinsic sizing and overflow constraints require page specs |
| Nested alignment | Grid/subgrid class indicators | **INFERRED:** subgrid intent from class indicators, HOME-CSS-001; only computed values explicitly recorded in evidence should be treated as confirmed | Exact nested element-to-track relations where computed evidence is missing |
| Fonts | Loaded CSSOM maps TX-02-Variable to Berkeley Mono normal/italic, format woff2-variations; Sagittaire Display Regular 400, Bold 700, Extralight 200, Extralight Italic 200, Thin Italic 100; Sagittaire Text Medium 500, Medium Italic 500, Light 300. All declare font-display:swap. Three preload hrefs were separately observed. | **CONFIRMED declarations:** HOME-CSSOM-001, HOME-CSS-001, ASSET-DOM-001 | Variable axes/weight range for TX-02, actual network-loaded face subsets, licensing and readiness timings |
| Title motion | Entrance opacity 0→1, Y 26→0, 560 ms cubic-bezier(0.16, 1, 0.3, 1), sample delays 280/340/400/460 ms; origin 0% 100%. Exit opacity 1→0/Y 0→−18 px, sampled 300 ms ease with 0/40/80/120 ms delays and center origin. New/old emphasis uses skew 14→0/0→−14 degrees and fades over 560 ms. | **CONFIRMED configuration/computed samples:** HOME-CSSOM-001, HOME-TIMED-DOM-001, HOME-CSS-001 | Exact scheduler/full cycle, continuous-frame trajectory/interruption and offscreen/resize lifecycle; sample stagger values apply to recorded word counts |
| Title cadence | 495 DOM reads over 12,014 ms bracket first-observed new phrases near 124–162, 4156–4192 and 8144–8172 ms; old/new nodes coexist. | **CONFIRMED sampled estimate:** approximately four-second insertion cadence, HOME-TIMED-DOM-001; not an exact 4000 ms timer or page T0 | Full eight-phrase period, exact scheduling origin/pause and reduced-motion runtime |
| Responsive title | `--type-3xl: clamp(2.07rem, 1.07rem + 2.5 * min(1vi, calc(1920px / 100)), 7rem)`; measured rem base 16 px. Floor 33.12 px; 65.12 px at 1920. | **CONFIRMED:** HOME-CSS-001, RESP-MATRIX-001, RESP-BOUNDARY-001 | Exact transient clipping/reflow during an active phrase change |
| Mobile navigation | Below 768 px: overlay opens/closes repeatedly; outside click and Escape close it; Tab reaches Home with a 1 px foreground ring. Resizing to 768 hides the trigger while aria-expanded stays true. | **CONFIRMED:** INT-MENU-001, RESP-MATRIX-001, RESP-BOUNDARY-001 | Complete focus cycle/trapping/restoration, scroll lock, return-to-mobile state and full positioning lifecycle |
| Media | Screen/camera chapter seek/play and 1.5× rate synchronize in tested samples. Both loop/autoplay/native-controls=false; screen muted=false, camera=true. Two CLI miniatures have loop/muted=true and autoplay/native-controls=false. | **CONFIRMED:** INT-VIDEO-001, ASSET-VIDEO-FLAGS-002 | Playback/viewport lifecycle, drift correction, media codec and complete loading/error states |
| Episode carousel | Four-card horizontal track; Next moves scrollLeft 0→327 px and enables Previous. | **CONFIRMED:** INT-EPISODES-001 | Snap/smooth timing, wheel/drag/key/touch controls, final disabled rules and exact reverse endpoint |
| Installer | Platform selection changes command; later Windows command click shows Copied to clipboard toast, Dismiss and icon replacement. Clipboard accessor instead returns prior documentation content. | **CONFIRMED UI feedback; UNKNOWN payload success:** INT-INSTALL-001, INT-INSTALL-COPY-002 | Clipboard/tool mismatch cause, icon/reset lifetime, failure/persistence/detection and repeat-copy behavior |
| Documentation history | Next navigates `/docs`→`/docs/the-dial`; Browser Back returns to `/docs`. | **CONFIRMED:** INT-DOCS-001 / INT-DOCS-HISTORY-001 | Scroll position and client-navigation mechanism |
| Declared motion alternatives | Reduced-motion CSS disables title entrance/emphasis and hides exit words, uses fade-only storm names, hides proof drifters/disables bob and caret, and exposes manual testimonial scrolling. Hover pauses testimonial animation; a focus-visible descendant selector switches tracks to manual scrolling without duplicates/mask. | **CONFIRMED declarations:** HOME-CSSOM-001 | Actual runtime reduced-motion/hover/focus activation, complete keyboard reachability and scheduler behavior |

The observed title values are specific measured behavior, not a general recommendation to animate all text. Reference technology indicators do not require the replacement to use the same framework.

## Replacement requirements

1. Preserve measured route/navigation contracts from [website-map.md](website-map.md) and [interaction-spec.md](interaction-spec.md).
2. Reproduce measured grids, title scaling, wrapping, font treatment, media composition, and overlay geometry at the viewport matrix and boundary widths.
3. Treat title progression, dual-media synchronization, horizontal scroll, and installer command state as behavioral contracts.
4. Develop coupled layout, motion, and interaction together per section, starting with the hero after shared foundations.
5. Keep unresolved timing, scroll, focus, media, asset and reduced-motion behavior visible in [unknowns.md](unknowns.md) rather than filling it with generic patterns.
6. Keep public website behavior separate from authenticated product/back-end functionality and irreversible flows.

## Provisional candidate architecture

**RECOMMENDATION, NOT IMPLEMENTED:** Choose the stack after the route/templates inventory, asset rights and hosting constraints are reviewed. A prerendered/SSR-capable public content architecture with small client interaction boundaries is a candidate, not a finding about the reference.

- Extract measured visual tokens and layout primitives once; keep their source confidence attached.
- Isolate the hero/title sequence, synchronized media, carousel, mobile navigation, and installer state into component contracts with explicit cleanup and interruption rules.
- Use CSS for measured transitions where it is sufficient. Evaluate an orchestration library only for confirmed dependencies that CSS/native APIs cannot reproduce reliably.
- Prefer native scrolling and grid behavior for the observed carousel/layout. Pinning, smooth-scroll overrides, or scroll scrubbing require confirmed requirements.
- Keep font/media provenance and route dependencies centralized, including approved replacements where rights or downloads are unavailable.
- Tie acceptance cases to stable section/animation/interaction IDs, not fragile incidental selectors from the reference.

Component boundaries and provisional data inputs are in [component-contracts.md](component-contracts.md). Decision options and tradeoffs are in [technical-decisions.md](technical-decisions.md).

## Technical/performance unknowns

No supported evidence establishes SSR versus CSR, client-side routing mechanism, route prefetching, image optimization, actual network-loaded font-face subsets/readiness beyond declared swap/preload leads, exact lazy-load thresholds, custom smooth scrolling, GSAP/Motion usage, long tasks, Core Web Vitals scores, or GPU compositing. Documentation Next/Back, loaded CSSOM face mappings, keyframes and alternative selectors are confirmed at their stated method level; they do not settle broader runtime mechanisms.

## Inspection limitations

- Asset download was refused; inspectable URLs/metadata do not establish local copies or reuse permission.
- Screenshots were viewed but not persisted. Do not cite a nonexistent local PNG as evidence.
- Reduced-motion emulation and timestamped frame recordings were unsupported. Loaded CSSOM nevertheless exposes confirmed reduced-motion declarations; runtime activation remains untested.
- Exact title scheduler/full cycle and scroll mechanisms remain unresolved; sampled cadence is approximately four seconds and sampled exit easing/stagger/origin are now confirmed.

These limitations constrain implementation readiness and quality gates; they are not evidence that the reference lacks the corresponding behavior.
