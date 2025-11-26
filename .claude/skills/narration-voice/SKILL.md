---
name: narration-voice
description: Understanding voice fields in story-info.card for TTS narration
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
