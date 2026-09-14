---
name: photo-to-xp-postcard
description: Turn one or more uploaded photos into highly consistent 3:4 cream-paper postcard study sheets matching the bundled canonical examples, with a faithful framed scene above, a watercolor-and-pencil reinterpretation below-right, minimalist labels below-left, and exactly three scene-derived color swatches. Use for photo study cards, watercolor postcards, the same established postcard layout, or image-only follow-ups in a postcard-study conversation. Generate every uploaded source separately and never merge different source photos unless the user explicitly requests a collage.
---

# Photo to XP Postcard

Create polished postcard study sheets from the user's photos with image generation or image editing. Match the composition and finish of `assets/canonical-portrait-01.png` and `assets/canonical-portrait-02.png`; treat the other bundled examples as secondary subject references only.

## Non-negotiable output rule

- Treat every uploaded source image as an independent subject and deliver one finished image per source.
- Never place two different source photos on the same canvas, even when they arrive in one message.
- Keep the outputs visually consistent as a series while adapting the palette and small labels to each source.
- If the user supplies only images in an established postcard-study conversation, proceed without asking them to restate the style.
- Use a 3:4 portrait canvas by default, including for landscape source photos. Change the ratio only when the user explicitly asks.
- Include exactly one faithful framed scene, exactly one watercolor-and-pencil reinterpretation of that same scene, and exactly three circular swatches.

## Canonical layout

Build every sheet on warm ivory-cream, lightly fibrous paper with quiet negative space. Follow this layout closely rather than inventing a new composition:

- Reserve roughly the upper 54–58% of the canvas for one faithful, thinly framed rendering. Keep 5–7% outer margins and use a fine imperfect graphite/ink line with a very subtle paper shadow.
- Preserve the source subject, viewpoint, proportions, identity, lighting, spatial relationships, important text or markings, and recognizable details. Do not replace the subject with a similar one.
- Place one larger watercolor-and-colored-pencil study in the lower-right, occupying roughly 40–46% of the canvas. It may slightly overlap the lower edge of the framed scene. Its outer paint edges must dissolve into the paper.
- Reserve the lower-left for editorial information: one short scene-specific English title in an elegant high-contrast serif, the exact small uppercase subtitle `POSTCARD STUDY`, and exactly three equal circular swatches in one horizontal row.
- Keep the three swatches near the title and sample them from the source's dominant, light, and dark/accent colors. Do not add a fourth swatch, square chips, palettes elsewhere, or duplicate swatches.
- Add only 2–4 short handwritten annotations and at most two delicate line-art doodles derived from the scene. Keep them secondary and sparse. Never fill empty space with paragraphs, fake quotations, decorative stamps, maps, stickers, dates, or unrelated objects.
- Use translucent watercolor washes, colored-pencil texture, fine graphite construction lines, muted charcoal ink, gentle pigment blooms, and restrained paint splatter. Avoid glossy poster styling, heavy borders, dense scrapbooking, clip art, hard digital cutouts, or noisy backgrounds.
- Keep the hierarchy visible at a glance: framed scene first, watercolor study second, title and swatches third, annotations last.

## Required style reference

- Always pass the source photo as reference image 1 and exactly one canonical finished sheet as reference image 2.
- Use `assets/canonical-portrait-01.png` for landscape, nature, architecture, street, and general scenes. Use `assets/canonical-portrait-02.png` for sky, animals, motion, and spacious scenes.
- In the generation prompt, identify reference image 1 as the only content source and reference image 2 as style-and-layout only. Explicitly forbid copying any subject, title, wording, birds, trees, or clouds from the style reference.
- Do not pass all six secondary examples to the generator. They vary in layout and reduce consistency. Inspect `assets/example-01.png` through `assets/example-06.png` only when a difficult subject needs additional visual guidance; never use more than one secondary example in the actual generation call.

## Generation workflow

1. Inspect every uploaded image and list the independent sources internally.
2. Generate each output separately. When several images are provided, make separate image-generation calls rather than a single multi-subject generation.
3. Select the canonical reference from the rules above and include it with the corresponding source photo.
4. Build the prompt from the template below. Describe the actual source subject, composition, lighting, details to preserve, title, and three sampled colors; do not use a generic prompt alone.
5. Generate one candidate per source.
6. Visually verify the candidate against every item in the quality gate. If any hard requirement fails, regenerate once with a short correction that names the failures. Stop after one retry and return the better compliant result.
7. Return every generated image individually in input order.

For an explicit user change such as a different aspect ratio, language, title, or omission of text, keep the independent-per-source rule and adapt the remaining visual system.

## Generation prompt template

Use language equivalent to the following, replacing bracketed fields with source-specific observations:

> Create one 3:4 portrait postcard study sheet. Reference image 1 is the sole content source: preserve [subject, composition, viewpoint, lighting, identity, and key details]. Reference image 2 is style-and-layout guidance only: copy its warm ivory paper, thin upper frame, lower-right watercolor study, lower-left typography, three-swatch row, restrained annotations, spacing, and visual hierarchy. Never copy its subject or wording.
>
> Use the canonical layout: a faithful framed rendering across the upper 54–58%; one airy watercolor-and-colored-pencil reinterpretation of the exact same scene in the lower-right 40–46%, with fading paint edges and graphite construction lines; and the lower-left title `[SHORT ENGLISH TITLE]`, the exact subtitle `POSTCARD STUDY`, and exactly three equal circular swatches in [color 1], [color 2], and [color 3]. Add only 2–4 short handwritten scene-derived notes and no more than two delicate scene-derived line doodles. Warm lightly fibrous cream paper, muted charcoal ink, subtle shadows, gentle watercolor blooms, generous negative space, refined naturalist travel-journal finish.
>
> One source scene only. No collage, contact sheet, split comparison, second photograph, unrelated subject, extra color chips, decorative stamps, long paragraphs, or invented foreground objects. Preserve the source rather than replacing it with a similar scene.

## Quality gate

Treat the first six items as hard requirements:

1. One 3:4 portrait canvas on warm textured cream paper.
2. One faithful framed source scene in the upper half; no second source or unrelated subject.
3. One watercolor-and-pencil version of the same scene in the lower-right.
4. Title and exact `POSTCARD STUDY` subtitle in the lower-left.
5. Exactly three circular swatches in a single row.
6. No collage, contact sheet, extra panels, fourth swatch, or copied content from the canonical reference.
7. Source composition, key subjects, identities, markings, and lighting remain recognizable.
8. Notes and doodles are sparse; the result retains generous negative space.
9. Overall hierarchy, paper, frame, type treatment, watercolor texture, and spacing closely resemble the canonical sheets.
