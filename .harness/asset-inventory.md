# Asset and generated-visual inventory

Source: ASSET-DOM-001/HOME-STRUCT-001, HOME-CSSOM-001, ASSET-VIDEO-FLAGS-002, and primary-source route evidence. **Availability is not permission to reuse.** No assets were downloaded; all external files below are **Available but permission/license unresolved** unless classified generated dynamically. Asset source URLs are inspection records, not local files. Font redistribution and proprietary media rights remain unknown. CSS font-face declarations are confirmed separately from actual requested subset/load status.

| Asset ID | Source / format | Confirmed intrinsic / display facts | Role / dependencies / loading |
|---|---|---|---|
| ASSET-LOGO-001 | Inline SVG, viewBox 0 0 281 144 | Header 62.44 × 32px; footer 120 × 61.49px at 1440px; currentColor | Shared marketing/editorial wordmark; vector source observed, not acquired |
| ASSET-FONT-001 | https://ampcode.com/fonts/SagittaireDisplay-Regular.woff2 | Preload as font/woff2; computed Sagittaire Display; declared Regular weight 400, woff2, font-display swap | Display text; actual load status/license/font metadata unknown |
| ASSET-FONT-002 | https://ampcode.com/fonts/SagittaireDisplay-ExtralightItalic.woff2 | Preload href confirmed; declared Sagittaire Display italic weight 200, woff2, font-display swap | Italic face mapping confirmed in HOME-CSSOM-001; actual usage/load status/license unknown |
| ASSET-FONT-003 | https://ampcode.com/fonts/TX-02-Variable.woff2 | Preload href confirmed; CSS maps this source to Berkeley Mono normal and italic, format woff2-variations, font-display swap | Family mapping confirmed; no weight range/axes declared in CSS. Actual variable-axis metadata, requested subset/load status, and license unknown |
| ASSET-FONT-004 | Sagittaire Text / Berkeley Mono computed families; CSS sources under /fonts/ | Sagittaire Text Medium 500, MediumItalic 500, and Light 300 use woff2 and font-display swap; Berkeley Mono mapping is recorded above | Feature headings / mono labels; actual requested subset/load status and font metadata/license unknown |
| ASSET-DEMO-SCREEN-001 | https://static.ampcode.com/docs/day-to-day-in-amp-screen-1080-v2.mp4 | Intrinsic videoWidth/videoHeight not captured; screen occupies 78.2143% of the display stage | 26:05 screencast screen; loop=false, autoplay=false, muted=false, native controls=false; custom controls; readyState 4 in sample |
| ASSET-DEMO-CAMERA-001 | https://static.ampcode.com/docs/day-to-day-in-amp-camera-1080.mp4 | Camera display width 20.7662%, left 79.2338% | Synchronized presenter; loop=false, autoplay=false, muted=true, native controls=false |
| ASSET-DEMO-POSTER-001/002 | https://static.ampcode.com/docs/day-to-day-in-amp-screen-poster.jpg ; https://static.ampcode.com/docs/day-to-day-in-amp-camera-poster.jpg | Poster attributes confirmed; dimensions unknown | Paused/loading demo presentation |
| ASSET-PUCK-GROUP-001 | https://ampcode.com/comet-busters/pucks/puck-{118,85,87,03,10,13,23}.webp (seven individually observed paths) | Each natural size 545 × 768px; sampled rendered square boxes vary 25.49–168.18px through transforms; alpha not inspected | Decorative drifters; empty alt; loading=lazy |
| ASSET-AVATAR-GROUP-001 | /home/orbs-avatars/{isaacbmiller1,rockatanescu,el_gemmmy,andrzejkrzywda,PopVerseYT,RavinBarthwal,greedymaximizer,FeifanZ,justine_chang39,...}.webp | Nine main portraits 40 × 40px from classes; compact 28px class leads; intrinsic size not captured | Attributed testimonials; duplicates share records; partial family inventory |
| ASSET-EPISODE-001 | https://static.ampcode.com/docs/orbs-get-started-in-orbs-thumbnail-v2.jpg | 1600 × 900px; display 283.70 × 159.58px at actual 1440px viewport | Episode 1; loading=lazy |
| ASSET-EPISODE-002 | https://static.ampcode.com/docs/orbs-portals-in-orbs-thumbnail.jpg | 1600 × 900px; same aspect/display sample | Episode 2; loading=lazy |
| ASSET-EPISODE-003 | https://static.ampcode.com/docs/orbs-add-a-dev-sign-in-thumbnail-v2.jpg | 1600 × 900px | Episode 3; loading=lazy |
| ASSET-EPISODE-004 | https://static.ampcode.com/docs/orbs-test-agent-friendliness-thumbnail-v2.jpg | 1600 × 900px | Episode 4; loading=lazy |
| ASSET-CLI-MEDIA-001 | https://static.ampcode.com/news/drop-the-neo-2.mp4 | Muted; paused sample at 2.638s after scroll; intrinsic size unknown | Local terminal demo; loop=true, autoplay=false, muted=true, native controls=false; visibility playback policy unknown |
| ASSET-CLI-MEDIA-002 | https://static.ampcode.com/news/agents-anywhere-demo-no-tui.mp4 | Muted; paused sample at 2.598s | Remote/local access demo; loop=true, autoplay=false, muted=true, native controls=false; visibility playback policy unknown |
| ASSET-NEWS-001 | https://static.ampcode.com/news/many-many-pucks-jungle.avif | 993 × 558px; display 980.09 × 108.13px in desktop row | Art-backed announcement; loading=lazy; crop behavior partly visual |
| ASSET-NEWS-002 | https://static.ampcode.com/news/shared-runners-background.avif | 993 × 558px; display 980.09 × 128.60px | Art-backed announcement; loading=lazy |
| ASSET-NEWS-003 | https://static.ampcode.com/news/the-mac-app-is-your-runner-hero.avif | 993 × 556px; display 980.09 × 128.60px | Art-backed announcement; loading=lazy |
| ASSET-NEWS-DETAIL-001 | https://static.ampcode.com/news/many-many-pucks-dark.png | Source URL confirmed by web; dimensions unknown | Representative news article screenshot |
| ASSET-APP-001 | App icon visible on /app | Source/dimensions not inventoried | App-download hero; not generated or downloaded here |
| ASSET-ORBS-VIDEO-GROUP-001 | Orb explainer hero user-content/artifacts MP4 plus 7 capability videos | Hero autoplay/muted/loop/controls true; other videos have native controls/muted/loop true and autoplay false | /what-are-orbs; URLs partially in browser-session outputs, not fully copied or acquired |

