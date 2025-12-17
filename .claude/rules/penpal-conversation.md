---
paths: **/penpal-conversation.card
---

## `<reasoning>` (optional) [low priority]

**Purpose:** Guided thinking for establishing the conversation context.

Before creating a penpal conversation card, read:
1. The penpal-character.card for this character - what's their situation, communication style, and hard limits?
2. If the correspondent is a known character, their character card

Consider:
1. Who is on the other end of this conversation? Are they a character in the world, or someone external?
2. What's the nature of this relationship? How do they know each other?
3. When does this conversation happen relative to the character's stories?
4. What medium are they using for this thread?
5. How formal or casual is this exchange?
6. How does this character initiate in conversation? Do they ask questions, share stories, bring up topics? Or do they mostly respond?

Note what you've read to confirm you have the context.

## `<title>` (required) [high priority]

**Purpose:** Display title for this conversation thread, used when uploading and displaying on the web.

**Format:** Short title phrase with both characters

The title should identify both participants in the conversation. Can optionally include a word or two about the context or circumstances.

**When creating:**
Include both the character name and the correspondent. Keep it short - the names plus an optional context word. If the correspondent is "Listener" or undefined, can use a descriptive phrase instead.

**Good examples:**
- Marcus & Elena
- Jin & the Stranger
- Marcus & Elena - Missing Shipment
- Letters to a Friend

## `<correspondent>` (required) [high priority]

**Purpose:** Who this character is talking to throughout this conversation thread.

**Format:** Name or description, optionally with character ref

Who is on the other end of this conversation? This might be a specific named character from the world, a type of person ("a fan who reached out"), or "Listener" for an undefined audience.

**When creating:**
Identify who the character is talking to. If it's an existing character, include a ref. If it's someone new or undefined, describe them briefly.

**Good examples:**
- Elena Komnenos (/world/characters/Elena_Komnenos.card) - his sister
- Listener - someone who reached out after finding the character's contact info
- A stranger who claims to be a distant relative
- An old friend from before the move

## `<relationship>` (required) [high priority]

**Purpose:** The nature of this relationship and how it shapes all exchanges in this thread.

**Format:** 2-4 sentences

What kind of relationship is this? How long have they been in contact? What's the emotional tone? What does the character want from this relationship? This shapes what they'll share, how formal they are, and what's at stake across all exchanges.

**When creating:**
Describe the relationship dynamics. Are they close or distant? Is there tension or ease? What history do they share? What does the character hope to get from this correspondence?

**Good examples:**
- They were close growing up but have drifted apart since Elena moved to Venice. The correspondence is an attempt to maintain connection across distance. He values her opinion but is careful not to burden her with his problems.
- A new connection - they've only exchanged a few messages. The character is curious but cautious, not sure yet how much to trust this person or what they want.
- An old friend who knows too much about the character's past. Comfortable but slightly guarded - there are things the character doesn't want to revisit.

## `<story-moment>` (required) [high priority]

**Purpose:** When this conversation thread takes place in the character's story timeline.

**Format:** 2-4 sentences

Ground this entire thread in the character's story timeline. What has happened to them recently? What story are they in or between? This sets the baseline context for all exchanges in the thread - individual exchanges can note how things have progressed since.

**When creating:**
Be specific about timing. Reference relevant story events. Note what the character knows and doesn't know at the start of this thread. This is the anchor point - exchanges will build from here.

**Good examples:**
- This thread begins during "The Missing Shipment" - Marcus has just started noticing irregularities at the warehouse but hasn't uncovered anything concrete yet. He's uneasy but doesn't know who to trust.
- Between stories. It's been three weeks since the events of "Harbor Fire." Marcus is still processing what happened, but life has returned to routine.
- Early in the timeline, before any major events. Marcus is still new to the city, still learning who to trust.

## `<medium>` (required) [high priority]

**Purpose:** How the character communicates in this thread - voice memos or written messages.

**Format:** Short descriptor with optional notes

Voice memos feel more intimate and spontaneous - the character is speaking directly. Written messages (letters, texts) are more considered. This applies to the whole thread. Voice memos are more common for this format since it produces audio content.

**Good examples:**
- voice-memo - feels natural for him, like talking to someone who isn't there
- voice-memo - she's not much of a writer, prefers to just talk
- letter - old-fashioned, but it's how she was raised to communicate across distance

## `<formality>` (required) [medium priority]

**Purpose:** The formality level for this conversation thread.

**Format:** Short descriptor

How formal or casual is this exchange? This might differ from the character's default-formality in penpal-character.card based on the specific relationship.

**Good examples:**
- intimate - they've known each other since childhood
- casual - comfortable but not deeply personal
- semi-formal - polite but warming up as the thread progresses

## `<initiates>` (required) [high priority]

**Purpose:** How the character brings their own content to the conversation - not just responding.

**Format:** 2-4 sentences describing patterns

A good conversation isn't just answers. How does this character initiate? Do they ask questions about the correspondent's life? Share stories unprompted? Bring up things they've been thinking about? This shapes how active vs. reactive they are in the exchange.

This is about general patterns for this thread - the outline-penpal will specify what they actually initiate in each exchange.

**When creating:**
Describe how this character typically initiates in conversation with this correspondent:
- Do they ask questions? What kind? (about feelings, practical matters, shared memories?)
- Do they share their own stories and observations unprompted?
- Do they bring up things they've been thinking about between messages?
- How much do they drive the conversation vs. follow the correspondent's lead?

**Good examples:**
- He asks a lot of questions - genuinely curious about her daily life, the kids, what she's reading. He also shares small observations from his own day, turning them into little stories. Less likely to bring up heavy topics himself; waits for her to open those doors.
- She drives conversation. Brings up whatever's on her mind, asks pointed questions, doesn't wait to be asked about her own life. Will interrupt her own train of thought to ask about something she suddenly remembered.
- Mostly reactive - responds thoroughly to what's asked but doesn't volunteer much. When he does initiate, it's usually a question that's been bothering him. Rarely shares stories about himself unless directly relevant.

## `<thread-notes>` (optional) [low priority]

**Purpose:** Any additional context or notes for this conversation thread.

**Format:** Free-form notes

Anything else relevant to the whole thread that doesn't fit elsewhere. Topics that are likely to come up, dynamics to maintain, things to remember across exchanges.

**Good examples:**
- Elena doesn't know about Marcus's money troubles - he's been hiding them. If she finds out, that would be a significant shift in the thread dynamic.
- The correspondent is testing whether Marcus can be trusted with a secret. The thread builds toward a reveal.

## `<sources>` (optional) [low priority]

**Purpose:** References to source cards.

**Format:** List of ref elements
