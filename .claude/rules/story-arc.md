---
paths: **/story-arc.card
---

## `<story-synthesis>` (required) [high priority]

**Purpose:** Ground the arc in source material before planning plot or identifying core elements.

Complete this section FIRST before any other arc work. It synthesizes the foundational inputs that should drive all arc decisions.

**When creating:**
Restate and expand on story-goal. What sensations, emotions, and experiences should readers have? What should linger after they finish? This synthesis should directly inform every core element and plot decision.

**Good examples:**
- From story-goal: "Build dread slowly, then release, ending with bittersweet hope."
Synthesis: The arc must create genuine escalating tension—not sudden shocks but mounting evidence of danger. The release needs to feel earned. The ending hope must be fragile and hard-won, not triumphant. Readers should feel the weight of what was risked and what was lost alongside what was saved.

## `<core-elements>` (required) [high priority]

**Purpose:** The load-bearing moments the story exists to deliver.

**Format:** List of <element id="ID"> elements with unique IDs

These are the essential scenes, transformations, reveals, or emotional payoffs that everything else builds toward. They're what justify the arc—the moments readers will remember.

**When creating:**
Identify the 2-6 moments this story MUST deliver. These can be:
- A pivotal scene ("the confrontation where she finally says no")
- A transformation ("she learns to trust her own judgment")
- A reveal ("the reader discovers the mentor was complicit")
- An emotional payoff ("the release of tension when they finally escape")
- Something wider ("the slow erosion of her certainty")

Give each a unique ID in ALL_CAPS—semantic but distinctive (BETRAYAL_SCENE, FIRST_KISS, REVELATION). These IDs will be referenced throughout other cards.

**When editing:**
- Does each element feel essential to the story's promise and goals?
- Are IDs unique and descriptive?
- Are there 2-6 elements (too few = missing structure; too many = not actually "core")?

**Good examples:**
- <core-elements>
  <element id="BETRAYAL_SCENE">The moment she realizes her mentor sold her out</element>
  <element id="TRUST_BUILT">Reader feels invested in the mentor relationship before it breaks</element>
  <element id="REVELATION">Reader discovers the true scope of the conspiracy</element>
  <element id="FINAL_CHOICE">She must choose between safety and exposing the truth</element>
</core-elements>

## `<core-elements-setup>` (required) [high priority]

**Purpose:** Prerequisites for each core element—working backwards from the big moments.

**Format:** List of <setup for="ID"> elements referencing core-element IDs

For each core element, describe what must be in place for it to land. This is working backwards: given this great moment, what makes it work?

**When creating:**
For each core element, write a natural language description considering:
- **Emotional investment**: What must reader feel before this moment?
- **Plot prerequisites**: What events make this moment possible/logical?
- **Anticipation**: How do we build excitement through story promises? (Anticipation is half of satisfaction—readers sensing something is coming enhances the payoff.)

Reference other core-element IDs where relevant (e.g., "TRUST_BUILT must happen before BETRAYAL_SCENE").

**Good examples:**
- <core-elements-setup>
  <setup for="BETRAYAL_SCENE">Reader must trust the mentor first—TRUST_BUILT must be complete. Plant subtle hints something is off so reader suspects but hopes not. Mentor needs opportunity and apparent motive established through earlier scenes.</setup>
  <setup for="TRUST_BUILT">Show mentor's genuine care and guidance. Reader should feel protective of this relationship. Establish what mentor has sacrificed for the protagonist.</setup>
  <setup for="REVELATION">Reader must care about the immediate stakes before learning their true scope. Plant clues that will recontextualize on reveal. Build sense that something bigger is happening.</setup>
  <setup for="FINAL_CHOICE">Both options must have real costs established. Reader should understand what she risks either way. The choice should feel impossible, not obvious.</setup>
</core-elements-setup>

## `<reasoning-plot-arc>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective plot arcs.

Before creating a plot arc, VERIFY that story-synthesis, core-elements, and core-elements-setup are complete. The arc connects these elements—don't proceed without them.

Read the synthesis to understand story-goals, story-promise, and character pressure points. Review core-elements to know what moments the arc must deliver. Review core-elements-setup to understand what builds to each moment.

When brainstorming, focus on:
- How do core elements connect into a coherent journey?
- What emotional logic links one core element to the next?
- How does the character-review inform the path between moments?

DON'T create a detailed beat list—that's what story-acts is for. The arc is about the shape of the journey, not every step along the way.

## `<plot-arc>` (required) [high priority]

**Purpose:** The narrative arc that connects core elements into a coherent journey.

