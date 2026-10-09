# Extracted design system

Reference measurements: HOME-CSS-001, HOME-CSSOM-001, RESP-MATRIX-001, RESP-BOUNDARY-001, ASSET-DOM-001 in [evidence-index.md](evidence-index.md). Values below are confirmed unless marked otherwise. These are reference facts, not an implemented token library.

## Palette and page surfaces

| CSS variable | Exact observed declared value | Resolved role |
|---|---|---|
| --background | light-dark(#dfdfc1,#091c1e) | Cream marketing/editorial; dark teal homepage |
| --foreground | light-dark(#0b0d0b,#f6fff5) | Near-black/light ivory text |
| --primary | light-dark(#1588b2,#f6833b) | Blue CTA on cream; orange CTA on homepage |
| --primary-foreground | light-dark(#dfdfc1,#091c1e) | Text against CTA |
| --muted-foreground | light-dark(#29564e,#978e81) | Declared global muted token; local player buttons instead measured rgb(156,164,156) |
| --border | light-dark(#b1b1a5,#7d665b) | Theme border; many decorative rules apply opacity |

Homepage body computed rgb(9,28,30), text rgb(246,255,245). Testimonial section computed rgb(5,16,15); testimonial heading #dfdfc1. Supporting marketing body rgb(223,223,193), text rgb(11,13,11). Docs body rgb(250,250,248), independent sans-serif article system. Do not infer every route follows OS color preference: cream pages rendered while preference was dark.

## Typography

| Role | Confirmed values |
|---|---|
| Homepage hero | Sagittaire Display, serif; weight 400; 53.12 px at 1440; line-height 47.808 px (0.9); tracking -3.1872 px (-.06em); balanced centered text; emphasis italic |
| Homepage demo/CLI/news H2 | Sagittaire Display; weight 400; sample 29.04 px, line-height 36.3 px, tracking -.04em |
| Large section headings | Sagittaire Display with type-2xl; text-specific emphasis italic; see page spec |
| Feature/card headings | Sagittaire Text family/class observed; type-lg; weight 500; tracking -.04em. CSS maps the normal 500 face to SagittaireText-Medium.woff2. Actual font requests were not inspected. |
| Body | System UI family stack; hero 17.728 px / 25.0674 px at 1440, 16 px mobile; base document 13 px / 20 px |
| Eyebrows | Berkeley Mono, monospace; sample 11.984 px / 16.9454 px; uppercase |
| Docs H1 | System UI; 40 px / 40 px in desktop measurement; article width 704 px |
| Pricing/Models/editorial display | Sagittaire Display, 96 px in desktop samples; separate from the homepage type-3xl scale |

Exact declared fluid variables (rem base16px in measurements): type-3xl=clamp(2.07rem,1.07rem + 2.5 * min(1vi,calc(1920px / 100)),7rem); type-2xl=clamp(1.73rem,1.18rem + 1.36 * min(1vi,calc(1920px / 100)),4.5rem); type-xl=clamp(1.44rem,1.14rem + .75 * min(1vi,calc(1920px / 100)),3rem); type-lg=clamp(1.2rem,1.04rem + .4 * min(1vi,calc(1920px / 100)),2.1rem); type-base=clamp(1rem,.91rem + .22 * min(1vi,calc(1920px / 100)),1.5rem); type-sm=clamp(.83rem,.77rem + .15 * min(1vi,calc(1920px / 100)),1.13rem); type-xs=clamp(.69rem,.65rem + .11 * min(1vi,calc(1920px / 100)),.94rem). --type-lh-tight=1.1; --type-lh-normal=1.414.

Preload hrefs are confirmed for TX-02-Variable.woff2, SagittaireDisplay-Regular.woff2 and SagittaireDisplay-ExtralightItalic.woff2. Loaded CSS font-face declarations now confirm Berkeley Mono maps to TX-02-Variable.woff2 (normal and italic; woff2-variations; font-display swap). No weight range or variable axes were declared in the inspected rule. Sagittaire Display declares Regular 400, Bold 700, Extralight 200, ExtralightItalic 200 and ThinItalic 100. Sagittaire Text declares Medium 500, MediumItalic 500 and Light 300. All those faces use font-display swap. Declarations do not establish actual network-loaded subsets or licensing. See [cssom-findings.md](evidence/observations/cssom-findings.md).

## Layout and finishing

Five tracks at 1024 px and above: 560fr 560fr 373fr 373fr 373fr. Three equal tracks at 768–1023 px; one below 768 px. --lens-cell-padding = clamp(.75rem,1.5vw,1.5rem). Desktop section padding is 56 px vertically and 59.0112 px horizontally at 1440; children add 21.6 px cell padding, yielding the visible content anchor at 80.6016 px. The nested grid defines the composition. Hero copy has a maximum width of 672 px; the title reserves space for its longest phrase; the storm stage is 560 px high. Header height is 80 px at 1440.

Global --radius = .5rem; header CTA radius 4 px; hero CTA radius 6 px; popover radius comes from rounded-md, with its exact computed number not recorded. Primary hero CTA: 78.75 × 38 px, type 16 px / 24 px. Header CTA: 70.07 × 30 px, type 13 px / 20 px. Sign In: 62.84 × 30 px, 1 px #7d665b border, 4 px radius.

Hero glow: column radial gradient 55% 70% at 30% 45%, rgba(255,138,60,.5) → rgba(196,84,28,.2) at 55% → transparent at 80%, blur 28 px. Corner warm gradient: rgba(255,170,90,.22) → rgba(196,84,28,.1), blur 28 px. Teal glow: rgba(70,160,110,.16), blur 40 px. Inline SVG fractal-noise grain: 160 × 160, baseFrequency .9, numOctaves 2, opacity .07. The dotted vertical rails and short heading ticks are visually confirmed; exact pseudo-element geometry remains UNKNOWN.

Layers observed: decorative absolute backdrop has pointer-events none; relative heading/content uses z60; storm particles vary across z55–75 in samples; explanatory popover has class z50; section foreground uses z10/z20. This is sampled layering, not an exhaustive z-index scale. The popover shadow measured a 1 px translucent-white ring plus black shadows at 6 px / 16 px and 2 px / 6 px; the settled sample had no animation.

Motion values are in [animation-spec.md](animation-spec.md). No general spacing/shadow scale beyond measured values is asserted.
