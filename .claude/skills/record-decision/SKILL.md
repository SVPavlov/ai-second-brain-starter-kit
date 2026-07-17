---
name: record-decision
description: Capture an important decision with its rationale and trade-offs, so future-you knows why. Use when the user says "record this decision", "document this decision", "we besloten...", or states in conversation that a choice has been made between options.
---

# Record decision  ·  "Record this decision"

Write down what was chosen, what was rejected, and why, while the reasoning is still fresh. The answer to "waarom hebben we dit ook alweer zo gedaan?" three months from now.

## Steps

1. **Detect the decision** from the conversation: what was chosen, what were the alternatives, what was the reasoning. Ask only for what is missing; the minimum is a title, the choice, and the why.
2. **Pick the depth.** Default is the quick record (five lines, one minute). Offer the full record only when the decision is high-stakes or contested (options with pros/cons, review criteria, stakeholders).
3. **Check for conflicts.** Search existing notes with `type: decision` for earlier decisions this one contradicts or supersedes. If found: never silently overwrite. Ask the owner, or add the question to `05-synthesis.md` (asks, never guesses). A superseded decision gets `status: superseded` plus a link to its successor; it is history, not garbage.
4. **File it** where it belongs, per the vault rules: about a client → `Clients/<client>/YYYY-MM-DD-decision-<slug>.md`; otherwise → `Projects/YYYY-MM-DD-decision-<slug>.md`. Frontmatter: `type: decision`, `tags`, `last_updated`, `related` (link the `[[client]]`, `[[project]]`, `[[people]]` involved), `status: active`.

   Quick record body:

   ```markdown
   # Decision: [title]

   **Chose:** [the option]
   **Over:** [the alternatives]
   **Because:** [the one-sentence reason]
   **Trade-off:** [what this costs or rules out]
   **Revisit if:** [condition or date]
   ```

5. **Close the loop.** Update the client `_index.md` hub (if client-related), update the `00-START-HERE.md` catalog, append one line to `04-log.md`. Confirm to the owner where it landed.

## Guardrails

- Record decisions that are strategic, hard to reverse, or whose reasoning will be forgotten. Do not record trivial or easily reversible choices; if asked to, say so and ask once.
- Data rules apply as everywhere: no client-confidential detail beyond what the vault may hold; when the decision text itself is sensitive, record the shape and link the source.
- A decision note states what WAS decided. It never edits history: changed circumstances produce a new decision note that supersedes the old one.
