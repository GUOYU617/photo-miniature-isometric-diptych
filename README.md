# Photo Miniature Isometric Diptych

A Codex skill for transforming a real photograph into a quiet 3:4 portrait editorial diptych:

- upper half: source-faithful photography;
- lower half: a recognizable isometric miniature paper model;
- exact 1:1 vertical split;
- source-derived color palette, restrained typography, and editorial paper texture.

## Installation

Copy this repository into your Codex skills directory:

```text
%USERPROFILE%\.codex\skills\photo-miniature-isometric-diptych
```

The entry point is [`SKILL.md`](SKILL.md). Supporting prompt compilation and quality-control rules are stored in [`references/`](references/).

## Structure

```text
photo-miniature-isometric-diptych/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── prompt-compiler.md
    └── quality-gate.md
```
