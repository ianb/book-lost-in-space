---
name: version-management
description: Using ske snapshot to archive card versions and manage semantic versioning. Use when finalizing edits to a card, when validation warns about content changes since last snapshot, or when you need to understand version drift between referenced cards.
---

# Version Management

## Using ske snapshot

```bash
ske snapshot path/to/file.card -m "Character needed stronger motivation" --no-feedback
ske snapshot path/to/file.card -m "Expanded backstory" --from-feedback="Motivation wasn't clear"
ske snapshot path/to/file.card -m "Added backstory" --no-feedback --todo-done=T1,T3
```

**Required options:**
- `-m` message - explain WHY the changes were made (not WHAT - the diff shows that)
- Either `--from-feedback="..."` OR `--no-feedback` (you must specify one)

**Optional:**
- `--todo-done=T1,T3` - Mark specified todos as done (removes them after archiving)

**What it does:**
- AI analyzes changes and determines bump type (major/minor/patch)
- Archives content to `.history.card` with changelog entry
- Clears reasoning fields after archiving
- Removes todos specified in `--todo-done` (errors if ID doesn't exist)
- Validates refs before snapshot (must pass before archiving)

## Writing Good Changelog Messages

**Focus on WHY, not WHAT.** The diff shows what changed; the message explains motivation.

Bad (describes WHAT):
- "Added backstory details"
- "Changed name from Bob to Robert"
- "Updated relationships section"

Good (explains WHY):
- "Character needed stronger motivation for betrayal"
- "Name felt too informal for the historical setting"
- "Clarified how Marcus knows the merchant guild contacts"

## Tracking Feedback

Use `--from-feedback` to capture user/reader feedback that guided the change. Transcribe or lightly paraphrase the important feedback. This will be analyzed to improve future instructions and guidance.

```bash
# Change based on feedback
ske snapshot character.card -m "Expanded backstory to show resentment" --from-feedback="Character's reason for betrayal wasn't clear"

# Change NOT based on feedback
ske snapshot passage.card -m "Fixed continuity error" --no-feedback
```

The feedback is stored in a `<from-feedback>` element in the changelog, separate from your `-m` message which explains your response to the feedback.

## When to Bump

**Major (1.0.0 → 2.0.0)**: Breaking changes
- Name changes
- Role changes
- Entity identity shifts

**Minor (1.0.0 → 1.1.0)**: Non-breaking additions
- New fields filled in
- Backstory expanded
- Relationships added

**Patch (1.0.0 → 1.0.1)**: Trivial fixes
- Typos
- Clarifications
- Formatting

## Version Drift

When references use old versions:

```bash
# Check a file's outgoing references for outdated versions
ske version-instruct path/to/file.card

# Find all files with outdated references TO a specific card
ske version-instruct --for /world/characters/Marcus
```

Both show changelogs and guidance for updating the references.

## History Files

Version archives are stored in `.history.card` files alongside each card:
- `character.card` → `character.history.card`
- Contains all archived versions with changelog entries
- Automatically managed - do not edit directly

## Batch Snapshots (Human Only)

**AGENTS: Do NOT use `--catch-up`. It is for human use only.**

If `ske validate` shows many files needing snapshot (more than ~10), tell the user:

> "There are N files needing snapshot. You can run them individually, or if you want to catch up quickly with a single message for all, you can run:
> `ske snapshot --catch-up -m "Batch catch-up" --no-feedback`
> Note: This applies the same changelog message to all files, so use it only when that's appropriate."

The `--catch-up` option:
- Finds and snapshots ALL files that need it
- Uses the same `-m` message for all files
- Warns about broken refs but proceeds (instead of erroring)
- Shows progress and success/error counts

This exists because snapshot intentionality matters - each file should have a meaningful changelog message. Batch mode sacrifices that for convenience when catching up on backlog.
