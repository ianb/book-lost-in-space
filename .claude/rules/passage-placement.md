---
paths: **/passage-placement.card
---

## `<reasoning-passage-placement>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective passage placement.

Before creating passage placement, read the context: Read this chapter's chapter-placement.card—what's the scene outline? Which scene does this passage belong to? Read exposition-plan.card—what exposition items should this passage deliver? If this isn't the first passage, read the previous passage's passage-placement.card—where did it leave off?

Identify the passage's purpose: What specific moment or beat from the scene does this passage cover? What must happen in this passage for the scene to work? Which exposition items from exposition-plan.card should be explained or revealed here? How does this passage connect to the next?

When revising, verify: Does it actually cover what the scene outline specified? Are key moments present? Is exposition being delivered at appropriate times? Does it connect smoothly to adjacent passages?

**Upstream revisions are okay:** If this passage's needs don't align well with chapter-placement.card or story-acts.card, it's appropriate to revise those upstream files rather than force the passage to fit. The story serves the reader, not the outline.

## `<passage-objective>` (required) [high priority]

**Purpose:** What this passage accomplishes within its scene

This states what specific moments or beats from the scene this passage covers. Should map directly to the scene outline from chapter-placement.card

**When creating:**
One sentence stating what this passage accomplishes. Reference the scene it belongs to. Focus on the objective—what it establishes, reveals, or advances—not just factual description.

**When editing:**
- Does it match what actually happens in the prose?
- Is it specific (not vague)?
- Does it connect to the scene outline?

**Good examples:**
- Establish Mira's methodical work routine and introduce the ledger discrepancy that will launch her investigation (Scene 1: Morning at harbor office)
- Reveal supervisor's complicity through his too-quick dismissal, breaking Mira's trust in authorities (Scene 2: Supervisor's dismissal)
- Show Mira's decision to investigate alone, transitioning her from dutiful clerk to lone investigator (Scene 3: Mira decides to investigate)

## `<scene-portion>` (required) [high priority]

**Purpose:** Which scene from chapter-placement this passage covers.

References the specific scene from the scene-outline in chapter-placement.card. A passage typically covers one scene or part of one scene.

**When creating:**
State which scene by name or number from chapter-placement.card. If the scene spans multiple passages, note which portion: "Scene 1 (first half)" or "Scene 3 (conclusion)".

**When editing:**
- Does it accurately reference the scene-outline?
- Is it clear what portion of the scene this covers?
- Does it match the passage-objective?

**Good examples:**
- Scene 1: Morning at the harbor office
- Scene 2: Supervisor's dismissal (full scene)
- Scene 3: Mira decides to investigate (opening)

## `<key-moments>` (required) [high priority]

**Purpose:** Specific events or realizations that must occur in this passage.

These are concrete moments that make the passage fulfill its objective. Should be specific enough to guide prose writing.

**When creating:**
List 1-3 key moments as brief bullet points. Each should be a specific action, dialogue exchange, or realization. Not themes or summaries.

**When editing:**
- Are these actually in the prose?
- Are they concrete moments (not vague descriptions)?
- Do they accomplish the passage-objective?

**Good examples:**
- - Mira cross-references the ledger against the manifest
- She finds three crates unaccounted for
- She decides to mention it to her supervisor

## `<character-focus>` (optional) [medium priority]

**Purpose:** Character interactions or developments in this passage.

How characters interact, what relationships develop, what internal changes occur. Keep this focused on what's unique to this passage.

**When creating:**
Describe character moments specific to this passage. What does the reader learn about the character here? What interaction defines this moment?

**When editing:**
- Is this actually shown in the prose (not just stated)?
- Is it specific to this passage (not general character traits)?
- Does it advance characterization meaningfully?

**Good examples:**
- Mira's methodical nature on display: she doesn't just notice the discrepancy, she triple-checks her math before raising it.
- The supervisor's dismissal is too quick, too casual—Mira notices he doesn't even look at the numbers she's showing him.

## `<exposition-in-passage>` (optional) [medium priority]

**Purpose:** Track which exposition items from exposition-plan.card this passage delivers.

**Format:** List of <explains id="ID"> or <reveals id="ID"> elements

This tracks where exposition actually lands, connecting passage content to the exposition-plan. Use <explains> for must-explain items and <reveals> for withhold items being disclosed.

This helps ensure nothing from exposition-plan is forgotten and that reveals happen at appropriate times.

**When creating:**
Check exposition-plan.card for items with reveal-before/reveal-after timing relevant to this passage. For each item this passage delivers:
- Use <explains id="ID"> for must-explain items, describing HOW it's explained
- Use <reveals id="ID"> for withhold items being disclosed, describing the reveal moment

Empty is fine if this passage doesn't deliver exposition items.

**When editing:**
- Do the IDs match exposition-plan.card?
- Is the timing appropriate (before/after conditions met)?
- Does the description match what's in the prose?

**Good examples:**
- <exposition-in-passage>
  <explains id="PROTAGONIST_IDENTITY">Through the opening scene at her desk</explains>
  <explains id="WORLD_SETTING">Harbor sounds, Mediterranean light, period details</explains>
</exposition-in-passage>
- <exposition-in-passage>
  <explains id="MENTOR_HISTORY">Through dialogue about their first meeting</explains>
  <reveals id="BETRAYER_IDENTITY">The moment she sees mentor's signature on the smuggling orders</reveals>
</exposition-in-passage>
- 

## `<sources>` (optional) [low priority]

**Purpose:** References to outline files used when creating this passage placement.

**Format:** List of <ref> elements pointing to source files

List any outline files you consulted. Typically includes chapter-placement.card for the scene outline.
