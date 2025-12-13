---
paths: **/story-arc.card
---

## `<reasoning-plot-arc>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective plot arcs.

Before creating a plot arc, read the context: Read story-info.card—what's the opening situation and premise? Read narrative-guide.card—what's the target length and tone? Read the character files for the main characters—what are their worldviews, flaws, and motivations? Confirm you've read these by briefly summarizing the core premise and character starting points.

When creating a plot arc, brainstorm options to achieve a compelling narrative that fits the character's traits and the story's tone:
- Does it feel true to the character's established worldview and flaws?
- Does it deliver on genre expectations while avoiding tired tropes?
- Does it fit the target length and emotional tone?

List three possible plot arcs. Then evaluate each against these criteria. Choose the arc that best serves the character and story, stating your choice explicitly and explaining why.

When revising, check for completeness and flow: Does the arc match the character's established traits? Do the beats escalate at the right rhythm? Does it deliver on genre expectations while avoiding clichés?

## `<plot-arc>` (required) [high priority]

**Purpose:** Complete plot arc description detailing the full narrative trajectory.

This is a substantial field—typically a page or more. Use bullet points to break down the narrative into clear beats. Cover the complete arc from opening situation through resolution, including all major turning points and complications. This is the detailed skeleton that guides all downstream writing.

**When creating:**
Write a detailed bullet-point outline covering:
- Opening situation: Where does the character start emotionally/physically?
- Inciting incident: What disrupts the status quo?
- Rising tension: What complications escalate the conflict? (multiple beats)
- Climax: What is the moment of highest tension or decision?
- Resolution: How does the character/situation change by the end?

Expect 10-20 bullets total. Each beat should be concrete enough to guide passage writing but flexible enough to allow creative execution.

**When editing:**
- Does it cover all major story beats (not just beginning and end)?
- Are the rising tension beats varied and escalating?
- Is it detailed enough to prevent plot meandering?
- Does it match what's actually happening in the story passages?

**Good examples:**
- - **Opening**: Mira works as a junior clerk in the harbor master's office, processing cargo manifests. She's methodical, keeps her head down, proud of her accuracy.
- **Inciting incident**: She notices a discrepancy in the ledger—three crates of wine recorded as delivered but not reflected in the tax collection. She mentions it to her supervisor, who dismisses it as a clerical error.
- **First complication**: Mira finds another discrepancy, then another. Someone is systematically skimming shipments. She begins quietly tracking the pattern...
[... 7-12 more beats covering investigation, threats, rising stakes, climax, resolution ...]
- - **Opening**: Kael is an apprentice healer, learning the trade from her mentor in a small border town. She believes healers serve everyone equally, without politics.
- **Inciting incident**: Late one night, a wounded man is brought to her door. She treats him, learning he's a fugitive wanted by the authorities for revolutionary activities.
- **First complication**: The authorities arrive the next morning, asking if anyone matching his description sought treatment. She lies, saying no.
- **Second complication**: The fugitive, recovering in her back room, explains his cause. She's torn—she disagrees with violence but can't deny the injustices he describes...
[... 8 more beats covering hiding him, moral conflict, discovery risk, climax decision, resolution ...]

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
