# image-prompt-writer

Grok Skill for generating detailed, ready-to-use image prompts for MiniMax image-01 or similar text-to-image models.

## Features

- **Target length**: ~1500 Chinese characters per prompt
- **Default style**: Sexy dressed (revealing but clothed), Japanese-style high-definition natural light, looking at the camera naturally
- **Large libraries** for maximum variety:
  - 100 character templates (Chinese, Japanese, Korean, Western female protagonists, blendable)
  - 60 high-definition artistic photography styles
  - 200+ scenes (indoor/outdoor)
  - 200+ sexy outfit variations
  - 100+ actions/poses
  - 50+ expressions
  - 80+ camera positions & compositions
- Supports real celebrity names (e.g. 王楚然)
- Multi-panel support (九宫格 etc.)

## Usage

When using with Grok:
- Say **“换”**, **“随便”**, or **“继续”** to generate a new random prompt with fresh person, scene, outfit, action, expression, camera, and style.
- Specify a person (e.g. “王楚然”) or scene to override.
- Say “九宫格” for multi-panel layouts.

## Structure

```
image-prompt-writer/
├── SKILL.md
├── CHANGELOG.md
├── README.md
├── evals/
│   ├── evals.json
│   └── triggers.json
└── references/
    ├── characters.md
    ├── styles.md
    ├── scenes.md
    ├── outfits.md
    ├── actions.md
    ├── expressions.md
    ├── cameras.md
    └── multi-panel.md
```

## License

For personal use with Grok / MiniMax image generation.