## Declared font-face records

HOME-CSSOM-001 confirms the following declarations. Sources are same-origin `/fonts/` files; see [CSS declaration findings](evidence/observations/cssom-findings.md). No fonts were exported.

| Family / source filename | Declared face / weight | Format / display |
|---|---|---|
| Sagittaire Display / SagittaireDisplay-Regular.woff2 | Regular 400 / normal | woff2 / swap |
| Sagittaire Display / SagittaireDisplay-Bold.woff2 | Bold 700 / normal | woff2 / swap |
| Sagittaire Display / SagittaireDisplay-Extralight.woff2 | Extralight 200 / normal | woff2 / swap |
| Sagittaire Display / SagittaireDisplay-ExtralightItalic.woff2 | ExtralightItalic 200 / italic | woff2 / swap |
| Sagittaire Display / SagittaireDisplay-ThinItalic.woff2 | ThinItalic 100 / italic | woff2 / swap |
| Sagittaire Text / SagittaireText-Medium.woff2 | Medium 500 / normal | woff2 / swap |
| Sagittaire Text / SagittaireText-MediumItalic.woff2 | MediumItalic 500 / italic | woff2 / swap |
| Sagittaire Text / SagittaireText-Light.woff2 | Light 300 / normal | woff2 / swap |
| Berkeley Mono / TX-02-Variable.woff2 | Normal and italic; no weight range/axes declared | woff2-variations / swap |

These declarations establish mapping and configured loading behavior. They do not establish which subset was requested, whether each face loaded, font-internal axis ranges, or reuse permission.

## Generated or layered visual dependencies

ASSET-GRAIN-001 is inline SVG noise at 160 × 160px with a filter, not a separate raster file. ASSET-GLOW-001 consists of layered CSS gradients/blur. ASSET-BENTO-001 is an HTML/SVG composition: all five homepage feature cards had zero img/video nodes, with 11/26/7/7/6 SVG nodes respectively. It must be specified as illustration anatomy, not treated as a screenshot file. Prompt bubbles are dynamic HTML records; the title uses text/span layers. The dotted rail/pseudo-element system and blurred-band mechanism remain incomplete. No Canvas/WebGL was established for the visible homepage; absence in inspected samples does not prove none exists anywhere.

Actual font subset/load status, font-internal variable-axis metadata, the full CSS asset manifest, media codecs/byte sizes, network priority, cached-variant policy, alt text for all content media, and authorized replacement policy are unresolved. The CSS-declared face mapping, weights where present, formats, and font-display are confirmed above. Asset-export refusal is a concrete limit; do not reacquire those assets through a different download mechanism.
