# Reconstruction risks

Risk levels are investigator judgments, not measured failure rates.

| ID / priority | Risk | Evidence/unknown dependency | Mitigation / verification |
|---|---|---|---|
| R-001 High | Historical homepage leads create the wrong website | Live HOME-STRUCT differs from the brief's leads | Use current page order; review dated content at implementation start |
| R-002 High | Correct final title but wrong motion | U-002; HOME-CSSOM-001 and HOME-TIMED-DOM-001 establish declared/computed motion and a sampled interval, not the complete lifecycle | Capture full cycle and exit; verify intermediate frames and wrapping |
| R-003 High | Font substitution shifts all geometry | ASSET-FONT/U-004; HOME-CSSOM-001 confirms face mapping, but actual load status, axes, and rights remain unknown | Approve fonts or replacement; validate wraps before grid polish |
| R-004 High | Product miniatures flattened into screenshots | Five bento cards use HTML/SVG, with zero img/video nodes | Specify illustration anatomy and state; compare grid clipping |
| R-005 High | Dual-media seek, rate, and sidebar states diverge | INT-VIDEO; U-008 | Separate orthogonal state axes; run sync/drift/error tests |
| R-006 High | P1 Orb page rebuilt as a static long article | Confirmed sticky navigation/media; U-009 | Capture section-linked media behavior before implementation |
| R-007 High | Screenshots/recordings claimed but missing | U-001/U-002 | Mark gates BLOCKED/PARTIAL explicitly; do not cite empty folders as coverage |
| R-008 High | Public assets assumed reusable | Download refusal; licenses unknown | Approve source/replacement manifest before asset integration |
| R-009 Medium | Mobile-overlay focus/resize breaks navigation | Expanded state persists at 768px; U-006 | Full keyboard, resize, repeat, and outside-click tests |
| R-010 Medium | One palette/type scale applied everywhere | Dark homepage, cream marketing, near-white docs | Template-specific token resolution and regression |
| R-011 Medium | Duplicate marquees cause accessibility problems | Duplicate groups and continuous loops; U-003. HOME-CSSOM-001 declares hover pause and reduced/focus-visible alternatives; runtime not exercised | Verify screen-reader order, Tab behavior, pause, and reduced motion against declared CSS |
| R-012 Medium | Global pixel score hides local defects | No saved baselines; varied font/scrollbar states | Local geometry/wrap tests and captures under matched conditions |
| R-013 Medium | Initial loader and lazy content misclassified | Transient 900px Chronicle sample; late assets | Wait for visible content/font/media state; record loading separately |
| R-014 Medium | Backend/auth scope creep | Authentication, checkout, settings, and workspace boundaries | Public entry contract only; no purchases, registrations, or private product actions |
| R-015 Medium | Large blur surfaces, media, and loops regress mobile performance | Inferred performance risks, no CPU trace; declared motion alternatives in HOME-CSSOM-001 have no runtime performance verification | Measure baseline before budgets; verify visibility/preference policies after evidence |
| R-016 Medium | Visible copy feedback mistaken for verified clipboard content | INT-INSTALL-COPY-002 confirms toast/icon feedback, but later clipboard read returned earlier docs source; U-007 leaves command payload and tool-versus-site cause UNKNOWN | Verify the current action's payload and feedback separately; do not declare command-copy success from toast text alone |

Each mitigation is future work or unresolved discovery; none is an implemented fix. The dependency order in implementation-plan begins with measured tokens and motion foundations, then the complete hero, the next complete sections, and cross-page verification.
