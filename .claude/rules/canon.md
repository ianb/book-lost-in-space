---
paths: world/canon/*.card
---

## `<reasoning-canon>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective canon entries

Before creating a canon entry, read the context: Read the passages or outlines that establish this fact. If the canon involves specific locations or characters, read those cards to understand how this fact affects them. Confirm you've read these by briefly summarizing what happened.

Identify the scope and impact: Is this fact truly universal across all story paths, or is it path-specific? What characters, locations, or items does it affect? Does it modify timeline ordering or social order? Will future passages or branches rely on this knowledge? Should this be a new entry or an updated version of existing canon?

When revising, verify: Is the fact clearly established in released content (not speculation)? Are all affected entities cross-referenced? Is the scope of impact clear?

## `<title>` (required) [high priority]

**Purpose:** Unique descriptive name for this canon entry

The title should be a concise noun phrase that identifies the canonical fact. Should provide enough context to be distinctive.

**When creating:**
Use concise noun phrases that include partial context (e.g., "Discovery of Wine Shipment Fraud" or "Kael Harbors Fugitive"). The default comes from the filename slug; adjust to preferred human-readable form. Avoid generic titles that could duplicate other entries. Make it specific enough that someone can identify what this canon is about from the title alone.

**When editing:**
Verify it's unique, identifiable, and concise.

**Good examples:**
- Discovery of Wine Shipment Fraud
- Kael Harbors Fugitive
- Mira Reports to Inspector

**Bad examples (avoid):**
- The Discovery *(too generic)*
- Mira Discovered Fraud in the Records *(full sentence)*

## `<summary>` (required) [high priority]

**Purpose:** One-sentence overview of the canonical fact

Concise statement of what changed and why it matters. Should capture the essential impact of this canon on the story world.

**When creating:**
Write one sentence stating what happened and its significance. Focus on the outcome and impact, not just the event. Make it clear what is now definitively true in the story world.

**When editing:**
Verify it's one sentence stating what changed and why it matters.

**Good examples:**
- Mira discovered systematic fraud in wine shipment records spanning three months, establishing that corruption exists within the Harbor Authority.
- Kael violated her legal obligation by harboring a wounded fugitive, putting her clinic and license at risk.

**Bad examples (avoid):**
- Something important happened at the harbor. *(too vague)*
- Mira found some discrepancies in records. *(no impact)*

## `<facts>` (required) [high priority]

**Purpose:** Concrete facts that are now canonically established

**Format:** Numbered list in Markdown format

Lists specific, verified facts that are now definitively true in the story world. Each fact should be concrete and actionable—something that affects how future content can be written.

**When creating:**
Create a numbered list of concrete facts. Include actors (who was involved), outcomes (what happened), constraints (what's now limited or impossible), and follow-up obligations (what must happen next). Avoid speculation—only include what has been established in released content. Each fact should be specific enough to guide future writing.

**When editing:**
Verify facts are concrete, established in content, and guide future writing.

**Good examples:**
- 1. Three months of wine shipment records show systematic discrepancies totaling significant amounts
2. Mira's supervisor dismissed her concerns without examining the evidence
3. The inspector is scheduled to arrive the next morning
4. Mira has the ledgers in her possession and can present them directly
- 1. The fugitive arrived at Kael's clinic with a stab wound during curfew hours
2. Kael treated the wound and allowed him to rest in the back chamber
3. City patrols passed by twice during the night
4. The fugitive's presence creates legal jeopardy for Kael if discovered

## `<people>` (optional) [medium priority]

**Purpose:** Characters affected by or involved in this canon

**Format:** List of <ref> elements with version references

Cross-references character files for people involved in or affected by this canonical fact. Maintains connections between canon and character development.

**When creating:**
Add a ref element for each character significantly involved. Use the format ``. Include version fragments if specific character versions matter. In the ref content, briefly note their role or how they're affected.

**When editing:**
Verify all major participants are referenced with involvement notes.

## `<locations>` (optional) [medium priority]

**Purpose:** Locations involved in this canonical event

**Format:** List of <ref> elements with version references

Links entity cards for places where this canon was established or that are affected by it. Maintains connections between canon and setting.

**When creating:**
Add a ref element for each relevant location. Use the format ``. In the ref content, briefly explain the location's relevance to this canon.

**When editing:**
Verify all significant locations are referenced with relevance notes.

## `<timeline>` (optional) [medium priority]

**Purpose:** Connection to timeline entry if the event has a fixed time

**Format:** Single <timeline> element with ref attribute

Links to the timeline entry that positions this canon in chronological context. Use when timing matters for continuity.

**When creating:**
Set the ref attribute to the relevant timeline entry path. In the content, include timestamp or scheduling notes if helpful. Only include if the timing of this canon matters for story continuity.

**When editing:**
Include only if timing matters; verify reference is current.

## `<notes>` (optional) [low priority]

**Purpose:** Author-facing reminders about follow-ups or implications

Internal notes for writers about what needs updating or tracking as a result of this canon. Not reader-facing.

**When creating:**
Keep brief. Use for reminders about follow-up tasks, implications for other content, or tracking needs. Examples: "Update arc 2 outline with fallout," "Check if this affects chapter 3 scene," "Track Mira's relationship with supervisor."

**When editing:**
Keep concise with specific follow-up needs identified.

**Good examples:**
- Update outline arc 2 with inspector investigation fallout
- Check if supervisor needs character development as antagonist
- Track how this affects Mira's standing at the Harbor Authority
