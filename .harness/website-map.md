# Website scope and route ledger

Investigation: 2026-10-09, Asia/Calcutta. Reference origin: `https://ampcode.com`. Discovery only; no application implementation, installation, account creation, or download execution occurred.

## Scope and evidence rules

- **P0:** homepage, including its public navigation, motion, responsive behavior and section interactions.
- **P1:** public top-level marketing/conversion/support pages. Legal/reference pages are included as supporting public destinations, using a representative long-form template rather than exhaustive legal-content reproduction.
- **P2:** publication, documentation and learning templates. Representative bodies are sampled; a discovered leaf is not automatically analyzed.
- **P3:** public authentication entries, authenticated settings/workspaces/projects, downloads and external services. Record entry and intent; stop at the boundary. A linked download is not an installed application.

Statuses: **B** = root investigator reports browser sampling; **T** = source-text/route extraction sampled; **L** = discovered link only; **E** = entry/boundary only. B is not completion of the seven-viewport matrix. T is not evidence for geometry, visual states or click outcomes. Loading/error/responsive/motion fields are UNKNOWN unless a linked browser specification says otherwise. A fetch failure is a tool limitation, not a confirmed broken website route.

Evidence sources: **SUP** = [supporting source records and resolved edges](evidence/observations/supporting-routes.json); **CONTENT** = [content evidence records](evidence/observations/content-templates.json) and [template reconnaissance](page-specs/content-template-recon.md); **ROOT** = the root investigator's [browser-template samples](page-specs/browser-template-samples.md) and [browser observation record](evidence/observations/browser-session.md). Stable observation IDs resolve through [evidence-index.md](evidence-index.md); all routes connect to [navigation-graph.md](navigation-graph.md). Detailed visual/behavior contracts belong to [page-specs/](page-specs/), [interaction-spec.md](interaction-spec.md), [animation-spec.md](animation-spec.md), [responsive-matrix.md](responsive-matrix.md), and [asset-inventory.md](asset-inventory.md). This ledger does not override those measurements.

## Principal route inventory

Full URLs are authoritative. Page titles below are extraction titles unless identified as a root-observed heading.

