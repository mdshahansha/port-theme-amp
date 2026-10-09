# Loaded stylesheet inspection — HOME-CSSOM-001

Reference: https://ampcode.com/, 9 October 2026. Codex IAB ID 2, actual viewport 1440 × 900, DPR 1; dark preference, reduced motion false. Read-only inspection of `document.styleSheets` and recursively nested CSS rules already loaded in the browser. No asset bundle or source file was downloaded. These are transcribed declarations, not raw stylesheet exports. This record supersedes the earlier unknowns about declared keyframe paths, font associations, and some preference/interaction selectors.

## Title and prompt storm

| Target | Confirmed declared behavior |
|---|---|
| Title word entrance | Opacity 0→1; translateY(var(--enter-distance,26px))→0. Transform origin 0px 100%. Earlier computed sample confirms 560 ms, cubic-bezier(.16,1,.3,1), both, with 60 ms entrance stagger. |
| Outgoing title word | Opacity 1→0; translateY(0)→calc(var(--exit-distance,18px) × -1). Thus the configured exit travels upward 18 px. Actual computed duration/easing/stagger are confirmed separately in timed-dom.md. |
| Emphasis replacement | New text: opacity 0→1 and skewX(var(--lean-from,14deg))→0. Old text: opacity 1→0 and skewX(0)→var(--lean-to,-14deg). Each declares 560 ms, cubic-bezier(.16,1,.3,1), both; origin 0px 100%. Exact invocation scheduling remains unknown. |
| Storm entrance | Opacity 0→1 and translateY(entry distance)→0; 420 ms, cubic-bezier(.16,1,.3,1), both. CSS fallback distance is 28 px; the measured inline configuration is 10 px. |
| Storm exit | Opacity 1→0 and translateY(0)→-0.4 × entry distance; 700 ms, ease, both. With the observed inline distance, configured travel is -4 px. Spawn frequency, lifetime and interruption remain unknown. |

Reduced-motion CSS disables title entrance/emphasis animations and hides `.exit-word`. Storm animation names switch to opacity-only fade keyframes; the timing declarations remain. Runtime preference activation and phrase scheduling were **not** tested, because preference emulation was not exposed.

## Testimonial motion, masks and access

Drifters start at left = -size - 40 px, then translateX from 0 to 100vw + size + 80 px. The reverse flag reverses travel and sets the facing angle to -90° instead of 90°. Nested bobbing alternates translateY -10→10 px and rotation face-10°→face+10°. Durations and negative delays are in animation-spec.md.

Marquee groups translateX to -100% in a linear repeated cycle. Sequence gap and trailing padding are both 1.25rem. The horizontal mask is transparent at the ends and solid from 6% to 94%. A parent row mask fades the last 24 px vertically.

The loaded selector `.ot-marquee:hover .ot-group` declares `animation-play-state: paused`. A `:has(.ot-mini:focus-visible)` branch disables group animation, permits horizontal scrolling, removes the mask, hides duplicate groups and removes trailing sequence padding. These selectors are **CONFIRMED declarations**; actual hover/focus activation was not exercised.

Reduced-motion CSS disables drifter/bob/group animations, hides drifters and duplicates, removes the mask, enables horizontal scrolling and removes sequence trailing padding. The terminal caret's animation is also disabled. Actual reduced-motion rendering remains **UNKNOWN**.

## Relevant font-face associations

All listed sources are same-origin `/fonts/` declarations with `font-display: swap`. A declaration does not establish that every face was requested or successfully loaded. No font files were acquired, and licenses and binary variable axes remain unknown.

| Family | Filename | Declared weight / style |
|---|---|---|
| Berkeley Mono | TX-02-Variable.woff2 | Normal and italic faces, format woff2-variations; no weight range or axis declaration observed |
| Sagittaire Display | SagittaireDisplay-Regular.woff2 | 400 / normal |
| Sagittaire Display | SagittaireDisplay-Bold.woff2 | 700 / normal |
| Sagittaire Display | SagittaireDisplay-Extralight.woff2 | 200 / normal |
| Sagittaire Display | SagittaireDisplay-ExtralightItalic.woff2 | 200 / italic |
| Sagittaire Display | SagittaireDisplay-ThinItalic.woff2 | 100 / italic |
| Sagittaire Text | SagittaireText-Medium.woff2 | 500 / normal |
| Sagittaire Text | SagittaireText-MediumItalic.woff2 | 500 / italic |
| Sagittaire Text | SagittaireText-Light.woff2 | 300 / normal |

Other loaded global font declarations exist, including Perfectly Nineties, Berkeley Mono V2, Amp Mono Symbols and KaTeX faces. Their presence alone does not make them visible homepage requirements. This inventory prioritizes the measured visual families.

## Limits

No preference was changed, no hover was synthesized, and no stylesheet was modified. CSS declarations answer what is configured; they do not establish full lifecycle ordering, offscreen pause/resume, load timing, interruption behavior or all responsive runtime states.
