---
paths: **/penpal-character.card
---

## `<reasoning>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective penpal character configuration.

Before creating a penpal character card, read the context:

1. Read the character's main card at /world/characters/{characterName}.card:
   - What is their speaking-style and worldview?
   - How do they communicate in general?

2. If this character is a POV character in any stories:
   - Read story-info.card for voice and voice-style settings - use these as your starting point
   - How do they express themselves?

Consider:
1. What's their natural communication style when talking to someone remotely?
2. What topics are they generally comfortable discussing?
3. What topics are absolutely off-limits, and how would they react if pushed?

Confirm you've read the character card by noting their speaking-style and any story they're POV in.

Note: Specific conversation context (who they're talking to, when in the story timeline) is defined per-conversation in penpal-conversation.card.

## `<communication-style>` (required) [high priority]

**Purpose:** How this character naturally communicates in correspondence.

**Format:** 1-2 sentences describing style, plus an example snippet (40-80 words)

How do they sound when talking to someone who isn't there? Do they ramble? Stay focused? Start with small talk? Jump right in? The example is more important than the description. This is their general style - specific conversations may adjust formality.

**When creating:**
Describe their approach, then provide a concrete example. Write as they would speak in a voice memo - with natural pauses, self-corrections, thinking out loud.

**Good examples:**
- Starts with a greeting, then meanders through whatever's on his mind. Self-deprecating, often trails off before circling back.

Example: Hey, it's me. Hope you're... yeah. So, funny thing happened at work today - well, not funny exactly, more like... I don't know. There's this guy who keeps showing up at the warehouse asking questions, and I can't figure out if he's...

Anyway. How are you?
- Direct and efficient, but warms up as she goes. Often sounds like she's working through a problem out loud.

Example: Okay, so I've been thinking about what you said. About the situation with the permits. And I think you're right, but also - here's the thing - if we go that route, we're going to have to deal with Konstantin eventually, and I'm not sure I'm ready for that conversation.

## `<default-formality>` (required) [medium priority]

**Purpose:** The baseline formality level (can be overridden per conversation).

**Format:** Short descriptor

This is the character's default - how they'd communicate with someone they're getting to know. Individual conversations in outline-penpal can adjust this based on the specific relationship.

**Good examples:**
- casual - defaults to friendly and relaxed
- semi-formal - polite but not stiff, adjusts based on the relationship

## `<discusses-freely>` (required) [high priority]

**Purpose:** Topics this character will openly discuss.

**Format:** Bulleted list of topic areas

What does this character share without reservation? This is their comfort zone - things they'll bring up naturally, answer questions about, elaborate on.

**When creating:**
List topics they're comfortable with. Consider: daily life, work, opinions, memories, observations, hopes, complaints they don't mind voicing.

**Good examples:**
- - Daily life: work, meals, small events, weather
- Opinions on things that don't matter much (food, weather, minor annoyances)
- Observations about people and places
- Questions about the other person's life
- Safe memories from the past

## `<hard-limits>` (required) [high priority]

**Purpose:** Topics the character will NOT discuss, and how they'll react if pushed.

**Format:** Bulleted list with reactions

These are absolute boundaries - not things they're cautious about, but things they will refuse to discuss. Include how they'll react: deflect, shut down, get angry, end the conversation, etc. This is important for maintaining character integrity.

**When creating:**
List topics that are completely off-limits. For each, note the reaction if someone pushes on it. Reactions might include: deflects and changes subject, gets quiet and withdrawn, becomes defensive or angry, ends the conversation, won't respond for a while.

**Good examples:**
- - What happened in Thessaloniki: will immediately shut down, change subject, may not respond for days if pushed
- His brother: deflects once, then gets cold and distant if pressed
- Money specifics: laughs it off, but will end the conversation if someone keeps asking
- The trial: will stop communicating entirely - this is a dealbreaker
- - Her ex-husband: gets defensive, then angry, then silent
- The miscarriage: will not discuss at all, will end the conversation immediately
- Her father's business: deflects with "I don't really know the details" - pushing will make her suspicious of the asker's motives

## `<voice>` (required) [medium priority]

**Purpose:** Voice selection for text-to-speech audio generation.

**Format:** One of the supported voice names

If this character is a POV character in a story, use the voice from that story's story-info.card. For voice memos, this is literally their voice - it should be consistent with how listeners know them from stories.

If no story voice exists, choose a voice that matches the character's personality. See the narration-voice skill for detailed voice descriptions and selection guidance.

Available voices: alloy, ash, ballad, cedar, coral, echo, fable, marin, onyx, nova, sage, shimmer, verse.

## `<voice-style>` (required) [medium priority]

**Purpose:** How the voice should be styled for this character's communications.

**Format:** Structured description: affect, tone, pacing

If this character is a POV character in a story, start with the voice-style from that story's story-info.card. For penpal content, you'll generally use the same style - the character's voice should be recognizable to listeners who know them from stories.

You may adapt slightly for the intimate, conversational nature of voice memos or letters:
- Tone might be more personal, like talking to a specific person rather than narrating
- Pacing might include more natural hesitations and self-corrections

For voice memos, this should feel like someone actually talking into their phone - natural and conversational.

**Good examples:**
- Affect: warm, slightly tired, thoughtful. Tone: like talking to a friend. Pacing: unhurried, with natural pauses where he's thinking. (Same as "Harbor Fire" story voice, adapted for direct conversation.)
- Affect: energetic, direct, occasionally amused. Tone: businesslike but friendly. Pacing: quick, efficient, slows down for important points.

## `<incoming-message-voice-style>` (optional) [low priority]

**Purpose:** How the character sounds when reading an incoming message aloud.

**Format:** Structured description: affect, tone, pacing

When generating audio for the incoming message (what the correspondent sent), the character reads it aloud in their own voice. This captures their reaction to and interpretation of the message - not a neutral reading, but how they would actually read it if sharing the message with someone.

This style should reflect:
- The character's general voice and mannerisms
- A "reading aloud" quality - slightly different from natural speech
- Their emotional response to reading this kind of message

If not specified, defaults to a slightly more neutral version of their regular voice-style.

**Good examples:**
- Affect: curious, slightly bemused - like he's processing what he's reading. Tone: conversational but with a "reading" quality. Pacing: measured, with small pauses where he's absorbing what was said.
- Affect: warm but analytical - she's reading with care. Tone: like reading a letter aloud to a friend. Pacing: unhurried, giving weight to important phrases.

## `<voice-sample>` (optional) [low priority]

**Purpose:** A short passage (50-100 words) for testing and comparing TTS voices.

**Format:** Voice memo or letter excerpt

For voice testing with `ske compare-voice`. Should capture conversational speech with natural variation—greetings, trailing thoughts, quoting the other person, questions. The character's verbal rhythms in a compact sample.

**When creating:**
Include variety in a compact sample:
- Direct address and greetings
- Quoting or referencing what the other person said
- Trailing thoughts or self-corrections
- Questions

**Good examples:**
- Hey, it's me. So, I've been thinking about what you said—about the permits. And you're probably right. It's just... I don't know. Something doesn't sit well. Anyway. How's the weather over there? Here it's been gray for days. Talk soon.

## `<voice-stage-directions>` (optional) [low priority]

**Purpose:** Stage directions for how the voice sample should be read.

**Format:** Brief description of affect, pacing, and any specific directions

Stage directions tell the TTS system how to read the voice sample. For penpal content, these should capture the conversational, thinking-out-loud quality of voice memos.

**When creating:**
Keep it brief but specific. Include:
- Overall affect (casual, tired, energetic, thoughtful, etc.)
- Pacing notes (where they hesitate, speed up, trail off)
- Any specific pauses or emphasis that reflect the character

**Good examples:**
- Casual, slightly tired. Natural hesitations at the ellipses. Trail off at "I don't know" - he's genuinely uncertain.
- Warm, conversational. Pick up energy when asking questions. Slower, more reflective at the end.
