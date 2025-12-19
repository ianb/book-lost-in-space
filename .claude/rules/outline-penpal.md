---
paths: **/outline-penpal.card
---

## `<reasoning>` (optional) [low priority]

**Purpose:** Guided thinking for planning the exchange.

Before creating a penpal outline, read the context:
1. Read the penpal-conversation.card for this thread - who is the correspondent, what's the relationship, and when in the story timeline is this happening?
2. Read the penpal-character.card - what do they discuss freely, and what are their hard limits?
3. If this isn't the first exchange, read the previous exchange:
   - Previous outline-penpal.card - what was discussed? What did the character share or avoid?
   - Previous passage-penpal.card - how did the character's last message end? What tone did they leave on?
   This continuity is essential - the conversation should flow naturally from what came before.
4. To find relevant context about the character across the codebase, use:
   ske search "topic from incoming message" --ref /world/characters/{characterName}.card

IMPORTANT: Check incoming-message first. If it still says "TBD DO NOT FILL", stop here - the message hasn't been provided yet. Do not fill in other fields until the incoming message is available.

Once the incoming message is provided, consider:
1. How much time has passed since the last exchange? A few hours? Days? Weeks?
2. What has happened in the character's life between exchanges? Make up small events - things they did, people they saw, thoughts they had. Use ((...)) for events that happened but may not be mentioned directly or revealed until later.
3. What has the correspondent sent? What are they asking, sharing, or expressing?
4. How does this connect to or follow up on the previous exchange (if any)?
5. Given the story-moment from penpal-conversation.card, what does the character know right now?
6. How does the character interpret this message - what do they notice, assume, or wonder about?
7. What emotional response does it provoke?
8. What will they share in response? What will they avoid?

Confirm you've read the context by noting the correspondent, relationship, hard limits, and (if applicable) what happened in the previous exchange.

## `<time-since-last>` (optional) [medium priority]

**Purpose:** How much time has passed since the previous exchange.

**Format:** Brief description of elapsed time

Imagine the rhythm of this correspondence. Are they messaging back and forth quickly? Is there a natural delay of days or weeks? Time passing adds texture - it gives the character things to report on, creates anticipation, and makes the exchange feel like part of a real ongoing relationship.

Leave empty for the first exchange in a thread.

**Good examples:**
- A few days - she's been busy with work but thinking about his last message
- Two weeks - longer than usual, he's been avoiding responding
- Just a few hours - she couldn't wait to reply
- Almost a month - life got in the way

## `<intervening-events>` (optional) [medium priority]

**Purpose:** What has happened in the character's life between exchanges.

**Format:** Bulleted list of events, using ((...)) for things that may not be mentioned directly

Life doesn't stop between messages. Make up small events that happened - mundane things, notable moments, thoughts they had, people they encountered. These give the character something to talk about and ground the exchange in ongoing life.

Use ((...)) for events that:
- Happened but the character might not mention
- Will be revealed gradually across exchanges
- Color their emotional state without being stated directly

Keep it grounded in the story-moment - what's plausible given where they are in the story?

