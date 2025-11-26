# Story Project using .card format

XML-based format for organizing story elements and narrative planning.

## Workflow

1. `ske guide` - Find next task and see TBD fields with line numbers
2. `ske create [path]` - Create a .card file from a template
3. Fill in fields using the instructions loop (see below)
4. `ske snapshot [path] -m "why"` - After editing, performs an AI-analyzed version bump
5. `ske validate` - Checks consistency and validity of edits, auto-commits result

### Instructions Loop

When filling in a card, iterate through fields one at a time:

1. `ske instructions /path.card` - See all TBD fields with line numbers
2. Pick a field to fill (reasoning fields first!)
3. `ske instructions '/path.card#/field-name'` - Get detailed guidance for that specific field (shows line number)
4. Edit the field in the file at the indicated line
5. Repeat from step 1 until all fields are filled

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

## Core Concepts

**References**: `<ref ref="/world/characters/Name.card#v1.2.0/element-name" role="Reason for reference" />`
References may include `#v1.0.0` to indicate a version, but this can also be added automatically by `ske validate`
When you use one .card file to generate or inform another file, use `<ref />` to note that reference and track dependencies.

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
