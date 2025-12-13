---
name: git-workflow
description: How git integrates with ske commands. ske validate auto-commits validation fixes, ske snapshot commits version archives. Use to understand what gets committed automatically vs manually, and how to control commit behavior.
---

# Git Workflow

## Auto-Commit

`ske validate` commits changes automatically if:
- Validation passes (no errors)
- Running in git repository
- Changes detected

## Commit Message Generation

Uses AI (default: gpt-5-mini) to generate commit message from diff:

```bash
ske validate                                    # Uses default
ske validate --provider anthropic              # Use Claude
ske validate --model gpt-4.1-mini              # Specific model
ske validate --no-commit                       # Disable auto-commit
```

## What Gets Committed

By `ske validate`:
- Updated ref versions
- Normalized XML formatting
- Brainstorm pool→used moves
- TODO reference fixes

By `ske snapshot`:
- Version archives (`.cardhistory` files)
- Cleared reasoning fields
- Version bumps

## .gitignore

`ske init` ensures `.ske/` directory (database, caches) is ignored.

## Manual Git Operations

For story content commits, use regular git:
```bash
git add characters/NewCharacter/
git commit -m "Add NewCharacter backstory"
git push
```
