---
name: photo-miniature-isometric-diptych
description: Transform a real photograph into a quiet 3:4 portrait editorial diptych with the source photograph in the upper half and its recognizable subject reinterpreted as a sparse isometric miniature paper model in the lower half. Use for 实景照片转微缩模型, 上实景下沙盘, 等距微缩景观, 纸面建筑模型, or photo-to-miniature editorial poster requests. Do not use for full-frame dioramas, cartoon miniatures, or unrelated 3D renders without a source photograph.
---

# Photo Miniature Isometric Diptych

Turn one supplied photograph into a single collectible editorial poster. Treat the source as the authority for identity, geometry, relationships, light, and palette; reinterpret only the lower panel.

## Read before working

- Read [prompt-compiler.md](references/prompt-compiler.md) before writing or submitting the production prompt.
- Read [quality-gate.md](references/quality-gate.md) before accepting or delivering an image.

## Modes

- **Analyze + generate — default:** inspect the source, make source-specific art-direction decisions, edit through `$legacy-imagegen`, inspect the result, and deliver the final raster.
- **Prompt only:** inspect the source when available and return the compiled production prompt plus avoid list; do not generate.
- **Analyze only:** return the subject hierarchy, source-derived palette, miniature translation plan, title, and layout risks.
- **Batch:** treat each photograph as an independent poster. Preserve every original, use distinct output names, inspect every output, and return a complete input/output manifest.

When the user supplies a photograph and asks for a transformation, use Analyze + generate without asking for choices that can be inferred from the image.

## Non-negotiable visual contract

### Canvas and split

- Use a **3:4 portrait canvas**.
- Split it into two horizontal regions of **exactly equal height**: upper 50% and lower 50%. The dividing axis is at 50% of canvas height.
- Do not let either panel dominate by area. Do not use an approximate 45/55 or 60/40 split, overlapping collage, tilted divider, inset photo, triptych, or border-heavy template.

### Upper half — photographic evidence

- Keep the original photograph recognizably intact: subject structure, viewpoint, proportions, pose, object count, spatial relations, material texture, natural light, and original color character.
- Permit only restrained high-end photographic grading associated with art magazines, independent publications, or exhibition photography.
- To fit the upper 3:2 panel, prefer a composition-aware crop or plausible extension of sky, ground, or peripheral environment. Never stretch, squash, bend, relocate, duplicate, or redesign the main subject.
- Do not place generated illustration, model textures, captions, or decorative graphics over story-critical photographic detail.

### Lower half — isometric miniature translation

- Extract the source's most identifiable **subject, silhouette, pose, and narrative relationship**. Preserve identity and relational logic rather than mechanically copying every texture.
- Rebuild the subject as one refined minimalist isometric miniature: a paper maquette, architectural model, or small landscape placed on a compact paper base.
- Use simplified volumes, crisp edges, clear hierarchy, fine ink lines, flat color planes, subtle shadows, and delicate paper grain.
- Surround the miniature with generous calm whitespace. Use base-edge cropping, scale contrast, and a restrained cast shadow to create delicacy, scale, and solitude.
- Add only a few subordinate elements when they clarify the story or scale. They must not become a second visual center.

### Palette, type, and tone

- Derive the entire lower palette from the source photograph. Select the most identifying colors, then reduce, purify, soften, and unify them into a limited palette.
- Preserve the source's warm/cool relationships and color personality. Separate volumes through value steps, neighboring hues, and small controlled color differences.
- Never impose a fashionable preset palette unrelated to the source.
- Derive one short English title from a visible theme, place, action, state, or mood. Do not invent a location, event, date, or proper noun not supported by the image or user context.
- Typography is thin, restrained, modern, and editorial. Add only a tiny number, short phrase, or micro-annotation when it improves rhythm. Align type with whitespace edges, the base, a horizontal axis, or the isometric geometry.
- Keep the overall mood quiet, poetic, precise, understated, and collectible.

## Workflow

1. Inspect the source with `view_image`. Record dimensions, orientation, main subject, recognizable silhouette, pose or structural axis, key relationships, natural palette, light direction, quiet regions, and any uncertain facts.
2. Choose the identity anchor: the one subject or relationship that must remain immediately recognizable in both halves.
3. Plan the exact 50/50 layout. Decide how the upper photograph fits without distortion and where the lower miniature, base, whitespace, shadow, and type will sit.
4. Reduce the source palette to 3–6 principal colors plus paper and ink neutrals. Do not name colors that are not visually supported.
5. Draft a short English title. Prefer 1–4 words. If the place is unknown, use a descriptive or emotional title rather than guessing.
6. Compile a source-specific prompt using [prompt-compiler.md](references/prompt-compiler.md). State the exact split and all source invariants more than once when needed for reliability.
7. Read and invoke `$legacy-imagegen` in edit mode with the real source image. Save to a new output path outside this skill folder; never overwrite the source.
8. Inspect the generated raster with `view_image` and apply [quality-gate.md](references/quality-gate.md). A valid file is not sufficient; visual compliance is required.
9. If a hard failure can be isolated, make one targeted regeneration that changes only the failed dimension. Recheck the entire contract afterward. Do not silently accept a structurally wrong split or unrecognizable subject.

## Output

Return:

- the final image inline and its absolute saved path;
- the selected English title;
- a concise note identifying the photographic anchor, miniature anchor, and source-derived palette;
- the exact prompt used;
- a brief QA result covering ratio, split, upper-photo fidelity, lower-model recognizability, palette, typography, and avoid-list compliance;
- for batch work, a verified input/output manifest for every source.

Do not claim pixel-exact preservation unless a deterministic compositing or comparison step actually established it. If the upper photograph changed materially after the allowed retry, report the limitation instead of calling the result complete.
