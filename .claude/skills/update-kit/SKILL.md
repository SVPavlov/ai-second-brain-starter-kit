---
name: update-kit
description: Fetch the latest shared kit (skills, commands, manual) into this vault without touching the owner's notes, and tell them what changed. Use when the user says "update my kit", "update mijn kit", "is my kit up to date", or asks whether there is a new kit version.
---

# Update kit  ·  "Update my kit"

Pull the newest shared parts of the framework (everything under `.claude/` plus `CLAUDE.md`) from the kit repository, show the owner what changed, and never touch their notes. Works the same on macOS and Windows (plain git, no shell tricks).

## Steps

1. **Check the remote.** `git remote get-url kit`. If it is missing, add it once:
   `git remote add kit https://github.com/SVPavlov/ai-second-brain-starter-kit.git`
2. **Fetch.** `git fetch kit`. If this fails (no network, no git), stop and tell the owner what failed; do not improvise a download.
3. **Compare versions.** Read `kit_version` from the local `CLAUDE.md` frontmatter and from `git show kit/main:CLAUDE.md`. Same version → report "up to date (vX)" and stop.
4. **Show what is coming.** Read `git show kit/main:.claude/CHANGELOG.md` and summarize the entries newer than the local version, in the owner's language, three lines or fewer per version.
5. **Protect local edits.** If the owner's `CLAUDE.md` or anything under `.claude/` has uncommitted or personal changes (`git status`, `git diff` on those paths), show the diff and ask before overwriting; suggest they park personal rules elsewhere for now. Never silently discard their work (asks, never guesses).
6. **Apply.** `git checkout kit/main -- .claude CLAUDE.md`, then commit in the owner's own repo: `kit update to vX`. Notes, folders and numbered files are never part of this checkout.
7. **Close.** Append one line to `04-log.md` (update-kit, from vY to vX). Report: new version, the changelog highlights, and anything the owner should do (a new skill to try, a rule that changed).

## Guardrails

- This skill updates ONLY `.claude/` and `CLAUDE.md`. If the checkout would touch anything else, stop: something is wrong with the repo layout.
- Never resolve a conflict between kit changes and owner changes silently; the owner decides.
- No git in this vault (not a repo)? Point the owner to the manual update path in the docs instead of improvising.
