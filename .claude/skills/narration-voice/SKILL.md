---
name: narration-voice
description: Configuring voice fields in story-info.card for text-to-speech audio generation. Use when setting up audio narration, choosing a voice personality, or preparing for the audio generation workflow (ske gen passage-voice, ske gen audio, ske gen audiobook).
---

# Narration Voice

Voice configuration in `story-info.card` controls text-to-speech audio generation.

## Three Voice Fields

Use `ske instructions /stories/StoryName/story-info.card` for complete voice list and field details.

### `<voice>` - Voice Selection

Choose the TTS personality: alloy, ash, ballad, cedar, coral, echo, fable, marin, onyx, nova, sage, shimmer, or verse.

Match narrator's age, gender, and personality.

### `<voice-style>` - Narration Performance

How the voice should perform. Use structured format:
```
Affect: [3-4 attributes]
Tone: [1-2 tones]
Pacing: [1-2 attributes]
Pronunciation: [only if needed]
```

**Examples**: Quick/tense/hurried for thriller, gentle/warm/measured for cozy mystery.

### `<voice-heading-style>` - Title Delivery

Simpler, neutral style for headings. Keep clear and steady, avoid drama. 1-2 sentences.

## Strategy

**Voice** = Cast the narrator (who)
**Voice-style** = Direct the performance (how)

**First-person**: Voice matches POV character's traits
**Third-person**: More neutral, professional narration

## When to Update

- Starting story (required)
- Tone shifts (minor bump)
- POV character changes (major bump)
- Fine-tuning (patch bump)

## Audio Generation Workflow

Once voice fields are configured:

1. **Generate voice directions**: `ske gen passage-voice` - Creates passage-voice.card files with per-passage narration instructions
2. **Generate audio**: `ske gen audio` - Produces MP3 files for each passage using TTS
3. **Create audiobook**: `ske gen audiobook` - Combines passage audio into chapter/story audiobooks
