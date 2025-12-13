---
paths: **/passage.card
---

## `<reasoning-passage>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective passages

Before writing, read the context: Read this passage's outline.card to understand the beat sequence. Read the narrative-guide.card for tone, style, and passage-length. If this isn't the first passage, read the previous passage to understand where it left off. Confirm you've read these by briefly stating the passage objective and target length.

Identify what this passage must express: What does this passage have to express beyond the factual beats? What is the intended emotional impact on the reader? How will you achieve it through word choice, pacing, and sensory detail? Which key-tensions from the story are in play?

Plan the delivery: How will you deliver the must-convey facts from outline.card without exposition dumps? What sensory details will ground the reader? Does the timeline align with previous passages?

When revising, verify: Does the prose express the intended emotion? Does it accomplish the passage objective? Is the passage-length appropriate? Does it flow smoothly from the previous passage?

## `<text>` (required) [high priority]

**Purpose:** The prose delivered to the reader

This is the actual passage text readers will experience. Follow the narrative-guide.card for tone, pacing, dialogue formatting, and style guidance. Keep within the passage-length specified in narrative-guide.card. Use writing-samples.card as guidance and examples for generating the text—these provide concrete models of the desired style and voice.

The outline.card uses annotations to guide prose writing:

**Hidden information ((like this))** — Background context, plot secrets, or facts the POV character doesn't know. Don't state these directly in prose; they're author knowledge that informs how you write the scene. If the outline says ((he's been taking bribes)), you don't write "he was taking bribes"—you write his nervous behavior that hints at guilt.

