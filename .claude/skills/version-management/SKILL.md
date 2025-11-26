---
name: version-management
description: Version strategy, ske snapshot usage, handling version drift
---

# Version Management

## Using ske snapshot

`ske snapshot path/to/file.card -m "Added backstory details"`

- AI analyzes changes and determines bump type (major/minor/patch)
- Archives old version automatically
- Assigns version to existing `<changelog-entry>` or uses `-m` message
- **Changelog focus**: Explain WHY changes were made, not WHAT (diff shows WHAT)

## When to Bump

**Major (1.0.0 → 2.0.0)**: Breaking changes
- Name changes
- Role changes
- Entity identity shifts

**Minor (1.0.0 → 1.1.0)**: Non-breaking additions
- New fields filled in
- Backstory expanded
- Relationships added

**Patch (1.0.0 → 1.0.1)**: Trivial fixes
- Typos
- Clarifications
- Formatting

## Version Drift

When references use old versions:

`ske version-instruct [path]` - See changelogs and update guidance
`ske version-instruct --for [entity]` - Find all outdated references to entity

## Manual Versioning

If not using `ske snapshot`, manually:
1. Bump `version="1.2.0"` attribute
2. Add `<changelog-entry version="1.2.0">...</changelog-entry>`
3. Run `ske validate` to archive
