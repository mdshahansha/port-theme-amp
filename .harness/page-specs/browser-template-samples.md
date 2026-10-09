# Supporting-page and content-template browser samples

These measurements supplement the earlier [source-text template reconnaissance](./content-template-recon.md). Where a browser finding below resolves a web-only UNKNOWN, the browser result takes precedence for the tested state and viewport. It does not establish untested responsive or interactive states.

Investigation: 2026-10-09, Asia/Calcutta. Root investigator used the Codex in-app browser, DPR 1, preferred dark scheme, and reduced motion false. Browser engine/version, zoom, locale, and isolated authentication-session state are UNKNOWN. Public pages rendered without sign-in. Unless stated otherwise, desktop samples are 1440 × 900px and mobile samples 390 × 844px. Coordinates are element measurements as reported by the root investigator; no animation timestamp is attached. Heights are sampled document heights, not invariant design requirements.

Primary provenance: [browser observation record](../evidence/observations/browser-session.md), IDs PAGE-PRICING-BROWSER-001, PAGE-P1-BROWSER-001, PAGE-CONTENT-BROWSER-001, and INT-DOCS-001. Supporting screenshots are session-only; no durable raw images or recordings are available in this package. Interaction contracts are in [interaction-spec](../interaction-spec.md).

## P1 — Pricing

