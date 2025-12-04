# Review User Feedback

You're being asked to review and address user feedback (critiques) on this story.

## Step 1: List Pending Critiques

First, get an overview of what's pending:
```bash
ske critique list --summary
```

Then list the critiques (shows 4 by default, sorted by passage position):
```bash
ske critique list
```

If there are more than 4, you can paginate with `--offset 4` or increase with `--limit 10`.

If there are no critiques, inform the user and stop.

## Step 2: Select a Critique

If there's only one critique, proceed with it.

If there are multiple critiques, consider:
- **Priority**: Earlier feedback numbers (C1, C2) came first
- **Context**: If the user mentioned a specific critique or topic, start there
- **Scope**: Simple fixes can be done quickly; complex ones may need discussion

If it's not obvious which to handle first, briefly list the options and ask the user which they'd like to address.

## Step 3: Investigate the Feedback

For the selected critique:

1. **Read the critique carefully** - Understand what the user is saying
2. **Find the referenced passage** - The critique includes `<ref role="Passage">` pointing to where feedback was given
3. **Read the passage** - Understand the current content
4. **Read surrounding context** if needed - Previous/next passages, character cards, story-arc

Consider:
- Is the feedback valid? Does it identify a real issue?
- Is the fix obvious, or are there multiple approaches?
- Does addressing this require changes to other passages?

## Step 4: Decide on Action

### If the feedback is invalid or out of scope:

Mark it appropriately:
```bash
ske critique mark /critiques/unconfirmed/User.card#/C## invalid -m "Reason why invalid"
# or
ske critique mark /critiques/unconfirmed/User.card#/C## ignored -m "Reason why not addressing"
```

Inform the user of your decision.

### If the fix is obvious and low-risk:

1. Make the edit directly to the passage
2. Briefly explain what you changed
3. Mark the critique as applied:
```bash
ske critique mark /critiques/unconfirmed/User.card#/C## applied /path/to/edited/passage.card -m "Brief description of fix"
```

### If the fix requires judgment or has multiple approaches:

1. Explain the feedback and what it's asking for
2. Propose your recommended approach (or present options)
3. Ask the user to confirm before making changes
4. Once confirmed, make the edits
5. Mark the critique as applied with the passage paths

### If you need more information:

Ask the user for clarification before proceeding. You might need to understand:
- The intended tone or effect
- Character motivations
- Plot implications
- Whether this connects to other story elements

## Step 5: Continue or Stop

After handling one critique, ask if the user wants to continue with the next one, or stop for now.

## Guidelines

**Proceed autonomously for:**
- Typos and grammatical errors
- Minor clarity improvements
- Obvious factual corrections within the story
- Small prose polish that matches the established voice

**Confirm with user for:**
- Changes that affect plot or character development
- Rewriting significant portions of text
- Feedback that conflicts with story-arc or narrative-guide
- Ambiguous feedback that could be interpreted multiple ways
- Changes that might affect other passages

**Always show your reasoning** when making non-trivial changes. Explain why the feedback is valid and how your edit addresses it.
