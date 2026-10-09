# Amp public website discovery harness

Reference: https://ampcode.com/ · Investigated 9 October 2026, Asia/Calcutta.

**Status: discovery pass delivered with unresolved fidelity blockers. Implementation has not started.** This is an evidence-backed investigation, not an unconditional implementation-ready sign-off. Quality gates are evaluated in [discovery-report.md](discovery-report.md). Resume discovery before signing off the high-risk unknowns; do not silently replace them with generic behavior.

The supplied repository initially contained no files, hidden entries, or application stack. Only this `.harness` is authorized output. The live homepage differs from the historical leads in the brief: remote orbs, a rotating title and prompt storm, demonstrations, testimonials, subscription routing, learning episodes, CLI installation, announcements and footer are the actual current sequence.

## Read and resume

1. Read this document and [progress.json](progress.json).
2. Read [unknowns.md](unknowns.md) and [evidence-index.md](evidence-index.md).
3. Open only the relevant page/motion/interaction specification.
4. Resolve the next recorded observation gap, update its evidence and affected contracts, then re-evaluate the gates.

## Evidence conventions

- **CONFIRMED:** directly measured DOM/computed CSS, observed browser action, or primary-source text. The method is always named; text extraction does not confirm visual behavior.
- **INFERRED:** an explanation supported by indicators but not directly established.
- **UNKNOWN:** not available or not tested. No guessed durations, easing, breakpoints, performance scores or implementation libraries.
- **NOT APPLICABLE:** the specific state does not apply, rather than merely being untested.
- Recommendations are future design/engineering decisions, never reference facts.

Browser observations are transcribed in `evidence/observations/browser-session.md` and measurement JSON. They are **not raw browser exports**. Screenshots were viewed in the investigation session but could not be saved by the browser runtime. No recording exists. Asset export was rejected because download permission was declined; no alternate download was attempted. Do not cite nonexistent image/recording files or treat online assets as licensed.

## Document map

| Area | Canonical documents |
|---|---|
| Routes and scope | website-map.md, navigation-graph.md, page-specs/ |
| Product/content | product-experience-analysis.md, product-storytelling.md, content-architecture.md |
| Visual system | design-system.md, responsive-spec.md, responsive-matrix.md |
| Components | component-inventory.md, component-contracts.md |
| Motion/behavior | animation-spec.md, animation-timelines.md, interaction-spec.md, interaction-state-machines.md |
| Assets | asset-inventory.md, asset-dependency-map.md |
| Engineering | architecture-analysis.md, technical-decisions.md, accessibility-review.md, performance-analysis.md |
| Future implementation/QA | implementation-plan.md, verification-plan.md, acceptance-criteria.md |
| Integrity/handoff | evidence-index.md, unknowns.md, risk-register.md, discovery-report.md, progress.json |

Web-only reconnaissance is retained in `page-specs/supporting-route-recon.md` and `page-specs/content-template-recon.md`. Later root browser results in `page-specs/browser-template-samples.md` supersede their specific unresolved leads; remaining text-only limitations still apply. Evidence JSON is under `evidence/observations/`, not alongside those page files.
