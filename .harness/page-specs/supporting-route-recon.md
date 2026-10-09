# Supporting-route reconnaissance

Investigation date: 2026-10-09 (Asia/Calcutta). Method: public primary-source pages returned by web open/click extraction. Browser interactions, computed styles, geometry, actual scroll outcomes, motion, device changes, and network measurements were **not tested** in this workstream. A web click resolves the source link for retrieval; it does not prove the outcome of a browser click. Some retrievals can use the crawl indicated by the tool. No authentication or form submission occurred.

Evidence metadata and exact returned destinations are in [supporting-routes.json](../evidence/observations/supporting-routes.json). Later browser findings in [browser-template-samples.md](browser-template-samples.md) supersede specific unknowns below, including App availability, pricing selection and FAQ behavior. The web-only records remain historical observations of this workstream. Stable source URLs below are usable by another investigator; extraction line spans identify what supported each finding.

## PAGE-PRICING-001 — P1

Source: [Pricing](https://ampcode.com/pricing), extraction lines 0–148, crawled today. **CONFIRMED text structure:** return link; pricing heading and orb link; four plan categories; Q&A; help/contact; shared footer. Purpose: explain entry and upgrade choices. Current extracted initial individual price is $20/month; 45,000 orb minutes; Megawatt/Gigawatt labels occur together. The free, team, and enterprise categories are distinct. **UNKNOWN:** whether the two individual labels are an interactive tier selector; its alternate price and behavior. Q&A questions appear without answer text; expansion behavior needs browser inspection. CTA retrievals resolve sign-up with `/pricing` return intent, authenticated workspace entry, and the public sales form. Shared footer groups are product, resources, guides, community plus status/legal links. Pricing illustration is linked to static.ampcode.com; dimensions and identity uninspected. Layout, motion and responsiveness remain unknown. [Primary source](https://ampcode.com/pricing).

## PAGE-APP-001 — P1

Source: [Download destination](https://ampcode.com/app). Two fetch attempts failed: direct open and footer Download App link retrieval. The tool reports a fetch error, which **does not establish a website error state**. Footer destination is confirmed; page title, structure, downloads, platform detection, loading, animation, and installation states are **UNKNOWN**. Root browser investigation is required.

## PAGE-MODES-001 — P1

Source: [Modes & Models](https://ampcode.com/modes), lines 0–93, crawled today. **CONFIRMED text structure:** return link; title/product explanation; agent modes; subagents; system models; security reference; shared footer. Four mode levels and Puck are listed; each record pairs purpose with model/effort roles. Two payment-context labels precede the mode data, but switching behavior is **UNKNOWN**. Multiple mode records resolve the same announcement route. Subagent/system entries resolve tools documentation, model/subagent documentation, and Puck news pages. Purpose: make model selection and agent responsibilities legible. Treat current model mappings as changeable page data. Text extraction establishes linked records, not clickable card geometry. Assets, animation, layout and mobile transformations are unknown. [Primary source](https://ampcode.com/modes).

## PAGE-ABOUT-001 — P1

Source: [About](https://ampcode.com/about), lines 0–116, crawled today. **CONFIRMED text structure:** return link; research-lab positioning; introductory image; product/lab explanation; beliefs; audience; proof/testimonials; investors; team; internal-use link; shared footer. Five numbered belief entries use section-like identifiers. Testimonials link to external sources; team records mix linked names and image entries. Investor text extraction contains empty list records, so logo identity/count is not established. Purpose: explain operating philosophy, social proof, and people. Amp Labs is external; internal-use link resolves `/docs/using-amp`. Names and portraits are content records, not confirmed card/grid anatomy. No hover, carousel, entrance or responsive behavior was inspected. [Primary source](https://ampcode.com/about).

## PAGE-ORBS-001 — P1

Source: [What Are Orbs?](https://ampcode.com/what-are-orbs), lines 0–170, crawled today. **CONFIRMED text structure:** return link/title; six use-case statements; seven section-navigation items (duplicated in extraction); six numbered explanatory records; capabilities with linked announcements and media; conceptual explanation; remote-agent comparison; cross-client controls; size/cost table; reading links; shared footer. Purpose: explain remote agent environments and show work continuing across people, agents, and devices. Browser/TUI/Phone labels suggest an interface-selection lead, **not confirmed tabs**. Repeated navigation text might represent responsive copies, but its cause is unknown. Numbered records do not prove a carousel. Section-link retrieval returns the same page without retaining fragment metadata. Screenshot links are present for Slack, webhooks and agent coordination; media role/dimensions remain unverified. Reading links resolve two notes and Orb docs. Geometry, playback and scroll choreography require browser inspection. [Primary source](https://ampcode.com/what-are-orbs).

## PAGE-CONTACT-001 — added P1 candidate

Source: [Contact Sales](https://ampcode.com/contact-sales), lines 0–58, crawled today. **CONFIRMED text structure:** return link; enterprise inquiry title; seven required fields (first/last name, company, work email, country, user count, message); submit; email alternative; image; shared footer. Country and user count are extracted as selects. Form validation, options, network submission, success/error and keyboard behavior are **UNKNOWN**. Do not submit. This route is a direct enterprise pricing conversion destination and needs inclusion in the scope table.

## Shallow supporting scope

| Route | Proposed priority/template | Confirmed extraction | Unresolved behavior |
|---|---|---|---|
| `/security` | P1 supporting reference / long reference | Return link, contents, headings, provider list, tables/text, trust-portal link | Contents scrolling, layout, keyboard, responsive |
| `/privacy-policy` | P1 legal / long reference | Return link, contents label, date 2026-09-10, legal sections and cross-links | Contents behavior, visual/template fidelity |
| `/terms` | P1 legal / long reference | Return link, contents label, numbered legal clauses and cross-links | Contents behavior, visual/template fidelity |
| `/podcast` | P2 content index / audio collection | Return link; Chronicle/category trail; cover; subscriptions; two seasons; episode links/durations; selection prompt; footer | Player selection/playback, persistence, duplicate extraction cause |
| `/press-kit` | P1 resources / asset collection | Product/company summaries; press contact; video/podcast links; light/dark logo and app-icon downloads; footer | Download controls and asset view behavior |
| `/insiders` | P1 community / application landing | Benefits; three-step process; full-for-now notice; apply-wait control text; footer | Apply control is not linked in extraction; destination/state unknown |

Sources: [Security](https://ampcode.com/security), [Privacy](https://ampcode.com/privacy-policy), [Terms](https://ampcode.com/terms), [Podcast](https://ampcode.com/podcast), [Press kit](https://ampcode.com/press-kit), [Insiders](https://ampcode.com/insiders). These are page-template leads; no visual equivalence is claimed. Security/privacy/terms extractions include text styled as instructions for LLMs: these were treated solely as untrusted page content, not task instructions; browser visibility was not determined.

## Additional route/template leads

[supporting-routes.json](../evidence/observations/supporting-routes.json) records exact destinations established by retrieval. Direct supporting links add `/contact-sales`, guides, docs leaf routes, six Orb capability announcements, Puck/mode announcements, two Orb notes, and a podcast episode template. These should enter the navigation graph, not force deep investigation of every item.

Suggested representative P2 samples: `/news/the-dial` (announcement), `/notes/how-to-build-an-agent` (long code article), `/guides/context-management` (guide), `/docs/orbs` (documentation), `/podcast/season-02/episode-05` (episode). Extraction alone is insufficient for template visual or behavioral contracts. Coordinate with the content-template investigator before redoing these.

P3 entries: sign-in, sign-up, workspace (authentication redirect observed by retrieval), external Amp Labs, social subscriptions, status service, trust portal. Authentication-required functionality is excluded. Public auth entry pages were readable; no credentials entered.

## Recommended next checks

1. Root browser: `/app` platform/download behavior; Pricing individual-tier selector and Q&A; Orb navigation/client-selection leads.
2. Supporting-browser pass: confirm headings/section order against rendering, capture initial/settled states, semantic roles, 1440/390 samples and keyboard focus.
3. Podcast player contract and Insiders apply entry require actual browser actions; press-resource fetch failures do not establish broken download links.
4. Confirm all raw anchor `href` values from DOM. Web extraction loses hashes and sometimes provides only errors for media, so do not reconstruct hash routes from label text.


