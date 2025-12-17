---
paths: **/passage-sleep.card
---

## `<reasoning-passage>` (optional) [low priority]

**Purpose:** Guided thinking for writing effective sleep prose.

Before writing, read the context: Read the outline-sleep.card for this piece - what's the setting, what sensory anchors should you return to, what topics can you meander through, what must you avoid? Read the narration-style from sleep-character.card - what rhythm and texture should the voice have?

Plan the delivery:
1. How will you open - action, observation, or simply being?
2. What sensory detail will you establish first?
3. How will thoughts meander without arriving anywhere urgent?
4. What will you return to (the sensory anchors)?
5. How will the piece end - fading out, settling deeper, or simply stopping in peace?

Confirm you've read the outline by noting the setting and 2-3 sensory anchors.

## `<text>` (required) [high priority]

**Purpose:** The prose delivered to listeners.

First-person narration from the character. Follows the narration-style from sleep-character.card. No plot, no conflict, no resolution - just presence. The character describes their setting, notices sensory details, lets thoughts drift through safe topics.

Key principles:
- Return to sensory anchors: Come back to the same sounds, textures, smells. Repetition with slight variation is calming.
- No questions: Don't plant "what will happen" or "I wonder why" thoughts.
- No urgency: Nothing needs doing. Nothing is pending.
- Meander, don't arrive: Thoughts can drift topic to topic without conclusion.
- Present tense, present moment: Stay in the now.

**When creating:**
Write in first person, present tense. Use short to medium sentences with natural pauses. Return to sensory anchors throughout. Let topics fade into each other without sharp transitions. End in stillness or gentle trailing off.

Follow the narration-style from sleep-character.card. Use the sensory-anchors from the outline. Stay within the meander-topics. Check against avoid-in-this-piece.

**When editing:**
- Does it match the narration-style from sleep-character.card?
- Does it use the sensory-anchors from the outline?
- Does it stay within the meander-topics?
- Have you checked against avoid-in-this-piece?
- Is there ANY tension, urgency, or unresolved question? (If yes, remove it)
- Does it feel calming to read aloud slowly?

## `<title>` (required) [high priority]

**Purpose:** Short, evocative title for the piece.

**Format:** 2-6 words

Should evoke the mood or setting without suggesting plot. Can reference the ambient setting, time of day, or dominant sensory element.

**When creating:**
Keep it simple and atmospheric. No verbs suggesting action. No questions.

**Good examples:**
- Late Evening Herbs
- Harbor Fog
- Candlelight and Rosemary
- The Quiet After

**Bad examples (avoid):**
- Waiting for Dawn *(suggests action)*
- Before the Storm *(implies tension)*

## `<voice-override>` (optional) [low priority]

**Purpose:** Override the character's default voice settings for this passage.

Use when you need to adjust voice or narration instructions for this specific piece. All subtags are optional—include only what you need to override.

Contains three optional subtags:
- `<voice>`: Override the TTS voice (same values as sleep-character.card)
- `<voice-style>`: Override the voice style/affect (same format as sleep-character.card)
- `<notes>`: Instructions for narration/delivery (passed to audio generation)

The `<voice>` and `<voice-style>` values are used by audio generation. The `<notes>` inform how the piece should be delivered.

**Good examples:**
- <voice-override>
  <notes>This piece is especially quiet - deliver even more softly than usual, with longer pauses between paragraphs.</notes>
</voice-override> *(Delivery notes for especially quiet piece)*
- <voice-override>
  <voice-style>Affect: dreamier, more distant than usual. Tone: almost whispering. Pacing: very slow, with long pauses.</voice-style>
</voice-override> *(Adjusting style for dreamier mood)*

## `<sources>` (optional) [low priority]

**Purpose:** References to the outline used.

**Format:** List of ref elements
