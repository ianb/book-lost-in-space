---
name: handling-validation-errors
description: Resolving errors and warnings from ske validate. Use when validation fails, when you see warnings about TBD values, outdated references, or missing snapshots, and need to understand how to fix them.
---

# Handling Validation Errors

## Common Errors

### XML Parsing Error

```
XML parsing error: [details]
```

**Fix**: Check the file for malformed XML - unclosed tags, invalid characters, or syntax errors.

### Required Field Empty

```
Required field <backstory> is empty
```

**Fix**: Fill the field with content or add a valid reference:
```xml
<backstory ref="/world/characters/Other#v1.0">See Other's backstory</backstory>
```

### Reference to Non-Existent Card

```
Reference points to non-existent card: /world/characters/Missing
```

**Fix**: Either:
- Create the entity: `ske create /world/characters/Missing`
- Change to TODO ref: `ref="/todo/world/characters/Missing"`
- Remove the reference

### Multiple Passages Concluding Chapter

```
Multiple passages marked as concluding chapter in Chapter_Name
```

**Fix**: Only the last passage in a chapter should have `<concludes-chapter>true</concludes-chapter>`.

### Element Value Not Allowed

```
<field-name> must be one of: value1, value2, value3 (got "invalid")
```

**Fix**: Check the field's allowed values in the cardspec or Claude rules when editing the file.

## Common Warnings

### File Needs Snapshot

```
File has changed since version 1.0.0 - run `ske snapshot path/to/file.card -m "..."` to create new version
```

**Fix**: Run snapshot to archive the current version:
```bash
ske snapshot path/to/file.card -m "Why you made these changes" --no-feedback
```

### Outdated Version References

```
Reference uses outdated version: /world/characters/Hero#v1.0 (current: v2.1) at <relationships>
```

**Fix**: Run for upgrade guidance:
```bash
ske version-instruct path/to/file-with-reference.card
```

Then update reference version and prose based on changelog.

### TBD Values

```
Found 5 TBD values (3 high, 2 medium)
  High (showing 3 of 3):
    /stories/MyStory/story-info.card
    ...
```

**Fix**: Check priorities with `ske guide`, fill high-priority TBDs first.

### TODO References

```
Found 3 TODO references
  TODO: /todo/world/characters/NewCharacter
```

**Fix**: Create the referenced entity when ready:
```bash
ske create /world/characters/NewCharacter
```

Validation will auto-fix the reference path from `/todo/...` to the real path.

### Missing Chapter/Passage Numbers

```
Missing chapter numbers: 2, 4 in story MyStory
Missing passage numbers: 3, 5 in chapter Chapter_Name
```

**Fix**: Chapter and passage directories should be numbered sequentially (1_Name, 2_Name, etc.). Either rename to fill gaps or add the missing chapters/passages.

### Old File Names

```
Story metadata files should be named 'story-info.card'
```

**Fix**: Rename deprecated files:
- `story-meta.card` → `story-info.card`
- `outline-arc.card` → `outline-story-arc.card`
- `outline-acts.card` → `outline-story-acts.card`

## Workflow

1. Run `ske validate`
2. Fix errors first (blocks validation success)
3. Address high-priority warnings
4. Run `ske validate` again to confirm fixes
