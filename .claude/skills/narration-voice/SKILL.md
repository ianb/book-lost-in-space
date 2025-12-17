---
name: narration-voice
description: Configuring voice fields in story-info.card for text-to-speech audio generation. Use when setting up audio narration, choosing a voice personality, or preparing for the audio generation workflow (ske gen passage-voice, ske gen audio, ske gen audiobook).
---

# Narration Voice

Voice configuration in `story-info.card` controls text-to-speech audio generation.

## Three Voice Fields

Edit story-info.card to configure voice settings. The rules provide guidance on available options.

### `<voice>` - Voice Selection

Choose the TTS personality. Match narrator's age, gender, and personality:

- **alloy**: Female, low pitch. Great for narration, mature, perhaps Black
- **ash**: Male, low pitch, deep and gravelly, cowboy-like
- **ballad**: Neutral/male, British accent, high pitched, younger/peppy
- **cedar**: Male, medium pitch, glitchy but engaged
- **coral**: Female, medium pitch, enthusiastic but impersonal, podcaster-like
- **echo**: Neutral, could be male or female, naive, very neutral
- **fable**: Neutral/female, British accent, upper class/posh, very neutral
- **marin**: Female, medium pitch, glitchy but very personal and engaging, younger
- **onyx**: Male, low pitch, deep and smooth, perhaps Black
- **nova**: Female, high pitch, engaged and personal, professional but engaging
- **sage**: Female, high pitch, perky and light, great for narration, very professional
- **shimmer**: Female, medium pitch, direct and personable, intimate
- **verse**: Male, medium pitch, smooth and professional, perhaps impersonal

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

## Per-Passage Voice Override

Override story-level voice settings for individual passages using `<voice-override>` in passage.card:

```xml
<voice-override>
  <voice>onyx</voice>
  <voice-style>Affect: deep, authoritative. Tone: ominous. Pacing: slow.</voice-style>
  <notes>This passage has a dreamlike quality—read with softer, distant tone.</notes>
</voice-override>
```

All subtags are optional—include only what you need:
- `<voice>`: Different TTS voice for this passage
- `<voice-style>`: Different performance style
- `<notes>`: Instructions for stage directions (passed to AI during passage-voice generation)

**Use cases**:
- Different character takes over narration
- Applying critique feedback to narration (use `<notes>`)
- Special tone for flashbacks, dreams, or dramatic moments

## Comparing Voices

Use `ske compare-voice` to generate audio samples for comparing different voices before committing to a choice:

```bash
# Compare voices using card's voice-style
ske compare-voice stories/My_Story/story-info.card --voice nova --voice coral

# Override voice-style for testing
ske compare-voice stories/My_Story/story-info.card --voice nova --voice coral --voice-style "Gentle, warm"

# Compare multiple voices AND multiple styles (generates all combinations)
ske compare-voice stories/My_Story/story-info.card \
  --voice nova --voice coral --voice shimmer \
  --voice-style "Warm, intimate" --voice-style "Cool, professional"

# Custom sample text with stage directions
ske compare-voice stories/My_Story/story-info.card --voice shimmer --text "Close your eyes..." --stage-directions "Slow, dreamy"
```

When using multiple `--voice` and `--voice-style` arguments, samples are generated for all combinations (e.g., 3 voices × 2 styles = 6 samples). Maximum 16 samples per invocation.

Works with story-info.card, sleep-character.card, and penpal-character.card. Samples are uploaded to R2 and cached by content hash.

### Voice Sample Fields

Add `<voice-sample>` and `<voice-stage-directions>` to cards for consistent voice testing:

- **writing-samples.card**: Add voice sample for story voice comparison
- **sleep-character.card**: Add voice sample for sleep narration testing
- **penpal-character.card**: Add voice sample for penpal voice testing

Without these fields, `compare-voice` extracts the first ~150 words from the first passage.

## Audio Generation Workflow

Once voice fields are configured:

1. **Generate voice directions**: `ske gen passage-voice` - Creates passage-voice.card files with per-passage narration instructions
2. **Generate audio**: `ske gen audio` - Produces MP3 files for each passage using TTS
3. **Create audiobook**: `ske gen audiobook` - Combines passage audio into chapter/story audiobooks
