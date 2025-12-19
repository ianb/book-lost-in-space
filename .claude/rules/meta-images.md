---
paths: meta-images.card
---

## `<cover-style>` (required) [high priority]

**Purpose:** Visual style description applied to all cover images

Describes the artistic style, color palette, mood, and visual approach for cover images. This style is combined with scene-specific prompts when generating covers. Focus on visual characteristics that create consistency across all covers.

**When creating:**
Describe the visual style in concrete terms. Include:
- **Color palette**: muted, vibrant, monochromatic, warm/cool tones
- **Artistic approach**: painterly, photorealistic, illustrated, minimalist
- **Mood/atmosphere**: moody, bright, mysterious, intimate
- **Typography style**: if covers include text, describe font style
- **Composition tendencies**: central focus, asymmetric, negative space

Keep it focused on visual characteristics, not story content. The same style should work for different scene subjects.

**When editing:**
Changes here affect all future cover generation. Consider regenerating reference images after significant style changes.

**Good examples:**
- Moody, atmospheric compositions with muted earth tones.
Painterly texture with visible brushstrokes.
Dark backgrounds with single illuminated focal element.
Bold serif typography in warm cream color.
- Clean minimalist design with generous negative space.
Limited palette: deep navy, gold accents, off-white.
Geometric shapes suggesting rather than depicting scenes.
Modern sans-serif typography.

**Bad examples (avoid):**
- A detective solving mysteries in a dark city *(describes story content, not visual style)*
- Nice and professional looking *(too vague)*

## `<cover-reference-prompt>` (required) [high priority]

**Purpose:** Scene description for generating the cover style reference image

Describes a scene or subject that will be generated as the style reference image. This image establishes the visual style that other covers will match. The prompt should be a pure scene description—style comes from cover-style, not here.

**When creating:**
Describe a scene or subject that:
- Represents the project's themes or mood abstractly
- Works well as a style exemplar (good composition, clear focal point)
- Is not a specific story scene (this is for style, not content)

Keep it simple and evocative. The reference image should demonstrate the style, not tell a specific story.

**When editing:**
After changing this, regenerate the reference image with `ske gen image reference`.

**Good examples:**
- A solitary figure standing at the edge of a forest at dusk
- An old wooden door with light streaming through the cracks
- A winding path through autumn mountains seen from above

**Bad examples (avoid):**
- A moody, atmospheric painting of a forest *(includes style direction)*
- Chapter 3 scene where Maria discovers the letter *(too specific/story-based)*

## `<project-cover-prompt>` (required) [medium priority]

**Purpose:** Scene description for the project's main cover image

Describes the scene or imagery for the project-level cover. This is the main cover representing the entire project, not individual stories. Style comes from cover-style; this is just the scene/subject.

**When creating:**
Describe imagery that represents the project as a whole:
- Captures the project's central themes or mood
- Works as a "series cover" if this project has multiple stories
- Is distinct from individual story covers

Focus on symbolic or thematic imagery rather than specific plot elements.

**When editing:**
After changing this, regenerate the project cover with `ske gen image project-cover`.

**Good examples:**
- Intertwining paths through mountain terrain, converging at a distant peak
- A collection of keys of different sizes and styles arranged in a circle
- City skyline at twilight with a single lit window

**Bad examples (avoid):**
- A beautiful watercolor of mountains *(includes style direction)*

## `<illustration-style>` (optional) [low priority]

**Purpose:** Visual style description for scene illustrations (future feature)

Placeholder for illustration style. Leave empty until illustration generation is implemented. When used, this describes the style for in-story scene illustrations, which may differ from cover style.

**When creating:**
Leave empty for now. This field will be used for scene illustrations within stories, which may have a different style than covers (e.g., more detailed, different color treatment).

## `<illustration-reference-prompt>` (optional) [low priority]

**Purpose:** Scene description for illustration style reference (future feature)

Placeholder for illustration reference prompt. Leave empty until illustration generation is implemented.

**When creating:**
Leave empty for now. When illustration generation is implemented, this will describe a scene to generate as the illustration style reference.
