# Timed DOM and copy follow-up

Reference: https://ampcode.com/, 9 October 2026. Codex IAB ID 2, actual 1440 × 900 viewport, DPR 1, dark preference, reduced motion false. Browser version/zoom remain unknown. All sampling was read-only against currently rendered DOM/computed styles; no screenshot recording or implementation code was produced.

## HOME-TIMED-DOM-001 — Headline transition samples

495 DOM reads were collected over 12,014 ms. Each read was bracketed by caller-side timestamps. This is a text/computed-style observation window, not a page-load T0 or frame-accurate recording. Relative times below are read intervals, rather than exact insertion timestamps.

| First sample of new phrase | Read interval from sampling start, ms |
|---|---|
| Agents that keep going | 124–162 |
| Share with teammates | 4156–4192 |
| Send prompt, close laptop | 8144–8172 |

Successive phrase insertions were approximately 4 seconds apart in this window. An exact 4000 ms scheduler, full eight-phrase cycle duration, offscreen behavior and interruption are **not** established. Do not convert this estimate into an exact timer fact.

New entering nodes and outgoing absolute nodes coexist at each sampled phrase change. New words retain 560 ms cubic-bezier(.16,1,.3,1) entrance animations delayed 280, 340, 400 and 460 ms for a four-word phrase. Outgoing words use 300 ms animations with computed easing **ease**, and delays 0, 40, 80 and 120 ms for the four-word outgoing phrase. Exit nodes disappear progressively afterward; removal timestamps are bounded by nonuniform reads.

A follow-up captured outgoing Ship / more at 300 ms with easing ease and delays 0 / 40 ms. Computed transform origins were 49.5742px 23.9023px and 57.9648px 23.9023px, consistent with each exit node's center. This differs from the explicitly declared entrance origin 0px 100%. Upward exit travel comes from HOME-CSSOM-001.

## ASSET-VIDEO-FLAGS-002 — Actual homepage media properties

| Media | loop | autoplay | muted | Native controls |
|---|---|---|---|---|
| Day-to-day screen MP4 | false | false | false | false |
| Day-to-day camera MP4 | false | false | true | false |
| drop-the-neo-2.mp4 | true | false | true | false |
| agents-anywhere-demo-no-tui.mp4 | true | false | true | false |

The last two are the CLI miniatures. Their loop property is now confirmed; whether viewport entry invokes playback is a separate lifecycle question. The custom day-to-day player supplies its own controls.

## INT-INSTALL-COPY-002 — New feedback observation

Selected Windows using the native Install platform select, then clicked the visible PowerShell command button. The accessibility tree added a heading **Copied to clipboard**, a Dismiss button, and a replacement adjacent icon node. This confirms visible feedback and supersedes the earlier single-click sample with no observed textual confirmation.

The browser session clipboard accessor returned content from the previously inspected docs Introduction page, rather than the selected command. Therefore command payload success is **UNKNOWN**; the cause may involve browser clipboard plumbing or site behavior and was not isolated. No installer command was executed. Icon details, toast/reset lifetime, permission-denied behavior and repeated-copy timing remain unknown.
