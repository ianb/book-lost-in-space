---
name: version-management
description: Using ske snapshot to archive card versions and manage semantic versioning. Use when finalizing edits to a card, when validation warns about content changes since last snapshot, or when you need to understand version drift between referenced cards.
---

# Version Management

This is step 6 of CARD_EDIT_LOOP: `ske snapshot`

## Using ske snapshot

```bash
ske snapshot path/to/file.card -m "Character needed stronger motivation" --no-feedback
ske snapshot path/to/file.card -m "Expanded backstory" --from-feedback="Motivation wasn't clear"
```

**Required:**
- `-m` message - explain WHY (not WHAT - the diff shows that)
- Either `--from-feedback="..."` OR `--no-feedback`

**What it does:**
- AI analyzes changes → determines bump type (major/minor/patch)
- Archives to `.cardhistory` with changelog
- Clears reasoning fields
- Validates refs before snapshot

## Writing Good Messages

Focus on WHY, not WHAT:
- Bad: "Added backstory details"
- Good: "Character needed stronger motivation for betrayal"

## Version Drift

When references use old versions:

```bash
ske version-instruct path/to/file.card          # Check outgoing refs
ske version-instruct --for /world/characters/X  # Find refs TO a card
```

## Batch Snapshots (Human Only)

**AGENTS: Do NOT use `--catch-up`.** If many files need snapshot, tell the user about `ske snapshot --catch-up`.
