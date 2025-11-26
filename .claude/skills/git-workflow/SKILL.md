---
name: git-workflow
description: Git integration with ske validate auto-commit
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

- Version archives (`.version.card` files)
- Cleared reasoning fields
- Normalized XML formatting
- Brainstorm pool→used moves
- TODO reference fixes

## .gitignore

`ske init` ensures `.ske/` directory (database, caches) is ignored.

## Manual Git Operations

For story content commits, use regular git:
```bash
git add characters/NewCharacter/
git commit -m "Add NewCharacter backstory"
git push
```
