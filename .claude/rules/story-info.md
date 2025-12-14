---
paths: **/story-info.card
---

## `<reasoning-story-info>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective story metadata.

Before creating story info, read the context: Read setting.card—what's the world like? Read meta.card—what's the narrative structure? If you've already created character files for potential protagonists, read those—what are their motivations and situations? Confirm you've read these by briefly stating the world context and any character possibilities.

Consider what makes this story worth telling: who drives the action, what immediate situation pulls the reader in, how the story should sound. The opening-situation is especially important—it should capture the destabilizing moment that starts the story.

When revising, check: Does the opening-situation match the actual story start? Is the voice appropriate for the tone?

## `<title>` (optional) [low priority]

**Purpose:** Story title that distinguishes it from other stories in the project.

**Format:** Short, descriptive title

Can be figured out later. Should be unique within the project and reflect the story's focus when decided.

## `<pov-character>` (required) [high priority]

**Purpose:** Primary character whose perspective drives this story.

**Format:** <pov-character ref="/world/characters/Name#v1.0" role="protagonist" />

Should reference an existing character using the ref attribute and role="protagonist". You may need to create the character first with `ske create /world/characters/{Character_Name}.card`

## `<opening-situation>` (required) [high priority]

**Purpose:** The destabilizing moment that pulls the reader into the story.

**Format:** 2-4 sentences describing the immediate predicament

This is the destabilizing force that breaks the normal and pulls the reader in. It's story-specific, not part of the general setting.

**When creating:**
Include pressure and immediate stakes. Leave solution open. Identify what's breaking normal that the reader feels immediately. Focus on current catalyst, not backstory.

**When editing:**
Verify it describes the story start with clear immediate stakes.

**Good examples:**
- The levy bell rings twice: once for collection, once for conscription. You have until sundown to decide whether to hide your son or offer him to the draft.
- The harbor master's ledger doesn't match your count. Someone has been skimming cargo, and the inspector arrives tomorrow.
- Your sister disappeared three days ago. The constable says she ran off, but her shoes are still by the door.

## `<story-goal>` (optional) [high priority]

**Purpose:** What the author/user wants this story to achieve for the reader.

**Format:** 1-2 sentences or 3-4 short bullet points

This is the user's goal - what experience or feeling they want the reader to have.
Examples: "The reader should feel relaxed", "Invoke a sense of awe", "Leave the reader
unsettled but hopeful". This gets piped directly into story CLAUDE.md to keep it
top-of-mind during all creation. Write something that REFLECTS what the user says,
concise and unambiguous so it works in isolation.

Focus on VISCERAL emotions - the physical, felt experiences readers have while reading.
Think about what sensations you want to create in the reader's body and mind:

**Threat/tension**: suspense (held-breath uncertainty), dread (approaching doom), shock/startle (jolt, flinch), anxious vigilance (braced, scanning), panic spike (urgent, breath-short)

**Curiosity/cognition**: curiosity pull (wanting-to-know that tugs forward), pattern-hunting (active theorizing, connecting), reveal-click (satisfying snap of understanding), surprise flip (reinterpretation whiplash)

**Moral heat**: outrage (hot indignation), justice appetite (need for reckoning), contempt (cold disgust), comeuppance anticipation (pleasure in setup for takedown)

**Social discomfort + humor**: cringe-comedy (secondhand embarrassment that stays funny), benign violation (wrong-but-safe thrill triggering laughter), delighted amusement (light grin, buoyant), absurd joy (laughter at gleeful wrongness)

**Warmth/attachment**: protectiveness ("don't hurt them" urgency), tender warmth (softened attention, safe closeness), belonging glow (cozy inclusion)

**Release**: relief (tension drops, exhale), cathartic release (pressure valve: tears or laughter)

**Body responses**: disgust/squeamishness (recoil), arousal/desire

**When creating:**
Ask the user what they want readers to feel or experience. Write their answer concisely.
This is not about plot or theme - it's about the intended effect on the reader.
Probe for the visceral, physical sensations: Do they want readers holding their breath?
Cringing? Feeling warm and safe? Hungry for justice?

