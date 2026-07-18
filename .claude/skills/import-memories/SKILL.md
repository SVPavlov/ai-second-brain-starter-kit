---
name: import-memories
description: Import exported ChatGPT or Claude conversation history into the vault, so a new brain starts full instead of empty. Use when the user says "import my memories", "import my chat history", "importeer mijn gesprekken", or mentions having an export file from ChatGPT or Claude.
---

# Import memories  ·  "Import my chat history"

A year of AI conversations is a year of context about your work, clients and thinking. This skill turns an export into a populated brain — the strongest onboarding accelerator there is.

## Steps

1. **Get the export.** Point the owner to the export route they need: ChatGPT (Settings → Data controls → Export data; a zip with `conversations.json` arrives by mail) or Claude (Settings → Privacy → Export data). They drop the file in `Inbox/`.
2. **Scout before processing.** Read the structure, count the conversations, report: how many, over what period, roughly what themes. Agree with the owner what to import: everything, work-only, or from a certain date. Big exports are processed in chunks; say how many passes it will take.
3. **Extract, per chunk:** clients and companies mentioned repeatedly → `Clients/<client>/` context notes; people → `People/` stubs; recurring projects → `Projects/`; approaches that worked → pattern candidates (via save-pattern, confirmed by the owner); facts about how the owner works → proposals for `01-me.md`. File with the standard frontmatter; source is "chat history import YYYY-MM" — sourced, always.
4. **The data tiers apply retroactively.** Old conversations can contain what today's rules would exclude (raw confidential material, regulated data). What crosses a tier gets skipped and reported, not imported.
5. **Big synthesis after.** An import this size guarantees conflicts and duplicates: run synthesis-run at the end and let the owner answer the top questions. Report the harvest: N clients, N people, N patterns, N proposals, plus what was skipped and why.
6. **Clean up:** the export file moves to `Sources/` (cold storage) or is deleted at the owner's choice — it contains everything, so it follows the private-repo rule either way. Catalog, `04-log.md`.

## Guardrails

- Never import silently; every pass ends with a short report of what was filed where.
- Chat history is the owner talking to an AI, not ground truth: facts extracted from it are marked with their date, and stale-looking ones become synthesis questions rather than current facts.
- Skip means skip: tier-crossing content is not summarized "safely" into the vault either. Report and leave it out.