This describes how your core elements connect—the emotional logic of the story, not a detailed beat list (that's what story-acts is for). Focus on the shape of the journey: how does one core moment lead to another? What's the overall trajectory?

**When creating:**
Build the arc around your core-elements:
- What's the opening situation that makes the first core element possible?
- How does each core element create the conditions for the next?
- What's the emotional trajectory—where do tension, investment, and stakes rise and fall?
- How do the core-elements-setup requirements get satisfied along the way?

Write prose or loose bullet points describing the journey. Focus on the connective tissue: the "why" that links moments together. Don't enumerate every scene—leave detailed beats for story-acts.

**When editing:**
- Does every core element appear in the arc?
- Does the arc explain HOW you get from one core element to the next?
- Is there emotional logic, not just plot logic?
- Does it address the setup requirements from core-elements-setup?

**Good examples:**
- The story opens with Mira in her routine—competent, methodical, trusting in the system. This establishes what TRUST_SHATTERED will destroy. The inciting discrepancy puts her on a path of discovery, with each finding deepening her investment (building toward REVELATION). As she investigates, we see her rely on her supervisor, her colleagues—establishing the relationships that will be tested. REVELATION lands in the middle, recontextualizing everything and making FINAL_CONFRONTATION both necessary and terrifying. The arc's emotional logic: from security through doubt through discovery through action—each stage making the next feel inevitable.
- The arc moves through three emotional phases: belonging, fracture, choice. In "belonging," we establish what Kael values—her neutral healer identity, her mentor relationship (setup for BETRAYAL). In "fracture," the fugitive's presence forces impossible choices, each small lie building pressure (setup for MORAL_BREAKING_POINT). In "choice," everything converges—she must act, and whatever she chooses defines who she becomes (FINAL_CHOICE). The core elements are the peaks; the arc is the path between them.

## `<reasoning-character-development>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective character development arcs.

Before creating a character development arc, read the context: Read the character file(s) for the main characters—what are their normal-life, worldview, self-concept, and flaws? Read the plot-arc you just created—what experiences will they go through? Confirm you've read these by briefly stating the character's starting beliefs and key plot experiences.

When creating character development, brainstorm options to achieve meaningful transformation that aligns with the plot:
- Does the transformation feel earned by the specific plot experiences?
- Does it challenge the character's starting beliefs or behaviors?
- Does it avoid being too dramatic (unrealistic) or too subtle (unnoticeable)?

List three possible development arcs. Then evaluate each against these criteria. Choose the best option, stating your choice explicitly and explaining why it creates the most meaningful character journey.

When revising, check: Does the transformation feel earned by plot events? Does it align with the character's established traits? Does it match how the character actually changes in written passages?

## `<character-development>` (required) [high priority]

**Purpose:** How the character(s) change over the course of the plot arc.

This describes the internal journey that parallels the external plot. Focus on how beliefs, behaviors, or relationships shift.

**When creating:**
Describe how characters evolve throughout the story:
- Starting state: What are the character's key beliefs, behaviors, or patterns at the beginning?
- Challenges: What plot events or realizations challenge their current state?
- Transformation: How do they respond and change? What shifts in their worldview, self-concept, or relationships?
- Ending state: Who have they become by the end? What's different?

Focus primarily on the main character/POV character, but can include other important characters if relevant.
Keep this concise (2-4 sentences for the main character, 1-2 sentences per additional character if included).
Character development should feel earned by the plot events and align with the character's established traits.

**When editing:**
- Does the starting state match the character's established worldview and flaws?
- Is the transformation caused by specific plot events (not just time passing)?
- Does the ending state feel earned and meaningful (not too dramatic or too subtle)?
- Does it match how the character actually changes in written passages?

**Good examples:**
- The clerk starts trusting authority and following rules. The investigation forces her to see how corruption operates at the highest levels, and she learns that sometimes the system can't be trusted to police itself. By the end, she's learned to act on her own judgment even when it means breaking the rules, but she's also learned the cost of that choice—she can't return to her old innocence.
- The healer begins believing her duty is purely medical—neutral, apolitical, helping whoever needs it. Protecting the fugitive forces her to recognize that neutrality is itself a political choice. She ends having chosen a side, accepting that her healing work is now inseparable from her politics, but unsure if she made the right choice.

## `<characters>` (optional) [low priority]

**Purpose:** List of characters that appear in this story, with refs to their character cards.

**Format:** List of <ref> elements pointing to character files with role attributes

List the characters that appear in this story. Use /todo/ refs for characters you plan to create later.
The role attribute should describe their function in the story (e.g., "protagonist", "antagonist", "mentor", "love interest").

Characters can emerge during writing—this list doesn't need to be complete upfront. Add characters as they become important enough to warrant a card.

Threshold for creating a character card: characters with dialogue in 2+ passages, characters who drive plot points, or characters whose motivations/backstory affect the narrative.

**Good examples:**
- <characters>
  <ref ref="/world/characters/Maya.card" role="protagonist" />
  <ref ref="/todo/world/characters/Frank.card" role="landlord, delivers inciting incident" />
  <ref ref="/todo/world/characters/Chen.card" role="regular customer, represents human connection" />
</characters>

## `<sources>` (optional) [low priority]

**Purpose:** References to other files used when writing this story arc outline.

**Format:** List of <ref> elements pointing to source files

List any files you consulted when creating this story arc. Typically includes story-info.card, setting.card, character files, or other foundational files. Story-arc is near the top of the outline hierarchy, so it typically doesn't reference other outline files.
