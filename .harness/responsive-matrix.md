# Viewport coverage

Measurements are in [home-matrix.json](evidence/measurements/home-matrix.json). Window dimensions were verified on the target tab. All seven required samples were inspected; this does not constitute complete visual or behavioral sign-off.

| Profile | Viewport, px | Layout/document width, px | Sample document height, px | Hero font size / line height, px | Grid | Coverage |
|---|---|---|---|---|---|---|
| Large desktop | 1920 × 1080 | 1905 | 7000 | 65.12 / 58.608 | 5 fractional tracks | Computed geometry; no persisted screenshot |
| Standard desktop | 1440 × 900 | 1425 | 6578 | 53.12 / 47.808 | 5 fractional tracks | Full-page/top visual inspection and deep interaction samples; images retained only in session |
| Small desktop | 1280 × 800 | 1265 | 6409 | 49.12 / 44.208 | 5 fractional tracks | Computed geometry |
| Tablet landscape | 1024 × 768 | 1009 | 6212 | 42.72 / 38.448 | 5 fractional tracks | Computed geometry |
| Tablet portrait | 768 × 1024 | 753 | 7149 | 36.32 / 32.688 | 3 equal tracks | Computed geometry and navigation state |
| Mobile | 390 × 844 | 375 | 9600 | 33.12 / 29.808 | 1 column | Top/scroll/menu/player visuals and actions; images retained only in session |
| Small mobile | 360 × 800 | 345 | 9701 | 33.12 / 29.808 | 1 column | Top visual inspection and computed geometry |

Adjacent-width samples used a height of 900 px:

| Width pair, px | Observed outcome |
|---|---|
| 639 / 640 | One column and hidden desktop navigation on both sides; no composition change |
| 767 / 768 | Navigation and section-grid switch |
| 1023 / 1024 | Section-grid switch |

Supporting pages were sampled mostly at 1440 × 900 and 390 × 844. Pricing's initial sample was explicitly measured at 1280 × 720, with 1265 px layout width; do not attribute that sample or its H1 value to 1440 px. Source-text-only secondary pages have no viewport claim. DPR 1 was confirmed; browser zoom remains unknown.

Full-page screenshot capture transiently removes the scrollbar. Its geometry cannot replace the ordinary viewport baseline. Media, sidebar and transcript actions changed page heights later; comparisons must use matching states.

The episode-thumbnail sample of 283.70 × 159.58 px belongs to the actual 1440 px homepage, within a 326.89 px card. A viewport request had applied to another selected tab; the thumbnail size is not a mobile measurement. The later 390 px hero phrase wraps were verified separately on the actual target tab.

Documentation at 390 px has a measured 320 × 844 px drawer and 374 × 412 px search panel. These component-state samples supplement the matrix and do not establish complete keyboard/focus containment or device-touch coverage.
