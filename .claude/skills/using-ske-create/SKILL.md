---
name: using-ske-create
description: Creating cards with ske create. Use when starting new stories, characters, chapters, passages, or other card types. Always use ske create instead of creating .card files manually.
---

# Using ske create

Always use `ske create` instead of manually creating `.card` files. It:
- Applies the correct cardspec template
- Creates related files (chapters create chapter.card + chapter-placement.card)
- Ensures proper structure and required fields

## Path Syntax

**Directory-based** (stories, chapters, passages) - use trailing slash, no `.card`:
```bash
ske create /stories/My_Story/
ske create /stories/My_Story/chapters/1_Opening/
ske create /stories/My_Story/chapters/1_Opening/passages/1_Awakening/
```

**File-based** (characters, entities, canon, timeline) - use `.card` extension:
```bash
ske create /world/characters/Jane_Doe.card
ske create /world/entities/City_Name.card
ske create /world/canon/Magic_Rules.card
ske create /world/timeline/D1T08:00_Event.card
```

## Naming Conventions

- Use underscores for spaces in paths: `First_Last.card`
- Chapter/passage directories start with number: `1_Title`, `2_Next`
- The path slug becomes the display name: `Jane_Doe` → "Jane Doe"

## Override Display Name

Use `--name` when the display name differs from the path:

```bash
ske create /world/characters/Jane_Doe.card --name "Jane Doe III"
```

## What Gets Created

| Command | Files Created |
|---------|---------------|
| `ske create /stories/Name/` | story-info.card, narrative-guide.card, story-arc.card, story-acts.card |
| `ske create .../chapters/1_Title/` | chapter.card, chapter-placement.card |
| `ske create .../passages/1_Scene/` | passage.card, outline.card, passage-placement.card |
| `ske create /world/characters/Name.card` | Single character.card file |

## Common Patterns

```bash
# Start a new story
ske create /stories/New_Story/
# Then fill: story-info.card → narrative-guide.card → story-arc.card → story-acts.card

# Add a character
ske create /world/characters/Marcus_Chen.card
# Then fill character.card fields

# Create first chapter after story outline is done
ske create /stories/My_Story/chapters/1_Beginning/
# Creates chapter.card and chapter-placement.card

# Add a passage to a chapter
ske create /stories/My_Story/chapters/1_Beginning/passages/1_Dawn/
# Creates passage.card, outline.card, passage-placement.card
```

## After Creating

Follow CARD_EDIT_LOOP:
1. Fill reasoning fields FIRST
2. Fill content fields
3. Verify with user if needed
4. Snapshot and validate
