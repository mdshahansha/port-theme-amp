# Confirmed relative motion timelines

No first-frame/page-load video exists. This document combines CSS-relative timelines with caller-clock-bracketed DOM samples, not absolute timings from navigation start. Sources: ANIM-HERO-001, HOME-MOTION-001, HOME-CSS-001, HOME-CSSOM-001 and HOME-TIMED-DOM-001 in [evidence-index.md](evidence-index.md).

## Four-word title entrance sample

The measured phrase was “Continue from your phone.” Relative times below use the CSS animation activation origin; they do not establish a page-navigation origin.

| Relative time | Event | End from declared 560 ms duration |
|---|---|---|
| 280 ms | Word 1 starts | 840 ms |
| 340 ms | Word 2 starts | 900 ms |
| 400 ms | Word 3 starts | 960 ms |
| 460 ms | Word 4 starts | 1020 ms |

Adjacent words start 60 ms apart and each runs for 560 ms, yielding 500 ms of overlap. This arithmetic follows recorded CSS configuration; it is not filmed completion evidence. Do not generalize the four-word sample to every phrase or to exit timing.

Declared entrance starts at opacity 0/translateY(26 px), ending opacity 1/Y 0 with origin 0% 100%. Exit travels 18 px upward and fades to 0; timed computed styles confirm 300 ms, ease, center origin and four-word delays 0/40/80/120 ms. New emphasis skews 14→0 degrees/fades in; old emphasis skews 0→−14 degrees/fades out; both use 560 ms and cubic-bezier(0.16, 1, 0.3, 1).

Old exit nodes and new delayed entry nodes coexist in the same sampled DOM transition. Four exit endpoints from declared duration/delays are +300/+340/+380/+420 ms, while entrance starts at +280/+340/+400/+460 ms from its CSS activation origin. Removal samples fall around transition +300…420 ms. These establish configuration and sampled coexistence, not continuously filmed overlap or exact navigation T0.

## Measured insertion cadence

HOME-TIMED-DOM-001 contains 495 read-only samples over 12,014 ms at 1440×900/DPR1, with caller clock readings bracketing each DOM read. First observed new-phrase read brackets were 124–162 ms (Agents), 4156–4192 ms (Share), and 8144–8172 ms (Send prompt). These support an approximately four-second insertion interval; differences between brackets span about 3.95–4.07 seconds. They are bounded observational estimates, not a serialized exact 4000 ms timer.

Exact scheduler origin, whole eight-phrase period, pause/offscreen behavior, interruption/re-entry and runtime reduced-motion scheduling remain unknown. A 300 ms exit duration does not define the phrase period or navigation-start delay.

## Continuous effects

Testimonial tracks and Puck drift/bob run in parallel with independent CSS clocks; the Puck outer loops have recorded negative delays. Exact loops are listed in [animation-spec.md](animation-spec.md). Title rotation continues during session inspections. These observations do not establish that effects are ordered after a navigation entrance, nor that every effect has the same clock origin.

No navigation/supporting-copy/CTA entrance sequence was established. Storm entrance is configured as 10 px downward→0 with fade-in over 420 ms; storm exit is 0→−4 px with fade-out over 700 ms and ease, using the measured 10 px inline distance. This does not establish particle creation frequency or overlap with title changes.

## Declared preference and interaction alternatives

Loaded CSSOM confirms title entrance/emphasis animations disabled and exit words hidden under reduced motion; storm uses fade-only names with retained timing. Proof drifters are hidden and bob/caret motion is disabled. Testimonial groups use manual horizontal scrolling, no mask/duplicates and zero right padding under reduced motion or a focused mini-card selector; hover pauses group animation. Actual preference/hover/focus activation and title scheduler behavior were not tested, so no runtime alternative timeline is asserted.

## Media action timeline

Clicking chapter 0:16 caused both media elements to seek/play; a subsequent sample read 16.311/16.316 seconds. The approximately 5 ms difference is a single measured sample, not a guaranteed synchronization tolerance. Selecting 1.5× changed both playback rates. A later pause was observed, but its cause is unknown.

Sidebar and caption toggles change layout/state while the media exists. They are independent control axes rather than playback prerequisites. Recording is needed to verify seek/loading/interruption behavior and establish a drift acceptance criterion.

## Required remaining capture

Record navigation start and useful frames at 0/150/300/500/750/1000/1500 ms, plus a complete phrase cycle at 1440 and 390 px widths, with font readiness noted. Repeat reload; capture early and mid-cycle exit, resize, offscreen/re-entry and reduced-motion behavior when tooling supports it.

These checkpoints are a future observation protocol, not claims that those frames were captured. Do not fill missing timings with conventional values such as 700 ms or ease-out. Future verification is defined in [verification-plan.md](verification-plan.md).
