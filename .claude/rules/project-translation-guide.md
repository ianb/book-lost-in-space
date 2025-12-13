---
paths: translation-guides/*.card
---

## `<notes>` (optional) [low priority]

**Purpose:** Project-specific guidance that supplements the shared audience guide

**Format:** Free-form text describing any project-specific translation considerations

Use this for guidance that applies only to this project, not to all translations for this audience. For example, if this project uses a particular dialect or has a unique narrative voice that requires specific handling.

**When creating:**
Add notes about any project-specific translation needs that aren't covered by the shared audience guide. This might include:
- Special handling for the narrative voice
- Project-specific terminology that differs from the shared guide
- Cultural references unique to this story
- Tone or register requirements specific to this project

**Good examples:**
- This story uses a more formal register than typical. Maintain formal address ("usted") even in dialogue between friends to reflect the historical setting.
- The narrator has a sardonic tone. Preserve irony and dry humor in translation rather than making it more direct.

## `<renames>` (optional) [medium priority]

**Purpose:** Character and place name translations specific to this project

**Format:** List of <rename> elements with ref, name, and translation attributes

Provides explicit translations for character names, place names, and other proper nouns that should be translated differently in this project than the shared audience guide suggests (or that aren't in the shared guide).

**When creating:**
Add a <rename> element for each name that needs explicit translation. Include:
- ref: Reference to the character/location card with version (e.g., "/world/characters/Joe.card#v1.0.0")
- name: The original name as it appears in the source
- translation: How it should appear in the translated text

Only include names that need explicit handling. Names that should stay the same (like most proper names) don't need entries.

**When editing:**
- Does each rename have a valid ref with version?
- Is the name attribute the exact source form?
- Is the translation appropriate for the target audience?
- Are all character and place names that need translation included?

**Good examples:**
- 

**Bad examples (avoid):**
-  *(missing version in ref)*
