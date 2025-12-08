---
name: handling-critiques
description: Managing the critiques/ directory where external reader feedback is stored. Use when critiques have been submitted through the web interface and need to be fetched, reviewed, addressed, or marked with status (confirmed, in-progress, done, ignored).
---

# Handling Critiques

Critiques are user feedback submitted through the web interface. They're fetched, reviewed, and marked with statuses as you address them.

## Directory Structure

```
critiques/
├── unconfirmed/    # Newly fetched, not reviewed
├── confirmed/      # Reviewed, will address
├── in-progress/    # Currently being worked on
└── done/           # Completed (kept for reference)
```

Note: `ignored` and `invalid` critiques are deleted (after archiving in `.history.card`).

## Commands

### Fetch New Critiques

```bash
ske critique fetch
```

Downloads new feedback from the server into `/critiques/unconfirmed/`. Requires `LOWLIGHT_API_KEY` and `LOWLIGHT_API_URL` (or `LOWLIGHT_LOCAL=1`).

### List Pending Critiques

```bash
ske critique list
```

Shows critiques that need attention (default: 4 most recent). Output includes the critique path for use with `ske critique mark`.

**Options:**
- `--status <statuses>` - Filter by status (default: unconfirmed,confirmed,in-progress)
- `--summary` - Show count summary instead of listing critiques
- `--sort <method>` - Sort by: passage, recent, shuffle, user, recent-user (default: passage)
- `--limit <n>` - Max critiques to show (default: 4)
- `--limit-users <n>` - Max different users to include
- `--limit-by-user <n>` - Max critiques per user
- `--offset <n>` - Skip first N critiques (pagination)

**Examples:**
```bash
ske critique list --summary           # Count by status
ske critique list --status unconfirmed --limit 10  # All unconfirmed
ske critique list --offset 4          # Next page
```

### Mark Critique Status

```bash
ske critique mark <critique-path> <status> [passage-paths...] [options]
```

**Arguments:**
- `critique-path` - Path like `/critiques/unconfirmed/User.card#/C42`
- `status` - One of: `unconfirmed`, `confirmed`, `in-progress`, `done`, `ignored`, `invalid`
- `passage-paths` - Optional paths to passages that address this critique

**Options:**
- `-m, --message <text>` - Reason for status change (stored in `<reason>` element)
- `--message-to-user <text>` - Message shown to user in web UI
- `--dry-run` - Preview changes without applying
- `--verbose` - Show detailed output

## Workflow

### 1. Fetch and Review

```bash
ske critique fetch
ske critique list
```

Read each critique to understand the feedback.

### 2. Confirm or Reject

For feedback you'll address:
```bash
ske critique mark /critiques/unconfirmed/User.card#/C42 confirmed
```

For feedback that won't be addressed:
```bash
ske critique mark /critiques/unconfirmed/User.card#/C5 ignored -m "Out of scope"
```

For invalid/misunderstood feedback:
```bash
ske critique mark /critiques/unconfirmed/User.card#/C10 invalid -m "Already fixed in v2.0"
```

### 3. Work on Confirmed Critiques

When starting work:
```bash
ske critique mark /critiques/confirmed/User.card#/C42 in-progress
```

### 4. Mark as Done

When done, include the passages you edited:
```bash
ske critique mark /critiques/in-progress/User.card#/C42 done \
  /stories/My_Story/passages/1_Opening/passage.card \
  -m "Added more description per feedback"
```

This adds `<ref>` elements with the current passage versions, showing which edits addressed the feedback.

## Status Meanings

| Status | Meaning | Directory |
|--------|---------|-----------|
| `unconfirmed` | Newly fetched, not reviewed | `critiques/unconfirmed/` |
| `confirmed` | Will address this feedback | `critiques/confirmed/` |
| `in-progress` | Currently working on it | `critiques/in-progress/` |
| `done` | Feedback has been addressed | `critiques/done/` |
| `ignored` | Won't address (archived, deleted) | - |
| `invalid` | Not applicable (archived, deleted) | - |

## Critique Card Structure

```xml
<critique id="C42" status="confirmed">
  <creator user-id="..." email="user@example.com" name="User Name" created="2025-12-03T14:30:00 America/Chicago" />
  <ref ref="/stories/My_Story#v1.2.3" story-version-id="..." role="Story" />
  <ref ref="/stories/My_Story/passages/1_Opening/passage.card#v1.2.3/text/progress-0.34" passage-id="..." role="Passage" />
  <feedback speech="true" audio-url="...">The transcribed feedback text...</feedback>
  <reason>Added more description per feedback</reason>
  <ref ref="/stories/My_Story/passages/1_Opening/passage.card#v2.0.0" status="done" role="Edited" />
</critique>
```

## When to Confirm with User

- Feedback that requires significant story changes
- Conflicting feedback from multiple users
- Feedback that might affect story direction

## When to Proceed Autonomously

- Minor prose improvements
- Clarity fixes
- Obvious errors or typos
- Feedback that aligns with existing story direction
