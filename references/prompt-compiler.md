# Prompt Compiler

Convert the visual analysis into one source-specific production prompt. Keep the prompt concrete; replace bracketed fields rather than leaving generic options.

## Required prompt order

```text
Use case: photo-to-miniature-isometric-editorial-diptych
Asset type: finished 3:4 portrait editorial poster
Input photograph: [identify the supplied image and its role as the sole factual and color source]

Primary request:
Create one unified 3:4 portrait poster divided horizontally into two regions of exactly equal height. The upper region occupies y=0–50%; the lower region occupies y=50–100%. Keep the dividing axis level and exact.

Upper 50% — preserved photograph:
[Name the subject, viewpoint, silhouette, pose, object count, relationships, materials, light direction, and colors that must remain unchanged.] Retain realistic texture, natural light, and the source's color atmosphere. Apply only restrained art-magazine or exhibition-photography grading. Fit the panel by [composition-aware crop / plausible extension of sky, ground, or peripheral environment]. Do not stretch, distort, duplicate, relocate, redesign, or illustrate the main subject.

Lower 50% — isometric miniature:
Translate [identity anchor] and [narrative relationship] into one refined minimalist isometric paper model or architectural maquette. Preserve [recognizable silhouette/pose/relationship], while simplifying detail into clean volumes, crisp edges, fine ink lines, flat color planes, subtle shadow, and delicate paper grain. Place it on [small paper base or terrain cut] with generous whitespace. Use only [few subordinate scale cues]; no second focal point.

Palette:
Extract all colors from the source photograph: [3–6 source-derived colors]. Preserve [warm/cool relationship]. Reduce noise and separate volumes with value steps and neighboring hues. Do not introduce an unrelated preset palette.

Typography:
Set the exact English title "[TITLE]" in thin restrained modern editorial type. Place it [specific quiet edge/base/axis location]. Optional microtext: "[exact text or none]". Keep type secondary to the image and spell all text exactly.

Mood and finish:
Quiet, poetic, restrained, precise, collectible independent-publication design; minimalist isometric illustration, miniature landscape, paper maquette, subtle tactile print finish.

Hard constraints:
3:4 portrait; exact 50/50 horizontal split; one photographic upper panel; one illustrated lower panel; upper subject fidelity; lower subject recognizability; source-derived limited palette; large lower whitespace; one visual center.

Avoid:
cartoon styling, cute toy proportions, glossy plastic CGI, high-saturation color clash, unrelated fixed palette, crowded scenery, second focal point, e-commerce render, generic template, dramatic cinematic VFX, heavy vintage yellowing, thick decorative border, approximate unequal split, diagonal division, overlapping collage, duplicated subject, warped photo, altered pose, invented architecture, invented place name, illegible or misspelled text, watermark, logo.
```

## Source-specific decisions

- **People or animals:** identity may depend on pose, direction of gaze, clothing silhouette, carried object, and interpersonal distance. Do not simplify these away.
- **Architecture:** preserve roofline, openings, massing, facade rhythm, and relation to terrain. Simplify surface clutter before structural features.
- **Landscape:** preserve the horizon, terrain profile, water/road path, vegetation masses, and scale cue that makes the place recognizable.
- **Vehicles or objects:** preserve proportion, orientation, defining profile, and interaction with the site; avoid turning them into generic toys.
- **Unknown text or signage:** do not reconstruct unreadable content. Omit it or reduce it to non-semantic marks.

## Title rule

Use evidence in this priority order:

1. user-provided title or place name;
2. clearly readable place or activity in the source;
3. visible subject and action;
4. a restrained mood title.

Keep the title short, natural, and exact. Never guess geography or events.
