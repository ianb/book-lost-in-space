---
name: creating-sleep-content
description: Creating sleep content - plotless, vibes-focused relaxation audio narrated by a character. Use when creating calming first-person content for listeners to unwind with.
---

# Creating Sleep Content

Sleep content is plotless, ambient narration by a character. No story consequences, no tension - just the character's voice describing peaceful moments, sensory details, and gentle wandering thoughts.

## Goals

- Relaxing audio that helps listeners unwind
- Character's authentic voice in a calm state
- Rich sensory details (sights, sounds, textures, warmth)
- Meandering, unhurried pacing
- No conflict, no stakes, no story progression

## Workflow

### 1. Create Character Config

```bash
ske create /sleep/Character_Name
```

This creates `sleep-character.card` which defines:
- Reference to `/world/characters/Character_Name.card`
- Ambient settings where the character finds peace (drawn from their story experiences)
- Sensory preferences - what they notice
- Safe topics they can meander through
- What to avoid (universal sleep-unfriendly topics + character-specific)
- Voice settings (inherit from story-info.card if POV character)
- Optional `voice-sample` and `voice-stage-directions` for testing voices with `ske compare-voice`

**Read first:**
- The character's main card for personality and speaking style
- Any stories where they're a POV character for story-vignettes and voice settings

### 2. Create Individual Pieces

```bash
ske create /sleep/Character_Name/1_Moonlit_Garden
```

This creates two cards:

**outline-sleep.card** (lightweight planning):
- Pick an ambient setting from sleep-character.card
- Choose sensory anchors to return to
- Note the character's calm internal state
- List topics to meander through
- Explicit avoid checklist for this piece

**passage-sleep.card** (the prose):
- First-person, present tense
- Meandering, unhurried
- Rich sensory description
- No plot, no conflict
- Gentle internal observations

### 3. Generate Voice Files

```bash
ske gen passage-voice sleep/Character_Name
```

Uses "minimal" mode - the text is already conversational, so only pause markers and stage directions are added.

## Writing Guidelines

- **Tense**: Present tense ("I notice...", "The air feels...")
- **Pace**: Slow, with natural pauses. Sentences can trail off.
- **Sensory**: Prioritize physical sensations - warmth, texture, ambient sounds
- **Internal**: Gentle observations, not analysis or worry
- **Transitions**: Drift between topics naturally, no hard cuts
- **Length**: Follow pacing-notes in outline-sleep.card

## What to Avoid

- Conflict or tension of any kind
- Unresolved questions or mysteries
- Character growth or realizations
- References to stressful story events
- Anything that might activate the listener's mind

## When to Confirm with User

- Which character to use
- General setting/mood preferences
- Any specific sensory elements to include or avoid

## When to Proceed Autonomously

- Specific sensory details
- Topic meandering order
- Word choices and phrasing
- Pacing and rhythm
