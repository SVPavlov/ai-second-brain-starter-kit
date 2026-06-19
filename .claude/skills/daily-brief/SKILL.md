---
name: daily-brief
description: Refresh the command center, the morning cockpit, from the brain plus an optionally pasted calendar. Use when the user says "daily brief", "what's my day", "morning briefing", or "refresh my command center".
---

# Daily brief  ·  "Daily brief"

Rebuild `02-command-center.md`, the daily cockpit. What changed, what's due, what needs you. (In cohort 1 this is a live dashboard; here it is the markdown stand-in.)

## Steps

1. **Ask once** for today's agenda if not pasted (paste from Outlook/calendar is fine; skipping is fine too).
2. **Gather** from the vault:
   - **What changed**: recent entries since the last brief (check `04-log.md`).
   - **What's due**: open items from `03-tasks.md`.
   - **What needs you**: count of open questions in `05-synthesis.md`; today's meetings to prep.
3. **For each meeting** on the pasted agenda: pull context from `Clients/` and `Projects/`. Flag meetings the brain knows nothing about (a signal, not a failure).
4. **Write `02-command-center.md`** with those three sections, set "Last refreshed", and keep it under one screen. Append one line to `04-log.md`.
5. **Show the brief** and offer to prep a specific meeting in depth (hands off to client-context) or rehearse one (grill-me). Nudge if open questions in `05-synthesis.md` are over 5 or stale over a week.

## Guardrails

- Never invent meeting times or attendees; only what was pasted or what the vault records.
- A brief that needs scrolling is a report, not a brief. Keep it tight.
