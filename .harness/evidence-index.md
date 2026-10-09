# Central evidence index

All observations use the client investigation date 2026-10-09, Asia/Calcutta. Classification means what the named method establishes. Root browser facts are transcribed from tool outputs; JSON contains normalized measurements, not raw captures. Every meaningful P0 interaction/animation maps to a section/component in home.md and its canonical inventory.

| Evidence ID | Persisted record | Coverage |
|---|---|---|
| REPO-001 | evidence/observations/browser-session.md | Initial empty folder, no stack |
| REPO-002 | evidence/observations/browser-session.md; architecture-analysis.md | Final Git metadata present; no application files outside the discovery harness |
| HOME-STRUCT-001 | evidence/measurements/home-sections.json; page-specs/home.md; evidence/observations/browser-session.md | Section order, geometry, DOM, and navigation |
| HOME-LOGO-NAV-001 | evidence/observations/browser-session.md; website-map.md | Homepage logo href /home click yields browser URL / |
| HOME-CSS-001 | design-system.md; evidence/observations/browser-session.md | Computed fonts, colors, grid, finishing, and inline variables |
| HOME-CSSOM-001 | [evidence/observations/cssom-findings.md](evidence/observations/cssom-findings.md) | Declared font-face mapping, formats, font-display, reduced-motion rules, hover pause, and focus-visible alternatives; runtime preference/hover/focus behavior not exercised |
| HOME-TIMED-DOM-001 | [evidence/observations/timed-dom.md](evidence/observations/timed-dom.md) | 495 reads over 12,014ms; approximate 4-second phrase intervals; computed 300ms/ease exit with 40ms stagger. Sampling start is not page-load T0 or a frame-accurate recording |
| RESP-MATRIX-001 | evidence/measurements/home-matrix.json | Seven actual viewport measurements |
| RESP-BOUNDARY-001 | responsive-spec.md; evidence/observations/browser-session.md | Adjacent-width measurements at 768/1024px |
| HOME-WRAP-001 | responsive-spec.md;evidence/observations/browser-session.md | Desktop/mobile phrase lines |
| HOME-MOTION-001 | animation-spec.md; animation-timelines.md; evidence/observations/browser-session.md | CSS animation configuration and continuous loops |
| HOME-SCROLL-001 | animation-spec.md; evidence/observations/browser-session.md | Forward, reverse, and reload scroll samples |
| INT-MENU-001 / INT-POPOVER-001 | interaction-spec.md; evidence/observations/browser-session.md | Open, close, Escape, outside click, first Tab, and resize |
| INT-INSTALL-001 / INT-EPISODES-001 / INT-VIDEO-001 | interaction-spec.md; evidence/observations/browser-session.md | Tested selection, scroll, and media-state results |
| ASSET-DOM-001 | asset-inventory.md; evidence/observations/browser-session.md | Sources, intrinsic dimensions/loading, and HTML/SVG distinction |
| ASSET-VIDEO-FLAGS-002 | [evidence/observations/timed-dom.md](evidence/observations/timed-dom.md); asset-inventory.md | Actual screen/camera and CLI-video loop, autoplay, muted, and native-controls properties; visibility playback lifecycle remains unknown |
| INT-INSTALL-COPY-002 | [evidence/observations/timed-dom.md](evidence/observations/timed-dom.md); interaction-spec.md | Windows-command toast/icon feedback confirmed; later clipboard accessor returned earlier docs source, leaving command payload success and tool-versus-site cause UNKNOWN |
| PAGE-PRICING-BROWSER-001 / PAGE-P1-BROWSER-001 | page-specs/browser-template-samples.md; evidence/observations/browser-session.md | Supporting marketing visual/state samples |
| PAGE-CONTENT-BROWSER-001 / INT-DOCS-001 | page-specs/browser-template-samples.md; evidence/observations/browser-session.md | Article/docs geometry and mobile drawer/search/history |
| Supporting WEB-* source IDs / PAGE-* route records | evidence/observations/supporting-routes.json; page-specs/supporting-route-recon.md | Primary-source text/URL retrieval; not visual behavior |
| Content OBS-CONTENT-* IDs | evidence/observations/content-templates.json; page-specs/content-template-recon.md | Representative families, authentication retrieval, and archive caveats |
| LIMIT-ASSET-001 / LIMIT-SCREENSHOT-001 | evidence/observations/browser-session.md; evidence/screenshots/README.md; evidence/recordings/README.md | Explicit capability/review limits |
| HARNESS-VALIDATION-001 | evidence/observations/harness-validation.json | Required files, JSON/local links, inventory-to-case mapping and application-file scope checks; documentation validation only |

Source URLs are included near web-derived claims and inside evidence JSON. The handoff uses stable observation IDs and public URLs; session-specific web-tool reference IDs have been omitted. Text-tool crawl freshness varies; root live-browser findings are authoritative for sampled presentation.

Session-only images are described in browser-session. No saved image files or recordings exist. The main durability gap is that a new engineer cannot independently compare pixels from this package. Gates must not PASS full visual/timed handoff solely because these Markdown files exist.


