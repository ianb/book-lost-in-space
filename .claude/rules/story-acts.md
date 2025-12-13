---
paths: **/story-acts.card
---

## `<reasoning-acts>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective story acts.

Before dividing the arc into acts, read the context: Read story-arc.card—what are the major turning points in the plot-arc? What character development must occur? Read reader-journey.card—what emotional shifts should the reader experience, and where? Read narrative-guide.card—what's the overall story length and pacing? Confirm you've read these by briefly summarizing the key plot beats, emotional arc, and target length.

When creating act structure, brainstorm options to achieve natural dramatic escalation and balanced pacing:
- Do the act breaks align with major turning points in the plot-arc?
- Do the act breaks align with major emotional shifts from reader-journey?
- Does tension escalate appropriately across acts?
- Are act lengths proportioned for the story's rhythm?

List three different act structures (varying number of acts: 2-act, 3-act, or 4-act; different ways to divide the plot beats). Then evaluate each structure against the criteria. Choose the structure that best serves the story's dramatic arc, stating your choice explicitly and explaining why.

When revising, check: Does each act have a clear dramatic purpose? Do the act divisions create natural escalation? Are acts proportioned appropriately for pacing?

## `<theme-intentions>` (required) [medium priority]

**Purpose:** Brief setup of which themes should appear and where they manifest.

Themes are shown, not stated. This field establishes intentionality about how themes will appear concretely in the story structure.

**When creating:**
For each major theme from narrative-guide.card, briefly note:
- The theme
- Where/how it manifests across acts (which acts foreground it, what makes it concrete)

Keep this concise—2-4 themes, 1-2 sentences each. The acts field will elaborate on specific manifestations.

**Good examples:**
- - **Automation vs. humanity**: Introduced in Act 1 through the kiosk comparison and Chen's need for human connection. Escalates in Act 2 as Maya confronts what efficiency costs. Resolved in Act 3 through her choice to persist.
- **Legacy and letting go**: Threaded throughout via Marcus's memory. Act 1 establishes the weight of inheritance. Act 3 forces Maya to define her own relationship to what she's received.
- - **Trust and betrayal**: Seeded in Act 1 through seemingly reliable characters. Undermined in Act 2 through accumulating inconsistencies. Shattered and rebuilt in Act 3.
- **The cost of truth**: Absent in Act 1 (ignorance is comfortable). Introduced in Act 2 as investigation has consequences. Central to Act 3's climax.

## `<acts>` (required) [high priority]

**Purpose:** Defines the act structure for the story.

Acts provide dramatic structure: each has an objective, faces conflict, and ends with a shift. Typically 2-4 acts depending on story length. Each act should feel purposeful, not arbitrary.

**When creating:**
Break the plot arc into 2-4 acts. For each act, specify:

**ACT [number]: [Title/Theme]**
- **Objective**: What must be accomplished in this act?
- **Conflict**: What opposes or complicates the objective?
- **Arc movement**: How does the character/situation shift by act's end?
- **Theme manifestation**: How do themes from theme-intentions appear concretely here?
- **Estimated length**: [X-Y words/paragraphs]

Each act should have a clear question or mission, mid-act escalation, and exit point. Acts should ladder into each other cohesively. Ensure every act ties back to at least one arc beat. Focus on dramatic function rather than mechanical structure.

For theme manifestation: be concrete. Not "explores automation vs. humanity" but "Maya compares her ritual to the kiosk's efficiency; Chen seeks human attention machines can't provide."

**When editing:**
Verify acts have distinct objectives, escalate properly, and match written passages.

**Good examples:**
- **ACT 1: Discovery**
- **Objective**: Mira must verify the ledger discrepancies are real and not clerical errors
- **Conflict**: Her supervisor dismisses her concerns; she must investigate quietly without arousing suspicion
- **Arc movement**: From trusting the system to realizing corruption exists at high levels
- **Theme manifestation**: "Trust in institutions" established through Mira's pride in accurate work; "Cost of truth" seeded as she notices supervisor's dismissiveness
- **Estimated length**: 800-1200 words (4-6 passages)

**ACT 2: Investigation**
- **Objective**: Track the pattern of theft and identify who's responsible
- **Conflict**: The smugglers notice her investigation and send warnings; she must choose between safety and truth
- **Arc movement**: From quiet clerk to active investigator, risking her security
- **Theme manifestation**: "Trust in institutions" crumbles as she discovers how high the corruption goes; "Cost of truth" becomes personal through threats to her family
- **Estimated length**: 1200-1800 words (6-9 passages)

**ACT 3: Confrontation**
- **Objective**: Expose the conspiracy while protecting her family
- **Conflict**: Direct threats force impossible choice between justice and safety
- **Arc movement**: From investigator to decision-maker, accepting consequences
- **Theme manifestation**: "Trust in institutions" resolved—she builds new trust in herself; "Cost of truth" paid in full, but shown to be worth it
- **Estimated length**: 800-1200 words (4-6 passages)

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
