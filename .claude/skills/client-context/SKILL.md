---
name: client-context
description: Brief the user on everything the brain knows about a client before a conversation or meeting. Use when the user says "brief me on <client>", "load my context", "what do I know about <client>", or "prep me for my call with <client>".
---

# Client context  ·  "Brief me on [client]"

A fast, honest briefing from the vault before client contact.

## Steps

1. **Read** `Clients/<client>/_index.md`, then every file it links (newest first), the related `People/` notes, and recent `Meetings/` that mention the client. Also grep the rest of the vault for the client name (mentions live in Projects/ and Patterns/ too).
2. **Brief, in this order:**
   - Status in one line (engagement, phase, mood if recorded)
   - Key people and roles (from `People/`)
   - Last contact: when, what happened, what was agreed
   - Open actions and promises (theirs and the owner's, from `03-tasks.md`)
   - Open questions or risks recorded in the vault
3. **Be honest about gaps.** If the vault has nothing recent, say "last entry is from <date>; the brain knows nothing after that." Never pad a thin briefing with plausible-sounding filler. Everything load-bearing cites its file.
4. **Offer one next step**: draft talking points, prep with grill-me, or update the hub after the meeting.

## Guardrails

- Only state what vault files support; cite the file.
- If the client folder does not exist, say so and offer to create the hub from what the owner tells you.
- Read-only: this skill briefs, it does not write (except, if asked, to start the hub).
