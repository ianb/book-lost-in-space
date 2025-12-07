---
name: using-ske-guide
description: Understanding ske guide output and priority system
---

# Using ske guide

## Project Overview Mode

```bash
ske guide
```

Shows valid next tasks ranked by priority:
- Extend storyline (incomplete passages)
- Fill important TBD values
- Create TODO entities
- Update outdated references

## Story-Specific Mode

```bash
ske guide stories/MyStory
```

When working on a specific story, use this to see:
- Next step in the story workflow (create chapter, create passage, complete outline)
- TBD values within that story only
- TODO references within that story
- Story cards needing attention

This is the recommended way to focus on story development without project-wide noise.

## Task Analysis Mode

```bash
ske guide /stories/MyStory/chapters/1/passages/5
```

If path doesn't exist, shows:
- Prerequisites needed
- What's blocking creation
- Recommended order

If path exists, shows:
- Completion status
- Missing optional files
- Natural next steps

## Priority Levels

**High Priority**: Shown by default
- Story continuation points
- High-priority TBD values
- Missing required fields

**Medium/Low Priority**: Use `--show-all-priorities`
- Minor TBDs
- Optional expansions
- Enhancement suggestions

## Workflow Integration

1. Start session: `ske guide`
2. Pick a task from the list
3. Run: `ske guide [path]` for that specific task
4. If blocked, resolve prerequisites first
5. If ready, run: `ske instructions [path]`
6. Make edits, snapshot, validate
7. Return to step 1
