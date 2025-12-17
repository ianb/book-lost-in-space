---
name: diction-checking
description: Detecting AI-typical word patterns in prose using ske critique diction. Use when reviewing passages for overused AI language patterns, or when managing project-level ignore rules for acceptable terms.
---

# Diction Checking

Ske includes a diction checker that identifies words and phrases commonly overused by AI language models. This helps maintain natural-sounding prose.

## Commands

### Check a Passage or Story

```bash
ske critique diction /stories/My_Story/passages/1_Opening/passage.card
ske critique diction /stories/My_Story  # Check entire story
```

**Options:**
- `--new` - Only show issues not previously reported
- `--clear` - Clear previously reported issues for the path
- `--verbose` - Show detailed loading/scanning info
- `--window <n>` - Window size for story analysis (default: 5)

### Ignore a Term

If a flagged term is intentional for your project (e.g., a character named "Elara"):

```bash
ske critique ignore-diction "Elara"
```

This adds the term to `diction-rules.json` at the project root. The term is matched case-insensitively and supports partial matching:

```bash
ske critique ignore-diction "face tight"  # Matches "face tightening"
```

If the match is ambiguous, the command shows all matches and asks you to be more specific.

## Priority Levels

- **HIGH**: Terms that strongly signal AI-generated text (e.g., "delve", "tapestry", "testament"). Flagged on every occurrence.
- **MEDIUM**: Iffy terms that become suspicious when frequent. Only flagged when exceeding thresholds.
- **LOW**: Normal words that might indicate AI overuse in large numbers.

## What Gets Checked

- Narrative terms ("delve", "tapestry", "palpable", "testament")
- AI-typical character names ("Elara", "Kael", "Blackwood", "Thorne")
- Overused phrases ("a journey of", "shed light on", "in the heart of")

## Project-Level Ignore Rules

The `diction-rules.json` file at project root stores ignored terms:

```json
{
  "ignore": [
    "Elara",
    "tapestry"
  ]
}
```

These terms are filtered from all diction checks (`ske critique diction` and `ske hook lint`).

## Integration with ske hook lint

When editing `passage.card` files, `ske hook lint` automatically runs diction checks and reports new issues. It uses the same ignore rules and tracks previously reported issues per passage.

## When to Ignore Terms

- Character names that happen to match AI-typical names
- Terms central to your story's theme (e.g., "tapestry" in a weaving-focused story)
- Technical terms appropriate to your setting

## When NOT to Ignore

- General overused words that could be replaced with varied vocabulary
- Phrases that feel clichéd even in context
- Terms flagged frequently across many passages
