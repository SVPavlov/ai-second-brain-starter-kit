---
name: track-stats
description: Compute usage statistics from the vault's own logs and produce the track's measurement one-liner, ready to paste in the group. Use when the user says "track stats", "my stats", "meetregel", "hoe vaak gebruik ik mijn brein", or wants their measurement line for a session close.
---

# Track stats  ·  "Track stats" / "meetregel"

The measurement line, computed instead of guessed. The vault already records what it does (`04-log.md`) and what its owner answers (`05-synthesis.md`); this skill turns that into the one-liner the track collects every session.

## Steps

1. **Pick the window.** Default: the last 14 days (one fortnight between sessions). The owner can name another window.
2. **Skills that actually run** — parse `04-log.md` lines in the window, count runs per skill. "Echt draaien" = 2 or more runs in the window; list those with their counts, mention one-off runs separately. If the log is empty or sparse, SAY SO — that is the honest finding, not a failure to hide. (Read-only skills log too since manual v0.2.1; runs before that update undercount lookups, name that caveat when it applies.)
3. **Synthesis answer rate** — from `05-synthesis.md`: how many questions surfaced in the window were answered, and of those, how many within 48 hours (compare asked/answered dates where present; where dates are missing, report answered/total and say the 48h split is not computable).
4. **Hours saved** — never computed, always asked: "Hoeveel uur denk je deze week bespaard te hebben? Eigen schatting is prima." One number, the owner's.
5. **Produce the line**, exactly in the track format, session number from the owner:

   `S<N> | skills die echt draaien: <namen> | uur bespaard deze week (schatting): <uren> | synthese-vragen beantwoord <48u: n/m`

   Show the line ready to copy, then a short breakdown underneath (runs per skill, questions open vs answered) so the owner sees where the numbers come from.
6. **Log the run** to `04-log.md` (track-stats, window, line produced).

## Guardrails

- Every number traces to a log line or a synthesis entry; no number without a source (always sourced). The only estimate is the owner's own hours figure, and it is labeled as such.
- Do not editorialize the result ("mooi!", "te weinig"); report, the owner interprets.
- If `04-log.md` shows days with no runs at all, offer one observation max: the daily routine may not be running. No lectures.