**Good examples:**
- - Had coffee with a coworker who asked about family
- ((Received a letter from Dad that he hasn't opened yet))
- Finished reading that book she mentioned
- Caught a cold, mostly better now
- ((Saw someone who looked like the correspondent on the street - thought about them all day))
- - Routine week at the warehouse
- ((Overheard something about the missing shipment - pretending he didn't))
- Made a new recipe, it turned out okay
- Slept badly a few nights

## `<incoming-message>` (required) [external priority]

**Purpose:** The message the character receives - the prompt for their response.

**Format:** The complete text of the incoming message

This field is filled EXTERNALLY by the user or another source - do not generate content for it. If it still contains "TBD DO NOT FILL", the message hasn't been provided yet and you should not proceed with filling other fields.

Once provided, this is what the correspondent sent. It should feel authentic to that relationship - matching the tone, concerns, and style of the correspondent.

**When creating:**
DO NOT FILL THIS FIELD. Wait for the user or external source to provide the incoming message. Only proceed with interpretation, emotional-response, and other fields after the incoming message has been provided.

**Good examples:**
- Hey, it's me. Got your message - finally, I was starting to think you'd forgotten how phones work. [laughs]

So listen, I talked to Dad. He's... you know how he is. He mentioned something about the property taxes again, and I couldn't tell if he was asking for help or just complaining. Have you heard from him?

Anyway, the kids are fine. Marco's learning to read - it's adorable, he gets so proud when he sounds out a word. I wish you could see him.

Call me back when you get this. Or send another one of your rambling voice memos. Either way. Miss you.

## `<interpretation>` (required) [high priority]

**Purpose:** How the character reads and interprets the incoming message.

**Format:** 2-4 sentences

What does the character notice in the message? What do they read between the lines? What assumptions do they make? This shapes their response - they're not responding to what was literally said, but to what they understood. Their interpretation is colored by the story-moment from penpal-conversation.card.

**When creating:**
Write in third person. Describe what the character picks up on - both explicit and implicit. Note any misreadings or assumptions that will shape the response. Consider how the story-moment (from penpal-conversation.card) affects what they notice.

**Good examples:**
- He notices Elena bringing up Dad early - that's not like her. She's worried, probably more than she's letting on. The mention of property taxes suggests Dad may have asked her for money, which means things are worse than Marcus thought. The stuff about the kids feels like she's trying to keep things light despite her concern.

## `<emotional-response>` (required) [high priority]

**Purpose:** The character's emotional reaction to receiving this message.

**Format:** 2-3 sentences

What does the character feel? This might be simple (happy to hear from them) or complex (a mix of love, guilt, and worry). The emotional state shapes the tone of their response. Consider how their current story circumstances amplify or complicate their reaction.

**When creating:**
Write in third person. Be specific about the emotions and what triggers them. If there's internal conflict, note it.

**Good examples:**
- Relief at hearing from her - it's been too long. But the bit about Dad sits heavy. He'd hoped Elena was sheltered from all that in Venice. There's guilt too: she's asking him questions he can't really answer, about a situation he's been avoiding.

## `<will-share>` (required) [high priority]

**Purpose:** What the character will openly share in their response.

**Format:** Bulleted list of topics/content

What will they talk about freely? This should align with discusses-freely from penpal-character.card, filtered through what's relevant to this exchange. Consider the relationship and story-moment from penpal-conversation.card. Include specific details they can share given what they currently know.

**When creating:**
List what the character will include in their response. Be specific about topics, anecdotes, questions they'll ask, memories they'll share. Ground it in their current story circumstances from penpal-conversation.card.

**Good examples:**
- - React warmly to her teasing about his message frequency
- Ask more about Marco's reading - what words has he learned?
- A memory of Elena learning to read when they were kids
- Observations about spring in the city, keeping it light
- Questions about her life - genuine interest

## `<initiates>` (required) [high priority]

**Purpose:** What the character brings to the conversation on their own - not just responding.

**Format:** Bulleted list of questions, stories, and topics

A good message isn't just answers. What does the character bring unprompted? Questions about the correspondent's life, stories from their own day, topics they've been thinking about. Reference the initiates pattern from penpal-conversation.card and make it specific for this exchange.

This is separate from will-share because these are things the character introduces, not things they're responding to. The correspondent didn't ask; the character is driving part of the conversation.

**When creating:**
List specific things the character will initiate:
- Questions they'll ask (about the correspondent's life, feelings, plans)
- Stories or observations they'll share without being asked
- Topics they'll bring up that the incoming message didn't mention
- Things from intervening-events they want to tell the correspondent about

Follow the pattern established in penpal-conversation.card's initiates field.

**Good examples:**
- - Ask how the children's school is going - she mentioned it last time
- Share the story about the strange customer at the warehouse yesterday
- Bring up that he's been thinking about visiting, maybe in the spring
- Ask what she's been reading lately
- Mention the dream he had about their childhood home
- - No questions this time - she's too wrapped up in her own news
- Tell the story of the argument she overheard at the market
- Bring up that she's considering a change (hint at it, don't explain)

## `<will-avoid>` (required) [high priority]

**Purpose:** What the character will avoid, minimize, or handle carefully.

**Format:** Bulleted list with notes on how they'll handle each

What won't they share, or what will they only address obliquely? Consider both the character's general patterns (from penpal-character.card) and what's specific to this exchange given the relationship and story-moment from penpal-conversation.card. Note the strategy for each.

**When creating:**
List what the character will avoid or handle carefully. For each, note the strategy: deflection, minimization, subject change, vague reassurance, humor, etc.

**Good examples:**
- - Dad and the property taxes: will acknowledge he's heard from Dad too, imply he's handling it, avoid revealing how bad it is. Deflect with "you know how he exaggerates"
- His own financial struggles: won't mention at all
- How long it's been since he called: brief self-deprecating joke, move on quickly
- His loneliness: absolutely won't mention - will redirect to asking about her

## `<knowledge-boundaries>` (optional) [medium priority]

**Purpose:** What the character doesn't know and therefore can't discuss.

**Format:** Bulleted list

What is outside this character's knowledge at this story-moment? They can't talk about things they don't know. This keeps the response authentic to what the character could actually say right now.

**When creating:**
List relevant knowledge gaps based on story-moment. Consider: what's happening elsewhere that they don't know about? What has changed since they last had information? What would they assume incorrectly?

**Good examples:**
- - Doesn't know the full extent of Dad's debts
- Doesn't know Elena has already sent Dad money
- Doesn't know about the political situation in Venice that Elena alluded to obliquely
- Assumes Elena's husband is doing well (may not be true)

## `<response-arc>` (optional) [medium priority]

**Purpose:** The structure and emotional arc of the response.

**Format:** 3-5 bullet points describing the message's flow

How will the response be structured? What's the emotional trajectory - does it start light and get heavier? Start with difficult things and end warm? This helps plan the pacing.

Messages vary widely in length (200-1500 words, averaging 400-700). A quick check-in might have 2-3 beats. A significant emotional exchange might have 5-6. Let the moment and the character's personality determine scope - some people write short, punchy messages; others ramble.

**When creating:**
Outline the message's structure: opening, middle sections, closing. Note the emotional tone of each section. Consider whether this is a quick exchange or a more substantial one - not every message needs many beats.

**Good examples:**
- 1. Warm, slightly self-deprecating opening (responding to her teasing)
2. Light section: react to Marco, share the memory of Elena learning to read
3. Brief careful section: acknowledge Dad's situation, reassure without lying
4. Redirect: ask about her life, genuine curiosity
5. Warm closing: express missing her, promise to be better about staying in touch

## `<sources>` (optional) [low priority]

**Purpose:** References to source cards.

**Format:** List of ref elements
