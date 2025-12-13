---
paths: **/voice-glossary.card
---

## `<characters>` (required)

**Purpose:** Character names extracted from the project

Automatically extracted from all character entities in the `/characters/` directory. Each character name appears once in a name element. This list is regenerated when running `ske gen passage-voice`.

## `<locations>` (required)

**Purpose:** Location names extracted from the project

Automatically extracted from location-type entities in the `/world/entities/` directory. Each location name appears once in a name element. This list is regenerated when running `ske gen passage-voice`.

## `<words>` (required)

**Purpose:** Words with unusual pronunciations or transcription needs

This section can be manually edited to improve transcription accuracy. Words are automatically added from passage-voice files during regeneration, but you can enhance them:

- Add pronunciation guides: ``
- Mark words to ignore: `` (won't be included in transcription prompts)
- Leave words without pronunciation: `` (still included in prompts)

Words are sorted alphabetically. When the glossary is regenerated, manual edits (pronunciation and ignore attributes) are preserved, and new words from passage-voice files are added automatically.

Important: If you delete a word, it may be re-added during regeneration. To permanently suppress a word, use `ignore="true"` instead of deleting it.
