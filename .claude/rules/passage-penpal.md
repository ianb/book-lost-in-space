---
paths: **/passage-penpal.card
---

## `<reasoning-passage>` (optional) [low priority]

**Purpose:** Guided thinking for writing the response message.

Before writing, read the context cards:

From **penpal-conversation.card** (thread-level context):
- **correspondent**: Who is the character talking to?
- **relationship**: What's the nature of this relationship?
- **story-moment**: Where is the character in their story? What circumstances color their response?
- **medium**: Voice memo, letter, or text message?
- **formality**: How formal/casual is this exchange?

From **outline-penpal.card** (this exchange):
- **incoming-message**: What exactly did the correspondent say?
- **interpretation**: How does the character read this message?
- **emotional-response**: What is the character feeling? This shapes the tone.
- **will-share**: The specific topics, anecdotes, and questions to include.
- **initiates**: What the character brings unprompted - questions they ask, stories they share, topics they introduce.
- **will-avoid**: What to deflect, minimize, or handle carefully - and the strategies for each.
- **knowledge-boundaries**: What the character doesn't know and can't discuss.
- **response-arc**: The structure and emotional trajectory of the response.

From **penpal-character.card** (character-level):
- **communication-style**: Voice and phrasing patterns.

Plan the delivery:
1. How will you open - responding to something specific from the incoming message?
2. What tone and pacing? (Match the emotional-response from the outline)
3. How will you handle each item in will-avoid? (Use the strategies noted)
4. How will you close?

Confirm you've read the context by noting the relationship, story-moment, 2-3 things from will-share, 1-2 things from initiates, and 1-2 things from will-avoid with their strategies.

## `<incoming-message>` (required) [high priority]

**Purpose:** The message that prompted this response, copied from outline-penpal.card.

Copy the incoming-message verbatim from outline-penpal.card. This keeps the full exchange together in the passage card - the message received and the response sent. Having both in one place makes the passage self-contained for reading or audio generation.

**When creating:**
Copy the exact text from outline-penpal.card's incoming-message field. Do not modify or summarize it.

## `<text>` (required) [high priority]

**Purpose:** The character's response message.

Written in first person as a complete message. The outline-penpal.card has done the thinking - this is where you execute that plan in the character's voice.

Key principles:
- Match the medium: voice memos feel spoken, letters feel written
- Follow response-arc: structure the message as the outline planned
- Include will-share: every item should appear in the response
- Execute will-avoid strategies: use the specific deflection/minimization approaches noted
- Honor knowledge-boundaries: don't reference things the character doesn't know
- Match emotional-response: the character's feelings should color the tone
- Ground in story-moment: their current circumstances shape what they say

**Narrate the moment:** The recipient can't see the character, but the character can describe everything:
- Their environment: where they are, what's around them, ambient sounds
- Their physical reactions: sighing, laughing, shifting in their seat, rubbing their eyes
- What they're doing: making tea, looking out the window, pacing
- Interruptions: a noise outside, someone calling them, a thought that distracts them

This narration brings the message alive - it's not just words, it's a person in a place having an experience.

**When creating:**
The outline has already planned this response. Your job is to deliver it in the character's voice.

From penpal-conversation.card:
- Ground details in **story-moment** - what's happening in their life affects what they say
- Match **medium** - voice memos are spoken, letters are written
- Use **formality** level for the exchange

From outline-penpal.card:
- Use **response-arc** as your structure (opening, middle sections, closing)
- Include every item from **will-share** - these are the specific topics, anecdotes, questions
- Include every item from **initiates** - the questions they ask, stories they share unprompted, topics they bring up. These are things the character drives, not responses.
- For each **will-avoid** item, use the strategy noted (deflection, humor, subject change, etc.)
- Stay within **knowledge-boundaries** - the character can't discuss what they don't know
- Let **emotional-response** color the tone throughout

From penpal-character.card:
- Follow **communication-style** for voice and phrasing

For voice memos: write as the character would actually speak - with natural pauses, self-corrections, trailing thoughts, verbal tics. Narrate the scene: describe where they are, what they're doing, how they're physically reacting. The listener should feel like they're there with the character.

For letters: use appropriate salutation and closing for the relationship. The narration can be subtler but still present - describe the moment of writing, the setting, physical sensations.

**When editing:**
Check against penpal-conversation.card:
- Is it grounded in story-moment?
- Does it match the medium (voice memo vs letter)?
- Is the formality level correct?

Check against outline-penpal.card:
- Does it follow the response-arc structure?
- Does it include everything from will-share?
- Does it include everything from initiates? (questions asked, stories shared, topics brought up)
- Does it properly execute each will-avoid strategy?
- Does it stay within knowledge-boundaries?
- Does the tone match emotional-response?

Check against penpal-character.card:
- Does it match communication-style?

Overall:
- Does the voice feel authentic to this character talking to this correspondent?
- Does it respond to specific things from the incoming message?

## `<title>` (required) [high priority]

**Purpose:** Short, descriptive title for the exchange.

**Format:** 2-6 words

Should identify the exchange by its key topic, the relationship, or the moment. Titles often reference what the incoming message was about or the emotional core of the response.

**When creating:**
Keep it simple. Can reference the correspondent, the main topic, or the emotional content.

**Good examples:**
- To Elena, About Dad
- News from the Harbor
- The Children's Progress
- After the Long Silence

**Bad examples (avoid):**
- Message 3 *(too vague)*
- The Lie About Father *(spoiler)*

## `<voice-override>` (optional) [low priority]

**Purpose:** Override the character's default voice settings for this message.

Use when you need to adjust voice or narration instructions for this specific message. All subtags are optional—include only what you need to override.

Contains three optional subtags:
- `<voice>`: Override the TTS voice (same values as penpal-character.card)
- `<voice-style>`: Override the voice style/affect (same format as penpal-character.card)
- `<notes>`: Instructions for narration/delivery (passed to audio generation)

The `<voice>` and `<voice-style>` values are used by audio generation. The `<notes>` inform how the message should be delivered.

**Good examples:**
- <voice-override>
  <notes>This message is more emotional than usual - deliver with more warmth and occasional hesitation on the difficult parts.</notes>
</voice-override> *(Narration notes for emotional delivery)*
- <voice-override>
  <voice>ash</voice>
  <voice-style>Affect: tired, vulnerable. Tone: quieter than usual. Pacing: slower, with longer pauses.</voice-style>
</voice-override> *(Different voice for a specific mood)*
- <voice-override>
  <notes>The character is trying to sound casual but there's tension underneath. Let that come through in the pacing.</notes>
</voice-override> *(Just delivery notes)*

## `<sources>` (optional) [low priority]

**Purpose:** References to the outline used.

**Format:** List of ref elements
