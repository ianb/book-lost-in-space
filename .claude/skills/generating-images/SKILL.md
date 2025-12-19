---
name: generating-images
description: Generating images for stories, projects, and characters. Use when creating cover art, character portraits, setting up visual styles, or generating reference images.
---

# Generating Images

Ske uses AI image generation to create cover art for stories and projects, and portraits for characters. The system uses reference images for visual consistency.

## Card Structure

### Project Level: `/meta-images.card`

Defines the visual style for the entire project:

```xml
<meta-images version="1.0.0">
  <cover-style>
    Moody, atmospheric compositions with muted earth tones.
    Painterly texture with visible brushstrokes.
    Dark backgrounds with single illuminated focal element.
  </cover-style>
  <cover-reference-prompt>
    A solitary figure standing at the edge of a forest at dusk
  </cover-reference-prompt>
  <project-cover-prompt>
    Intertwining paths through mountain terrain, converging at a distant peak
  </project-cover-prompt>
</meta-images>
```

### Story Level: `/stories/{Story}/story-images.card`

Auto-created when a story is created. Contains story-specific cover prompts:

```xml
<story-images version="1.0.0">
  <cover-style />  <!-- Empty = inherit from meta-images -->
  <cover-prompt>
    A woman's silhouette against a rain-streaked window, city lights blurred beyond
  </cover-prompt>
</story-images>
```

## Key Principle: Separate Style from Scene

**Prompts are pure scene descriptions.** Style is applied separately.

- **cover-style**: Visual characteristics (colors, texture, mood, composition)
- **cover-prompt / cover-reference-prompt / project-cover-prompt**: Scene/subject description only

Bad prompt (includes style):
> A moody, atmospheric painting of a woman at a window

Good prompt (scene only):
> A woman's silhouette against a rain-streaked window, city lights blurred beyond

## Commands

```bash
# 1. Generate the style reference image first
ske gen image reference

# 2. Generate the project cover
ske gen image project-cover

# 3. Generate story covers (uses reference for style matching)
ske gen image cover                    # All stories
ske gen image cover stories/My_Story   # Specific story
ske gen image cover --force            # Regenerate existing
```

## Generated Files

| Command | Output File |
|---------|-------------|
| `ske gen image reference` | `/images/cover-reference.png` |
| `ske gen image project-cover` | `/images/cover.png` |
| `ske gen image cover` | `/stories/{Story}/images/cover.png` |

## Workflow

### Setting Up Project Images

1. **Fill meta-images.card** with `ske create /meta-images.card`:
   - Write cover-style describing the visual approach
   - Write cover-reference-prompt (a scene that exemplifies the style)
   - Write project-cover-prompt (symbolic imagery for the project)

2. **Generate the reference image**:
   ```bash
   ske gen image reference
   ```
   This creates `/images/cover-reference.png` which establishes the visual style.

3. **Generate project cover**:
   ```bash
   ske gen image project-cover
   ```

### Creating Story Covers

1. **Fill story-images.card** (created automatically with the story):
   - Leave cover-style empty to inherit project style
   - Write cover-prompt describing evocative imagery for the story

2. **Generate the cover**:
   ```bash
   ske gen image cover stories/My_Story
   ```
   If a reference image exists, it's used to match the style.

## Style Inheritance

Stories inherit cover-style from meta-images.card by default. To override:

```xml
<story-images version="1.0.0">
  <cover-style>
    Bright, saturated colors with strong contrast.
    Graphic novel style with bold outlines.
  </cover-style>
  <cover-prompt>A hero leaping between rooftops at sunset</cover-prompt>
</story-images>
```

Only override when a story needs a distinctly different visual approach.

## Writing Good Prompts

### Cover Style (meta-images.card)

Describe visual characteristics:
- Color palette: muted, vibrant, monochromatic, warm/cool
- Artistic approach: painterly, photorealistic, minimalist
- Mood/atmosphere: moody, bright, mysterious
- Composition: central focus, asymmetric, negative space

### Cover Prompts

Describe evocative imagery:
- Focus on mood and symbolism, not literal plot events
- Avoid spoilers - suggest rather than depict
- Think about what would intrigue a reader
- Keep it simple and evocative

**Character References**: If the cover includes a character, add `<ref>` tags at the end:
```xml
A woman standing at the edge of a cliff, wind in her hair <ref ref="/world/characters/Elena.card" />
```

The character's headshot image will be included in the generation prompt to ensure accurate depiction. Characters without headshots will trigger a warning.

Good examples:
- "An old pocket watch lying open on autumn leaves, its hands stopped at midnight"
- "Two hands reaching toward each other across a gap, one in shadow, one in light"
- "A lighthouse beam cutting through fog, a small boat barely visible"
- `A man silhouetted against a stormy sky <ref ref="/world/characters/Marcus.card" />`

Bad examples:
- "The detective discovering the body in the library" (too literal/spoilery)
- "Something mysterious" (too vague)
- "A beautiful watercolor painting of..." (includes style in prompt)

## Regenerating Images

