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

Avoid specific or identifiable characters. If people appear, they should be anonymous silhouettes, distant figures, or shown from behind. The reference establishes style, not character identity.

**When creating:**
Describe a scene or subject that:
- Represents the project's themes or mood abstractly
- Works well as a style exemplar (good composition, clear focal point)
- Is not a specific story scene (this is for style, not content)
- Avoids identifiable people—use silhouettes, distant figures, or no people at all

Keep it simple and evocative. The reference image should demonstrate the style, not tell a specific story or establish character appearances.

**When editing:**
After changing this, regenerate the reference image with `ske gen image reference`.

**Good examples:**
- A silhouette standing at the edge of a forest at dusk
- An old wooden door with light streaming through the cracks
- A winding path through autumn mountains seen from above
- A distant figure walking along an empty beach at sunset

**Bad examples (avoid):**
- A moody, atmospheric painting of a forest *(includes style direction)*
- Chapter 3 scene where Maria discovers the letter *(too specific/story-based)*
- A young woman with red hair looking over her shoulder *(identifiable character)*

## `<project-cover-prompt>` (required) [medium priority]

**Purpose:** Scene description for the project's main cover image

Describes the scene or imagery for the project-level cover. This is the main cover representing the entire project, not individual stories. Style comes from cover-style; this is just the scene/subject.

**Character References**: If the cover includes characters, refer to them by name in the prompt text and add `<ref>` tags at the end to reference their character cards. The character's headshot image will be included and labeled with their name, so the prompt text must use the same name to connect the description to the reference image. Format: `<ref ref="/world/characters/Character_Name.card" />`

Characters without a headshot image will trigger a warning during generation.

**When creating:**
Describe imagery that represents the project as a whole:
- Captures the project's central themes or mood
- Works as a "series cover" if this project has multiple stories
- Is distinct from individual story covers
- If including characters, use ref tags to ensure visual consistency

Focus on symbolic or thematic imagery rather than specific plot elements.

**When editing:**
After changing this, regenerate the project cover with `ske gen image project-cover`.

**Good examples:**
- Intertwining paths through mountain terrain, converging at a distant peak
- A collection of keys of different sizes and styles arranged in a circle
- City skyline at twilight with a single lit window
- Marcus silhouetted against a sunset, overlooking the city below <ref ref="/world/characters/Marcus.card" />

**Bad examples (avoid):**
- A beautiful watercolor of mountains *(includes style direction)*

## `<illustration-style>` (optional) [medium priority]

**Purpose:** Visual style description for character portraits and illustrations

Describes the artistic style for character portraits (headshots and full-body images). This may differ from cover style—portraits often benefit from more detailed, realistic rendering while covers can be more atmospheric or symbolic.

**When creating:**
Describe the visual style for character portraits. Include:
- **Rendering approach**: realistic, stylized, painterly, graphic
- **Detail level**: highly detailed, moderately detailed, simplified
- **Color treatment**: natural colors, stylized palette, muted tones
- **Background**: should typically be neutral/simple for portraits
- **Lighting**: soft, dramatic, natural

If empty, falls back to cover-style.

**When editing:**
After changing this, regenerate the illustration reference with `ske gen image illustration-reference`, then regenerate character portraits.

**Good examples:**
- Realistic portrait style with soft natural lighting.
Detailed facial features and textures.
Muted, natural color palette.
Subtle painterly quality while maintaining likeness accuracy.
- Stylized illustration with clean lines and bold shapes.
Simplified but expressive features.
Limited color palette with strong contrast.

**Bad examples (avoid):**
- Nice looking portraits *(too vague)*

## `<illustration-reference-prompt>` (optional) [medium priority]

**Purpose:** Scene description for generating the illustration style reference image

Describes a scene that will establish the visual style for character portraits and illustrations. This should be a medium-complexity scene with multiple elements that demonstrates the desired rendering style—not a close-up portrait or a specific project character.

**When creating:**
Describe a scene that:
- Has medium complexity with multiple elements (figures, objects, environment)
- Avoids close-ups of faces—use mid-distance or environmental shots
- Shows the level of detail and rendering approach you want
- Is generic enough to work as a style reference (not specific characters)

The reference should demonstrate how the style handles various elements (people at a distance, objects, lighting, textures) rather than focusing on facial detail.

**When editing:**
After changing this, regenerate the reference with `ske gen image illustration-reference`.

**Good examples:**
- A market stall with a vendor arranging colorful fabrics, customers browsing nearby, morning light filtering through awnings
- A small workshop interior with tools on the wall, a figure working at a bench, afternoon light from a window
- Two travelers on a dusty road, one pointing toward a distant village, rolling hills in the background

**Bad examples (avoid):**
- A middle-aged merchant, neutral expression, looking slightly to the right *(close-up portrait)*
- Marcus the silk merchant in his shop *(too specific)*
- A painterly illustration of a market scene *(includes style)*
