---
paths: world/timeline/*.card
---

## `<reasoning-event>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective timeline events

Before creating a timeline event, read the context: Read related canon entries to understand what happened. Read relevant outlines or passages to understand the sequence of events. If other timeline entries exist nearby, read them to avoid scheduling conflicts. Confirm you've read these by briefly summarizing when and what happens.

Identify the event's impact: What changes because this event happens? Which characters are involved and how? Will it affect other characters, locations, or future events? If the event doesn't affect multiple elements or future passages, consider whether a timeline entry is necessary.

When revising, verify: Is the timing consistent with surrounding events? Are all affected characters and locations referenced? Does the event description provide enough detail for consistency?

## `<details>` (optional) [high priority]

**Purpose:** Description of what happens during this event

Provides factual description of the event for reference by other passages that may coincide with or reference this moment. Ensures consistency when multiple story threads interact.

**When creating:**
Write a concise, factual description of what happens. Include who's involved, what they're doing, and why it matters. Focus on observable facts that other passages might need to reference. Keep it brief but informative—enough detail to prevent contradictions when other content references this moment.

**When editing:**
- Is it concise and factual (not narrative prose)?
- Does it describe what happens and why it matters?
- Would it help prevent scheduling conflicts?
- Does it include enough detail for other passages to reference?

**Good examples:**
- Inspector Greaves arrives at the Harbor Master's Office to begin his scheduled audit of cargo records. His arrival creates pressure for Mira to present her evidence of fraud.
- A wounded fugitive arrives at Kael's clinic during curfew hours, forcing Kael to choose between her legal obligations and her healer's oath. Patrols are active in the district.
- Mira presents three months of fraudulent wine shipment records to Inspector Greaves, implicating her supervisor in the corruption.

**Bad examples (avoid):**
- Something important happens. *(too vague)*
- The inspector strode through the door, his boots echoing on the wooden floor, as Mira clutched her ledgers nervously. *(narrative prose)*

## `<characters>` (optional) [medium priority]

**Purpose:** Characters involved in this event

**Format:** List of <ref> elements with version references

Links to character files for people participating in this event. Helps track character schedules and prevents having the same character in two places at once.

**When creating:**
Add a ref element for each participant. Use the format ``. In the ref content, include a brief note about their role or involvement. This helps prevent scheduling conflicts where the same character appears in multiple places simultaneously.

**When editing:**
- Are all participants referenced?
- Do the notes explain their roles?
- Are version references current if needed?
- Does this prevent scheduling conflicts?

## `<location>` (optional) [medium priority]

**Purpose:** Where this event occurs

**Format:** Single <location> element with ref and role attributes

Links to the entity card where this event takes place. The role attribute briefly describes what happens at this location during the event.

**When creating:**
Set the ref attribute to the entity path (e.g., `/world/entities/Harbor_Office`). If the entity doesn't exist yet, use `/todo/world/entities/Location_Name`. Set the role attribute to briefly describe what happens here (e.g., "site of fraud revelation" or "fugitive treated"). In the content, you can add additional context if helpful.

**When editing:**
- Is the entity reference correct?
- Does the role attribute clarify what happens?
- If using /todo/, should the entity be created now?

**Good examples:**
- 
-
