---
name: creating-penpal-content
description: Creating penpal content - character correspondence via voice memos or letters. Turn-based exchanges where a character responds to incoming messages. Use when creating interactive character communication content.
---

# Creating Penpal Content

Penpal content is character correspondence - voice memos or letters where a character responds to incoming messages. Each exchange is a turn: an incoming message (provided externally) and the character's response.

## Goals

- Authentic character voice in direct communication
- Turn-based exchanges that feel like real correspondence
- Character stays true to their knowledge, boundaries, and personality
- Grounded in story timeline - what does the character know right now?

## Structure

```
penpal/
  {CharacterName}/
    penpal-character.card              # How this character communicates
    {ConversationName}/
      penpal-conversation.card         # Thread context (who, when, relationship)
      {number}_{slug}/
        outline-penpal.card            # Incoming message + response planning
        passage-penpal.card            # The response
```

## Workflow

### 1. Create Character Config

```bash
ske create /penpal/Character_Name
```

This creates `penpal-character.card` which defines:
- Reference to `/world/characters/Character_Name.card`
- Communication style with example (how they talk in messages)
- Default formality level
- Topics they discuss freely
- Hard limits (what they won't discuss, and how they react if pushed)
- Voice settings (inherit from story-info.card if POV character)
- Optional `voice-sample` and `voice-stage-directions` for testing voices with `ske compare-voice`

**Read first:**
- The character's main card for speaking-style and worldview
- Any stories where they're a POV character for voice settings

### 2. Create a Conversation Thread

```bash
ske create /penpal/Character_Name/Fan_Letter
```

This creates `penpal-conversation.card` which defines:
- Who the correspondent is (a character, "Listener", or description)
- The relationship between them
- When in the story timeline this happens (story-moment)
- Medium (voice-memo, letter, text-message)
- Formality level for this thread

### 3. Create Exchanges

```bash
ske create /penpal/Character_Name/Fan_Letter/1_Intro
```

This creates two cards:

**outline-penpal.card**:
- `incoming-message`: **DO NOT FILL** - wait for external input
- `interpretation`: How the character reads the message
- `emotional-response`: What they feel
- `will-share`: Topics and content to include
- `will-avoid`: What to deflect and how
- `knowledge-boundaries`: What they don't know
- `response-arc`: Structure of the response

**passage-penpal.card**:
- Copy of incoming-message (for complete exchange in one file)
- The character's response in their voice
- Title for the exchange

### 4. The External Message Flow

**Important:** The `incoming-message` in outline-penpal.card says "TBD DO NOT FILL". This is intentional - the message comes from the user or an external source.

1. User/external source fills `incoming-message` in outline-penpal.card
2. Only then: fill the rest of outline-penpal.card (interpretation, response planning)
3. Then: create passage-penpal.card with the response

If `incoming-message` still says "TBD DO NOT FILL", stop and wait.

### 5. Generate Voice Files

```bash
ske gen passage-voice penpal/Character_Name/Fan_Letter
```

Uses "minimal" mode - the text is already conversational.

## Writing Guidelines

- **Voice**: Match communication-style from penpal-character.card
- **Medium awareness**: Voice memos feel spoken (pauses, self-corrections); letters feel written
- **Story-grounded**: The character only knows what they know at story-moment
- **Relationship-appropriate**: Match formality and intimacy to the relationship
- **Boundaries**: Use will-avoid strategies faithfully (deflection, humor, subject change)

## When to Confirm with User

- Which character to use
- Who the correspondent is
- The nature of the relationship
- When in the story timeline this happens

## When to Proceed Autonomously

- Response planning (interpretation, emotional-response, will-share/avoid)
- Writing the response once outline is complete
- Specific phrasing and voice details
- Deflection strategies for avoided topics

## Key Principle

The character responds to what's actually in the incoming message, filtered through:
- Their relationship with the correspondent
- Their current story circumstances (story-moment)
- Their personality and hard limits
- What they actually know right now
