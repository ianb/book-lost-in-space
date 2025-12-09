---
name: managing-todos
description: Using the ske todo commands to track tasks within cards. Use when you need to add follow-up work items to a card, check pending todos across the project, or mark todos as complete during snapshot.
---

# Managing Todos

Todos are lightweight tasks embedded directly within cards. Unlike critiques (external feedback), todos are internal reminders for work that needs to be done on a card.

## XML Structure

```xml
<todos>
  <todo id="T1">Add more backstory about family history</todo>
  <todo id="T2" status="in-progress">
    Reconcile timeline with merchant guild events
    <ref ref="/world/factions/merchant-guild.card" />
  </todo>
</todos>
```

## Commands

### Add a Todo

```bash
ske todo add path/to/card.card -m "Description of work needed"
ske todo add path/to/card.card -m "Check consistency" --ref /other/card.card
```

- Creates a `<todos>` element if it doesn't exist
- Auto-generates the next available ID (T1, T2, etc.)
- IDs are never reused (scans card + history for used IDs)
- Outputs full reference: `Added todo path/to/card.card#/T1`

### List Todos

```bash
ske todo list                    # Current directory, default limit 5
ske todo list stories/           # Specific directory
ske todo list --limit 10         # Show more
ske todo list --offset 5         # Pagination
ske todo list --status active    # Filter by status
```

**Status filters** (default: active, in-progress):
- `active` - Default status (no attribute)
- `in-progress` - Currently being worked on

### Mark Todo Status

```bash
ske todo mark path/to/card.card#/T1 in-progress
ske todo mark path/to/card.card#/T1 done
ske todo mark path/to/card.card#/T1 ignored -m "No longer needed"
```

**Statuses:**
| Status | Meaning | Effect |
|--------|---------|--------|
| `active` | Default, needs attention | Stays in card (removes status attr) |
| `in-progress` | Currently working on | Stays in card |
| `done` | Completed | **Removed from card** |
| `ignored` | Won't do | **Removed from card** |
| `invalid` | No longer applicable | **Removed from card** |

When marked done/ignored/invalid, the todo is immediately removed from the card. The history remains in `.history.card` if the card was snapshotted while the todo existed.

### Complete Todos During Snapshot

```bash
ske snapshot path/to/card.card -m "Added family backstory" --no-feedback --todo-done=T1,T3
```

The `--todo-done` flag:
- Validates that specified IDs exist (errors if not found)
- Removes todos after archiving (like how reasoning is cleared)
- Use for todos completed as part of the work being snapshotted

For todos NOT related to the snapshot, use `ske todo mark` separately.

## Workflow

### Adding Todos While Working

When you notice follow-up work needed while editing a card:

```bash
# After editing a character card, you realize timeline needs checking
ske todo add /world/characters/Marcus.card -m "Verify merchant guild timeline" \
  --ref /world/factions/merchant-guild.card
```

### Reviewing Todos

```bash
# Check what needs attention
ske todo list

# Or for a specific area
ske todo list stories/My_Story/
```

### Completing Todos

When you complete work that addresses a todo:

```bash
# If completing as part of a snapshot
ske snapshot /world/characters/Marcus.card -m "Fixed timeline" --no-feedback --todo-done=T1

# If completing separately
ske todo mark /world/characters/Marcus.card#/T1 done
```

## Todos vs Critiques

| Aspect | Todos | Critiques |
|--------|-------|-----------|
| Source | Internal (agent-created) | External (user feedback) |
| Location | Embedded in cards | Separate files in `critiques/` |
| Workflow | Simple add/mark/list | Fetch, confirm, address cycle |
| Persistence | Removed when done | Archived for reference |

Use todos for:
- Follow-up work you identify while editing
- Reminders about consistency checks
- Tasks to revisit later

Use critiques for:
- External reader/user feedback
- Tracking user-reported issues

## Change Detection

Todos do NOT affect whether a card is considered "changed" for versioning. Adding, modifying, or removing todos won't trigger "needs snapshot" warnings.