**Character inner states ((POV: ...) or ((Name: ...))** — The messy, fragmentary texture of what characters are experiencing internally. Use these to guide word choice, body language, pacing, and subtext. In limited POV, the POV character's inner state shapes the prose voice; other characters' inner states inform how you write their external behavior. A character whose inner state is ((just get her out of here)) will have clipped dialogue, restless movements, forced smiles.

**Introductions [Introduces: ...]** — Flags that the reader doesn't know something yet and the prose needs to provide it. For a new character: their name, who they are, what they look like. For a concept: what it means, how it works. For a location: what it looks like, what it feels like. The annotation specifies what the reader needs to understand. Convey these naturally through action, dialogue, and observation rather than exposition—but the information does need to get across.

**When creating:**
Write the passage following the beats from outline.card. Use sensory details and concrete moments. Keep passage markdown clean—headings rarely needed, focus on paragraphs. Use italics/bold per narrative guide conventions.

**When editing:**
- Does the prose match the style in writing-samples.card?
- Does it follow all beats from outline.card?
- Are ((hidden info)) elements reflected through behavior/subtext, not stated directly?
- Do character inner states (((POV: ...)), ((Name: ...))) shape word choice and body language?
- Are [Introduces: ...] elements conveyed naturally through action/dialogue?
- Is the passage-length appropriate?
- Does it express the intended emotional impact?
- Does it flow smoothly from the previous passage?

## `<summary>` (optional) [low priority]

**Purpose:** Author-facing quick reference

One sentence describing what happens in this passage. Can contain spoilers since it's for authors, not readers.

## `<leaves-off>` (optional) [low priority]

**Purpose:** Handoff state and narrative promises for future passages

Captures two things: (1) where this passage leaves the reader and character - the state that the next passage will pick up from, and (2) any narrative promises or setups made in this passage that later passages must fulfill. Different from summary: summary describes what happened, leaves-off describes what future passages need to know.

**When creating:**
After writing the passage, note:

Immediate state: Where are we physically? What time is it? What is the character's emotional state? What tension or question carries forward?

Narrative promises: What has been foreshadowed, hinted at, or set up that must pay off later? Any objects introduced that need to reappear? Any questions raised that need answers? Any character intentions stated that need follow-through? If a character says "I'll deal with that tomorrow" or "We should talk about this later" - that's a promise to the reader.

**When editing:**
- Does it capture the essential handoff state?
- Would the next passage writer know where to start?
- Does it note any unresolved tension or question?
- Are all narrative promises and setups recorded? (Chekhov's gun: if you introduce something, note that it needs payoff)
- Any dialogue that implies future action?

**Good examples:**
- Maya alone in dark cafe, campaign at $3,400, uncertain if watching success unfold or failure begin. Twenty-six days left. She mentioned calling her mother "when this is over" - that call should happen. *(Captures state and a narrative promise)*
- Chen has left, Maya alone understanding what Groundwork really is. Eight days remaining. The envelope Chen left on the table hasn't been opened yet. *(Notes setup that needs payoff)*

**Bad examples (avoid):**
- Maya launched her campaign and it stalled. *(Just repeats summary)*
- Maya found the old photograph in the drawer. [Should note: photograph introduced, needs to matter later or be explained] *(Misses the setup)*

## `<title>` (required) [high priority]

**Purpose:** Short, descriptive passage title shown in readers and UIs

A concise title that captures the essence or key beat of the passage without spoiling outcomes. Should reflect the story's tone.

**CRITICAL: Titles must not spoil what happens.** Readers see passage titles before reading, often in a table of contents or chapter list. A spoiler title ruins the reader's experience by revealing outcomes, twists, betrayals, deaths, or decisions before they unfold in the prose. The title should evoke the setting, mood, or situation—never the resolution.

**When creating:**
Keep it concise (2-6 words). Write after the prose is complete so you can capture what actually happens.

**No spoilers:** The title should describe where/when/who, not what happens or how it ends. Think "Chapter 1: The Harbor" not "Chapter 1: Marcus Gets Betrayed." A reader glancing at the title should have no idea what's about to unfold.

**When editing:**
- Is it concise (2-6 words)?
- Does it capture the passage's essence?
- **Does it completely avoid spoilers?** (Would a reader know the outcome from the title alone?)
- Does it reflect the story's tone?

**Good examples:**
- Morning at the Harbor
- A Letter Arrives
- The Supervisor's Office
- An Unexpected Visitor

**Bad examples (avoid):**
- Niketas Betrays Marcus *(spoiler - reveals betrayal)*
- Father's Last Words *(spoiler - reveals death)*
- She Chooses to Stay *(spoiler - reveals decision)*
- The Hidden Letter *(spoiler - reveals discovery)*
- Introduction *(too vague)*

## `<include-if>` (required)

**Purpose:** One or two sentences describing the pressure ending the passage.

## `<include-if>` (required)

**Purpose:** Enumerate available options if stored inline.

## `<sources>` (optional) [low priority]

**Purpose:** References to the outline.card used to generate this passage

**Format:** List of <ref> elements with version references

Track which outline.card version was used when creating or updating this passage. Maintains dependency lineage.

## `<voice-override>` (optional) [low priority]

**Purpose:** Override the story's default voice settings for this passage

Use when a different character takes over narration for this passage, or when you need to adjust voice/narration instructions based on critique feedback. All subtags are optional—include only what you need to override.

Contains three optional subtags:
- `<voice>`: Override the TTS voice (same values as story-info.card)
- `<voice-style>`: Override the voice style/affect (same format as story-info.card)
- `<notes>`: Instructions for narration/stage directions (passed to passage-voice generation)

The `<voice>` and `<voice-style>` values carry directly into passage-voice.card and are used by audio generation. The `<notes>` are provided to the AI when generating passage-voice.card to inform stage directions.

**Good examples:**
- <voice-override>
  <voice>onyx</voice>
  <voice-style>Affect: deep, authoritative, grave. Tone: ominous. Pacing: slow, deliberate.</voice-style>
</voice-override> *(Different narrator for this passage)*
- <voice-override>
  <notes>The narrator should sound more hesitant in the opening. Add pauses before each of Marcus's decisions. The confrontation scene needs more vocal tension.</notes>
</voice-override> *(Narration notes from critique feedback)*
- <voice-override>
  <notes>This passage has a dreamlike quality—read with a softer, more distant tone throughout.</notes>
</voice-override> *(Just voice notes, no voice change)*
