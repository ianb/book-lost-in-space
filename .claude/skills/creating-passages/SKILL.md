---
name: creating-passages
description: Creating passages with ske create, filling placement/outline/passage cards, and the writing workflow. Use when ready to write prose after chapter structure is defined, or when adding new scenes to an existing chapter.
---

# Creating Passages

## Command

```bash
ske create /stories/Story_Name/chapters/1_Chapter/passages/1_Scene_Name
```

Creates: passage-placement.card, outline.card, passage.card

## When to Create

- **passage-placement.card**: Create after chapter-placement.card (for chapter passages) or story-acts.card (for story-level passages) but before outline.card.
- **outline.card**: Build after scene outlines but before drafting prose. Update when passages change beats or when new branches are added.
- **passage.card**: Create or update a passage after its outline is approved. Revise whenever prose, timeline, or choice structure changes.

## Workflow Strategy

1. **Map to chapter scenes** - passage-placement.card
2. **Plan the passage** - outline.card (goals, beats, act)
   - Use `ske instructions` for field guidance
   - Ask user if passage goals are unclear
3. **Write the prose** - passage.card
   - Fill `<reasoning>` FIRST (voice, tone, key moments)
   - Check narrative-guide for POV, length bounds, tone
   - Check writing-samples for voice consistency
   - Use `ske instructions` for field details

## When to Confirm with User

- Passage goals if unclear from outline
- Major character decisions/reveals
- Significant plot developments

## When to Proceed Autonomously

- Prose details (show reasoning)
- Specific word choices
- Scene descriptions