| Route / page ID | Priority and full URL | Title; purpose | Entry; template candidate | Investigation and evidence |
|---|---|---|---|---|
| ROUTE-HOME / PAGE-HOME-001 | P0 · https://ampcode.com/ | Homepage; introduce agent/work environment and convert users | Direct; unique marketing landing | B, root owns deep inspection; ROOT |
| ROUTE-PRICING / PAGE-PRICING-001 | P1 · https://ampcode.com/pricing | Pricing — Amp; explain plan/usage choices | Home/footer; plan comparison | B at initial 1280 × 720 and mobile 390 × 844 + T; WEB-PRICING-001, PAGE-PRICING-BROWSER-001, INT-PRICING-001, INT-FAQ-001 |
| ROUTE-APP / PAGE-APP-001 | P1 · https://ampcode.com/app | Root heading: Download Amp; Apple-device download entry | Home/footer; download landing | B at 1440 × 900 and 390 × 844; public rendering resolves web-fetch gap; WEB-APP-001, PAGE-P1-BROWSER-001; downloads not clicked |
| ROUTE-MODES / PAGE-MODES-001 | P1 · https://ampcode.com/modes | Modes & Models - Amp; explain task/model roles | Footer; structured model reference | B at 1440 × 900 plus mobile selection state + T; WEB-MODES-001, PAGE-P1-BROWSER-001, INT-MODES-001 |
| ROUTE-ABOUT / PAGE-ABOUT-001 | P1 · https://ampcode.com/about | About - Amp; lab philosophy, proof and people | Footer; company/story landing | B at 1440 × 900 + T; WEB-ABOUT-001, PAGE-P1-BROWSER-001 |
| ROUTE-ORBS / PAGE-ORBS-001 | P1 · https://ampcode.com/what-are-orbs | What Are Orbs? - Amp; explain remote agent environments | Home/footer/pricing; feature narrative | B at 1440 × 900 and 390 × 844 + T; WEB-ORBS-001, PAGE-P1-BROWSER-001 |
| ROUTE-CONTACT / PAGE-CONTACT-001 | P1 · https://ampcode.com/contact-sales | Contact Sales - Amp; enterprise inquiry | Pricing enterprise CTA; public form | T only; WEB-CONTACT-001; no submission |
| ROUTE-SECURITY / PAGE-SECURITY-001 | P1 · https://ampcode.com/security | Security Reference - Amp; trust/security reference | Footer/modes; long reference | T shallow; WEB-SECURITY-001 |
| ROUTE-PRIVACY / PAGE-PRIVACY-001 | P1 · https://ampcode.com/privacy-policy | Privacy Policy - Amp; legal reference | Footer/auth/legal cross-links; long reference | T shallow; WEB-PRIVACY-001 |
| ROUTE-TERMS / PAGE-TERMS-001 | P1 · https://ampcode.com/terms | Terms - Amp; legal reference | Footer/auth/legal cross-links; long reference | T shallow; WEB-TERMS-001 |
| ROUTE-PRESS / PAGE-PRESS-001 | P1 · https://ampcode.com/press-kit | Press Kit - Amp; press information and brand resources | Footer; asset resource page | T shallow; WEB-PRESS-001 |
| ROUTE-INSIDERS / PAGE-INSIDERS-001 | P1 · https://ampcode.com/insiders | Amp; community application entry | Footer; benefit/process landing | T shallow; WEB-INSIDERS-001; apply control unresolved |
| ROUTE-CHRONICLE / PAGE-CHRONICLE-001 | P2 · https://ampcode.com/chronicle | Chronicle - Amp; publication index | Footer/article trail; grouped index | B DOM/content sample + T; initial loading geometry is unreliable; PAGE-CONTENT-BROWSER-001, OBS-CONTENT-CHRONICLE-001 |
| ROUTE-NEWS-PUCKS / PAGE-NEWS-PUCKS-001 | P2 · https://ampcode.com/news/many-many-pucks | Many, Many Pucks - Amp; product announcement | Home/Chronicle; announcement detail | B at 1440 × 900 + T; PAGE-CONTENT-BROWSER-001, OBS-CONTENT-NEWS-001 |
| ROUTE-DOCS / PAGE-DOCS-INTRO-001 | P2 · https://ampcode.com/docs | Introduction \| Amp Docs; getting started and exploration | Home/footer; documentation article | B at 1440 × 900 and mobile 390 × 844 interactions + T; PAGE-CONTENT-BROWSER-001, INT-DOCS-001, OBS-CONTENT-DOCS-SHELL-001 / OBS-CONTENT-DOCS-INTRO-001 |
| ROUTE-DOCS-CLI / PAGE-DOCS-CLI-001 | P2 · https://ampcode.com/docs/cli | Getting Started With the CLI \| Amp Docs; local setup/reference | Home/docs; documentation with install selector | B at 1440 × 900 + T; PAGE-CONTENT-BROWSER-001, OBS-CONTENT-DOCS-CLI-001 |
| ROUTE-DOCS-ORBS / PAGE-DOCS-ORBS-001 | P2 · https://ampcode.com/docs/orbs | Orbs Overview \| Amp Docs; remote-work reference | Home/Orbs/docs; documentation article | T; OBS-CONTENT-DOCS-ORBS-001 |
| ROUTE-DAY / PAGE-DAY-001 | P2 · https://ampcode.com/docs/using-amp/a-day-in-amp | Working Day to Day in Amp - Amp; demonstrate daily use | Home/learning hub; video/transcript | T; OBS-CONTENT-DAY-001 |
| ROUTE-SCREENCAST-START / PAGE-SCREENCAST-001 | P2 · https://ampcode.com/docs/using-amp/screencasts/orbs/get-started-in-orbs | Get Started in Orbs · Orbs from Zero - Amp; opening tutorial | Home/docs/series; episodic video | T; OBS-CONTENT-SCREENCAST-001; crawl reported six days old |
| ROUTE-SCREENCAST-PORTALS / PAGE-SCREENCAST-002 | P2 · https://ampcode.com/docs/using-amp/screencasts/orbs/portals-in-orbs | Episode-two content sampled; tutorial continuation | Home/previous episode; episodic video | T supporting sample; OBS-CONTENT-SCREENCAST-001; exact browser title unrecorded |
| ROUTE-USING-HUB / PAGE-USING-HUB-001 | P2 · https://ampcode.com/docs/using-amp | Using Amp - Amp; team/practice learning hub | About/mobile menu/learning trail; learning hub | T; OBS-CONTENT-USING-HUB-001; face hover/tap is source-stated, not tested |
| ROUTE-DOCS-PUCK / PAGE-DOCS-PUCK-001 | P2 · https://ampcode.com/docs/puck | Docs article; product-assistant reference | News/docs; documentation article | T relationship sample; CONTENT; detailed page contract incomplete |
| ROUTE-NOTE-AGENT / PAGE-NOTE-AGENT-001 | P2 · https://ampcode.com/notes/how-to-build-an-agent | How to Build an Agent - Amp; long tutorial | Footer/Chronicle; code-rich editorial | B at 1440 × 900 + T; PAGE-CONTENT-BROWSER-001, OBS-CONTENT-NOTE-001 |
| ROUTE-GUIDE-CONTEXT / PAGE-GUIDE-CONTEXT-001 | P2 · https://ampcode.com/guides/context-management | Context Management in Amp - Amp; archived guide | Footer; illustrated guide | T; OBS-CONTENT-GUIDE-001; archive state preserved; TOC integrity unresolved |
| ROUTE-PODCAST / PAGE-PODCAST-001 | P2 · https://ampcode.com/podcast | Raising an Agent — a podcast by Quinn Slack and Thorsten Ball - Amp; audio collection | Footer; season/episode index | T shallow; WEB-PODCAST-001; player untested |
| ROUTE-PODCAST-EPISODE / PAGE-PODCAST-EPISODE-001 | P2 · https://ampcode.com/podcast/season-02/episode-05 | Stop Boxing In Your Agent — Raising an Agent - Amp; episode detail | Podcast index; episode detail | T retrieval only; SUP podcast resolved edge; not thorough template analysis |

