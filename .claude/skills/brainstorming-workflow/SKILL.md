---
name: brainstorming-workflow
description: Using brainstorm pool/used directories for idea management
---

# Brainstorming Workflow

## Structure

```
brainstorm/
  pool/                     Unused ideas
    locations.card
    scenes.card
    secrets-and-clues.card
    choices.card
    endings.card
    plot-arcs.card
  used/                     Referenced ideas (auto-managed)
```

## When to Create Brainstorm Files

Begin once story-info.card, setting.card, and main character exist. Add ideas as outlines crystallize.

## Adding Ideas

Edit files in `brainstorm/pool/`:

```xml
<brainstorm>
  <idea name="Night_Audit" role="scene">
    Night audit at the sea-gate office reveals discrepancy
  </idea>
</brainstorm>
```

## Using Ideas

Reference from story files:

```xml
<ref ref="/brainstorm/pool/scenes#/Night_Audit" role="Tense discovery scene"/>
```

## Automatic Management

When `ske validate` runs:
- **Pool → Used**: If referenced, moves to `brainstorm/used/`
- **Used → Pool**: If no longer referenced, moves back
- **Updates refs**: Changes `/pool/` to `/used/` in referencing files

## Idea Properties

- Unversioned (opposite of canon)
- Use `name` attribute (title-like)
- Use `role` attribute (scene, location, character, etc.)
- Text only, no refs
- Referenced by slugified name: `/brainstorm/pool/scenes#/Night_Audit`
