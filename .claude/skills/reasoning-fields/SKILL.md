---
name: reasoning-fields
description: How to use reasoning fields effectively in .card files
---

# Reasoning Fields

## Purpose

Reasoning fields guide your thinking. They're meta-commentary for the agent, not story content.

Types: `<reasoning>`, `<reasoning-character>`, `<reasoning-plot-arc>`, `<reasoning-{field}>`

## Workflow

1. **Fill reasoning FIRST** - Work through your thinking
2. **Then fill content** - Based on your reasoning
3. **Validate archives** - `ske validate` clears reasoning for next edit

## After Archiving

When `ske validate` archives a version:
- Reasoning cleared automatically
- First reasoning field gets comment: `<!-- For instructions: ske instructions ... -->`
- Ready for next edit cycle

**Always fill reasoning before content fields.**
