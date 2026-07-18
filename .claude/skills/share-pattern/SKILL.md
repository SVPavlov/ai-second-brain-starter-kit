---
name: share-pattern
description: Stage a sanitized pattern or skill for the group's shared library, with the owner approving exactly what leaves the vault. Use when the user says "share this with the group", "deel dit met de groep", "share this pattern", or wants to contribute something that worked to the shared layer.
---

# Share pattern  ·  "Share this with the group"

The upward path: what worked for you, made safe, offered to the group. Save-pattern keeps knowledge for YOUR next engagement; share-pattern is the extra gate that lets it leave your vault.

## Steps

1. **Pick the thing.** An existing `Patterns/` note, or something from the conversation (route that through save-pattern first — only filed patterns get shared). Skills you wrote yourself can be shared the same way.
2. **Sanitize AGAIN, stricter.** Patterns are sanitized by construction, but leaving the vault raises the bar (defense in depth): no client names or identifying combinations (industry + size + region can be enough), no numbers that betray a deal, no colleagues' personal details, and strip or flatten `[[wikilinks]]` — they leak your vault's structure and mean nothing outside it. Rewrite examples to be generic.
3. **Owner reads the EXACT text.** Show the staged copy in full and get an explicit yes. What the owner has not read, does not leave (this is the shared-layer rule from the data tiers, enforced).
4. **Stage it** in `Shared-outbox/<kebab-name>.md` with lightweight frontmatter: `type: shared-pattern`, `contributed: YYYY-MM-DD`, `status: staged`. The outbox is the airlock: staged means approved-to-leave, not yet left.
5. **Offer the routes out** (the group decides its governed route in session 3; until then, two work): paste it in the track's group chat for discussion, or — for the git-comfortable — a pull request to the kit repository, where review-before-merge is the quality gate. Mark `status: submitted` with the route and date once it actually left.
6. **Log** one line to `04-log.md` (what was shared, which route).

## Guardrails

- Nothing leaves without the owner reading the exact outgoing text. No exceptions, including "it's obviously clean".
- When in doubt about identifiability, tokenize more, not less — and say what you generalized so the owner can judge.
- The outbox never contains drafts-in-progress; only owner-approved copies. Everything else lives in `Patterns/`.
