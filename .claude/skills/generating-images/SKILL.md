---
name: generating-images
description: Generating cover images for stories and projects. Use when creating or updating cover art, setting up visual styles, or generating reference images.
---

# Generating Images

Ske uses AI image generation to create cover art for stories and projects. The system uses style reference images for visual consistency across all covers.

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

Good examples:
- "An old pocket watch lying open on autumn leaves, its hands stopped at midnight"
- "Two hands reaching toward each other across a gap, one in shadow, one in light"
- "A lighthouse beam cutting through fog, a small boat barely visible"

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
