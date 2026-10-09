# Amp representative content templates — source-text discovery

Investigation date: 2026-10-09, user timezone Asia/Calcutta. This independent workstream used only `web.run` opens, finds, and link clicks for site inspection. No browser interaction, application code, package installation, form submission, or authentication occurred.

## Evidence limits

- CONFIRMED below means confirmed in the primary site's extracted page text or a reported link destination/redirect. It does **not** mean visually confirmed in the root browser.
- Browser version, viewport, DPR, zoom, locale, OS of the fetcher, color scheme, reduced motion, and session cookies are UNKNOWN. Authentication entry pages were obtainable; private content was not inspected.
- Extraction may contain hidden responsive variants, repeated navigation, omitted interactive markup, or index/cache artifacts. Repeated blocks do not prove repeated visible sections.
- Geometry, typography, exact colors, position/stickiness, breakpoints, hover/focus, load choreography, media playback, chapter seeking, scrolling, history, and copy results are UNKNOWN for this workstream.
- Most fetched pages report a crawl on the investigation date. Screencast episodes report a crawl six days earlier; auth sign-up reports two days earlier. Thus these results supplement, rather than replace, fresh live-browser verification.

## Representative scope

| ID | Priority | Primary URL / title | Candidate template | Status |
|---|---|---|---|---|
| PAGE-CHRONICLE-001 | P2 | https://ampcode.com/chronicle — Chronicle - Amp | Grouped publication index | Content/navigation sampled |
| PAGE-NEWS-PUCKS-001 | P2 | https://ampcode.com/news/many-many-pucks — Many, Many Pucks - Amp | Announcement detail | Content/navigation sampled |
| PAGE-DOCS-INTRO-001 | P2 | https://ampcode.com/docs — Introduction \| Amp Docs | Documentation article | Content/navigation sampled |
| PAGE-DOCS-CLI-001 | P2 | https://ampcode.com/docs/cli — Getting Started With the CLI \| Amp Docs | Documentation article with installation selector | Content/navigation sampled |
| PAGE-DOCS-ORBS-001 | P2 | https://ampcode.com/docs/orbs — Orbs Overview \| Amp Docs | Documentation article | Content/navigation sampled |
| PAGE-DAY-001 | P2 | https://ampcode.com/docs/using-amp/a-day-in-amp — Working Day to Day in Amp - Amp | Video and timestamped transcript | Content/navigation sampled |
| PAGE-SCREENCAST-001 | P2 | https://ampcode.com/docs/using-amp/screencasts/orbs/get-started-in-orbs — Get Started in Orbs · Orbs from Zero - Amp | Episodic screencast | Content/navigation sampled |
| PAGE-NOTE-AGENT-001 | P2 | https://ampcode.com/notes/how-to-build-an-agent — How to Build an Agent - Amp | Long editorial tutorial | Content/navigation sampled |
| PAGE-GUIDE-CONTEXT-001 | P2 | https://ampcode.com/guides/context-management — Context Management in Amp - Amp | Archived illustrated guide | Content/navigation sampled |

Only these representatives are content samples; the many publication posts and docs destinations are not individually investigated. Template reuse is INFERRED from repeated extracted structures, not confirmed component/code reuse. Three linked pages were additionally opened to establish relationships: `/docs/puck`, `/docs/using-amp`, and the second Orbs episode `/docs/using-amp/screencasts/orbs/portals-in-orbs`.

## Template observations

### OBS-CONTENT-CHRONICLE-001

