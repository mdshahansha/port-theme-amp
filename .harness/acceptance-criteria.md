# Future acceptance matrix

**Status: PLANNED, NOT EXECUTED.** No application exists for testing. The 40 cases below combine confirmed replacement constraints with clearly marked proposed future thresholds. All 26 current motion/interaction IDs map to cases; newly discovered important effects or controls must receive a mapping before handoff. Evidence IDs resolve through [evidence-index.md](evidence-index.md).

## Matrix

| Requirement ID | Reference behavior or requirement | Specification / target | Proposed method and pass/fail criterion | Priority / evidence required |
|---|---|---|---|---|
| ACC-SCOPE-001 | Reconstruct scoped public website only | website-map.md; navigation-graph.md / all routes | Every observed entry maps to a scoped route, template, external/authenticated boundary or explicit unknown; no invented routes | P0 / route and destination records |
| ACC-REPO-001 | Empty initial project; implementation prohibited in discovery | architecture-analysis.md / discovery folder | No application/package/configuration changes; progress implementation_started remains false | P0 / REPO-001 and filesystem review |
| ACC-GRID-001 | One column below 768; three at 768–1023; five at 1024+ | responsive-spec.md; page-specs / observed grid | Computed track counts match at required samples and 767/768, 1023/1024 boundaries | P0 / RESP-MATRIX-001, RESP-BOUNDARY-001, HOME-CSS-001 |
| ACC-GRID-002 | Desktop five-track ratio 560:560:373:373:373 | design-system.md; page-specs / observed grid | Ratios and documented spans agree within calibrated measurement tolerance; no assumption that every section uses all tracks identically | P0 / HOME-CSS-001 and section bounds |
| ACC-TYPE-001 | Sagittaire Display/Text, Berkeley Mono, system-ui; declared face/style/weight/swap and three preload leads | design-system.md; asset-inventory.md / text | Match measured roles/metrics and CSSOM face map including TX-02→Berkeley; verify approved sources/actual loaded subsets. Variable axes/range and licensing remain unresolved | P0 / HOME-CSS-001, HOME-CSSOM-001, ASSET-DOM-001, provenance |
| ACC-TYPE-002 | Exact title clamp; 33.12 px floor and 65.12 px at 1920 sample | responsive-spec.md; design-system.md / observed title | Match `clamp(2.07rem, 1.07rem + 2.5 * min(1vi, calc(1920px / 100)), 7rem)` at measured rem base 16 px, plus wrapping at each width | P0 / HOME-CSS-001, RESP-MATRIX-001, RESP-BOUNDARY-001 |
| ACC-VIS-001 | Section geometry and visual order | page-specs / all P0 sections | Proposed: major bounds within 2 CSS px under identical conditions; exact order, anchors, wraps and crop; tolerance calibrated before use | P0 / persisted reference and implementation captures/bounds |
| ACC-VIS-002 | Measured color/surface/detail tokens | design-system.md / all measured components | Exact computed values agree; estimated values explicitly retained or remeasured; material visual differences reviewed manually | P0 / HOME-CSS-001 and section evidence |
| ACC-MOT-001 | Per-word title entrance 560 ms, cubic-bezier(0.16, 1, 0.3, 1); four-word delays 280/340/400/460 ms | animation-spec.md; animation-timelines.md / ANIM-HERO-001 | Exact declared timing/easing/sample delays; intermediate trajectory matches beyond final frame; no generalization to every word count | P0 / HOME-CSS-001, HOME-MOTION-001 plus timestamped frames |
| ACC-MOT-002 | Exit 300 ms ease, four-word delays 0/40/80/120 ms, center origin, fade/upward 18 px; entrance origin 0% 100% | animation-spec.md / ANIM-HERO-001 | Match separate exit metadata/path/origin and emphasis skew paths; continuous trajectory/interruption still require frame tests | P0 / HOME-CSSOM-001, HOME-TIMED-DOM-001 and future frames |
| ACC-CADENCE-001 | Approximately four-second insertion cadence from 495 DOM reads over 12,014 ms | animation-timelines.md / ANIM-HERO-001 | Comparable cadence within agreed observational tolerance; do not assert exact 4000 ms timer/full eight-phrase period; full-cycle/offscreen/interrupt tests remain unresolved | P0 / HOME-TIMED-DOM-001 and matched future samples |
| ACC-MOT-003 | Important animation lifecycle | animation-spec.md / each listed effect | Trigger/sequence/repeat/reverse/interruption/final state agree; proposed duration tolerance ±50 ms or ±5% after capture calibration | P0 / effect metadata, trigger log and intermediate frames |
| ACC-SCR-001 | Scroll behavior/mechanisms incomplete | animation-spec.md; page-specs / relevant effects | Start/end/progress, scrub/pin/reset/reverse and history measured before acceptance; UNKNOWN cases cannot pass | P0 / scroll positions/bounds/captures |
| ACC-MENU-001 | Mobile overlay below 768; repeat open/close, Escape/outside closure; resize hides trigger while expanded=true | interaction-spec.md; component-contracts.md / navigation | Measured entries/geometry/closure reproduce; explicit decision addresses expanded=true at hidden trigger without silently changing reference facts | P0 / INT-MENU-001, RESP-BOUNDARY-001 and state evidence |
| ACC-MENU-002 | Tested Tab-to-Home ring; full keyboard/focus lifecycle untested | accessibility-review.md; interaction-spec.md / overlay | Preserve 1 px foreground ring and reachable Home; resolve full cycle/trap/restoration/scroll lock separately, with deliberate improvements documented | P0 / INT-MENU-001 keyboard/state logs; unresolved cases blocked |
| ACC-VIDEO-001 | Dual synchronized custom-control media; demo loop/autoplay/controls=false; camera muted, screen unmuted | interaction-spec.md; component-contracts.md / media | Recorded seek/rate/state and media flags match; 5 ms drift is one sample, not a tolerance; loading/end/pause lifecycle needs separate evidence | P0 / INT-VIDEO-001, ASSET-VIDEO-FLAGS-002 and state logs |
| ACC-CAR-001 | Four episode cards; scrollLeft 0→327 px; Previous enables | interaction-spec.md; component-contracts.md / episode track | Exact sampled state/change match; endpoints, smooth/snap/drag/keyboard behavior require separate evidence | P0 / INT-EPISODES-001 plus position/state evidence |
| ACC-INSTALL-001 | Platform-specific command state | interaction-spec.md; component-contracts.md / installer | Each platform yields its exact recorded command and selection state; no command execution; persistence/error states unresolved | P0 / INT-INSTALL-001 and platform/state records |
| ACC-COPY-001 | Windows copy displays toast/Dismiss/icon replacement; payload accessor returned prior docs content | interaction-spec.md; component-contracts.md / installer | UI feedback matches; independently verify exact command clipboard payload, dismissal/reset/repeat/error. Payload success/tool-site mismatch remains blocked, despite success text | P0 / INT-INSTALL-COPY-002 and independent clipboard/state evidence |
| ACC-INT-001 | All important controls have behavioral contracts | interaction-spec.md / all P0 interactions | One future case per interaction ID, with applicable hover/focus/pressed/open/loading/error/reversal/mobile states; safe rapid/repeated action cases pass | P0 / complete interaction-ID to test mapping |
| ACC-NAV-001 | Routes, CTAs, anchors and history | website-map.md; navigation-graph.md / scoped routes | Expected URL/outcome at click/direct entry/refresh/back/forward; external/auth boundaries documented; scroll restoration follows evidence | P0/P1 / destination/history observations |
| ACC-DOCS-HISTORY-001 | `/docs`→Next The Dial→`/docs/the-dial`→Back→`/docs` | interaction-spec.md; navigation-graph.md / docs | Exact recorded URL sequence; do not infer scroll restoration or router technology | P2 / INT-DOCS-001, INT-DOCS-HISTORY-001 |
| ACC-RESP-001 | Seven required samples plus boundaries | responsive-matrix.md / all P0 sections | Actual viewports inspected and captured; composition/order/wrap/crop/overflow match at all samples and transition boundaries | P0 / RESP-MATRIX-001, RESP-BOUNDARY-001, new paired captures |
| ACC-RESP-002 | Touch equivalents and active-state resize | responsive-spec.md; interaction-spec.md / interactive components | Match observed touch behavior; no meaningful action depends only on hover; repeated actions/resize during open/playing states meet agreed contract | P0 / touch-like/device and state evidence |
| ACC-RM-001 | CSSOM declares title/storm/proof/caret alternatives; runtime preference untested | accessibility-review.md; animation-spec.md / motion | Rules match declared alternatives; runtime rendering/scheduling/focus/manual scrolling remains BLOCKED until real preference/input testing | P0 / HOME-CSSOM-001 plus preference/input captures and logs |
| ACC-ASSET-001 | Important asset identities/provenance | asset-inventory.md; asset-dependency-map.md / all assets | Approved source/replacement, correct ratio/crop/display/loading and route dependency; public URL never implies permission | P0/P1 / asset metadata and authorization status |
| ACC-A11Y-001 | Semantic/accessibility requirements | accessibility-review.md / all scoped controls/templates | Applicable semantic/label/landmark checks and manual keyboard/focus/touch review pass; deliberate improvements documented separately | P0 / audit report plus manual sequences |
| ACC-PERF-001 | No measured performance baseline yet | performance-analysis.md / first load, scroll, media/motion | Establish comparable device/network baseline, then agree budgets; no new accepted layout-shift/frame/main-thread/media regressions | P0 / reliable traces/captures, not fabricated scores |
| ACC-REG-001 | Shared changes must not break completed routes | verification-plan.md / dependency matrix | Required affected viewport/route/state/motion checks pass after shared type/nav/CSS/layout/motion/breakpoint/asset changes | P0 / test run and discrepancy records |
| ACC-STORM-001 | Entrance 420 ms cubic-bezier, Y10→0/fade-in; exit 700 ms ease, Y 0→−4/fade-out | animation-spec.md / ANIM-STORM-001 | Match configured paths/timing and mobile presence; reduced fade-only declaration matches but runtime/generation/lifecycle untested; sample positions not fixed | P0 / HOME-CSSOM-001, HOME-MOTION-001 and frames |
| ACC-PROOF-001 | Known Puck travel/bob paths; three −100% track loops/masks; declared hover/focus/reduced modes | animation-spec.md / ANIM-PROOF-001, ANIM-PROOF-002 | Exact durations/delays/direction/paths/masks match; actual seams/hover/focus/preference/re-entry require runtime tests | P0 / HOME-CSSOM-001, HOME-MOTION-001 and loop/input captures |
| ACC-CARET-001 | Caret CSS blink 1 s linear infinite; reduced CSS animation none | animation-spec.md / ANIM-TERMINAL-001 | Match metadata/alternative declaration; blink duty cycle and runtime preference require further tests | P0 / HOME-CSS-001, HOME-CSSOM-001 and frames |
| ACC-CLI-MEDIA-001 | Two CLI MP4s loop/muted=true and autoplay/controls=false | animation-spec.md; asset-inventory.md / ANIM-CLI-MEDIA-001 | Approved media/composition/flags match; viewport play/pause/loading lifecycle remains unresolved | P0 / ASSET-DOM-001, ASSET-VIDEO-FLAGS-002 and state evidence |
| ACC-INSTALL-MOT-001 | Command inner transform transition 0.5 s linear | animation-spec.md / ANIM-INSTALL-001 | Match declaration; resolve trigger/travel/interruption before signing off motion | P0 / HOME-CSS-001 and trigger/frame evidence |
| ACC-BAND-001 | Blurred subscription band; settled wrapper has transform/animation none | animation-spec.md / ANIM-TOKENS-001 | Match observed visual state; child/JS/scroll lifecycle remains blocked until inspected | P0 / HOME-CSS-001 and future lifecycle evidence |
| ACC-CONTROL-001 | Transition/focus class indicators; settled popover has animation none | animation-spec.md; interaction-spec.md / ANIM-CONTROL-001 | Match measured states only; resolve hover/pressed/timing rather than treating classes as tested behavior | P0 / HOME-CSS-001 and future input-state captures |
| ACC-POPOVER-001 | Orb/proposition clicks open distinct 288 px explanations; Escape closes | interaction-spec.md / INT-POPOVER-001 | Correct measured content variant/bounds and Escape transition; remaining hover/outside/mobile/focus behavior unresolved | P0 / INT-POPOVER-001 |
| ACC-PRICING-001 | Megawatt→Gigawatt updates $20→$200/month and CTA; FAQ second closes first | interaction-spec.md / INT-PRICING-001, INT-FAQ-001 | Exact tested selected/expanded states and label/value changes; reversal/keyboard/timing require follow-up | P1 / PAGE-PRICING-BROWSER-001 and state observations |
| ACC-MODES-001 | With ChatGPT Sub pressed true; other option false | interaction-spec.md / INT-MODES-001 | Match recorded pressed styling/state; model data changes/persistence/keyboard remain unconfirmed | P1 / PAGE-P1-BROWSER-001 and state observations |
| ACC-DOCS-CONTROL-001 | Mobile drawer/search, Orbs query results, Escape; Copy Page click lacks durable text confirmation | interaction-spec.md / INT-DOCS-NAV-001, INT-DOCS-COPY-001 | Match tested open/filter/close states; full focus cycle/selection/copy payload/reset/error blocked pending evidence | P2 / INT-DOCS-001 |

