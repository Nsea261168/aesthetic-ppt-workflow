# Aesthetic PPT Workflow

A Codex skill for making polished, editable PowerPoint decks through a three-step workflow:

1. **Outline first**: clarify story, page order, subtitles, body points, and visual intent before touching PPT.
2. **Visual preview second**: study references, generate background directions, and compare page rhythm before committing to a style.
3. **Editable PPT third**: build the final `.pptx` with editable text, labels, frames, photos, diagrams, notes, and generated backgrounds.

The goal is not to add more decoration. The goal is to help Codex learn visual judgment: how to read references, understand why a page feels beautiful, and turn that judgment into a usable presentation.

## What This Skill Is Good At

- Turning rough briefs into clear PPT outlines.
- Creating 3 visual preview directions before final production.
- Learning from reference images without copying them.
- Using generated images as atmosphere, structure, or background.
- Re-composing text and diagrams around the image instead of merely replacing the wallpaper.
- Producing editable PowerPoint slides instead of flattened screenshots.
- Avoiding generic circular-arrow process diagrams and flat card grids.

## Install

Download this folder and place it inside your Codex skills directory:

```text
~/.codex/skills/aesthetic-ppt-workflow
```

On Windows, this is usually:

```text
C:\Users\<your-user-name>\.codex\skills\aesthetic-ppt-workflow
```

Then invoke it in Codex:

```text
Use $aesthetic-ppt-workflow to help me create a PPT from this brief.
```

## Folder Structure

```text
aesthetic-ppt-workflow/
├─ SKILL.md
├─ README.md
├─ agents/
│  └─ openai.yaml
└─ references/
   └─ style.md
```

## Recommended Workflow

### Step 1: Outline

Ask Codex to read your source material and create only the outline first.

Example:

```text
Use $aesthetic-ppt-workflow. Read my brief and create an 8-page PPT outline for a 3-minute presentation. Do not generate the PPT yet.
```

The outline should include:

- slide count and time allocation
- page order and narrative logic
- subtitle for each slide
- body points
- visual suggestion

### Step 2: Preview

Ask Codex to generate or design multiple visual directions.

Example:

```text
Based on the outline, generate 3 full-deck visual preview collages. Each collage should include all slides in order, all thumbnails must be 16:9, and each direction should use a coherent visual system.
```

Use your own reference images if you have them. The skill tells Codex to learn:

- color pairing
- text placement
- quiet regions for readability
- path-like composition
- image-to-text balance
- information density

### Step 3: Editable PPT

After choosing a visual direction, ask Codex to create the final PPT.

Example:

```text
Use the selected preview direction. Build an editable 16:9 PPT. Use generated backgrounds as visual assets, but keep text, labels, diagrams, page numbers, and notes editable.
```

## Design Philosophy

This skill assumes that beauty can be learned through careful observation.

A strong PPT page usually has:

- one dominant idea
- one clear reading path
- enough empty space for the eye to rest
- a restrained color system
- images that carry meaning, not decoration
- typography hierarchy that makes the page readable from a distance

For process and system pages, prefer natural or spatial paths:

- mountain ridge
- river curve
- road
- tree growth
- vortex
- light direction
- contour line

Avoid defaulting to circular-arrow flowcharts, evenly spaced cards, or generic node-link diagrams.

## Privacy

This public version intentionally removes personal background, campaign context, organization names, real identities, and private project details. It keeps only reusable workflow and aesthetic judgment rules.

When using this skill with your own materials, avoid committing private evidence images, internal documents, or generated decks unless you have permission to publish them.
