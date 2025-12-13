---
paths: **/translation-guide.card
---

## `<audience-notes>` (optional) [medium priority]

**Purpose:** Regional expectations and translation approach for this locale

**Format:** Use <summary> for actionable guidance and <reasoning> for research or rationale

Describes what liberties translators should take and why those choices fit this locale. Helps translators understand the target audience's expectations and cultural context.

**When creating:**
Write a concise summary (2-3 sentences) stating the translation approach: formal vs casual, how literal to be, what cultural adaptations are needed. In the reasoning section, explain why these choices work for this locale—reference cultural norms, banned approaches, or tonal tradeoffs. Use specific guidance that helps translators make consistent decisions.

**When editing:**
- Is the summary concise (2-3 sentences)?
- Does it give clear direction on liberties to take?
- Does the reasoning explain cultural context?
- Would a translator understand the approach?

## `<terminology>` (optional) [high priority]

**Purpose:** Canonical translations for story-specific terms

**Format:** Add a <reasoning> element for overall approach, then list <term> entries with source, translation, and optional note attributes

Ensures consistent translation of character names, locations, technology, and idioms. Prevents translators from inventing different translations for the same term.

**When creating:**
Add a reasoning element explaining the overall approach (transliterate names? translate locations?). Then list each important term as ``. Include character names, location names, technology terms, and recurring idioms. Use the note attribute for pronunciation guides or register reminders.

**When editing:**
- Does the reasoning explain the overall approach?
- Are all important terms listed?
- Is each translation consistent with the reasoning?
- Do notes clarify ambiguous choices?

**Good examples:**
- 

## `<translation-notes>` (optional) [medium priority]

**Purpose:** Stylistic guidelines for consistent translation

**Format:** One <note> element per guideline

Lists specific rules about tense, punctuation, typography, and acceptable liberties. Helps maintain consistent voice across all translated passages.

**When creating:**
Create one note element for each stylistic rule. Cover: tense handling (keep original or adapt?), punctuation norms for this locale, typography conventions (quotes, dashes), acceptable liberties (can translators restructure sentences?), formality level. Each note should be actionable and specific.

**When editing:**
- Is each note specific and actionable?
- Do they cover tense, punctuation, formality?
- Are they consistent with audience-notes?
- Would they prevent common translation errors?

**Good examples:**
- 

## `<cultural-guidance>` (optional) [medium priority]

**Purpose:** How to adapt cultural references for this locale

**Format:** Each <guideline> contains <context> (what appears in English) and <guidance> (how to adapt it)

Provides specific instructions for handling references that might not resonate with the target audience. Encourages necessary cultural adaptation while maintaining consistency.

**When creating:**
For each cultural element that needs adaptation, create a guideline with context (the English reference) and guidance (how to handle it). Explain when to keep references literal, when to find cultural equivalents, and when to add brief explanations. Emphasize consistency—similar references should be handled similarly.

**When editing:**
- Does each guideline include both context and guidance?
- Are the adaptations consistent with each other?
- Do they preserve the original's tone and impact?
- Would they help with similar future references?

**Good examples:**
- 

## `<simplification-strategy>` (optional) [high priority]

**Purpose:** Plain instructions for how to simplify passages (for {locale}-simple translations)

**Format:** Write plain instructions describing the simplification approach

Defines exactly how to create simplified versions. This text is used directly in AI prompts for generating simplified translations. Must preserve narrative form (not summaries), maintain POV and event sequence, and specify what to preserve vs. what to simplify.

**When creating:**
Write clear, direct instructions for simplification. Choose a strategy based on your story's needs:

- **Bedtime story**: Aggressive simplification (~25% length) for younger audiences, removes side plots and decorative details
- **Same shape, simpler**: Lexical/syntactic flattening, preserves structure but uses simpler words and sentences
- **Non-technical adult**: Removes jargon and complexity without aggressive shrinking
- **Bar story retell**: Casual, compressed like oral storytelling (no more than 5 short paragraphs)
- **Emotional spine**: Focuses on feeling arc while keeping narrative form (3-6 paragraphs)

For each strategy, specify: target audience, length target, what must be preserved (POV, tense, events, emotions), what should be simplified (vocabulary, sentences), and what can be removed. Keep it as continuous narrative, not summaries or beat lists.

**When editing:**
- Does it specify a clear simplification approach?
- Does it preserve narrative form (not summaries)?
- Does it state what must be preserved vs. simplified?
- Is the target audience and length clear?
- Would the instructions work directly in an AI prompt?

**Good examples:**
- Rewrite this story as if you're telling it to a 9-year-old at bedtime.

Constraints:
- Keep it a continuous story, not bullets or analysis
- Keep the same main characters, POV, and order of events
- Use simple words and short sentences; avoid figurative/poetic language
- Remove side plots, long descriptions, and most backstory
- Target length: about one quarter of the Original
- Simplify this story without changing the story itself.

Rules:
- Keep the same POV, tense, and sequence of events
- Keep all major events and emotional turns
- Replace complex sentences with short, direct sentences
- Replace rare or literary words with common everyday words
- Remove decorative description that doesn't change what happens or how someone feels

Output: the rewritten story, not a summary or analysis.

## `<notes>` (optional) [low priority]

**Purpose:** Additional reminders for translators and automation

**Format:** Short paragraphs or bullet lists

Catch-all for practical details like date formats, number formatting, currency, measurements, or other locale-specific conventions.

**When creating:**
Add practical reminders that don't fit other categories. Include: date/time formats, number formatting (decimals, thousands separators), currency conventions, measurement units, or any automation-specific notes. Keep brief and actionable.

**When editing:**
- Are these genuinely helpful reminders?
- Could they prevent translation errors?
- Are they concise?

**Good examples:**
- - Use dd/mm/yyyy date format (European standard)
- Use 24-hour time format
- Use periods for thousands separator, commas for decimals (e.g., 1.234,56)
