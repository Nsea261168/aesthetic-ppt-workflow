---
name: aesthetic-ppt-workflow
description: Create polished presentation workflows that learn the user's visual taste through outline planning, multiple style preview collages, preference questions, reference-image analysis, AI-generated backgrounds, and editable PPT production. Use when building or revising slide decks from briefs, evidence images, user examples, imagegen backgrounds, or when the user wants a presentation that matches their content and aesthetic instead of a generic template.
---

# Aesthetic PPT Workflow

## Core Rule

Build PPTs in three stages. Do not skip stages unless the user explicitly asks.

1. Plan the story and slide outline.
2. Learn the user's aesthetic through references, preview variants, and preference questions.
3. Build an editable PowerPoint deck with generated backgrounds, real text, diagrams, masks, images, and notes.

Do not produce a rushed PPT when visual assets cannot be accessed or saved. Stop and discuss the blocked step with the user.

## Stage 1: Outline

Read the user's brief, source documents, required audience, speech duration, evidence images, and reference images.

Output only the deck outline unless the user asks to continue:

- slide count and speech duration
- page order and narrative logic
- each slide's subtitle
- body points
- visual suggestion

Do not generate a PPT file during this stage.

## Stage 2: Aesthetic Learning And Visual Preview

Use image generation when the task needs visual style exploration, generated backgrounds, hero scenes, or full-deck preview collages.

For PPT preview collages:

- generate 3 visually distinct directions, not just color swaps
- include every slide in correct order
- keep each thumbnail 16:9
- keep one coherent visual system inside each direction
- make the preview readable enough to compare hierarchy, rhythm, and mood

After showing previews, ask the user what they prefer before producing the final PPT. Ask about concrete visual traits:

- which direction feels closest to the desired mood
- which pages feel too dense, cheap, flat, loud, or restrained
- which reference examples should be learned from
- what should be preserved, softened, enlarged, simplified, or made more dramatic

Study user-provided references as evidence of taste. Learn their composition logic instead of copying surface decoration:

- where text is allowed to land
- how color contrast creates hierarchy
- how images fade into quiet reading zones
- how paths, curves, light, and spatial depth guide the eye
- how dense information is reduced into one clear visual argument
- how image areas and plain color areas cooperate
- when a page needs a quiet reading zone instead of more decoration

After the user chooses a direction, generate or select key backgrounds. Save project-bound generated images into the workspace, preferably:

```text
assets/imagegen/
```

If the image-generation tool does not expose a local file path, ask the user to manually save or download the generated images into the workspace before building the PPT. Do not substitute simple vectors or generic template graphics without confirmation.

The user's feedback is part of the work product. Carry it forward as a style brief for the final deck.

## Stage 3: Editable PPT

Use a PowerPoint creation or editing tool for the final `.pptx`. The final deck must use editable PowerPoint objects for:

- titles and body text
- labels and diagram nodes
- simple masks, frames, and translucent text carriers
- evidence photos
- page numbers and footers
- speaker notes

Generated images may be used as backgrounds or main visual assets, but do not flatten an entire slide into a bitmap.

After placing a background, re-compose the slide around that image. Do not merely swap a new background behind old coordinates.

Use generated imagery for atmosphere, spatial structure, and emotional tone. Use editable PPT objects for clarity, hierarchy, and iteration.

## Asset Handling

Treat images by role:

- `evidence-*`: proof images from the user's real work. Insert them to support claims.
- `ref-*`: aesthetic reference images. Learn color, rhythm, layout, and path logic; do not copy blindly.
- `bg-*` or `assets/imagegen/*`: generated or chosen PPT backgrounds.

Rename messy assets when useful. Preserve originals unless the user asks otherwise.

## Visual Guidance

For detailed layout and visual rules, read `references/style.md` before making or revising a deck.

Key defaults:

- fresh editorial style with natural-tech tension
- white or light-gray base, deep ink text, one warm accent, one cool accent
- large decisive headings, restrained support text
- background images remain visible and meaningful
- no cheap circular-arrow flowcharts
- use mountain, river, road, tree, vortex, light, contour, and growth paths for information flow
- evidence images are proof, not decoration
- prefer user-confirmed taste over preset style rules

## QA

Render every final slide before delivery. Inspect the full-size images for:

- text overflow or cramped typography
- background fighting the text
- labels detached from the visual path
- evidence images used as clutter
- page numbers and footers becoming unreadable
- generated backgrounds being over-covered by panels

If a user manually improves the deck, inspect the revised PPT visually and update the skill with durable layout lessons when asked.
