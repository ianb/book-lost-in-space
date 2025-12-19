---
paths: **/summary.card
---

## `<sources>` (required) [low priority]

**Purpose:** References to source files used to generate this summary

Lists the passage.card and any previous summaries consulted during generation. Used to detect when regeneration is needed due to source changes.

## `<narrative-promises>` (required) [low priority]

**Purpose:** Track foreshadowing, Chekhov's guns, and story setups

Narrative promises are implicit commitments to the reader - when you show a gun on the wall, readers expect it to fire. This section tracks which promises have been fulfilled, which have lapsed (abandoned), and which remain open.

## `<facts>` (required) [low priority]

**Purpose:** Track established canon facts and detect continuity conflicts

Facts are significant details that matter for long-term story continuity - character traits, world-building details, relationship changes. Does not include transient details like current location or what someone is wearing.

## `<timing>` (required) [low priority]

**Purpose:** Track story timeline and temporal flow

Records when the passage starts and ends, how much time passed since the previous passage, and whether the timing is plausible given character actions.

## `<characters>` (required) [low priority]

**Purpose:** Track character and entity presence in the scene

Records which characters appear, enter, or exit during the passage, and which entities (locations, organizations) are relevant. Character refs use /todo/ prefix if the character doesn't exist yet.

## `<story-so-far>` (required) [low priority]

**Purpose:** Rolling cumulative summary of the story up to this point

A concise bullet-point summary that gets rewritten each passage. Each passage adds new significant events and prunes details that become irrelevant as the story progresses. Focus on plot-relevant events, not atmospheric details.

## `<emotional-journey>` (required) [low priority]

**Purpose:** Track emotional beats, surprises, and character development for this passage

Non-cumulative per-passage analysis of the reader's emotional experience. Includes:
- Emotional beats: 1-3 significant emotional moments
- Surprises: Moments that subvert reader expectations (based on story so far)
- Character development: Moments where characters grow, change, or reveal themselves

## `<locations>` (optional) [low priority]

**Purpose:** Track physical locations where the story takes place and how they connect

Records locations mentioned in each passage, building a cumulative map of the story's geography. Each passage identifies where it takes place and any new descriptive details about locations. Connections between locations are tracked, including both explicit connections (character walks through door) and inferred connections (apartment building probably has a street entrance).