## Inventory-to-case coverage

This is a mapping for future tests, not proof that contracts are fully measured or passed. All current inventory IDs are accounted for:

| Inventory IDs | Acceptance cases |
|---|---|
| ANIM-HERO-001 | ACC-MOT-001, ACC-MOT-002, ACC-MOT-003, ACC-CADENCE-001 |
| ANIM-STORM-001 | ACC-STORM-001, ACC-MOT-003 |
| ANIM-PROOF-001, ANIM-PROOF-002 | ACC-PROOF-001, ACC-MOT-003 |
| ANIM-TERMINAL-001 | ACC-CARET-001 |
| ANIM-VIDEO-001 | ACC-VIDEO-001 |
| ANIM-CLI-MEDIA-001 | ACC-CLI-MEDIA-001 |
| ANIM-INSTALL-001 | ACC-INSTALL-MOT-001 |
| ANIM-EPISODES-001 | ACC-CAR-001 |
| ANIM-TOKENS-001 | ACC-BAND-001 |
| ANIM-CONTROL-001 | ACC-CONTROL-001 |
| INT-NAV-001 | ACC-SCOPE-001, ACC-NAV-001 |
| INT-MENU-001 | ACC-MENU-001/002 |
| INT-POPOVER-001 | ACC-POPOVER-001 |
| INT-VIDEO-001 | ACC-VIDEO-001, ACC-INT-001 |
| INT-EPISODES-001 | ACC-CAR-001 |
| INT-INSTALL-001 | ACC-INSTALL-001 |
| INT-INSTALL-COPY-002 | ACC-COPY-001 |
| INT-CARD-001 | ACC-VIS-002, ACC-CONTROL-001, ACC-NAV-001 |
| INT-PRICING-001, INT-FAQ-001 | ACC-PRICING-001 |
| INT-MODES-001 | ACC-MODES-001 |
| INT-DOCS-NAV-001, INT-DOCS-COPY-001 | ACC-DOCS-CONTROL-001 |
| INT-DOCS-HISTORY-001 | ACC-DOCS-HISTORY-001 |
| INT-AUTH-ENTRY-001 | ACC-SCOPE-001, ACC-NAV-001; public boundary only |

## Measurement qualifications

- The 2 px geometry and ±50 ms/±5% timing tolerances are **proposed project thresholds**, not observed reference values. Tighten or recalibrate after capture capability and rasterization variance are understood.
- No SSIM/pixel-difference percentage, performance score, synchronization tolerance or exact full-cycle timer is fabricated. Exit ease is now measured; approximately four-second insertion cadence remains an observational estimate.
- A final-frame match cannot pass an animation case without trigger/intermediate/lifecycle evidence.
- Unsupported cases must have explicit BLOCKED/UNKNOWN state and recovery task; file existence is not verification.

## Case schema and completion

Each future result must record: requirement ID; page/section/component and evidence IDs; conditions; starting state; input; expected state/value; observed value; tolerance; result; local evidence; discrepancy/limitation; owner and follow-up. Additional discovered P0 items must be appended or mapped to these cases without erasing their distinct contracts.

The current discovery limitations prevent unconditional implementation sign-off. Final A–F discovery gates remain the root investigator's evidence-backed assessment.
