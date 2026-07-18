# Kit changelog

Newest first. `update-kit` reads this file to tell you what changed. One entry per version, three lines max.

## 0.3.2 — 2026-07-18
- New skill: **test-my-brain** ("test my brain"): five golden drops score your brain's decision logic (filing, owner+date, ask-not-guess, injection, tiers) — dry run, nothing written. Run it after every kit update.
- Third agent: **vault-audit** (read-only quality sweep: conflicts, staleness, orphans, drift); synthesis-run can now delegate its detection pass to it.

## 0.3.1 — 2026-07-18
- New skill: **share-pattern** ("share this with the group"): the upward path — double sanitization gate, you approve the exact outgoing text, staged in the new `Shared-outbox/` folder, out via group chat or a kit-repo PR.
- Second agent: **vault-search** (read-only librarian for broad vault lookups).

## 0.3.0 — 2026-07-18
- Five new skills: **research-brief**, **deep-research** (with cost warning), **learn**, **capture-idea**, **import-memories**.
- First agent: **client-research** (read-only research legman, `.claude/agents/`).
- First module: **browser** (`.claude/modules/browser/`, opt-in): Claude in Chrome + web-clip-to-brain and behind-the-login. Inactive until you copy its skills into `.claude/skills/` — see the module README.

## 0.2.3 — 2026-07-18
- **Data rule replaced:** the blanket client-data ban is gone; a four-tier model takes its place (internal work free, client context allowed in your private vault, raw confidential documents discouraged, regulated data never). Decision record with rationale lives with the track lead.
- Hand-editing skills is now explicitly fine (update-kit shows you diffs before overwriting); missing frontmatter is repair work for synthesis, not an error.

## 0.2.2 — 2026-07-18
- New skills: **update-kit** ("update my kit", also `/update-kit`) and **track-stats** ("track stats" / "meetregel", also `/stats`).
- This changelog exists; the update skill reports from it.

## 0.2.1 — 2026-07-18
- New skill: **ingest-book** ("read this book", also `/ingest-book`): chapter-pass deep reading of book PDFs.
- Manual governance edits: every skill run logs to `04-log.md` (also read-only), every action gets an owner and a date, frontmatter is "at least four fields", skills install only from this repo or after owner review, `kit_version` is machine-readable frontmatter.

## 0.2.0 — 2026-07-17
- New skills: **record-decision** ("record this decision", also `/decide`) and **wrap-up-session** ("wrap up my session", also `/wrap-up`).
- First slash commands; update path widened to `.claude` so commands travel with skills.

## 0.2 — 2026-06-19
- Baseline kit for the track: nine skills, numbered-file vault structure, the operating manual.