**Good examples:**
- The reader should feel cozy and safe, like curling up with a warm drink.
- Invoke wonder and slight unease - beautiful but wrong.
- - Reader feels the weight of impossible choices
- Build dread slowly, then release
- End with bittersweet hope
- - Cringe-comedy: secondhand embarrassment that stays funny
- Pattern-hunting satisfaction as clues connect
- Comeuppance anticipation building to cathartic release
- Suspense tension building to shock, then protective warmth for the survivor.

## `<visibility>` (required) [high priority]

**Purpose:** Controls who can access this specific story

Determines the access level for this story. Can override the project-level visibility, but cannot be more permissive than the project allows.

Choose the appropriate visibility level:
- **private**: Only administrators can see (default for new stories, use during development)
- **beta**: Visible to beta readers who can provide feedback
- **member**: Requires login to access
- **public**: Visible to everyone
- **deprecated**: Hidden, typically replaced by a newer version

Start with "private" and change to more permissive levels when the story is ready for readers.

## `<audiences>` (optional) [low priority]

**Purpose:** Target audiences for this specific story (overrides project default)

**Format:** One audience slug per line, or empty to inherit from meta.card

Specifies which audiences this story should be generated for. When empty, inherits the audiences from meta.card. Use this to override the project-level setting for individual stories.

This is primarily used during translation generation (`ske gen translations`) and uploads to determine which audience versions to create for this specific story.

**When creating:**
Leave empty to use the project default from meta.card. Only specify audiences here if this story needs different translations than the project default. Same format as meta.card: one slug per line, with optional glob patterns and exclusions.

**When editing:**
Update when this story needs different audience targeting than the project default. An empty element inherits from meta.card.

**Good examples:**
- 
- main
es

## `<voice>` (required) [medium priority]

**Purpose:** Voice selection for text-to-speech audio generation.

**Format:** One of the supported voice names

Choose a voice that matches your story's tone and narrator. Consider if your voice IS the main character, or is a narrator. Available voices:
- alloy: Female, low pitch. Great for narration, somewhat older/mature, perhaps Black
- ash: Male, low pitch, deep and gravelly, cowboy-like
- ballad: Neutral/male, British accent, high pitched, younger/peppy
- cedar: Male, medium pitch, glitchy but engaged
- coral: Female, medium pitch, enthusiastic but impersonal, podcaster-like
- echo: Neutral voice, could be male or female, naive, very neutral
- fable: Neutral/female, British accent, upper class/posh, very neutral
- marin: Female, medium pitch, glitchy but very personal and engaging, younger feeling
- onyx: Male, low pitch, deep and smooth, perhaps Black
- nova: Female, high pitch, engaged and personal, professional but engaging
- sage: Female, high pitch, perky and light, great for narration, very professional
- shimmer: Female, medium pitch, direct and personable, intimate
- verse: Male, medium pitch, smooth and professional, perhaps impersonal

## `<voice-style>` (required) [medium priority]

**Purpose:** Description of how the voice should be styled for this story's narration.

**Format:** Structured description covering affect, tone, pacing, and pronunciation (if needed)

Describe the reader's vocal style. Include affect (3-4 attributes like gentle, quick, easy going), tone (1-2 attributes like warm, cynical), pacing (1-2 attributes like steady, measured, hurried), and pronunciation quirks or accents only if relevant.

**Good examples:**
- Affect: gentle, thoughtful, slightly world-weary, warm. Tone: melancholic but hopeful. Pacing: measured, unhurried.
- Affect: quick, sharp, suspicious, alert. Tone: cynical. Pacing: brisk, staccato.
- Affect: easy going, friendly, earnest, optimistic. Tone: warm and inviting. Pacing: steady with natural rhythm. Pronunciation: slight Southern accent, soft r's.

**Bad examples (avoid):**
- Nice and clear *(Too vague)*
- Tone: warm. Pacing: steady. *(Missing affect attributes)*
