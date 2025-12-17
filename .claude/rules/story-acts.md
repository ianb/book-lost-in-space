---
paths: **/story-acts.card
---

## `<reasoning-acts>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective story acts.

Before dividing the arc into acts, read the context: Read story-arc.card—what are the core-elements? What does core-elements-setup say must be established for each? Read reader-journey.card—what emotional shifts should the reader experience? Read exposition-plan.card—what must be revealed and when?

Story-arc identifies WHAT moments the story must deliver (core elements).
Story-acts shows HOW to structure the delivery—the detailed beats, pacing, and progression.

When creating act structure, consider:
- Which core elements does each act build toward or deliver?
- What setup from core-elements-setup must this act accomplish?
- Do the act breaks align with major emotional shifts from reader-journey?
- Which exposition items (from exposition-plan) does this act need to deliver?

List different act structures, evaluate each, and choose the one that best serves the core elements.

## `<theme-intentions>` (required) [medium priority]

**Purpose:** Brief setup of which themes should appear and where they manifest.

Themes are shown, not stated. This field establishes intentionality about how themes will appear concretely in the story structure.

**When creating:**
For each major theme from story-arc.card#/themes-and-questions, briefly note:
- The theme
- Where/how it manifests across acts (which acts foreground it, what makes it concrete)

Keep this concise—2-4 themes, 1-2 sentences each. The acts field will elaborate on specific manifestations.

**Good examples:**
- - **Automation vs. humanity**: Introduced in Act 1 through the kiosk comparison and Chen's need for human connection. Escalates in Act 2 as Maya confronts what efficiency costs. Resolved in Act 3 through her choice to persist.
- **Legacy and letting go**: Threaded throughout via Marcus's memory. Act 1 establishes the weight of inheritance. Act 3 forces Maya to define her own relationship to what she's received.
- - **Trust and betrayal**: Seeded in Act 1 through seemingly reliable characters. Undermined in Act 2 through accumulating inconsistencies. Shattered and rebuilt in Act 3.
- **The cost of truth**: Absent in Act 1 (ignorance is comfortable). Introduced in Act 2 as investigation has consequences. Central to Act 3's climax.

## `<acts>` (required) [high priority]

**Purpose:** Defines the act structure with explicit connections to core elements.

**Format:** List of <act number="N" builds-toward="ELEMENT_IDS"> elements

Acts provide dramatic structure: each has an objective, faces conflict, and ends with a shift. Typically 2-4 acts depending on story length. Each act should feel purposeful, not arbitrary.

This is where detailed beats live. Story-arc identifies core elements and their setup. Story-acts shows HOW to structure delivery: all beats needed to build to core elements, bridging content and pacing, objectives and conflicts per segment.

**When creating:**
Break the plot arc into 2-4 acts. For each act, use this structure:

<act number="N" builds-toward="ELEMENT_ID, ELEMENT_ID">
  <objective>What must be accomplished</objective>
  <conflict>What opposes or complicates the objective</conflict>
  <delivers>
    - What setup from core-elements-setup this act accomplishes
    - Which exposition items from exposition-plan it delivers (optional)
    - Key beats and scenes
  </delivers>
  <arc-movement>How character/situation shifts</arc-movement>
  <theme-manifestation>How themes appear concretely</theme-manifestation>
  <estimated-length>X-Y words</estimated-length>
</act>

The builds-toward attribute lists core-element IDs this act works toward. Multiple acts can build toward the same element. The delivers field explains what setup, exposition, and beats the act contains.

**When editing:**
- Does every core element appear in at least one act's builds-toward?
- Does delivers address the core-elements-setup requirements?
- Do acts escalate properly?
- Are exposition items being delivered at appropriate times?

**Good examples:**
- <acts>
  <act number="1" builds-toward="TRUST_BUILT, PATTERN_DISCOVERY">
    <objective>Mira must verify the ledger discrepancies are real and not clerical errors</objective>
    <conflict>Her supervisor dismisses her concerns; she must investigate quietly</conflict>
    <delivers>
      - Setup for TRUST_BUILT: scenes showing supervisor's guidance and care
      - Setup for BETRAYAL_SCENE: subtle hints something is off
      - Delivers PROTAGONIST_IDENTITY, WORLD_SETTING, PATTERN_DISCOVERY
      - Key beats: opening routine, first discrepancy, supervisor dismissal, quiet investigation begins
    </delivers>
    <arc-movement>From trusting the system to realizing corruption exists</arc-movement>
    <theme-manifestation>"Trust in institutions" established through Mira's pride in accurate work</theme-manifestation>
    <estimated-length>800-1200 words (4-6 passages)</estimated-length>
  </act>
  <act number="2" builds-toward="BETRAYAL_SCENE, REVELATION">
    <objective>Track the pattern of theft and identify who's responsible</objective>
    <conflict>The smugglers notice her investigation and send warnings</conflict>
    <delivers>
      - Completes setup for BETRAYAL_SCENE: mentor has opportunity and motive
      - Setup for REVELATION: clues about larger conspiracy
      - Delivers MENTOR_HISTORY
      - Key beats: pattern emerges, first threat, confrontation with supervisor
    </delivers>
    <arc-movement>From quiet clerk to active investigator, risking security</arc-movement>
    <theme-manifestation>"Trust in institutions" crumbles as corruption revealed</theme-manifestation>
    <estimated-length>1200-1800 words (6-9 passages)</estimated-length>
  </act>
  <act number="3" builds-toward="FINAL_CHOICE">
    <objective>Expose the conspiracy while protecting her family</objective>
    <conflict>Direct threats force impossible choice between justice and safety</conflict>
    <delivers>
      - BETRAYAL_SCENE lands here
      - REVELATION lands here
      - FINAL_CHOICE climax
      - Reveals BETRAYER_IDENTITY
    </delivers>
    <arc-movement>From investigator to decision-maker, accepting consequences</arc-movement>
    <theme-manifestation>"Cost of truth" paid in full, shown to be worth it</theme-manifestation>
    <estimated-length>800-1200 words (4-6 passages)</estimated-length>
  </act>
</acts>

## `<chapter-breakdown>` (optional) [low priority]

**Purpose:** Map acts to chapters for implementation planning.

If the story uses chapters, describe how acts translate into chapter structure. Each chapter can span multiple acts or focus on specific act elements. If the story doesn't use chapters (meta.card#/use-chapters is false), leave this empty.

**Good examples:**
- Chapter 1: Act 1 (Discovery)
Chapter 2-3: Act 2 (Investigation) - longer act split across two chapters
Chapter 4: Act 3 (Confrontation)
- Act 1 (Setup): Chapter 1-2
Act 2 (Escalation): Chapter 3-5
Act 3 (Crisis): Chapter 6-7
Act 4 (Resolution): Chapter 8

## `<sources>` (optional) [low priority]

**Purpose:** References to outline files used when writing this story acts outline.

**Format:** List of <ref> elements pointing to source files

List any outline files you consulted when creating story acts. Typically includes story-arc.card.
