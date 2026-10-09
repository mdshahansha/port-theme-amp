# Component inventory

Observed anatomy is confirmed; names and proposed abstraction boundaries are recommendations. Contracts in [component-contracts.md](component-contracts.md) cover the high-risk foundations. Root browser and web evidence IDs resolve in [evidence-index.md](evidence-index.md).

| ID / proposed component | Primitive/composite | Confirmed anatomy/use | Variants and behavioral dependency |
|---|---|---|---|
| COMP-GRID-001 / Lens grid | Primitive | Marketing aligned rails/cell padding, one/three/five tracks | Section-specific spans; fluid cell padding; 768/1024 boundaries |
| COMP-TYPE-001 / Display heading | Primitive | Sagittaire Display with italic word emphasis | Homepage fluid title vs96px editorial/pricing vs sans-serif docs |
| COMP-NAV-001 / Marketing navigation | Composite | Wordmark, primary links, Sign In, Start | Main links vs48px mobile trigger and dim overlay; article breadcrumb variant |
| COMP-CTA-001 / Link button | Primitive | Filled primary and outlined secondary anchors | Dark orange/teal vs cream blue;4/6px radii; actual focus/hover coverage partial |
| COMP-POPOVER-001 / Explanation | Composite | Trigger,288px content, shadow/layer | Orb definition vs product-surface list; Escape closes |
| COMP-HERO-001 / Prompt storm | Composite | Decorative haze/grain, dynamic prompt wrappers, reserved rotating H1, copy, CTA | Coupled word animation and responsive wrapping; fixed stage560px |
| COMP-PLAYER-001 / Screencast | Composite | Two streams/posters, stage panes, controls, chapters, transcript | Desktop sidebar; mobile chapters/transcript; media/layout state axes |
| COMP-BENTO-001 / Linked feature | Composite | Caption/H3/tick/support text plus HTML/SVG miniature | Portal, phone diff, event orbit, multiplayer chat, terminal; unequal spans |
| COMP-PROOF-001 / Testimonial | Composite | Attributed quote, avatar, external link | Prominent grid vs compact320px repeating track; decorative duplicate groups |
| COMP-EPISODES-001 / Lesson strip | Composite | Header/summary/CTA/arrows +four linked episode cards | Horizontal overflow; disabled first previous state |
| COMP-INSTALL-001 / CLI command | Composite | Platform select/button variants, command text, copy icon | Homepage constrained column vs docs wider row; three command values |
| COMP-NEWS-001 / Announcement row | Composite | Date, serif title, summary, whole-row link | Flat vsAVIF art background; grid date/title on desktop, stack mobile |
| COMP-FOOTER-001 / Directory | Composite | Wordmark/status/legal +Product/Resources/Guides/Community | Shared marketing/editorial; docs independent shell |
| COMP-PRICING-001 / Plan card | Composite | Title/price/features/CTA/detail popovers | Hobby/Individual/Teams/Enterprise; Individual tier tabs |
| COMP-FAQ-001 / Single-open questions | Composite | Button/expanded answer | Pricing state Q1→Q2 closes Q1; close-current/key behavior open |
| COMP-DOCS-001 / Docs shell | Composite | Header, search, sticky grouped sidebar, article, Markdown actions, next/previous | Mobile320px nav drawer and search dialog; white reading palette |
| COMP-ARTICLE-001 / Editorial body | Composite | Breadcrumb, date/author, heading, prose/media/code | News inline-heading images; note long code; archived guide anchors |

Typography, navigation, grid and asset changes cross many templates. Player/sidebar changes affect section geometry and downstream scroll positions. Hero title cannot be extracted as a generic rotating-label primitive until actual schedule/interruption rules are resolved. Exact props, event schemas, data fetching and component APIs are not observed and must be designed in the implementation task.
