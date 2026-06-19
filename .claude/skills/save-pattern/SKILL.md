---
name: save-pattern
description: Capture a reusable thing that worked, an approach, a template, a play, so it is there for the next engagement. Use when the user says "save this as a pattern", "remember how I did this", or "make this reusable".
---

# Save pattern  ·  "Save this as a pattern"

Turn something that worked into reusable knowledge in `Patterns/`, stripped of the client specifics so it travels.

## Steps

1. **Identify the pattern** from the conversation or a named note: the approach, the structure, the play, why it worked.
2. **Generalize.** Strip client-identifying details (names, numbers, anything confidential). A pattern is the transferable shape, not the engagement it came from. If the owner wants the worked example kept, link the source note rather than copying client data into `Patterns/`.
3. **Write** `Patterns/<short-kebab-name>.md`: frontmatter (`type: pattern`, `tags`, `last_updated`, `related`), a one-line "use this when...", the steps or structure, and what made it work. Link related people/clients/projects with `[[wikilinks]]` only where non-confidential.
4. **Update `00-START-HERE.md`** catalog and append one line to `04-log.md`. Confirm where it landed.

## Guardrails

- Patterns are sanitized by construction; never let client-confidential detail into `Patterns/`.
- Prefer updating an existing pattern over a near-duplicate.