## Route contract summaries

The homepage logo's observed href is https://ampcode.com/home. A later click left the browser at https://ampcode.com/ with the homepage visible (HOME-LOGO-NAV-001). Treat `/home` as a discovered P0 navigation alias with this tested click outcome; direct hard-entry behavior and the redirect mechanism remain unknown. It is not a second independent page template.

These outlines supplement the linked evidence; full visual contracts are in the browser-template samples. Where controls merely appear in extraction, state transitions remain UNKNOWN. Browser findings below resolve only the tested state and viewport.

| Page IDs | Extracted content sequence | Shared/unique components and assets | Public interaction leads; known outcome / gap |
|---|---|---|---|
| PRICING | Heading → four plan categories → Q&A → help → footer | Return link/footer; pricing records, tier labels, static-host image | Browser Gigawatt selection changes $20 to $200/month and CTA to Get Gigawatt; opening FAQ Q2 closes Q1; auth/sales destinations resolved; keyboard/timing unknown |
| APP | Icon / Apple-device H1 → beta notice → download section and two platform blocks | App icon; two platform downloads; desktop download blocks side by side | Public rendering and desktop/mobile composition sampled; exact download hrefs confirmed; binaries/TestFlight not opened or installed |
| MODES | Intro → modes → subagents → system roles → security → footer | Return/footer; structured linked model data | Browser mobile payment-context click sets one aria-pressed true and the other false; resulting data changes incompletely captured; news/docs links resolve |
| ABOUT | Positioning/image → beliefs → audience → proof → investors → team → use link → footer | Return/footer; portrait/proof/logo leads | External proof/lab leads; team behavior untested here |
| ORBS | Use cases → section navigation → six records → capabilities/media → explanations → cross-client labels → sizes → reading → footer | Return/footer; seven anchor links; native hero video autoplay=true; seven capability videos autoplay=false; all eight muted/loop/native-controls=true; cost table | Root confirms sticky navigation/media in sampled state; Browser/TUI/Phone were not found as interactive controls; hash landing, scroll linkage and lifecycle remain unknown |
| CONTACT | Inquiry heading → required field set → submit/email → image → footer | Return/footer; labeled inputs/selects/message field | Validation/options/results unknown; no data submitted |
| SECURITY / PRIVACY / TERMS | Return/contents → long structured reference | Candidate common reference shell; cross-links | Contents/anchors/focus/overflow untested; legal body is original content, not reusable copy authorization |
| PRESS | Product/company → contact → media resources → brand downloads → footer | Return/footer; SVG-logo and app-icon asset references | Resource/download entry only; media retrieval errors do not prove broken links |
| INSIDERS | Benefits → application process → capacity notice → application control → footer | Return/footer; benefit and process records | Apply label appears without resolvable link; state/outcome unknown |
| CHRONICLE | Categorized publication/series entries | Return/footer; dated entry records; external-video leads | Later browser full DOM confirms category content; initial loading height/H1 absence are not settled geometry; filter absence not established universally |
| NEWS-PUCKS | Trail/date → image-bearing heading → body/screenshot → docs → footer | Return/footer; announcement body; inline-headline images and screenshot; desktop geometry sample | Docs destination resolved; depicted product menu is article media; responsive/motion lifecycle unknown |
| DOCS / DOCS-CLI / DOCS-ORBS / DOCS-PUCK | Repeated grouped docs navigation → article/copy control → body → next/previous | Desktop docs/CLI sidebar confirmed; selector/code blocks in CLI; article media varies; Orbs/Puck remain source-text samples | At 390, Docs drawer 320 × 844 and search 374 × 412 open/close with Escape; search query filters; Next The Dial and Back verified; Copy Page label unchanged, clipboard unverified; install link extraction failed |
| DAY | Learning links → video/presenter → chapters → timestamped transcript | Dedicated media/chapter/transcript composition | Timestamp buttons extracted; seeking/sync/playback unknown |
| SCREENCAST-START / SCREENCAST-PORTALS | Learning navigation → player/readout → series/chapters → article → adjacent episodes | Dedicated episodic media composition | Series/chapters represented; playback/selection/seek unknown |
| USING-HUB | Team/practice/guide/video/time-capsule links | Team-face preview lead; learning bridge | Source asks hover/tap; response/dismissal/touch contract unknown |
| NOTE-AGENT | Metadata/title → prose/prerequisites → code/tool stages → conclusion → footer | Editorial shell; code/terminal blocks; desktop typography/geometry sample | Long-block overflow, mobile composition and external navigation need browser verification |
| GUIDE-CONTEXT | Archived heading/notice → illustrated guide → reading/TOC → footer | Archive notice; ten image references | TOC sections may be absent from extraction; no broken-anchor claim |
| PODCAST / PODCAST-EPISODE | Index: cover/subscriptions → seasons/episode records → selection prompt → footer; episode: retrieval only | Podcast cover; episode player lead | Playback/loading/seeking/persistence unknown; external subscriptions entry only |

