---
paths: **/narrative-guide.card
---

## `<reasoning>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective narrative guides.

Before creating a narrative guide, read the context: Read story-info.card—what's the mood and rating? Read story-arc.card—what's the emotional trajectory? What does the prose need to support?

Answer these questions for the guide:
1. Tone: How should the prose feel? (This is prose style, not story mood—story mood is in story-info)
2. Voice: How formal or informal is dialogue and narration?
3. Prohibitions: Are there forbidden tropes, words, or structural patterns?
4. Rhythm: How should pacing behave (paragraph length, beats per passage)?
5. Devices: What narrative devices should recur (motifs, rhetorical questions, sensory emphasis)?
6. Constraints: How tightly should passage length be controlled to fit product constraints?

When updating a narrative guide, check:
1. Consistency: Does the guide match how the story is actually being written?
2. Completeness: Are there prose patterns or constraints that need to be documented?
3. Clarity: Are the specifications actionable enough to guide writing decisions?

## `<tone>` (required) [high priority]

**Purpose:** How the prose should feel—the language quality, not the story's emotional register.

This is PROSE TONE—how the writing sounds—not story mood (that's in story-info). A horror story (mood: dread) might use lyrical, literary prose (tone). A cozy mystery (mood: warm) might use spare, punchy prose (tone). Tone and mood can align or create interesting tension.

Think about: sentence rhythm, vocabulary register, imagery density, narrative distance. Is the prose urgent or measured? Lyrical or spare? Intimate or detached?

**When creating:**
Use 1-5 short descriptors describing prose quality. Think about how the language should feel on the page: lyrical, spare, urgent, measured, intimate, detached, literary, punchy, atmospheric, conversational. Include any prose constraints (e.g., "dreams symbolic only", "no breaking the fourth wall").

Don't repeat story mood here—focus on the writing style that will support that mood.

**When editing:**
Verify it describes prose quality (not story mood) and guides writing style decisions.

**Good examples:**
- Spare and urgent—short sentences, active verbs, minimal interiority
- Lyrical and atmospheric—rich sensory detail, longer sentences, allow reflection
- Intimate and conversational—like being told a story, direct address allowed
- Literary with restraint—precise language, earned imagery, no sentimentality
- Punchy and kinetic; dreams symbolic only; no breaking fourth wall

**Bad examples (avoid):**
- Dark and foreboding *(This is story mood, not prose tone)*
- About a rebellion against taxes *(Plot summary, not tone)*
- Interesting and engaging *(Too vague)*

## `<reading-level>` (optional) [medium priority]

**Purpose:** Describe literacy band or familiarity baseline for readers.

**Format:** Text like "Middle grade", "General adult", or "7th–8th grade".

This sets vocabulary complexity, sentence structure, and conceptual sophistication. Be extremely brief but specific. Consider both literal reading level and emotional maturity expected. Should be specific (not vague like "kids") and match the actual complexity of the prose.

**Good examples:**
- Upper YA (15–17)
- General adult
- Middle grade (8–12)
- Literary fiction, college-educated readers

**Bad examples (avoid):**
- Kids *(Vague)*
- Adults *(Too broad)*

## `<narrative-stance>` (required) [high priority]

**Purpose:** Explicitly define the narrative perspective and temporal framework for the prose.

This is the fundamental POV and tense contract with the reader. Must be consistent unless variations are explicitly noted. Specify: person (first/second/third), tense (present/past), omniscience (only if it's not limited omniscience), and any viewpoint or tense variations that occur in the story (e.g., flashbacks, perspective shifts). Use concise phrasing like "Second person, present tense, limited" or "Third person omniscient, past tense with present tense flashbacks". Should match how passages are actually written.

**Good examples:**
- Second person, present tense, limited
- Third person limited, past tense with present tense flashbacks
- First person, past tense, omniscient narrator
- Third person limited, present tense, single POV character

**Bad examples (avoid):**
- Second person? *(Ambiguous)*
- Third person limited *(Missing tense)*

## `<passage-length>` (optional) [high priority]

**Purpose:** Define the expected prose length range for each passage.

Length varies by story type and medium. Interactive stories often use shorter passages (100-200 words), traditional narratives use longer scenes (500-2000 words), literary fiction may use even longer passages. Set ranges that serve the story and reading experience.

**When creating:**
Express as range or ceiling: "80–180 words", "≤250 words", "500-1500 words per scene". Include reasoning if necessary. Consider: What creates good pacing for this story? What fits the reading context (mobile, web, print)?

**When editing:**
Verify range matches actual passage lengths and serves pacing.

**Good examples:**
- 90–150 words *(Interactive fiction with frequent decision points)*
- ≤220 words, prefer 3 short paragraphs *(Mobile reading with short attention spans)*
- 500-1200 words per scene *(Traditional chapter-based narrative)*
- 800-2000 words, allow up to 3000 for climactic scenes *(Literary fiction with room for depth)*
- 200-400 words *(Flash fiction collection format)*

## `<pacing>` (optional) [medium priority]

**Purpose:** Comprehensive pacing and rhythm guidance for prose flow and reader engagement.

This specifies the story's rhythm: how fast it moves, how sentences flow, how information is revealed. Different stories need different pacing.

**When creating:**
Specify tempo, sentence structure, beat density, dialogue ratio, ending patterns, digression limits, exposition approach, and narrative curve. Use concise, actionable descriptions that guide prose decisions.

**When editing:**
Verify it's specific enough to guide writing and matches actual rhythm.

**Good examples:**
- Tempo: brisk. Sentences: medium, medium variation, few clauses. Beats: ~3 beats per 100 words. Dialogue: ~40% of words. Endings: cliffhanger every 2-3 passages. Digressions: brief asides only. Exposition: sprinkle ≤20 words at a time. Curve: rising.
- Tempo: moderate. Sentences: short to medium, high variation, many clauses. Beats: ~2 beats per 100 words. Dialogue: ~25% of words. Endings: soft cadence. Digressions: up to 15%. Exposition: front-load allowed. Curve: wave.
- Tempo: slow-burn. Sentences: long, low variation, many clauses. Beats: ~1 beat per 100 words. Dialogue: ~15% of words. Endings: reflective. Digressions: none. Exposition: sprinkle ≤30 words at a time. Curve: slow-rise.
- Tempo: intimate and measured. Sentences: varied, favor medium-long. Beats: ~2 per 100 words, allow quiet stretches. Dialogue: ~30%. Endings: emotional resonance. Digressions: character reflection encouraged. Exposition: weave naturally. Curve: gentle rise and fall.

**Bad examples (avoid):**
- Fast pacing with good dialogue *(Too vague)*
- Tempo: brisk. Sentences: short. *(Missing key elements)*

## `<dialogue>` (optional) [low priority]

**Purpose:** Structural formatting rules for dialogue presentation on the page.

This specifies how dialogue looks on the page, not what characters say. Focus on formatting, turn-taking, attribution, and special markup.

**When creating:**
Specify only structural formatting, not content. Focus on deviations from normal: line breaks, attribution tags, turn length, special markup (trail-offs, interruptions, non-verbals), multi-speaker formatting, media presentation. Use concise notation for normal defaults.

**When editing:**
Verify it covers structural formatting (not character voice) and matches passages.

**Good examples:**
- Line breaks: one per speaker. Attribution: "said/asked" default, name when >2 speakers, drop after 3 exchanges. Turn length: ≤50 words. Markup: "..." for trail-offs, "—" for interruptions, italics for thoughts. Multi-speaker: allowed every 5+ passages, format as rapid-fire exchanges. Media: [texting] brackets, *headlines* italics. *(Fast-paced thriller or action fiction)*
- Line breaks: allow same-line replies for quick exchanges. Attribution: always name, mid-sentence tags. Turn length: ≤30 words, exceptions for monologues. Markup: "..." for pauses, "—" for cuts, (sigh) for non-verbals. Multi-speaker: frequent, use dashes for rapid-fire. Media: "quoted" for texts, CAPS for headlines. *(Contemporary YA with texting/social media)*
- Standard formatting: one speaker per line, "said/asked" tags, ≤40 words per turn, "..." for trail-offs, "—" for interruptions, italics for thoughts. No multi-speaker quickfire. Media in brackets. *(Literary fiction or traditional narrative)*

**Bad examples (avoid):**
- Characters speak formally, avoid slang *(Content-focused, not structural)*
- Line breaks should be one speaker per line unless there are quick exchanges in which case same-line replies are acceptable *(Too verbose)*

## `<style-donts>` (optional) [low priority]

**Purpose:** Explicit prohibitions.

List clichés, structural habits, or tonal missteps to avoid. This field is typically built over time from user/author feedback as patterns emerge that don't work for this specific story. Build this reactively rather than proactively.

**When creating:**
You can wait for author/user feedback to build this list. Add items as you discover patterns that don't work for this story. Most stories start with this field empty.

**When editing:**
Build from actual feedback; verify items are specific and actionable.

**Good examples:**
- No "you realize" constructions. Avoid "suddenly" and "just then". No rhetorical questions to the reader.
- Avoid weather-as-mood. No dream sequences. Don't use "literally" for emphasis.
