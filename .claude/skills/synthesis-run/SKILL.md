---
name: synthesis-run
description: The recurring quality pass that keeps the brain trustworthy. Detects conflicts/ambiguity/staleness, surfaces the top few as questions for the user, heals orphans, rebuilds the catalog. Use when the user says "run synthesis", "clean up my brain", or weekly.
---

# Synthesis run  ·  "Run synthesis"

*Detection may be delegated: where the vault-audit agent is available, dispatch it for the read-only sweep (it reports ranked findings) and keep the question-writing and owner dialogue here. The split keeps flag-never-resolve intact by construction.*

The quality mechanism. You detect, rank, and write questions; the owner answers. **You flag, the owner resolves. Never auto-resolve a contradiction.** The prime directive: when in doubt, ask, never guess.

## Phases

1. **Preflight.** Read `05-synthesis.md` to see the last run and carry forward unanswered questions. Budget your reading: the numbered root files plus notes touched in the last ~30 days, not the whole vault.
2. **Detect.** Scan recent content against the rest of the vault. Tag each finding and keep only those with evidence (file + quote):
   - `[conflict]` two notes assert incompatible facts
   - `[identity]` a mention that may be an existing person/client ("Henrik" vs `People/Henrik Voss.md`)
   - `[stale]` a time-bound fact past its shelf life, or a client untouched 60+ days
   - `[gap]` a task or decision with no owner or date
   - `[unclassified]` something filed with low confidence
   - `[drift]` a decision 14+ days old with no follow-through
3. **Rank and cap.** Score each finding 1 to 5; double it if the entity shows up in the next few days' meetings. **Write only the top 3.** The cap is the point: three questions get answered, twenty get ignored. A skipped question comes back lower; three skips and it parks.
4. **Write** to `05-synthesis.md` under `## Questions`, plain language, each tagged and sourced:
   ```
   - [ ] [conflict] <date> · "<claim A>" (file) vs "<claim B>" (file). Which is true?
   ```
   Then walk the owner through them one at a time (including older unanswered ones). Each answer is one of:
   - **TAP** a direct answer → update the notes, bump `last_updated`, move the question to `## Answered` with the answer + date.
   - **CTX** an answer with context → their free text becomes the source of truth; update notes, create stub notes + links for any new entities. The richest path.
   - **IDK** → do not park it; next run, go dig across the vault and name who to ask.
   - **SKIP** → it returns tomorrow, lower. Three skips, it parks in `## Answered`.
5. **Heal orphans.** Find notes the catalog does not reference and notes nothing links to. Link them where they belong, or propose moving stale ones to `Archive/` (owner confirms moves).
6. **Rebuild `00-START-HERE.md`** to match the vault. Append a run line to `05-synthesis.md ## Run log` and one line to `04-log.md`. Report in five lines or fewer, leading with how many questions remain open.

## Guardrails

- Phase 2 to 4 are the heart. If time is short, do detect + top-3 + rebuild and say you skipped healing.
- Never delete; archive. Never resolve; ask.
- Mechanics stay invisible: the owner sees meaningful questions, not detector names in the prose.
