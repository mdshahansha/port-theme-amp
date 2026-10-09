# Phase 1 discovery report

Reference: [Amp](https://ampcode.com/). Investigation date: 9 October 2026, Asia/Calcutta. Target folder: `C:\Users\mdsha\Desktop\amp-port\.harness`.

**Outcome: the discovery pass is documented, but full implementation-ready fidelity is not signed off.** No application code, components, animations or dependencies were created or changed. Critical remaining gaps are recorded rather than filled with assumed behavior.

## 1. Scope

The route ledger contains 26 principal entries plus observed linked route families and P3 boundaries. The homepage received the deepest investigation: eight sections plus footer, all seven requested viewport sizes, additional boundary measurements, media/platform/menu controls, computed typography/colors and selected motion/scroll samples. Five supporting marketing destinations were browser-sampled: Pricing, App, Models, About and What Are Orbs. Chronicle, a news detail, documentation Introduction and CLI, a long note, and docs Next/Back navigation were also browser-sampled. Source-text reconnaissance extends coverage to sales, trust/legal, community, podcast, learning and representative content families. Each route's method and completeness are explicit in [website-map.md](website-map.md).

Authenticated workspaces/projects/settings, account completion, purchases, download execution and external services are excluded beyond public entries and destinations. No credentials or forms were submitted. Browser sampling is not exhaustive state coverage. A fresh tab was created, but an isolated browser profile was unavailable. Browser version, renderer OS, zoom and browser locale remain unknown. Screenshots were viewed but could not be persisted by the browser runtime; no recordings were available. Asset export was rejected by automatic approval review because download permission was declined.

## 2. Design findings

The current homepage presents remote agents and orbs, rather than assuming the older themed sections in the brief. Its identity combines dark teal (#091c1e), ivory (#f6fff5), orange (#f6833b), large Sagittaire display type, italic emphasis, monospace labels, dotted rails, atmospheric glow/grain, asymmetric capability cards and moving social proof. Supporting marketing/editorial pages use cream; docs use near-white and a separate sans-serif reading system.

The homepage grid changes from one to three tracks at 768 px and from three to five at 1024 px. Typography is fluid between transitions. The exact title clamp, 560 px hero stage, nested grid padding, section boundaries and mobile phrase wraps are documented. CSS font-face declarations establish Berkeley Mono→TX-02 and the relevant Sagittaire face associations; actual loaded subsets, variable axes and licenses remain unverified. Shared controls, marketing navigation/footer, installer, screencast, cards and template shells have explicit contracts.

## 3. Motion findings

The hero uses word entrances, not character animation. Computed entrance duration is 560 ms with cubic-bezier(.16,1,.3,1); a four-word sample delays at 280/340/400/460 ms. Exit words travel upward 18 px over 300 ms with easing ease and a 40 ms stagger. A bounded DOM sampling window observed approximately four-second phrase insertions; the exact scheduler and complete cycle are not established. Emphasis skew, prompt-bubble entrance/exit paths, Puck travel/bobbing and three testimonial-loop durations are recorded.

Loaded CSS declares hover pause and keyboard/reduced-motion manual scrolling for testimonial rows, title animation suppression, fade-only prompt bubbles and a static caret. Runtime preference activation remains untested. Homepage scrolling behaved as ordinary flow in sampled passes; that does not establish the absence of all scroll effects. The Orb explainer has sticky navigation/media. Complete load-frame choreography, offscreen lifecycle, interruption and precise Orb scroll progress remain open.

## 4. Interaction findings

Confirmed samples include popover dismissal with Escape; mobile menu repeat/open, outside-click/Escape dismissal and Tab-to-Home focus; platform-dependent installation commands; episode-track movement; synchronized chapter seeking/rate changes; caption/sidebar/transcript expansion; pricing tier and exclusive FAQ selection; model payment-context pressed state; and docs drawer/search/Next/Back behavior. A later copy click produced a toast and icon replacement, but the browser clipboard accessor returned previous docs content, so command payload success is not established.

The custom media player is a major reconstruction risk. Fullscreen success, mute/webcam behavior, seeking drag, recovery and drift correction were not verified. Complete overlay focus cycles, touch equivalence and all control loading/error states remain incomplete. Navigation maps distinguish observed hrefs, text-resolved redirects and clicked outcomes.

## 5. Technical findings

Confirmed mechanisms include loaded CSS keyframes/transitions, inline SVG, layered HTML feature illustrations, native videos under custom controls, lazy image attributes, font preloads and static media delivery. Svelte/SvelteKit is **inferred** from class signatures and immutable asset paths; exact versions, server rendering/hydration, routing internals and source libraries are not established. No GSAP, Motion or WebGL dependency is claimed.

The supplied project began empty, so no replacement stack is selected as an existing fact. Architecture recommendations separate reference requirements from future choices. Performance analysis records long-running decorative motion, blur/media/font risks without invented Core Web Vitals, CPU or frame-rate scores.

## 6. Risks and unknowns

The highest-priority gaps are durable screenshots and timed motion captures, complete hero/storm lifecycle, runtime reduced-motion/keyboard/touch behavior, remaining media states, Orb scroll choreography and approved asset/font use. URL availability does not grant reuse rights. Exact asset acquisition, font axes and licensing remain unresolved. Lower-depth P1/P2 routes need the visual/state coverage appropriate to the final implementation scope. See [unknowns.md](unknowns.md) and [risk-register.md](risk-register.md) for impact and next checks.

## 7. Artifacts created

All requested canonical files are present. Their roles are:

| Purpose | Files |
|---|---|
| Resume and scope | README.md, progress.json, website-map.md, navigation-graph.md |
| Product and narrative | product-experience-analysis.md, product-storytelling.md, content-architecture.md |
| Visual and responsive system | design-system.md, responsive-spec.md, responsive-matrix.md |
| Reuse contracts | component-inventory.md, component-contracts.md |
| Motion and state behavior | animation-spec.md, animation-timelines.md, interaction-spec.md, interaction-state-machines.md |
| Media and provenance | asset-inventory.md, asset-dependency-map.md |
| Engineering review | architecture-analysis.md, technical-decisions.md, accessibility-review.md, performance-analysis.md |
| Future build and verification | implementation-plan.md, verification-plan.md, acceptance-criteria.md |
| Evidence and gaps | evidence-index.md, unknowns.md, risk-register.md, this report |

`page-specs/` holds homepage anatomy, browser template samples and two source-reconnaissance records. `evidence/` contains measurement JSON, observation ledgers and explicit screenshot/recording limitations. The evidence files are transcribed observations, not raw browser exports. There are no saved screenshot images, recordings or acquired third-party assets in this package. The future acceptance matrix contains 40 planned cases and maps all 26 current motion/interaction inventory IDs; those implementation tests have not been run.

## 8. Recommended implementation strategy

First close the fidelity blockers and agree the actual stack and asset policy. Follow the supplied implementation sequence: measured foundations and shared motion lifecycle → complete hero layout/motion/interactions → each following section as a complete experience → supporting templates and cross-page regression. Phases 2–10, dependencies, complexity, checkpoints and acceptance criteria are planning documents only. Motion and interaction phases must not postpone behavior that determines layout, wrapping or clipping. Verify paired viewport/state captures, intermediate motion frames and keyboard/touch/reduced-motion behavior before marking a section complete.

## 9. Quality gates

| Gate | Result | Reason |
|---|---|---|
| A — Coverage | PARTIAL | All current homepage sections and major controls/motion families are inventoried; complete lifecycle/edge states and some supporting public paths remain shallow or untested. |
| B — Visual precision | PARTIAL | All seven sizes, main geometry, typography, colors and important asset leads are measured. Durable image comparisons, some finishing details and supporting-page boundary/state geometry are missing. |
| C — Behavioral precision | PARTIAL | Selected transitions, destinations, mobile and reverse-scroll samples are documented. Complete load/scroll lifecycle, runtime preference handling, keyboard/touch equivalence and media/error behavior remain incomplete. |
| D — Evidence integrity | PASS | Important findings have method/evidence references and explicit confidence. Rejected captures, transcribed evidence, mixed viewport conditions and conflicting observations are disclosed; superseded claims are reconciled. This pass does not certify durable visual evidence. |
| E — Implementation readiness | PARTIAL | Components, architecture risks, dependency order and testable future cases are defined, but unresolved high-risk behavior/assets prevent unconditional fidelity sign-off. |
| F — Handoff readiness | BLOCKED | Another engineer can resume from the package, but still needs critical motion/runtime and durable visual evidence to implement without rediscovery. |

No completion percentage is assigned. The next authorized work remains discovery gap closure; implementation has not started. This report ends the present investigation pass without claiming the mandatory full-readiness outcome.

