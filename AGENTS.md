# Story Project using .card format

XML-based format for organizing story elements and narrative planning.

## Workflow

1. `ske guide` - Find next task project-wide, or `ske guide stories/StoryName` for story-specific guidance
2. `ske create [path]` - Create a .card file from a template
3. Fill in fields using the instructions loop (see below)
4. `ske snapshot [path] -m "why you made changes" --no-feedback` or `--from-feedback="user's feedback"` - After completing edits to a file, performs an AI-analyzed version bump. The message should explain *why* (motivation, goal), not *what* (the diff is self-explanatory). You MUST specify either `--no-feedback` or `--from-feedback="..."` to indicate whether changes were guided by user/reader feedback. Use `--from-feedback` to transcribe or paraphrase feedback that led to this change - this will be analyzed to improve future guidance.
5. `ske validate` - Checks consistency and validity of edits, auto-commits result
6. Return to `ske guide` to find the next task

When working on a specific story, prefer `ske guide stories/StoryName` to see only the next step and TBDs for that story.

### Instructions Loop

When filling in a card:

1. `ske instructions /path.card` - See all TBD fields with line numbers
2. Pick a field to fill (reasoning fields first!)
3. `ske instructions '/path.card#/field-name'` - Get detailed guidance for that specific field (shows line number)
4. Edit the field in the file at the indicated line (fill reasoning + its associated content field together)
5. Repeat from step 1 until all fields are filled

For simple fields (like `full-name`) you may skip step 3 if the purpose is obvious. For complex fields, always get instructions first.

The `#/field-name` syntax targets a specific field. Line numbers help you locate fields quickly.

Example:
```
$ ske instructions /meta.card
...
## Other fields
  title: TBD (line 3)
    ske instructions /meta.card#/title
  narrative-structure: TBD (line 6)
    ske instructions /meta.card#/narrative-structure

$ ske instructions '/meta.card#/title'
<title-instructions>
  Line 3
  Purpose: Official title of the project or story
  ...
</title-instructions>
```

## Management

`ske mv old-path.card new-path.card` - renames the file AND updates all references

Do NOT commit files yourself, allow `ske validate` to handle commits

You may put freeform notes in `.md` files

`*.history.card` files show the history of a card file. Auto-managed, do not edit.

## Todos

Cards can have embedded todos for tracking follow-up work:

- `ske todo add path.card -m "Work needed"` - Add a todo
- `ske todo list` - See pending todos
- `ske todo mark path.card#/T1 done` - Mark complete (removes from card)
- `ske snapshot path.card -m "msg" --todo-done=T1` - Complete todos during snapshot

Use for internal reminders, not external feedback (use critiques for that).

## Core Concepts

**References**: `<ref ref="/world/characters/Name.card" role="Reason for reference" />`
When you use one .card file to generate or inform another file, use `<ref />` to note that reference and track dependencies.
Leave off version numbers (like `#v1.0.0`) - `ske validate` adds them automatically.

**TBD**: Most fields start out like `<name>TBD</name>` meaning the field has not been visited. `ske tbd` helps scan for TBD fields.

**Reasoning**: `<reasoning>` fields - Fill FIRST before content. These will be auto-cleared after archiving.
`ske instructions [path]` will give you specific instructions on how to fill out these fields.

Reasoning is like homework the agent should do before editing a field.

## File layout

All paths are rooted at the project root (this directory). The project represents the world in which all stories are embedded.

`stories/` - individual named stories; each may have its own pov-character
`world/` - canon that applies across all stories
`brainstorm/` - ideas the agent can use for storybuilding, but are NOT yet canon
`translation-guides/` - lists different locales and audiences for which the story can be repurposed
`docs/` - free-form notes on the project

## Reporting Issues

The user is also the developer of `ske`. If you encounter what appears to be a bug in `ske` (unexpected errors, incorrect behavior, confusing output), tell the user so they can triage or fix the issue.