Reference: [Pricing](https://ampcode.com/pricing). Evidence: PAGE-PRICING-BROWSER-001, INT-PRICING-001, INT-FAQ-001.

CONFIRMED browser sample: initial viewport **1280 × 720px**, rather than the standard desktop profile. Body background `#dfdfc1` and foreground `#0b0d0b` remain cream/dark text despite the dark color-scheme preference. H1 font size and line height are both 96px; rectangle x=24, y=160, w=1217px. Mobile H1 is 72px and pricing cards stack.

Individual tier tabs show Megawatt $20/month and Gigawatt $200/month. Selecting Gigawatt updates the selected tab and CTA to Get Gigawatt. Clicking FAQ Q1 then Q2 leaves only Q2 expanded. Tab keyboard handling, exact card geometry, responsive boundary, expansion timing, and scroll shifts remain UNKNOWN. Do not infer checkout behavior from an authentication href.

## P1 — Download app

Reference: [App](https://ampcode.com/app). Evidence: PAGE-P1-BROWSER-001.

CONFIRMED browser result resolves the earlier web-fetch failure: this page renders publicly. Desktop cream body; sampled document height 1379px and usable document width 1425px. H1 font size/line height 72/72px; rectangle x=160.5, y=360, w=1104, h=72px. Download Amp H2 starts at y=701px; macOS and iPhone/iPad H2s at y=765px use 24px type and are side by side on desktop. Mobile heading wraps onto multiple lines; exact wraps and mobile measurements were not supplied.

Measured download hrefs:

- macOS: https://static.ampcode.com/mac/latest.dmg
- Apple beta: https://testflight.apple.com/join/Skjdm6qe

Neither download link was clicked. Transfer behavior, installation, availability, redirects, and native-app states are UNKNOWN/OUT OF SCOPE.

## P1 — Models and modes

Reference: [Modes](https://ampcode.com/modes). Evidence: PAGE-P1-BROWSER-001, INT-MODES-001.

CONFIRMED desktop document height 2095px. H1 font size 96px; rectangle x=200.5, y=128, w=1024, h=96px. Section headings use 12px type: Agent Modes y=364px; Subagents y=1011.59px; System Models y=1307.59px.

On mobile, clicking With ChatGPT Sub sets its `aria-pressed` to true and the other payment-context button to false. Resulting model-data changes were incompletely captured. Preserve this as a verified selection-state contract; data filtering, pricing differences, transition timing, keyboard behavior, and persistence remain UNKNOWN.

## P1 — About

Reference: [About](https://ampcode.com/about). Evidence: PAGE-P1-BROWSER-001.

CONFIRMED desktop document height 4794px. H1 font size 75.84px, line height 83.424px; rectangle x=250.195, y=227.476, w=924.609, h=166.844px.

Recorded section starts:

| Content / landmark | Measured y (px) |
|---|---:|
| What We Believe | 845.49 |
| Software after Software | 899.71 |
| Who We Work With | 1360.41 |
| Proof region | 2460.60 |
| Investors | 3374.13 |
| Team | 3768.35 |

These positions establish desktop narrative landmarks only. The exact element semantics of the proof region, responsive transformation, media loading, and section-specific motion remain UNKNOWN in this sample. A multi-line heading rectangle does not establish per-line animation.

## P1 — What are orbs?

Reference: [What Are Orbs?](https://ampcode.com/what-are-orbs). Evidence: PAGE-P1-BROWSER-001.

| Measurement | Desktop 1440 × 900 | Mobile 390 × 844 |
|---|---|---|
| Document height | 9651px | 11428px |
| H1 font size / line height | 60 / 51.6px | 40 / 34.4px |
| H1 rectangle | x=80.60, y=195.203, w=610.59, h=51.59px | x=28, y=99.39, w=319px; height not supplied |

CONFIRMED sticky navigation top is 96px; media panel top is 0. Seven anchor navigation links were found. Browser, TUI, and Phone were not found as interactive controls in the inspected state. The hero is a native video with autoplay, muted, loop, and controls all true. The seven capability videos have autoplay=false, muted=true, loop=true, and controls=true. This resolves whether those observed assets are static imagery, but does not prove uninterrupted playback or establish scrubbing.

Scroll linkage, chapter activation, exact sticky start/end boundaries, mobile sticky changes, reverse-scroll behavior, and reduced-motion alternatives remain UNKNOWN. A long document plus sticky media is insufficient evidence to assign a pin duration or scrub timeline.

## P2 — News article

Reference: [Many, Many Pucks](https://ampcode.com/news/many-many-pucks). Evidence: PAGE-CONTENT-BROWSER-001; source-text observation OBS-CONTENT-NEWS-001.

CONFIRMED desktop cream surface and sampled document height 1581px. H1 font size 96px; rectangle x=407.49, y=484, w=706.92, h=107.516px. An `aside` element measures x=59.007, y=647.51, w=326.89, h=583.3px. Its precise visual/content role should be established from further browser evidence before assigning a reusable component name.

These measurements resolve source-text typography/geometry unknowns for one desktop article state only. The image-bearing headline's motion, image sizes, exact responsive layout, and article loading sequence remain UNKNOWN. The article screenshot depicts product controls; those depicted controls are not public website interactions.

## P2 — Documentation shell and CLI

References: [Introduction](https://ampcode.com/docs), [CLI](https://ampcode.com/docs/cli). Evidence: PAGE-CONTENT-BROWSER-001, INT-DOCS-001; source-text OBS-CONTENT-DOCS-SHELL-001.

CONFIRMED desktop docs surface `#fafaf8`. Introduction document height 2402px and usable width 1430px. H1 uses system-ui at 40px font size / 40px line height; rectangle x=369, y=142, w=704px. Sidebar `aside` is 280px wide, sticky at top 48px, and measured 852px tall. CLI repeats the H1 geometry and has sampled document height 4299px; its installer uses wide platform buttons plus a command.

This browser evidence resolves the web-only uncertainty about whether grouped docs navigation is a desktop sidebar. It does not establish sidebar scroll-container behavior, collapse rules at intermediate widths, or active-link scrolling.

CONFIRMED mobile interactions:

- Navigation opens a drawer 320px wide and the full 844px viewport height; Escape closes it.
- Search opens a 374 × 412px dialog at x=8, y=8 with combobox and listbox. Query `orbs` filters results; Escape closes.
- Copy Page was clicked; the captured label remained Copy Page. Clipboard payload was not read.
- Next The Dial navigates to `/docs/the-dial`; browser Back returns to `/docs`.

Complete focus trapping, result selection, no-results/error states, copy feedback timing, shortcut execution, scroll restoration, and client-routing mechanism remain UNKNOWN. The global command-selector contract is in interaction-spec; no command was executed.

## P2 — Long editorial tutorial

Reference: [How to Build an Agent](https://ampcode.com/notes/how-to-build-an-agent). Evidence: PAGE-CONTENT-BROWSER-001; source-text OBS-CONTENT-NOTE-001.

CONFIRMED desktop document height 21678px. H1 font size 96px / line height 76.8px; rectangle x=407.49, y=200, w=700, h=153.594px. This gives a desktop long-article typography/geometry sample distinct from the docs shell. Code-block overflow, article anchor behavior, mobile wraps, reading progress, and animation remain UNKNOWN. The source's example application code is content; none was executed or generated as implementation.

## P2 — Chronicle

Reference: [Chronicle](https://ampcode.com/chronicle). Evidence: PAGE-CONTENT-BROWSER-001; source-text OBS-CONTENT-CHRONICLE-001.

The first browser sample showed document height 900px and no H1 during loading. **Do not use that height or absence as a settled design baseline.** Later full DOM inspection found Notes, Guides, Follow Amp, News, Time Capsules, and Videos. No filter was apparent in that inspection; this does not prove filters or dynamic controls are absent in all states.

Settled document height, section positions, grid/card dimensions, loading completion timing, pagination, and responsive composition remain UNKNOWN. Source extraction repeats some categories, which may reflect hidden layouts; visible duplication has not been established.

## Coverage and remaining limitations

Only the listed browser samples receive geometry/state confirmation here. Source-text samples `/docs/orbs`, the two video-learning families, and the archived context guide retain their earlier visual and interaction unknowns. P1/P2 measurements are narrower than the seven-profile P0 homepage matrix. Assets were not downloaded, and reuse authorization remains unresolved. No supporting-page motion timeline should be marked complete from these settled browser measurements.
