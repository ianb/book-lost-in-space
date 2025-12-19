# Story Project using .card format

## CARD_EDIT_LOOP

1. `ske guide` - Find next task → See: `using-ske-guide`
2. `ske create [path]` - Create .card files (NEVER create manually) → See: `using-ske-create`
3. Fill fields (reasoning fields FIRST) → See: `reasoning-fields`
4. Verify with user before finalizing
5. `ske snapshot [path] -m "why" --from-feedback="..."` → See: `version-management`
6. `ske validate` - Check consistency, auto-commit → See: `handling-validation-errors`
7. Return to step 1

## Card Path Syntax

Paths reference cards and elements within them. All paths are rooted at the project-level:

```
/path/to/card.card                    # Just the card
/path/to/card.card#/element           # Element within card
/path/to/card.card#/parent/child      # Nested element
/path/to/card.card#v1.2.0             # Specific version
/path/to/card.card#v1.2.0/element     # Element at specific version
```

The `#` separates the file path from the fragment. Version (`v1.2.0`) and element path (`/element`) are both optional.

## Command Examples

### Navigation & Discovery

```bash
ske guide                                    # What should I work on?
ske guide stories/MyStory                    # What's next for this story?
ske search "character name"                  # Find mentions
ske search --ref world/characters/Jane.card  # What references Jane?
ske search "betrayal" --kind passage         # Search only passages
```

### Creating & Editing

Use `ske create` instead of creating files directly

```bash
ske create /stories/NewStory/              # Create a new story
ske create /world/characters/Bob.card        # Create a character
ske mv world/characters/Bob.card world/characters/Robert.card  # Rename
ske set passage.card#/voice-override/notes "Speak slowly here" --append # Sometimes it is easier to set fields this way than to Edit
```

### Versioning

```bash
ske snapshot stories/MyStory/passages/1_Passage/passage.card -m "Revised opening"
ske snapshot world/characters/Jane.card -m "Added backstory" --from-feedback="User wanted more depth"
ske validate                                 # Check & auto-commit
```

### Todos & Critiques

```bash
ske todo list                                # Show pending todos
ske todo add /world/characters/Jane.card -m "Needs backstory"
ske critique list                            # Show pending critiques
ske critique mark C42 done                   # Mark critique resolved
```

## Core Concepts

**References**: `<ref ref="/path.card" role="reason" />` - Leave off versions, current version is automatically added

**TBD**: Placeholder fields. Fill via CARD_EDIT_LOOP.

**Reasoning fields**: Fill FIRST before content fields.

**Automatic linting**: `ske hook lint` runs automatically when .card files are written. Do not run it manually.

**Surfacing decisions**: When you make creative or interpretive decisions (character motivations, tone, plot directions, resolving ambiguity), summarize these for the user under a "Creative Choices I Made" heading so they can review and adjust.

## File Layout

```
stories/           # Individual stories
  MyStory/
    story-info.card
    passages/
      1_Opening/
        passage.card
        outline.card
world/             # Shared canon (characters, settings, entities)
  characters/
  entities/
  setting.card
brainstorm/        # Ideas, NOT canon
critiques/         # User/agent feedback
```

## Skills

Use skills proactively—invoke when starting work they cover:
`using-ske-guide`, `using-ske-create`, `creating-passages`, `creating-chapters`, `creating-stories`, `handling-critiques`, `handling-validation-errors`

@docs/PROSE_NOTES.md
