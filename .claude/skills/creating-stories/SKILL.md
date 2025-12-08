---
name: creating-stories
description: Creating new stories and understanding how stories fit within a project. Use when starting a new narrative, setting up story structure (acts, arc), or understanding the relationship between project-level settings (meta.card, narrative-guide.card) and story-specific overrides.
---

# Creating Stories

## Command

```bash
ske create /stories/Story_Name
```

Creates: story-info.card, narrative-guide.card, writing-samples.card, intro.card, outline files.

## When to Create Story Elements

- **story-info.card**: Create a story when you have a clear protagonist and basic premise. You can start with minimal setup and expand the world-building as you develop the story.
- **narrative-guide.card**: Establish before touching setting, characters, or outlines. Create story-level overrides when tone or constraints diverge significantly from the default. Revisit whenever the core promise changes (new audience, tone shift, narration switch).
- **setting.card**: Draft after doing a brief review of meta.card and narrative-guide. Update when stakes or world logic shift materially.
- **story-arc.card**: Draft before writing detailed scenes. Revisit after major structural changes or playtest feedback.
- **story-acts.card**: Produce after finalizing the arc but before outlining scenes. Update when rearranging story structure or rebalancing pacing.
- **exposition-plan.card**: Create after you have story-info, setting, and a clear understanding of what information readers need. Should be created before or alongside writing the first passage.
- **writing-samples.card**: Produce samples after setting the narrative guide. Update whenever tone shifts or new POV styles appear.
- **meta.card**: Initialize when starting a project or new story arc. Update as soon as scope, POV characters, or production details change.

## Workflow Strategy

1. **Ask user first**: Story concept, POV character, genre/tone
2. **Fill story-info.card** - Use `ske instructions` for field guidance
3. **Fill outlines** (story-arc, story-acts) - Work through in reasoning, get user confirmation on act structure
4. **Create first chapter**: `ske create /stories/Story_Name/chapters/1_Title`

## When to Confirm with User

- Story title and concept
- POV character selection
- Act structure (number and purpose of acts)
- Major plot points

## When to Proceed Autonomously

- Detailed outline reasoning
- Passage-level scene descriptions
- Specific word choices
