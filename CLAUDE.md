# Story Project using .card format

## CARD_EDIT_LOOP

1. `ske guide` - Find next task (or `ske guide stories/StoryName`)
2. `ske create [path]` - Create .card files (NEVER create manually)
3. Fill fields (reasoning fields FIRST) - rules provide guidance automatically
4. Verify with user before finalizing
5. `ske snapshot [path] -m "why" --no-feedback` - Version bump
6. `ske validate` - Check consistency, auto-commit
7. Return to step 1

## Quick Reference

- `ske mv old.card new.card` - Rename with reference updates
- `ske todo add/list/mark` - Manage card todos
- Do NOT commit; `ske validate` handles commits

## Core Concepts

**References**: `<ref ref="/path.card" role="reason" />` - Leave off versions, auto-added.

**TBD**: Placeholder fields. Fill via CARD_EDIT_LOOP.

**Reasoning fields**: Fill FIRST before content fields.

## File layout

- `stories/` - individual stories
- `world/` - shared canon
- `brainstorm/` - ideas, NOT canon

## Skills

Use skills proactively—invoke when starting work they cover:
`creating-passages`, `creating-chapters`, `creating-stories`, `handling-critiques`