Page ID cells abbreviate the `PAGE-…` IDs above. Animation, responsive transformation, focus/hover/active/disabled/loading/error behavior and dimensions outside the tested states are UNKNOWN unless independently documented by root. Route navigation facts are link retrievals or DOM href observations unless a specific tested browser outcome is stated. Shared footer repetition is confirmed in source extraction; its visual/component-code reuse is inferred.

## Discovered leaves and family scope decisions

These exact URLs came from links, not route-name guessing. **L** means linked but not individually analyzed. **T-r** means retrieval/content lead only, with no thorough visual/behavior specification. They enter the navigation graph; deep repeated-template coverage is deferred unless a representative reveals a distinct variant.

| Family / route IDs | Full URLs | Origin and status | Scope decision |
|---|---|---|---|
| ROUTE-HOME-DOCS-LEADS | https://ampcode.com/docs/using-amp/screencasts/orbs · https://ampcode.com/docs/orbs/portals · https://ampcode.com/docs/orbs/event-driven · https://ampcode.com/docs/collaborate/multiplayer · https://ampcode.com/docs/the-dial · https://ampcode.com/docs/cli/remote-control | ROOT homepage hrefs; L; The Dial browser navigation entry verified by INT-DOCS-001 | P2; docs/learning variants; body analysis not established for these leaves |
| ROUTE-HOME-SCREENCAST-LEADS | https://ampcode.com/docs/using-amp/screencasts/orbs/add-a-dev-sign-in · https://ampcode.com/docs/using-amp/screencasts/orbs/test-agent-friendliness | ROOT homepage hrefs; L | P2 same series family; two episode representatives sampled above |
| ROUTE-HOME-ORB-ANCHORS | https://ampcode.com/docs/orbs#review-changes-and-browse-files · https://ampcode.com/docs/orbs#use-the-terminal | ROOT homepage hrefs; L anchors; base article T | P2 same route, separate navigation/scroll contracts; browser landing not established here |
| ROUTE-HOME-NEWS-LEADS | https://ampcode.com/news/plaid-mode · https://ampcode.com/news/opus-5.5 · https://ampcode.com/news/less-noise · https://ampcode.com/news/shared-runners · https://ampcode.com/news/the-mac-app-is-your-runner | ROOT homepage hrefs; L | P2 announcement family; Many Many Pucks is representative |
| ROUTE-MODES-NEWS-LEADS | https://ampcode.com/news/the-dial · https://ampcode.com/news/meet-puck · https://ampcode.com/news/talk-to-puck | SUP resolved mode-record links; T-r | P2 announcement family; content retrieval is not full page analysis |
| ROUTE-MODES-DOCS-LEADS | https://ampcode.com/docs/tools · https://ampcode.com/docs/models-and-subagents | SUP resolved role links; T-r | P2 documentation family; multiple role cards converge on these pages |
| ROUTE-ORBS-NEWS-LEADS | https://ampcode.com/news/portals · https://ampcode.com/news/agents-in-orbs · https://ampcode.com/news/multiplayer · https://ampcode.com/news/schedule · https://ampcode.com/news/slack-integration · https://ampcode.com/news/event-driven-orbs · https://ampcode.com/news/from-agent-to-agent | SUP Orbs capability links; T-r | P2 announcement family; Slack extraction exposes carousel controls, a distinct lead needing representative investigation |
| ROUTE-ORBS-NOTE-LEADS | https://ampcode.com/notes/putting-an-agent-in-an-orb · https://ampcode.com/notes/what-i-want-to-tell-you-about-orbs | SUP Orbs reading links; T-r | P2 note family; deep long-article sample exists |
| ROUTE-INSIDERS-NEWS-LEAD | https://ampcode.com/news/amp-free-is-full-for-now | SUP community-notice link; T-r | P2 announcement family |
| ROUTE-DOCS-NAV-FAMILY | Numerous grouped docs leaf links appear in sampled docs navigation; exact exhaustive href inventory not captured here | CONTENT source text; discovery breadth only | P2; explicitly incomplete leaf census; do not fabricate routes or mark all documentation analyzed |
| ROUTE-CHRONICLE-CONTENT-FAMILY | Numerous publication/video/series entries appear in the sampled Chronicle | CONTENT source text; discovery breadth only | P2; representatives define candidates, not every body; exact exhaustive href inventory remains pending |

