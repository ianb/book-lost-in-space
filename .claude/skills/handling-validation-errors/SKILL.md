---
name: handling-validation-errors
description: Understanding and resolving ske validate errors and warnings
---

# Handling Validation Errors

## Common Errors

### Missing Changelog Entry

```
File has been modified but no unversioned changelog-entry found
```

**Fix**: Add `<changelog-entry>` without version attribute, or run:
```bash
ske snapshot path/to/file.card -m "Description of why"
```

### Required Field Empty

```
Required field <backstory> is empty
```

**Fix**: Fill the field or add valid reference:
```xml
<backstory ref="/world/characters/Other#v1.0">See Other's backstory</backstory>
```

### Reference to Non-Existent Entity

```
Reference points to non-existent entity: /world/characters/Missing
```

**Fix**: Either:
- Create the entity: `ske create /world/characters/Missing`
- Change to TODO ref: `ref="/todo/world/characters/Missing"`
- Remove the reference

### Multiple Passages with concludes-chapter=true

```
Multiple passages marked as concluding chapter
```

**Fix**: Only the last passage in a chapter should have `<concludes-chapter>true</concludes-chapter>`.

## Common Warnings

### Outdated Version References

```
Reference uses outdated version: /world/characters/Hero#v1.0 (current: v2.1)
```

**Fix**: Run for upgrade guidance:
```bash
ske version-instruct path/to/file-with-reference.card
```

Then update reference and prose based on changelog.

### TBD Values

```
Found 5 TBD values (3 high, 2 medium)
```

**Fix**: Check priorities with `ske guide`, fill high-priority TBDs first.

### TODO References

```
TODO reference: /todo/world/characters/NewCharacter
```

**Fix**: Create the referenced entity when ready:
```bash
ske create /todo/world/characters/NewCharacter
```

Validation will auto-fix the reference path.

## Workflow

1. Run `ske validate`
2. Fix errors first (blocks validation)
3. Address high-priority warnings
4. Run `ske validate` again to confirm
