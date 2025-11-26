---
name: creating-entities
description: Creating characters, entities, canon, timeline - when and workflow
---

# Creating Entities

## Characters

```bash
ske create /world/characters/First_Last
```

**When to create**:
- They are mentioned by name in prose
- They have dialogue or significant interactions
- They influence the plot or other characters
- They appear in multiple passages
- You anticipate they will be a key character in the story

**Don't create for**:
- Unnamed background extras ("a guard", "the merchant")
- One-sentence mentions with no impact
- Generic roles without individuality

**Workflow**: Fill core identity first, mark relationships TBD, expand later. Use `ske instructions` for fields.

## Entities

All stable named things that aren't characters should be documented as entities at `/world/entities/Name.card`.

```bash
ske create /world/entities/Place_Name
```

**Entity types include**:
- Locations (cities, buildings, landmarks, regions)
- Organizations (guilds, factions, companies, governments)
- Religions and belief systems
- Countries and political entities
- Groups of people (ethnic groups, social classes, professions)
- Artifacts and significant objects
- Institutions (schools, courts, temples)
- Languages or traditions

**Entity structure**:
- `entity-type`: A short label (location, city, organization, religion, artifact, faction, etc.)
- `summary`: 1-2 sentence quick reference
- `description`: Bulleted list of stable facts for future reference

**When to create**: Document an entity when it:
- Becomes a recurring element in the story
- Influences choices or establishes canon facts
- Needs consistent details across multiple passages
- Has facts that should be remembered

**Don't create for**:
- Generic one-off mentions with no story impact
- Background elements that don't need consistency

**Workflow**: Start with entity-type and summary, add description bullets as details emerge. Use `ske instructions entity` for field guidance.

## Canon

```bash
ske create /world/canon/Fact_Name
```

**When to create**: Capture a canon entry when an outline or passage reveals information that should persist across branches, or when a major event changes the world state.

**Use for**: Established lore, world rules, historical events that multiple passages reference.

## Timeline

```bash
ske create /world/timeline/D1T08:00_Event_Name
```

**Format**: `D{day}T{hour:minute}_Event_Name`

**When to create**: Create an event when a passage, canon entry, or outline establishes a notable occurrence anchored to a specific time. Include both past events referenced in exposition and future commitments players must hit.

## General Timing

- **Before writing**: Core characters, main entities (key locations, organizations)
- **During writing**: Supporting cast, new entities as discovered
- **After writing**: Canon entries to solidify established facts
