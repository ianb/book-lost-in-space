---
name: creating-chapters
description: Creating chapters, workflow strategy, scene breakdown
---

# Creating Chapters

## Command

```bash
ske create /stories/Story_Name/chapters/1_Chapter_Title
```

Creates: chapter.card, chapter-placement.card

## Prerequisites

Story outlines must exist first (story-arc, story-acts).

## When to Create

- **chapter.card**: Define chapter metadata after establishing outline acts and major beats. Update when reordering passages or renaming the chapter.
- **chapter-placement.card**: Create after story-acts.card is complete but before writing passages. Update when story acts change or chapter structure is revised.

## Workflow Strategy

1. **Fill chapter.card** - Use `ske instructions` for fields
2. **Map acts to chapter** - chapter-placement.card
3. **Break into scenes** - chapter-placement.card (typical: 3-7 scenes)
4. **Create first passage**: `ske create .../passages/1_Scene_Name`

## When to Confirm with User

- Chapter structure (number of scenes)
- Major chapter events
- Ending/cliffhanger approach

## When to Proceed Autonomously

- Individual scene details
- Dialogue and descriptions
