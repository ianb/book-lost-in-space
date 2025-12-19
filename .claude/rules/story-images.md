---
paths: **/story-images.card
---

## `<cover-style>` (optional) [low priority]

**Purpose:** Optional style override for this story's cover

When empty, the story inherits the cover style from `/meta-images.card`. Only populate this if the story needs a different visual approach than the project default. Most stories should leave this empty for consistency.

**When creating:**
Leave empty unless this story requires a distinctly different visual style from the project. If overriding, describe the complete visual style as you would in meta-images.card. Partial overrides are not supported—if you override, provide the full style description.

**When editing:**
Consider whether this story truly needs a unique style. Overriding breaks visual consistency with other stories in the project. If you're overriding for good reason, ensure the style is fully described.

**Good examples:**
- 
- Bright, saturated colors with strong contrast.
Graphic novel style with bold outlines.
Dynamic action composition.
Hand-lettered typography.

## `<illustration-style>` (optional) [low priority]

**Purpose:** Optional style override for this story's illustrations (future feature)

Placeholder for illustration style override. Leave empty until illustration generation is implemented. When used, overrides the project-level illustration style for this story only.

**When creating:**
Leave empty for now. This field will be used when illustration generation is implemented.

## `<reasoning-cover>` (optional) [medium priority]

**Purpose:** Guided thinking for crafting the cover prompt

Before writing the cover prompt, consider what imagery would best represent this story. Think about:
- What visual moment or symbol captures the story's essence?
- What mood should the cover convey?
- What would intrigue a reader without spoiling the story?
- How does this relate to the project's visual style?

**When creating:**
Read the story-info for mood and story-goal. Review the outline if available. Consider what single image could represent the story's themes or central conflict. The cover should evoke the story's feeling, not depict a specific scene literally.

**When editing:**
Revisit reasoning when the story's direction changes significantly, or if the current cover doesn't resonate with the story's final form.

## `<cover-prompt>` (required) [high priority]

**Purpose:** Scene description for generating this story's cover image

Describes the scene, subject, or imagery for the story cover. This is a pure scene description—do NOT include style directions here. Style comes from cover-style (or meta-images.card if inheriting). The prompt should evoke the story's themes symbolically rather than depicting specific plot events.

**When creating:**
Describe imagery that captures the story's essence:
- Focus on mood, atmosphere, and symbolic elements
- Avoid literal depictions of plot events (no spoilers)
- Keep it evocative and suggestive rather than explicit
- Think about what would make a reader curious

The image generator will combine this with the style settings from cover-style or meta-images.card.

**When editing:**
After changing this, regenerate the cover with `ske gen image cover stories/{storySlug}`.

**Good examples:**
- A woman's silhouette against a rain-streaked window, city lights blurred beyond
- An old pocket watch lying open on autumn leaves, its hands stopped at midnight
- Two hands reaching toward each other across a gap, one in shadow, one in light
- A lighthouse beam cutting through fog, a small boat barely visible in the distance

**Bad examples (avoid):**
- A moody, atmospheric painting of a woman at a window *(includes style direction)*
- The detective discovering the victim's body in the library *(too literal/spoilery)*
- Something mysterious *(too vague)*
- Book cover with title "The Mystery" in gold letters *(includes typography)*
