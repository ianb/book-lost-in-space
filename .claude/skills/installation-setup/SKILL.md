---
name: installation-setup
description: Installing ske CLI and initializing new story projects
---

# Installation & Setup

## Installing ske CLI

Install the `ske` command-line tool globally:

```bash
npm install -g https://story-assets.ianbicking.org/packages/ske/dist/memory-atlas-ske-0.0.0-dev.tgz
```

**Note**: Version number may change. Check latest URL by running `npm run pack-upload` in the ske repository.

Verify installation:
```bash
ske --version
```

## Initializing a New Project

```bash
mkdir my-story-project
cd my-story-project
ske init
```

## What `ske init` Creates

**Project structure**:
```
.ske/                       Internal directory (gitignored)
  config                    Project configuration
  focus                     Current focus path
  index.v1.sqlite          Entity database

meta.card                   Project metadata
narrative-guide.card        Writing guidelines
writing-samples.card        Example passages
setting.card                World overview

characters/                 Character pool
locations/                  Location pool
canon/                      Canonical facts
timeline/                   Timeline events
stories/                    Story content

brainstorm/
  pool/                     Brainstorm ideas
    locations.card
    scenes.card
    secrets-and-clues.card
    choices.card
    endings.card
    plot-arcs.card

docs/
  RESEARCH.md               User research notes
  NOTES.md                  Agent preference notes
  ske/instructions/         Local instruction templates
```

**Git setup**:
- Initializes git repository if none exists
- Creates `.gitignore` with `.ske/` excluded
- Makes initial commit

## Initial Configuration

After `ske init`, fill in core files:

1. **meta.card** - Project identity
   - Title, author
   - Narrative structure (linear/CYOA)
   - Use chapters (true/false)

2. **narrative-guide.card** - Writing rules
   - Reading level, tone, rating
   - POV and tense
   - Passage length bounds

3. **setting.card** - World basics
   - What-where-when
   - Social order, themes
   - Realism level

## First Steps After Init

```bash
ske validate                          # Check initial setup
ske create /world/characters/Protagonist    # Create main character
ske create /stories/First_Story       # Create first story
ske guide                             # See what to work on next
```

## Updating ske

To update to latest version:
```bash
npm install -g https://story-assets.ianbicking.org/packages/ske/dist/memory-atlas-ske-0.0.0-dev.tgz
```

Re-run `ske init` in existing projects to:
- Update skill files in `.claude/skills/`
- Update instruction templates in `docs/ske/instructions/`
- Refresh database schema (non-destructive)
