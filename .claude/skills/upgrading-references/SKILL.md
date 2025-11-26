---
name: upgrading-references
description: Using ske version-instruct to update outdated version references
---

# Upgrading References

## Finding Outdated References

When `ske validate` shows:
```
Reference uses outdated version: /world/characters/Marcus#v1.0 (current: v3.0)
```

## Getting Upgrade Guidance

```bash
ske version-instruct path/to/passage.card
```

Shows:
- What changed between versions
- Current entity state
- Current passage text
- Specific upgrade suggestions

## Example Workflow

```bash
$ ske version-instruct stories/MyStory/chapters/1/passages/2/passage.card

UPGRADE INSTRUCTIONS: /world/characters/Marcus in passage 2

Current reference: /world/characters/Marcus#v1.0.0
Current version:   /world/characters/Marcus#v3.0.0
Version gap:       2 major versions behind

=== CHANGES SINCE v1.0.0 ===

v1.0.0 → v2.0.0 (major):
  - Name changed: Marcus Bellini → Marco Bellini
  - Change summary: "Character renamed for authenticity"

v2.0.0 → v3.0.0 (major):
  - Role changed: Merchant → Information Broker
  - Change summary: "Revealed true profession"

=== UPGRADE GUIDANCE ===

1. Update reference to #v3.0.0
2. Change all instances of "Marcus" to "Marco"
3. Consider if merchant role still fits scene context
```

## Making Updates

Edit the passage:
1. Update `<ref>` version: `ref="/world/characters/Marcus#v3.0.0"`
2. Update prose based on changes
3. Add reasoning about compatibility
4. Run `ske snapshot -m "Updated Marcus reference to v3.0"`
5. Run `ske validate` to confirm

## Finding All References to Entity

```bash
ske version-instruct --for /world/characters/Marcus
```

Shows all files referencing Marcus with version info.
