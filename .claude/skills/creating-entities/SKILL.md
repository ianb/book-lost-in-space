---
name: creating-entities
description: Creating characters, entities (places, objects, organizations), canon facts, and timeline events. Use when deciding which story elements need their own card for tracking, when a character appears by name, or when world details need consistent reference across passages.
---

# Creating Entities

Follow CARD_EDIT_LOOP for each card created.

## Characters

`ske create /world/characters/First_Last`

**Create when**:
- Mentioned by name in prose
- Has dialogue or significant interactions
- Influences plot or other characters
- Appears in multiple passages

**Don't create for**: unnamed extras, one-sentence mentions, generic roles.

## Entities

`ske create /world/entities/Place_Name`

For stable named things that aren't characters: locations, organizations, religions, artifacts, factions, institutions.

**Create when**:
- Recurring element in story
- Needs consistent details across passages
- Has facts that should be remembered

**Don't create for**: generic one-off mentions, background elements.

## Canon

`ske create /world/canon/Fact_Name`

For established lore, world rules, historical events referenced across passages.

## Timeline

`ske create /world/timeline/D1T08:00_Event_Name`

Format: `D{day}T{hour:minute}_Event_Name`

For notable occurrences anchored to specific times.
