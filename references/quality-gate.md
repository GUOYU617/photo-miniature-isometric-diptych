# Quality Gate

Inspect the final raster at full-frame scale and zoomed detail. Mark each item pass, fail, or uncertain.

## Hard failures

Any item below blocks acceptance:

- canvas is not portrait 3:4;
- the horizontal boundary is not exactly at mid-height or the regions are not visually 1:1;
- the upper half is missing, illustrated, heavily restyled, stretched, warped, or materially changes the main subject;
- the lower half is not isometric, does not read as a miniature/paper model, or cannot be linked to the source at a glance;
- subject count, pose, silhouette, key structure, or narrative relation changes in a way that changes identity;
- lower colors are dominated by an unrelated preset palette;
- the scene is crowded or contains a competing second focal point;
- title spelling is wrong, illegible, unsupported, or contains invented factual information;
- output contains a watermark, logo, obvious generation artifact, or unintended extra panel.

## Review dimensions

1. **Geometry:** 3:4 portrait; exact level 50/50 split; no overlap or inset template.
2. **Upper fidelity:** subject, viewpoint, proportions, pose, relationships, material, light, and color remain plausible and source-faithful.
3. **Miniature identity:** the lower subject is immediately recognizable through silhouette, pose, massing, or relationship.
4. **Isometric model language:** coherent isometric projection, simplified volumes, paper base, fine linework, flat planes, restrained shadow, subtle paper grain.
5. **Whitespace and hierarchy:** generous lower whitespace, one clear center, minimal support elements, calm scale cues.
6. **Palette:** limited and visibly derived from the upper image; warm/cool character preserved; no arbitrary accent color.
7. **Typography:** short English title, thin editorial treatment, exact spelling, quiet placement, no factual invention.
8. **Tone and exclusions:** quiet, poetic, restrained, refined; no cartoon, glossy plastic 3D, high-saturation clash, e-commerce, clutter, or generic-template look.

## Correction policy

When only one dimension fails, regenerate with a narrow instruction such as:

```text
Change only [failed dimension]. Preserve the source photograph, exact 3:4 canvas, exact 50/50 split, miniature identity, palette, title, and every passing element unchanged.
```

After correction, reassess all eight dimensions because image edits can disturb previously correct features. If a hard failure remains after the allowed retry, report it plainly and do not label the image verified.