Source: [Chronicle](https://ampcode.com/chronicle), extracted lines 0–175. CONFIRMED: return-to-home and Chronicle links; Featured, Notes, Guides, News with RSS, Time Capsules, Videos, and named video-series categories. Entries carry titles, dates, and summaries; video entries include external YouTube links. Many Many Pucks appears under News; the older agent tutorial is also linked from this index. INFERRED purpose: organize product changes, practical experience, and brand/editorial proof. UNKNOWN: visible category ordering and duplicate-block treatment, empty Guides appearance, filters, pagination, grid geometry, and interactions.

### OBS-CONTENT-NEWS-001

Source: [Many, Many Pucks](https://ampcode.com/news/many-many-pucks), lines 0–47. CONFIRMED: home-return link; Chronicle/type/title breadcrumb; publication date; headline with four inline image references; short explanatory body; product screenshot; docs lead; shared grouped footer. The screenshot resolves to `https://static.ampcode.com/news/many-many-pucks-dark.png`. Dimensions and color-scheme variants are UNKNOWN. The depicted product menu is article media, not a publicly interactive menu on this page. The docs lead resolves to `/docs/puck`. Preserve image-bearing headline content as a distinct variant until browser evidence establishes its presentation and motion.

### OBS-CONTENT-DOCS-SHELL-001

Sources: [Introduction](https://ampcode.com/docs), [CLI](https://ampcode.com/docs/cli), [Orbs](https://ampcode.com/docs/orbs), all extracted navigation lines 0–83. CONFIRMED repeated grouped navigation includes onboarding, Orbs, CLI, Apple apps, Puck, collaboration, customization, reference, support, and enterprise. Each sample has the label Copy Page, an H1, article content, and end-of-article next/previous navigation where available. UNKNOWN whether navigation is a sidebar, collapsible, sticky, mobile drawer, or keyboard-searchable. Copy Page control semantics/result are not established by extraction. Reuse this as a candidate documentation template, with article-specific body modules; do not assume a framework or CMS.

### OBS-CONTENT-DOCS-INTRO-001

Source: [Introduction](https://ampcode.com/docs), lines 84–113. CONFIRMED content flow: product summary with differentiators → six-step Quickstart → linked opening screencast → Explore by work surface → Puck lead → Next The Dial. Quickstart mixes public learning pages with account/project settings entry points. It is a navigational onboarding sequence, not evidence of a live step-completion widget. Root homepage messaging should be reconciled against the live-browser record; this page's model names are content that may change.

### OBS-CONTENT-DOCS-CLI-001

Source: [CLI](https://ampcode.com/docs/cli), lines 84–180. CONFIRMED body sequence: overview, installation, use, account management, shell completion, image attachment, execution location, updates, editor connection. Installation exposes Mac/Linux/WSL, Windows, Homebrew labels and a Select representation. Default extracted command is `curl -fsSL https://ampcode.com/install.sh | bash`. This is website content, not an instruction to run it during discovery. Workspace install link points to `/install`; fetching failed, so its public/authenticated rendering is UNKNOWN. Selector changes, command copy feedback, focus, and responsive transformation need browser verification. Footer article navigation leads from Desktop to Keybindings.

### OBS-CONTENT-DOCS-ORBS-001

Source: [Orbs](https://ampcode.com/docs/orbs), lines 84–140. CONFIRMED: feature overview → use rationale → capacity explanation → review/files → terminal → Apple-device follow-along → upload paths → sync command examples → CLI/TUI starts → next steps. Editorial, screencast, support, setup, customization, and cost links supplement the prose. Previous Pricing and Next Getting Started appear at the end. Product capabilities described here are documentation content; their authenticated application behavior was not reproduced or tested.

### OBS-CONTENT-DAY-001

Source: [Working Day to Day](https://ampcode.com/docs/using-amp/a-day-in-amp), lines 0–133. CONFIRMED: Docs/Chronicle/Using Amp links; headline; presenter and 26:05 duration; initial 00:00 time and 1× rate; 15 chapter labels; timestamped Transcript section. Timestamp entries are represented as buttons by the extractor. INFERRED they support video seeking; actual click, keyboard, active-chapter following, autoplay, pause, loading, captioning, persistence, and synchronization are UNKNOWN. Preserve chapters and transcript as separate linked content structures in the future contract.

### OBS-CONTENT-SCREENCAST-001

Source: [Get Started in Orbs](https://ampcode.com/docs/using-amp/screencasts/orbs/get-started-in-orbs), lines 0–31; [episode two](https://ampcode.com/docs/using-amp/screencasts/orbs/portals-in-orbs). CONFIRMED: shared learning navigation, 14:38 player readout with 1× rate, four-episode series, eight chapters for current episode, title/presenter/summary, next-episode lead, Episodes list. Episode two repeats the pattern and adds Previous/Next Episode links. Series and chapter state behavior, transcript availability, player source, assets, seek/click outcomes, and visible duplication remain UNKNOWN. This differs sufficiently from a generic documentation article to require a dedicated template candidate.

### OBS-CONTENT-NOTE-001

Source: [How to Build an Agent](https://ampcode.com/notes/how-to-build-an-agent), lines 0–826. CONFIRMED: home-return and Chronicle/Note breadcrumb; author/date; headline and subtitle; prose, prerequisites, code blocks, terminal conversation examples, tool-building stages, conclusion, and grouped footer. External references include Go, Anthropic console/docs, and video/podcast leads. Long code and terminal blocks create a horizontal-overflow verification requirement, but actual overflow is UNKNOWN. This is a dated tutorial and brand narrative rather than current product onboarding. No example commands or code were executed or copied into an application.

### OBS-CONTENT-GUIDE-001

Source: [Context Management](https://ampcode.com/guides/context-management), lines 0–155. CONFIRMED: return-home; headline; explicit Archived notice identifying an earlier context/model era; illustrated concepts; operational subsections; Further Reading; On this page anchor list; shared footer. Ten image references appear. The extracted TOC includes Shell Mode and Fork, while corresponding sections are absent from extracted body: **possible stale TOC or extractor omission**, not a confirmed broken anchor. Scrolling/anchor destinations need browser verification. Preserve the archive status; do not silently modernize the guide during faithful reconstruction.

## Supporting learning hub

[Using Amp](https://ampcode.com/docs/using-amp) is a confirmed bridge among team profiles/practices, longer guides, screencasts, and time capsules. Its text explicitly instructs hovering or tapping faces for profile previews. This is source-stated behavior, not interaction-confirmed evidence. Add the team-face preview and linked practice article to future investigation scope; it could require a distinct interactive learning-hub component.

## Navigation and P3 boundaries

| Entry | Confirmed destination / outcome | Scope |
|---|---|---|
| Article Return to Amp | https://ampcode.com/ | P0 |
| Article Chronicle breadcrumb | https://ampcode.com/chronicle | P2 |
| Chronicle News RSS | https://ampcode.com/news.rss; extractor refuses RSS media type | External-format feed, not a confirmed site error |
| Article Puck docs lead | https://ampcode.com/docs/puck | Additional P2 sample |
| Article footer Start; Intro Sign Up | https://ampcode.com/auth/sign-up | P3 entry: email/provider form available publicly |
| Article footer Sign In | https://ampcode.com/auth/sign-in | P3 entry: email/provider/passkey controls in extraction |
| Intro Sign in with ChatGPT | https://ampcode.com/settings/model-routing?add=chatgpt → https://ampcode.com/auth/sign-in?returnTo=/settings/model-routing?add%3Dchatgpt | Authentication boundary; no sign-in attempted |
| Intro Add Your Code | https://ampcode.com/projects?newProject=1 → auth provider authorization boundary; tool denied following | P3; private project workflow not inspected |
| CLI workspace install | https://ampcode.com/install; fetch failed | Public/authenticated entry unresolved |
| Article Download App | https://ampcode.com/app; fetch failed | Supporting P1 destination unresolved here |
| Article status link | ampcodestatus.com | P3 external lead; service body not inspected |
| Publication video entries | YouTube | P3 external leads; videos not opened |

Auth sign-up exposes email plus ChatGPT/Google/Apple providers; sign-in additionally exposes passkey and legacy-page fallback links. Authentication was not bypassed. Provider redirect URLs, private account data, and nonces were not persisted.

## Handoff priorities

1. Root live-browser findings remain authoritative for visual/motion claims.
2. Browser-sample the docs shell, installation selector/copy control, article header variants, guide anchors, and both video structures.
3. Resolve the learning hub's stated hover/tap face previews before reusing it as a static listing.
4. Verify colors/media variants and intrinsic dimensions; public availability does not establish asset-reuse permission.
5. Preserve the distinction between content describing Amp product interactions and actual public website interactions.
