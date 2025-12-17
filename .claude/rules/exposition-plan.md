---
paths: **/exposition-plan.card
---

## `<reasoning-exposition-plan>` (optional) [low priority]

**Purpose:** Guided thinking for planning exposition throughout the story

Before creating the exposition plan, read the context: Read story-arc.card to understand core-elements and their setup requirements. Read reader-journey.card to understand emotional goals. Read setting.card for world details.

**Identify what readers must understand and WHEN:**
- What must readers know before specific core elements can land?
- What world/character information supports the emotional journey?
- What setup does each major scene require?

**Identify what to withhold and UNTIL WHEN:**
- What information creates intrigue if delayed?
- What reveals would be spoiled if explained too early?
- What mysteries drive reader engagement?

**Plan timing around emotional goals:**
- Exposition should support the reader journey, not just inform
- Timing should serve story beats (reveal-before core elements, withhold-until trust is established)

## `<must-explain>` (required) [high priority]

**Purpose:** Information readers need to understand the story, with timing constraints

**Format:** List of <item id="ID" reveal-before="condition"> elements

Each item gets a unique ID (ALL_CAPS, semantic) for reference in other cards. The reveal-before attribute describes WHEN this information must be established—using natural language that can reference core-element IDs, story beats, or reader states.

Include both opening exposition (protagonist identity, world basics) and later reveals (character backstory needed before a betrayal lands, world rules needed before magic is used).

**When creating:**
For each piece of exposition readers need:
1. Give it a unique ID (PROTAGONIST_IDENTITY, WORLD_MAGIC, MENTOR_HISTORY)
2. Set reveal-before to describe when it must be established
3. Describe what needs to be explained

Timing can reference:
- Core elements: "reveal-before BETRAYAL_SCENE"
- Story events: "reveal-before any magic use"
- Reader states: "reveal-before reader needs to understand character motivations"
- Opening: "reveal-before end of opening" or "immediately"

**When editing:**
- Does each item have a unique, descriptive ID?
- Is the reveal-before timing appropriate and clear?
- Can each be shown through action/dialogue/sensory detail?
- Are IDs referenced correctly in story-acts or passage-placement?

**Good examples:**
- <must-explain>
  <item id="PROTAGONIST_IDENTITY" reveal-before="end of opening">Mira is a young woman, early twenties, works as a cargo clerk at the harbor</item>
  <item id="WORLD_SETTING" reveal-before="end of opening">Port city with Mediterranean feel, roughly 1800s-equivalent technology</item>
  <item id="PATTERN_DISCOVERY" reveal-before="investigation begins">She has noticed discrepancies in the shipping records that don't add up</item>
  <item id="MENTOR_HISTORY" reveal-before="BETRAYAL_SCENE">The supervisor took her under his wing when she started, taught her everything, covered for her mistakes</item>
</must-explain>
- <must-explain>
  <item id="HEALER_IDENTITY" reveal-before="immediately">Kael is a healer in her thirties, runs a clinic in the lower district</item>
  <item id="MARTIAL_LAW" reveal-before="authorities arrive">The city is under martial law with patrols</item>
  <item id="MAGIC_EXISTS" reveal-before="any healing">Magic healing exists in this world with specific costs</item>
  <item id="HEALER_OATH" reveal-before="MORAL_BREAKING_POINT">Kael swore to heal all who need it, regardless of who they are</item>
</must-explain>

## `<withhold>` (optional) [medium priority]

**Purpose:** Information to deliberately withhold until the right moment

**Format:** List of <item id="ID" reveal-after="condition"> elements

Each withheld item gets a unique ID and a reveal-after condition describing when it CAN be revealed. This tracks secrets, mysteries, and delayed reveals that drive narrative tension. The reveal-after is the condition that must be met BEFORE the information can be disclosed.

Can be empty for stories without mystery elements.

**When creating:**
For each piece of information to withhold:
1. Give it a unique ID (BETRAYER_IDENTITY, TRUE_STAKES, PAST_TRAUMA)
2. Set reveal-after to describe when revelation becomes appropriate
3. Describe what's being withheld

Timing can reference:
- Emotional states: "reveal-after trust in mentor is established"
- Story events: "reveal-after reader cares about the characters"
- Core elements: "reveal-after TRUST_BUILT"
- Other exposition: "reveal-after HEALER_OATH is established"

**When editing:**
- Does each item have a unique, descriptive ID?
- Is the reveal-after timing appropriate?
- Will withholding create intrigue (not confusion)?
- Do these connect to story-arc core elements?

**Good examples:**
- <withhold>
  <item id="BETRAYER_IDENTITY" reveal-after="trust in supervisor is established">Who actually authorized the smuggling operation</item>
  <item id="TRUE_SCOPE" reveal-after="reader is invested in Mira's investigation">Whether the smuggling is part of something larger than trade fraud</item>
  <item id="MIRA_ASSIGNMENT" reveal-after="REVELATION">Why Mira was assigned to this position at this specific time</item>
</withhold>
- <withhold>
  <item id="FULL_OATH" reveal-after="reader sees Kael's compassion">The full oath Kael swore and under what circumstances</item>
  <item id="SCAR_ORIGIN" reveal-after="MORAL_BREAKING_POINT">Why the fugitive has a scar Kael seems to recognize</item>
  <item id="PAST_HARBORING" reveal-after="current choice is made">Whether Kael has harbored fugitives before</item>
</withhold>
-
