# Aesthetic PPT Workflow

A Codex skill for making polished, editable PowerPoint decks through an aesthetic-learning workflow.

This skill is not just a PPT generator. Its core idea is that a good agent should learn the user's taste before producing the final deck:

1. **Outline first**: clarify story, page order, subtitles, body points, and visual intent before touching PPT.
2. **Aesthetic learning second**: create different preview directions, ask the user what they prefer, study user examples, and generate background imagery around that taste.
3. **Editable PPT third**: build the final `.pptx` with generated backgrounds plus editable text, labels, masks, frames, photos, diagrams, notes, and page numbers.

The goal is not to add more decoration. The goal is to help Codex learn visual judgment: how to read references, understand why a page feels beautiful, and turn that judgment into a usable presentation.

## What This Skill Is Good At

- Turning rough briefs into clear PPT outlines.
- Creating 3 visual preview directions before final production.
- Asking targeted style-preference questions instead of guessing blindly.
- Learning from reference images without copying them.
- Using image generation for atmosphere, structure, and background scenes.
- Using PPT tools for editable text, simple masks, labels, diagrams, and evidence placement.
- Re-composing text and diagrams around the image instead of merely replacing the wallpaper.
- Producing editable PowerPoint slides instead of flattened screenshots.
- Avoiding generic circular-arrow process diagrams and flat card grids.

## Why This Skill Is Different

Many PPT workflows can produce decent slides. This skill focuses on **learning taste**.

It treats every preview, user comment, and reference image as evidence:

- If the user likes one preview but dislikes another, Codex should ask what caused that reaction.
- If the user uploads examples, Codex should extract layout rules: text zones, color rhythm, image weight, curve logic, density, and restraint.
- If the deck needs generated imagery, Codex should use image generation to create background structure and mood.
- If the final file must be useful, Codex should use PowerPoint tooling to keep text, labels, masks, and diagrams editable.

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
|-- SKILL.md
|-- README.md
|-- agents/
|   `-- openai.yaml
|-- examples/
`-- references/
    `-- style.md
```

## Style Examples

The `examples/` folder is intentionally empty in the public repository.

Put your own style references there when using this skill locally:

- PPT decks whose visual style you want Codex to learn
- exported slide screenshots
- reference images for color, layout, typography, or atmosphere
- before/after slides that explain your taste

Then ask Codex to study them:

```text
Use $aesthetic-ppt-workflow. Study the files in examples/ and summarize what visual rules you should learn before creating my PPT.
```

Good examples help Codex learn:

- where text should sit
- how much visual density is acceptable
- what kind of background feels premium rather than noisy
- how imagegen backgrounds should leave quiet zones for editable PPT text
- what masks, labels, and simple shapes should be created with PPT tools

The default `.gitignore` avoids committing common private slide assets such as `.pptx`, `.pdf`, images, spreadsheets, and documents. This keeps the public repo clean while still letting each user keep their own local reference library.

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

### Step 2: Preview And Learn Preference

Ask Codex to generate or design multiple visual directions.

Example:

```text
Based on the outline, generate 3 full-deck visual preview collages. Each collage should include all slides in order, all thumbnails must be 16:9, and each direction should use a coherent visual system.
```

Then respond with your preference:

```text
I prefer version B's clean background and version C's page 4 flow. Version A feels too loud. Please learn from these two reference images: I like the pale text zones, curved visual path, and restrained accent color.
```

The skill tells Codex to learn:

- color pairing
- text placement
- quiet regions for readability
- path-like composition
- image-to-text balance
- information density
- what the user explicitly likes and dislikes

### Step 3: Editable PPT

After choosing a visual direction, ask Codex to create the final PPT.

Example:

```text
Use the selected preview direction. Build an editable 16:9 PPT. Use generated backgrounds as visual assets, but keep text, labels, diagrams, page numbers, and notes editable.
```

The final deck should use image generation and PPT tooling together:

- image generation creates background mood, spatial depth, covers, closing pages, and metaphor scenes
- PPT tooling creates editable titles, body text, masks, labels, diagrams, evidence-photo frames, footers, and speaker notes

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