Use `--force` to regenerate existing images:

```bash
ske gen image reference --force
ske gen image project-cover --force
ske gen image cover --force
```

After changing cover-style or cover-reference-prompt in meta-images.card, regenerate the reference image first, then regenerate covers to apply the new style.

---

## Character Portraits

Generate portrait images for characters based on their physical-description and portrait-prompt. Portraits use the **illustration style** (distinct from cover style) for more detailed, realistic character rendering.

### Project Setup: Illustration Style

In `/meta-images.card`, add illustration style fields:

```xml
<meta-images version="1.0.0">
  <!-- Cover fields... -->

  <illustration-style>
    Realistic portrait style with soft natural lighting.
    Detailed facial features and textures.
    Muted, natural color palette.
    Subtle painterly quality while maintaining likeness accuracy.
  </illustration-style>
  <illustration-reference-prompt>
    A middle-aged merchant in simple period clothing, neutral expression, looking slightly to the right
  </illustration-reference-prompt>
</meta-images>
```

### Character Card Fields

Added to `/world/characters/{Name}.card`:

```xml
<character version="1.0.0" name="Marcus">
  <!-- ... other fields ... -->
  <physical-description>
    5'10", medium build with some belly, brown skin, black hair (short, starting to thin at the crown), brown eyes, rounded face with a broad nose. Appears late 20s. Hands are calloused from dock work.
  </physical-description>
  <headshot-prompt>
    A man in his late 20s with brown skin, a rounded face, and a broad nose. Short black hair, starting to thin at the crown. Brown eyes with a calm, steady gaze. Neutral, relaxed expression. Dark wool tunic with a linen collar visible at the neckline.
  </headshot-prompt>
  <full-body-prompt>
    Man in his late 20s with a calm expression. Medium build with some belly. Dark wool tunic over a linen shirt, leather belt with a small pouch, practical boots worn from use. Standing in a relaxed but attentive pose, weight slightly on one foot, hands loosely at sides.
  </full-body-prompt>
</character>
```

**headshot-prompt**: Highly detailed, comprehensive description of face, hair, expression, and upper clothing.

**full-body-prompt**: Very detailed for body/outfit, but only brief face description (headshot reference handles facial accuracy).

### Portrait Commands

```bash
# 1. Generate the illustration style reference first
ske gen image illustration-reference

# 2. Generate headshots (shoulders up)
ske gen image headshot                              # All characters
ske gen image headshot world/characters/Marcus.card # Specific character
ske gen image headshot --force                      # Regenerate existing

# 3. Generate full body portraits (uses headshot as reference)
ske gen image portrait                              # All characters
ske gen image portrait world/characters/Marcus.card # Specific character
ske gen image portrait --force                      # Regenerate existing
```

### Generated Files

| Command | Output File |
|---------|-------------|
| `ske gen image illustration-reference` | `/images/illustration-reference.png` |
| `ske gen image headshot` | `/world/characters/images/{Name}/headshot.png` |
| `ske gen image portrait` | `/world/characters/images/{Name}/full-body.png` |

### Character Portrait Workflow

1. **Set up illustration style** in meta-images.card (illustration-style and illustration-reference-prompt)

2. **Generate illustration reference**:
   ```bash
   ske gen image illustration-reference
   ```
   Creates `/images/illustration-reference.png` which establishes the portrait style.

3. **Generate headshot**:
   ```bash
   ske gen image headshot world/characters/Marcus.card
   ```
   Creates a shoulders-up portrait using the illustration reference for style. Character's name displayed at the bottom.

4. **Generate full body portrait**:
   ```bash
   ske gen image portrait world/characters/Marcus.card
   ```
   Uses both the illustration reference (for style) and the headshot (for facial consistency). Shows full body in a standing pose with name at the bottom.

### Writing Portrait Prompts

**headshot-prompt** - Highly detailed, comprehensive description:
- Face: Skin tone, facial structure (round, angular, etc.), distinctive features
- Eyes: Color, shape, expression
- Hair: Color, length, style, texture
- Age appearance: How old they look
- Expression: Neutral and relaxed (this is a reference portrait)
- Upper clothing: What's visible at collar/neckline/shoulders
- Accessories at head/neck level

**full-body-prompt** - Detailed body, brief face:
- Brief general face description (age, expression - headshot handles details)
- Complete outfit in detail
- Body type and build
- Stance and posture
- Hand positions and body language

Good headshot example:
> A man in his late 20s with brown skin, a rounded face, and a broad nose. Short black hair, starting to thin at the crown. Brown eyes with a calm, steady gaze. Neutral, relaxed expression. Dark wool tunic with a linen collar visible at the neckline.

Good full-body example:
> Man in his late 20s with a calm expression. Medium build with some belly. Dark wool tunic over a linen shirt, leather belt with a small pouch, practical boots worn from use. Standing in a relaxed but attentive pose, weight slightly on one foot, hands loosely at sides.

### Style Inheritance

Portraits use `illustration-style` from meta-images.card. If not set, falls back to `cover-style`.
