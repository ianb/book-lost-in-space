---
paths: world/characters/*.card
---

## `<reasoning-character>` (optional) [low priority]

**Purpose:** Guided thinking for creating effective characters.

Before creating a character, read the context: Read setting.card—what's the world, time period, and cultural context? If story-info.card exists, read it—what's the story premise and who's the protagonist? If other character files exist (especially for related characters), read those—what personalities and relationships already exist? Confirm you've read these by briefly stating the setting context and story role you're creating for.

Answer these questions to create the character:
1. Story purpose: What is this character's story role in the narrative? How do they affect the plot or other characters?
2. Character depth: Is this a POV character (needs deep detail), supporting character (moderate detail), or minor character (minimal detail)?
3. Setting fit: Do the name, social-role, and details fit the time period and cultural context? Would someone from this setting recognize this character as authentic?
4. Distinctiveness: What makes this character different from other characters? What's their unique voice or perspective?
5. Relationships: Who does this character know? What relationships matter to the story?
6. Completeness: Which fields are essential for this character's story role? Which can be TBD or omitted?

When updating a character, check:
1. Consistency: Does this character's description align with how they've been portrayed in existing passages?
2. Completeness: Are the essential fields filled for this character's story role?
3. Authenticity: Do the details still fit the setting and time period?

## `<story-role>` (required) [high priority]

**Purpose:** What function this character serves in the story.

This describes their narrative function, not their social status. Start with a short label, then optionally expand on it. What does this character DO for the story? What conflict do they create or resolve? What would be lost without them?

**When creating:**
Start here: figure out why this character exists before filling in details. Begin with 1-3 words for the role label (protagonist, antagonist, mentor, catalyst, etc.), then you can expand on what they do. If creating reactively from existing text, identify what function they're already serving.

**When editing:**
Verify it describes narrative function, not social status.

**Good examples:**
- protagonist
- antagonist: this character will keep the protagonist from achieving their goals and divert them into other interesting subplots
- mentor: provides guidance and wisdom that the protagonist needs but also has their own agenda that may conflict with what's best for the protagonist
- catalyst: sets events in motion through their actions or presence, forcing other characters to react and make difficult choices

**Bad examples (avoid):**
- important character *(Too vague)*
- merchant *(This is social-role, not story-role)*

## `<full-name>` (required) [high priority]

**Purpose:** The character's full name as it appears in the story.

The name must be unique within the project and fit the setting and time period.

**When creating:**
Use the character's preferred or common name. Include titles only if they're part of how the character is addressed. For characters with multiple names, pick the primary one (aliases go in the aliases element). If creating a character that hasn't been named yet, invent a placeholder name that fits the setting.

**Good examples:**
- Marcus Bellini
- Eirene Komnenos
- Sofia the Silk Merchant

**Bad examples (avoid):**
- Bob Smith *(Doesn't fit 1470 Constantinople)*
- Marcus (the merchant) *(Descriptors go in social-role field)*

## `<aliases>` (optional) [low priority]

**Purpose:** Alternative names or titles the character is known by.

**Format:** Semicolon-separated list

Include nicknames, titles, or alternative names. Omit if character has no aliases.

**Good examples:**
- Marco; Marcus the Brave
- Mr. K

## `<age>` (optional) [medium priority]

**Purpose:** Character's age.

**Format:** Number, descriptive range, or TBD

Specify at the level of detail required for the story. Consider: Does age affect how they interact with others? Their experience level?

**When creating:**
Use specific numbers when exact age matters. Use ranges like "late twenties" or "middle-aged" when approximate age is sufficient. Use TBD if age hasn't been determined yet. Can be omitted if truly irrelevant.

**Good examples:**
- 28
- late twenties
- middle-aged
- TBD

**Bad examples (avoid):**
- old *(Too vague)*
- 28 years, 4 months, 2 days *(Too specific when not needed)*

## `<pronouns>` (required) [high priority]

**Purpose:** Character's pronouns.

**Format:** Standard pronoun format: he/him, she/her, they/them

## `<social-role>` (required) [high priority]

**Purpose:** Character's profession AND how others view them in society.

Include both their profession and social class/standing. This is how society categorizes them. Should be recognizable to readers familiar with the setting.

**When creating:**
Keep it concise. Include profession and social standing where both matter. Examples: Merchant (respected), Silk Weaver (working class), beggar, Guard Captain.

**Good examples:**
- Merchant (respectable, middling wealth)
- Silk Weaver (working class)
- beggar
- Guard Captain (minor authority)

**Bad examples (avoid):**
- Sad person *(Emotional state, not social role)*

## `<overview>` (required) [high priority]

**Purpose:** A brief summary of who the character is, from the lens of the story and their story-role.

Capture their essence as it relates to the story. This is what readers/AI need to understand the character quickly and how they fit into the narrative.

**When creating:**
Write 3-5 sentences. Show who they are through their situation, relationships, and what they're dealing with. Avoid overly sharp characterizations - let complexity and contradiction emerge naturally.

Do NOT include:
- Full backstory (use backstory field instead)
- Physical description (use physical-description field instead)
- Detailed relationships (use relationships field instead)

**When editing:**
Verify it connects to story-role and reveals character through situation.

**Good examples:**
- A trader who came to Constantinople five years ago, leaving something behind. Works the harbor warehouses, keeps his head down mostly, but people know he's reliable when a deal needs discretion. He's built a life here but hasn't quite settled into it. Has a daughter back home he sends money to, though the letters have gotten shorter over time.
- She's been working the docks since her husband died, keeping the family's trade connections alive through a mix of favors owed and secrets known. Smart about who owes what to whom. Her kids are almost grown now, and she's not sure what happens when they don't need her to hold things together anymore. The harbor masters respect her, but she's never quite one of them.

**Bad examples (avoid):**
- A person who lives in the city and works at the harbor. *(Too vague, no depth)*
- A cautious trader seeking redemption. Distrusts authority but values loyalty. *(Too sharp, contradictory traits as labels)*

## `<worldview>` (optional) [medium priority]

**Purpose:** How the character THINKS the world works.

**Format:** 2-3 short sentences

This shapes how they interpret events and make decisions. Most important for POV characters.

**When creating:**
Write in first person, in the character's voice and with their (perhaps limited) perspective. Keep it simple and concrete. Show how they see cause and effect, what they believe about how things work.

**When editing:**
Verify it's in the character's voice and reveals how they interpret events.

**Good examples:**
- Coach's face tells me if I'm safe. If he frowns, I run harder. Teachers like me when I'm tired because I talk less.
- I read the room before I read the homework. If the air dips, I toss a joke or pass snacks. Later I'm mad nobody noticed I was tired.
- Silence is louder than the baby crying. If the monitor is quiet, I hover in the doorway and count breaths.
- I assume I'm right unless someone brings numbers I respect. Pauses feel like invitations, so I take them. When people bristle, I think they're tired, not that I'm loud. Later I edit myself in my head and keep most of it.
- Every window is a mirror if I let it be. I tug the shirt, then pretend I was fixing the tag. Compliments land as "try harder tomorrow." Photos feel like traps; I offer to take them so I'm not in them.
- Everything official looks like it assumes I already know. I read it twice, still feel dumb, then ask a friend and feel less dumb. I nod in offices so they don't see me guessing. Later I rewrite the instructions in plain words for myself.

## `<self-concept>` (optional) [medium priority]

**Purpose:** How they see themselves.

**Format:** One sentence, first person

What do they believe about themselves? This may differ from how others see them. Most important for POV characters.

**When creating:**
Write one sentence from their perspective in first person. Avoid overly sharp self-assessments - people's self-concepts are often softer and more uncertain than external descriptions.

**Good examples:**
- I'm the one people come to when something needs doing, though I wish sometimes they'd just handle things themselves.
- I know I try too hard to make people like me, but I can't seem to stop doing it anyway.
- I'm good at my work when I'm not second-guessing myself, which lately has been less often than I'd like.
- People think I'm funny, and I lean into that because it's easier than whatever else they might think.

## `<motives-braided>` (optional) [medium priority]

**Purpose:** Character's core drives and motivations.

**Format:** Three-ply drive: protect X • get Y • uphold Z

The "braided" aspect means these drives can conflict or reinforce each other, creating natural story tension.

**When creating:**
List 2-4 concrete drives that can push against each other. Use the bullet format: protect X • get Y • uphold Z. Focus on immediate, actionable drives rather than abstract values.

**When editing:**
Verify drives are concrete, can conflict, and suggest actions.

**Good examples:**
- Keep baby safe • Sleep through the night once • Hold marriage together
- Protect crew from fines • Win better routes • Keep union strong
- Avoid another eviction • Save enough for a car • Stay clean this year
- Keep patients alive • Cover student loans • Stay on nights for the pay diff
- Shield friend from charges • Clear my own record • Keep cousin loyal
- Protect sister's dowry • Earn a journeyman mark • Avoid conscription
- Guard the river crossing • Learn one true name • Keep mother's charm from fading

## `<emotional-baseline>` (optional) [medium priority]

**Purpose:** Default mood and emotional regulation.

**Format:** 1-2 sentences

Describe their resting state and how they typically regulate emotions. Include what makes them spike or break from baseline. This shapes how the character normally acts AND how they react to events.

**Good examples:**
- Generally keeps things light, deflects with humor when things get tense. Gets quiet and withdrawn when he feels cornered, which people sometimes mistake for agreement.
- Steady and practical most of the time, the person others lean on. Brittle under sustained pressure though - once the cracks start showing she has trouble holding it together.
- Warm and engaged with people she trusts, more reserved with strangers. Criticism hits harder than it should and she dwells on it for days.

## `<moral-compass>` (optional) [medium priority]

**Purpose:** What creates impossible choices for this character.

**Format:** 2-3 sentences

Focus on boundaries and values that can conflict. Where does mercy override duty (or not)? What lines won't they cross? This generates story tension when drives push against principles.

**When creating:**
Identify non-negotiables and negotiables. Include red lines they won't cross. Focus on principles that can create dilemmas when they conflict with motives. Avoid overly sharp moral stances - most people's ethics are more situational and conflicted than they'd admit.

**When editing:**
Verify it creates potential for dilemmas.

**Good examples:**
- Family comes first, even when they probably don't deserve it. Has bent the rules for relatives before and probably will again, though each time it sits a little worse. Won't hurt kids - that's a line that holds.
- Tries to be honest in business dealings, mostly because a reputation for straight dealing is valuable. Everything else is negotiable depending on who's asking and what's at stake. Promised things have to be delivered on, or at least explained.
- Won't break an oath once given, which is why he's gotten very careful about what he swears to. Avoids working with slavers when he can, though "when he can" has gotten more flexible over the years.

## `<flaws>` (optional) [medium priority]

**Purpose:** What gets in their way; how they sabotage themselves and cause trouble for others.

**Format:** 2-3 sentences

Focus on traits and patterns that create obstacles or complications. These drive plot by making success harder, creating additional problems, or causing difficulties for other characters.

**When creating:**
Describe personality flaws, fears, bad habits, or patterns that cause problems for themselves and others. Avoid overly sharp or dramatic formulations - real flaws are usually more mundane and harder to see clearly.

**Good examples:**
- Has a hard time letting go of old grievances, even when holding onto them makes everything harder. Doesn't trust authority figures, which means he often works around official channels when going through them would be simpler. Takes a long time to make decisions because he's always second-guessing.
- Believes people are basically good and means well, which leads to trusting the wrong people more often than she should. Doesn't really understand how political maneuvering works and thinks being right should be enough. Limited connections in the city, partly because she hasn't been here long and partly because she doesn't know how to build that kind of network.
- Tends to smooth things over and avoid direct confrontation, which means problems fester until they blow up. People think he agrees with them when he's really just staying quiet. Has trouble saying no even when he should.

## `<backstory>` (optional) [medium priority]

**Purpose:** Character's history and formative experiences.

**Format:** Concise list of key events and experiences

Focus on what's relevant to the current story. These are the events that explain who they are now.

**When creating:**
List formative events that shape who they are now. Keep entries concise - one or two sentences each. Include events that explain their current situation, relationships, skills, flaws, and motivations. Can use TBD if you'll fill this in later. Can be omitted entirely for minor characters.

**When editing:**
Verify it explains current behaviors without excessive detail.

**Good examples:**
- - Grew up in a coastal town, father was a fisherman who died when she was 12
- Mother remarried a merchant, moved to the city
- Learned the trade working in stepfather's warehouse
- Married at 19, husband died of fever three years later
- Took over managing his trade connections to support herself
- - Youngest of four siblings, only one who learned to read
- Apprenticed to a clerk at 14
- Caught in a fire at the counting house when he was 16, still has scars on his hands
- The clerk he worked for was accused of embezzlement (may or may not have been guilty)
- Has worked at the harbor for the past five years, keeps his head down

## `<normal-life>` (optional) [medium priority]

**Purpose:** What normal life looks like for this character.

**Format:** 2-4 sentences or short paragraphs

This establishes the baseline that story events will disrupt or transform. It's what's at stake when things go wrong.

**When creating:**
Describe their typical day-to-day life when the story isn't happening. What's their normal schedule and routine? What do they take for granted as just how things are? Focus on what's relevant - the baseline that story events will interrupt.

**When editing:**
Verify it establishes a clear routine showing what's at stake.

**Good examples:**
- Marcus wakes before dawn to check the ledger, walks the warehouse perimeter, then opens shop at first bell. Most days the same customers visit with routine problems: torn shipments, delayed payments, standard guild business. Regular accounts and inventory records are part of the daily work.
- She wakes at 6 for school, packs lunch, catches the 7:15 bus. After school she works at the diner until 9, then does homework. Weekends she sleeps in until 10, does laundry, runs errands. This schedule repeats week after week.
- Her routine centers on the baby's schedule: feeding every three hours, naps, basic care tasks. Meals happen around feeding times, laundry gets done when there's a moment, bills are paid on their usual dates. Most evenings are quiet at home.
- Classes run from 8 to 3, then the library until 5, then a shift at the coffee shop until closing. Weekends are for assignments, meal prep, and calling home. This is just how the semester goes.

## `<secrets>` (optional) [medium priority]

**Purpose:** Secrets the character keeps from others.

**Format:** 1-3 sentences

What would they only confess in the darkest moment? This fuels endings and bittersweet notes.

**When creating:**
Write what this character hides, maybe even from themselves. Can be set to blank if not relevant to the story.

**When editing:**
Verify it's actually secret with consequences if revealed.

**Good examples:**
- I switched the labels on the blood samples. The report everyone trusts is mine.
- The fire wasn't an accident. I pulled the batteries from the alarms first.
- I'm not "from" here. I changed my last name after the charge was dismissed.
- I know who my father is. He comes into the shop on Thursdays and doesn't recognize me.
- I told her the letter never came. It did. I hid it in the cookbook.
- I changed my testimony after the hallway talk. Nobody asked why the details shifted.
- I loved my kid less when he reminded me of his dad. I was kind, but I pulled back.
- I sometimes hope my sister stumbles so I can be the strong one again.

## `<narrative-lens>` (optional) [medium priority]

**Purpose:** What this character notices first; their preferred frame.

**Format:** 1-2 sentences, third person

This shapes what gets described in their POV passages. Different characters in the same scene will notice different things.

**When creating:**
Describe in third person what this character's attention naturally goes to. People, systems, textures, threats? What do they see first?

**When editing:**
Verify it's specific and fits the character.

**Good examples:**
- She notices people first - their hands, their expressions, who defers to whom.
- He sees the structure of things: trade routes, power flows, weak points.
- Textures catch her eye: worn wood, quality fabric, the sheen of fresh fish.

## `<internal-monologue-style>` (optional) [low priority]

**Purpose:** Cadence, texture, and voice of this character's thoughts.

**Format:** 1-2 sentence style description, followed by "Example:" and 40-80 words of first-person narration sample

This is the most concrete way to establish consistent voice. The example is more important than the description.

**When creating:**
First describe how this character thinks: In lists? In flowing associations? In questions? What's the cadence and texture?
Then provide a concrete sample of their internal voice in first person, prefixed with "Example:". The sample should demonstrate the style you described.

**When editing:**
Verify the example matches description with distinctive cadence.

**Good examples:**
- Clipped, tactical lists. Thinks in fragments, assessing threats and options without elaboration.

Example: I watch the guard rotation from the shadow of the dye-works. Three at the gate, two more I can't see yet. The third bell rings in ten minutes - shift change, if the dockmaster's still following protocol. If. That's the word that gets you killed. I count coins without moving my hands. Not enough for a straight bribe. Never is.
- Spiraling associations. Thoughts flow from one thing to the next, each connection leading deeper into memory or anxiety.

Example: The gate reminds me of home, which reminds me why I left, which brings me back to why I'm here. The same pattern: running from one problem into another. But this time feels different. This time I have a plan. Or at least the start of one. The coins in my pocket feel heavier than they should.
- Question-driven and self-doubting. Interrogates own decisions, second-guessing every choice.

Example: What was I thinking, coming here alone? Why did I think this would work? The guard's eyes are on me now, and I can't tell if it's suspicion or just boredom. Should I approach? Should I wait? Every option feels wrong, and the longer I hesitate, the more wrong it becomes.

## `<speaking-style>` (optional) [medium priority]

**Purpose:** Word choices, formality level, sentence patterns, and how this character speaks to others.

**Format:** 1-2 sentence style description, followed by "Example:" and 40-80 words of dialogue sample

The example is more important than the description. This affects both dialogue and internal monologue. Include address-forms here if they're notable to the character.

**When creating:**
First describe their speaking style: What level of formality? Any loanwords? Swears allowed or avoided? Does this character have distinctive sentence patterns (fragments, rhetorical questions, parallelism)?
Then provide a concrete sample of their actual speech, prefixed with "Example:". The sample should demonstrate the style you described and show vocabulary, rhythm, and formality in context.

**When editing:**
Verify the example matches description with distinctive style.

**Good examples:**
- Working-class informal with Greek loanwords. Direct and unpretentious, comfortable with casual profanity.

Example: "The dockmaster's being a malaka again. I told him the shipment was late, and he just shrugged. Like it's my problem his boats can't keep schedule. Look, I need access to the warehouse - the guild seal's on the manifest. Unless you want to explain to Master Komnenos why his goods are sitting on the dock?"
- Educated but not formal; avoids crude language. Uses precise vocabulary and measured pauses.

Example: "I need access to the warehouse. Master Komnenos approved the shipment - the guild seal's on the manifest." She produces the document, letting him see the wax, the mark, the weight of official paper. "Unless there's some... complication?"
- Tends to trail off or backtrack. Uncertain phrasing, lots of qualifiers and hedges.

Example: "I thought - well, I wasn't sure, but it seemed like maybe we should check the warehouse? If that's... I mean, I know you said the shipment wasn't due until tomorrow, but the manifest said today. Or I think it did. I could be remembering wrong."
- Over-explains when nervous. Gives more context and justification than needed, as if anticipating objections.

Example: "The thing is, the shipment's running late, and I know that's not your fault - the roads have been terrible with all the rain - but I really need to get into the warehouse today because there's a customer expecting delivery first thing tomorrow, and if I don't have it ready they'll probably go to another merchant next time, which, you know, I understand, business is business."

## `<humor-style>` (optional) [low priority]

**Purpose:** If and how humor surfaces for this character.

**Format:** 1-2 sentences description, plus 1-3 examples

Not all characters are funny. Set to blank to assert it is not important.

**When creating:**
Describe what kind of humor this character uses and when. Provide short example quotes that show it. Avoid overly sharp or witty formulations unless the character is specifically that quick.

**When editing:**
Verify it fits the character's personality.

**Good examples:**
- Self-deprecating when uncomfortable. "Yeah, well, I'm real good at making things worse, so..."
- Gentle teasing with people she trusts. "You're going to tie that knot all day or are we actually leaving?"
- Deflects with observations about small absurdities. "The cat's been sitting in that same spot for three hours. I think he's broken."

## `<physical-description>` (optional) [medium priority]

**Purpose:** Factual physical details for consistency.

This is for stability, not poetry. Record objective facts that need to stay consistent when the character appears.

**When creating:**
Write 2-4 sentences of objective facts: height, build, skin color, hair color and style, eye color, facial features, age appearance. Include details like shapeliness, facial structure, distinctive features. Avoid metaphor or interpretation. Keep descriptions neutral and factual.

**Good examples:**
- 5'10", medium build with some belly, brown skin, black hair (short, starting to thin at the crown), brown eyes, rounded face with a broad nose. Appears late 20s. Hands are calloused from dock work.
- Tall (6'2"), lean but angular rather than graceful, pale complexion with freckles across shoulders and arms, red hair (shoulder length, wavy, usually tied back), green eyes, narrow face with a sharp chin. Appears early 30s. Small scar on left eyebrow.
- Short (5'4"), stocky build with broad shoulders, olive skin, gray hair (balding, keeps what's left very short), blue eyes, square face with deep-set eyes. Appears 50s. Missing part of his left ear.
- Average height (5'6"), soft build, tan skin, dark brown hair (long, usually in a braid), dark eyes, round face with full cheeks and a small mouth. Appears mid-20s. Shapely, though she tends to wear loose clothing.

**Bad examples (avoid):**
- Mediterranean features, dark hair, watchful eyes. Usually wears earth-toned merchant robes. Slight beard. *(Too poetic, not factual)*
- An attractive middle-aged person. *(Too vague)*

## `<relationships>` (optional) [low priority]

**Purpose:** How this character connects to other characters.

**Format:** Standard types: family, friend, rival, business, romantic, mentor, other

This is primarily a housekeeping field, updated reactively as characters interact in the story. Don't fill proactively - add relationships as they emerge.

## `<headshot-prompt>` (optional) [low priority]

**Purpose:** Highly detailed description for AI-generated headshot portrait (shoulders up).

Write a comprehensive, highly detailed prompt for generating a shoulders-up portrait against a neutral background. This should be detailed enough that an AI image generator can create an accurate, consistent likeness. The character's name will be displayed at the bottom.

Generated file: `world/characters/images/{CharacterName}/headshot.png`

Include detailed descriptions of:
- Face: Skin tone, facial structure (round, angular, etc.), distinctive features
- Eyes: Color, shape, expression
- Hair: Color, length, style, texture (curly, straight, etc.)
- Age appearance: How old they look
- Expression: Neutral and relaxed (this is a reference portrait)
- Upper clothing: What's visible at collar/neckline/shoulders
- Accessories: Jewelry, hair ornaments, etc. visible in a headshot

Keep the background neutral - don't describe settings or environments.

**When creating:**
Write 3-5 detailed sentences. Be specific about every visible feature - vague prompts produce inconsistent results. Include skin tone, facial structure, eye color and shape, hair color/length/style, age appearance, expression, and upper clothing. Use physical-description as a source but write the prompt to be self-contained and comprehensive.

**Good examples:**
- A man in his late 20s with brown skin, a rounded face, and a broad nose. Short black hair, starting to thin at the crown. Brown eyes with a calm, steady gaze. Neutral, relaxed expression. Dark wool tunic with a linen collar visible at the neckline.
- A woman in her early 30s with olive skin and a narrow, angular face. Long dark brown hair pulled back in a practical braid. Dark eyes, slightly deep-set. Composed, neutral expression with a direct gaze. Simple undyed linen dress, neckline plain and unadorned.
- A man appearing in his 50s with pale, weathered skin and a square jaw. Balding, with close-cropped gray hair on the sides. Blue eyes with crow's feet at the corners. Missing part of his left ear. Calm, neutral expression. Rough homespun tunic, fraying at the collar.

**Bad examples (avoid):**
- Dark wool tunic with a linen collar visible. Neutral expression. *(Too vague, will produce inconsistent results)*
- Full merchant's outfit with belt, pouch, and boots. *(Describes full outfit, not headshot)*
- Angry scowl, teeth bared in rage. *(Too expressive for a reference portrait)*

## `<full-body-prompt>` (optional) [low priority]

**Purpose:** Description for AI-generated full body portrait (standing pose).

Describe the character for full body portrait generation - standing in a relaxed pose against a neutral background. The headshot image is used as a reference to maintain facial consistency, so only include a brief general face description here. The character's name will be displayed at the bottom.

Generated file: `world/characters/images/{CharacterName}/full-body.png`

This prompt should be very detailed for the body, but rely on the headshot reference for facial accuracy. Include:
- Brief general face description (age range, general expression - the headshot handles details)
- Complete outfit (clothing from head to toe, era-appropriate)
- Body type and build
- Stance and posture
- Hand positions and body language
- Any carried items or accessories

Keep the background neutral - don't describe settings or environments.

**When creating:**
Write 3-5 detailed sentences. Start with a brief face description (the headshot reference handles facial details). Then describe the full outfit in detail, body type, stance, and body language. Reference their social-role for appropriate attire.

**Good examples:**
- Dark wool tunic over a linen shirt, leather belt with a small pouch, practical boots worn from use. Standing in a relaxed but attentive pose, weight slightly on one foot, hands loosely at sides.
- Simple working-class dress in undyed linen, sleeves rolled up, worn apron tied at the waist. Standing with arms crossed, feet planted firmly, the stance of someone used to long hours on their feet.
- Fine silk robes in deep blue with gold embroidery, flowing to the ankles. Hands clasped in front, posture formal and upright, the composed bearing of court life.

**Bad examples (avoid):**
- Tall figure with brown hair, wearing a blue tunic. *(Includes physical details that belong in physical-description)*
- Walking through the marketplace carrying a basket. *(Describes a scene, not a portrait)*