## Authentication, download and external boundary ledger

| ID | Full entry/destination | Intent and observable entry | Investigation / exclusion |
|---|---|---|---|
| ROUTE-SIGN-UP | https://ampcode.com/auth/sign-up | Start/account creation; email/provider entry returned | P3 E; public entry only; no submission |
| ROUTE-PRICING-SIGN-UP | https://ampcode.com/auth/sign-up?returnTo=/pricing | Pricing signup/paid-tier entry; pricing return intent | P3 E; SUP link retrieval; query preservation required |
| ROUTE-SIGN-IN | https://ampcode.com/auth/sign-in | Account entry; email/provider/passkey representations | P3 E; public entry only; no authentication |
| ROUTE-WORKSPACE | https://ampcode.com/workspace → https://ampcode.com/auth/sign-in?returnTo=/workspace | Team creation/access; retrieval redirects to sign-in | P3 E; authenticated workspace excluded |
| ROUTE-CHATGPT-SETTINGS | https://ampcode.com/settings/model-routing?add=chatgpt → https://ampcode.com/auth/sign-in?returnTo=/settings/model-routing?add%3Dchatgpt | Connect subscription; homepage/docs lead; auth boundary | P3 E; CONTENT reported redirect; private setup excluded |
| ROUTE-PROJECT-CREATE | https://ampcode.com/projects?newProject=1 | Add code/create project; tool stopped at authorization boundary | P3 E; CONTENT; private project workflow excluded |
| ROUTE-INSTALL | https://ampcode.com/install | CLI workspace installation lead | P1/P3 unresolved; CONTENT fetch failed; need entry classification; installation excluded |
| DEST-MAC-DOWNLOAD | https://static.ampcode.com/mac/latest.dmg | macOS app download href on `/app` | P3 download boundary; ROOT at 390; not clicked/installed |
| DEST-APPLE-BETA | https://testflight.apple.com/join/Skjdm6qe | iPhone/iPad beta href on `/app` | P3 external beta entry; ROOT at 390; not clicked |
| DEST-LAB | https://amplabs.com | Research-lab/enterprise-engineering link from About/Pricing | P3 external; body not in reconstruction scope |
| DEST-STATUS | https://ampcodestatus.com | Footer operational status | P3 external; body not investigated |
| DEST-TRUST | https://trust.ampcode.com | Security report request | P3 external; no report requested |
| DEST-SPOTIFY | https://open.spotify.com/show/1AL44JiuDAszIPDnLNzBIu | Podcast subscription | P3 external; retrieval title only, no playback |
| DEST-FEED | https://ampcode.com/news.rss | Chronicle News feed | Feed representation excluded from visual template; retrieval unsupported media type |
| DEST-BRAND-ASSETS | https://ampcode.com/logo-light.svg · https://ampcode.com/logo-dark.svg · https://ampcode.com/app-icon.svg | Press-kit brand downloads | Assets, not page routes; availability does not establish reuse permission |
| DEST-EXTERNAL-LEADS | YouTube, X, GitHub, press videos, podcast RSS, email links | Proof/subscription/media/contact leads seen in extraction | P3; some exact hrefs omitted/fetch-failed; record DOM destinations before replacement implementation |

## Root-report provenance and unresolved scope

ROOT observations were supplied by the root investigator on the investigation date and persisted in the linked browser-template samples and observation record. Desktop samples use 1440 × 900 and mobile samples 390 × 844 unless stated otherwise; pricing's initial sample is 1280 × 720 with 1265 px layout width. Supporting and content web workstreams never used the Cua browser. Root's public `/app` rendering resolves the earlier web-only fetch gap. Supporting download links remain unclicked.

Root additionally browser-sampled `/news/many-many-pucks`, `/docs`, `/docs/cli` and `/notes/how-to-build-an-agent` at 1440 × 900. Chronicle's initial loading sample is unsuitable for settled geometry; later full DOM content was sampled. Docs mobile drawer/search and Next The Dial/Back were tested. These updates do not mark all documentation leaves or all P2 states investigated.

This inventory is a scoped census, not a claim that every nested public URL was deeply investigated. P0/P1 fidelity completeness must be assessed from the linked specifications and matrix. Critical remaining route work: install-entry classification; Insiders apply destination; raw hash landing verification; podcast playback template; exact external href census; deeper P2 responsive/motion/state coverage. No private/backend reconstruction is planned.
