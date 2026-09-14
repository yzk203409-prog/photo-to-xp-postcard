---
name: photo-to-xp-postcard
description: Turn one or more uploaded photos into matching cream-paper postcard study sheets that pair a framed faithful scene with a watercolor-and-pencil reinterpretation, minimalist labels, and three scene-derived color swatches. Use when the user asks for the same postcard layout, a photo study card, a watercolor postcard treatment, or uploads images in an established postcard-study context. Generate every uploaded source as a separate image; never merge different source photos into one composition unless the user explicitly asks for a collage.
---

# Photo to XP Postcard

Create polished portrait-format postcard study sheets from the user's photos with image generation or image editing.

## Non-negotiable output rule

- Treat every uploaded source image as an independent subject and deliver one finished image per source.
- Never place two different source photos on the same canvas, even when they arrive in one message.
- Keep the outputs visually consistent as a series while adapting the palette and small labels to each source.
- If the user supplies only images in an established postcard-study conversation, proceed without asking them to restate the style.

## Visual system

Build each sheet on warm cream, lightly textured paper in a clean editorial composition:

- Use a portrait canvas, normally 3:4, with generous margins and quiet negative space.
- Place a faithful framed rendering of the source scene in the upper portion. Preserve the recognizable subject, viewpoint, proportions, lighting mood, and important details.
- Add a looser watercolor-and-pencil study of the same scene below and toward the right. Let edges fade naturally into the paper; include delicate graphite construction lines and restrained handwritten annotations.
- Place compact minimalist typography and short labels in the lower-left area. Prefer a scene-specific English title plus a tiny subtitle such as `POSTCARD STUDY`; keep wording sparse rather than filling the page with text.
- Add exactly three small circular color swatches sampled from the source image near the lower-left typography.
- Use muted ink, subtle shadows, fine framing lines, and an elegant travel-sketchbook mood. Avoid glossy poster styling, heavy borders, dense decoration, or noisy backgrounds.

## Generation workflow

1. Inspect every uploaded image and list the independent sources internally.
2. Generate each output separately. When several images are provided, make separate image-generation calls rather than a single multi-subject generation.
3. Include the corresponding source photo as the primary reference for that output. When helpful, also include `assets/photo-to-sketch-reference.jpg` to ground the photo-to-hand-drawn relationship; use it only as a style reference and exclude its phone interface or exact architecture.
4. State explicitly in the generation prompt that only one source scene may appear and that no collage, contact sheet, multi-panel comparison, or unrelated subject may be added.
5. Verify that the output contains one source scene, one watercolor interpretation of that same scene, three swatches, cream paper, and no other uploaded photo.
6. Return every generated image individually and preserve the input order.

For an explicit user change such as a different aspect ratio, language, title, or omission of text, keep the independent-per-source rule and adapt the remaining visual system.

## Prompt core

Use language equivalent to:

> Transform this single source photo into one refined portrait postcard study sheet on warm cream paper. Preserve the scene faithfully in a framed upper image. Below-right, reinterpret the same scene as an airy watercolor-and-pencil architectural or observational sketch with fading edges and subtle handwritten notes. In the lower-left, add restrained editorial typography, one short scene-specific title, the small label “POSTCARD STUDY,” and exactly three circular swatches sampled from the photo. Generous negative space, tactile paper grain, muted ink, delicate lines, cohesive handcrafted travel-journal aesthetic. This canvas must represent only this source photo; do not combine it with any other image and do not create a collage or contact sheet.
