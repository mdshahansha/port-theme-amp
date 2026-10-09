# Content architecture

This document records structure without reproducing long reference prose. Canonical section content roles are in [page-specs/home.md](page-specs/home.md); URLs in [website-map.md](website-map.md).

| Family | Data/content units | Public conversion/navigation |
|---|---|---|
| Homepage | Eight rotating phrases with word emphasis; brief proposition; six demo shortcuts/15 chapters; five capability cards; attributed proof records; four usage labels; four episode cards; platform command records; six announcements; four footer groups | Sign-up, docs, pricing, episode details, article index, settings/auth boundary |
| Pricing | Four plan categories, two Individual tiers, feature lists with detail popovers, nine FAQ questions | Sign-up with pricing return intent, workspace/auth, Contact Sales |
| App download | App icon, platform headline, beta notice, two download blocks and requirements | macOS DMG, TestFlight, bug-report docs |
| Models | Payment-context toggle, mode records, subagent records, system models | Announcements, docs/security |
| About | Intro, beliefs, audience, testimonials, investors, team | Amp Labs external, internal-use learning hub, social proof |
| Orb explainer | Hero native video; numbered conceptual sections; anchored capability/story/size/reading sections | Public docs and announcements; no authenticated product rebuilt |
| Chronicle | Featured/category records, dated notes/news, guides, social follow links, time capsules and video entries | Article, learning, podcast and external video templates |
| Editorial/news | Breadcrumb, date/author, display headline, optional inline heading imagery, body/media/code/reading leads | Chronicle and shared footer |
| Documentation | Grouped navigation, search, article headings/body, page Markdown controls, local anchors and Previous/Next | Public learning links mixed with authenticated onboarding entries |
| Screencast | Screen/camera sources, player metadata, chapter/transcript records, series episodes | Seek within media and navigate lessons |
| Legal/security | Long reference sections/contents and external trust leads | Legal cross-links; primary-source text sampled only |

Template reuse is inferred from repeated anatomy, not confirmed source component identity. Preserve archived guide status and original content order; avoid replacing historical tutorial/model data with a current API tutorial. Pricing/model mappings and announcement dates are dated snapshot data that may change after this investigation. Private product interface elements shown in media/illustrations are presentation content, not public website controls.

Proposal for implementation: maintain typed content records and route/media provenance separately from presentation, with explicit article modules and local heading IDs. This is a future architectural recommendation, not an inferred CMS claim.
