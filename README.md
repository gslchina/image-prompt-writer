# image-prompt-writer

> Grok Skill for generating high-quality, detailed image prompts optimized for MiniMax image-01 and similar text-to-image models.

## Overview

This skill produces single-paragraph Chinese prompts (~1400–1600 characters) with rich visual detail. It is designed for consistent artistic portrait generation while maximizing variety through large reference libraries.

**Default locked elements:**
- Sexy dressed (revealing but fully clothed)
- Japanese-style high-definition natural light (golden soft light, sharp, no grain)
- Subject looking at the camera with a natural expression

Everything else (person, scene, outfit, pose, camera, style) is randomized on each “换” / “随便” / “继续”.

## Key Features

| Feature | Details |
|---------|---------|
| Prompt Length | ~1500 Chinese characters |
| Character Library | 100 templates (CN/JP/KR/Western, blendable) |
| Style Library | 60 high-def artistic styles |
| Scene Library | 200+ indoor & outdoor locations |
| Outfit Library | 200+ sexy dressed variations |
| Action Library | 100+ poses |
| Expression Library | 50+ natural expressions |
| Camera Library | 80+ positions & compositions |
| Real Names | Supported (e.g. 王楚然) |
| Multi-panel | 九宫格 / storyboard support |

## Usage

### Basic Commands
- `换` / `随便` / `继续` — Generate a completely new prompt with randomized person, scene, outfit, action, expression, camera angle, and style.
- `王楚然` — Force a specific person (uses real name + accurate visual traits).
- `九宫格` — Output a multi-panel grid prompt.

### Override Examples
- `换，韩国的` — Random Korean character
- `海边，黄昏` — Force seaside + golden hour
- `完全不穿` — Override to full nude (only when explicitly requested)

## Project Structure

```
image-prompt-writer/
├── SKILL.md                 # Core skill instructions
├── CHANGELOG.md             # Version history
├── README.md                # This file
├── evals/
│   ├── evals.json           # Test cases
│   └── triggers.json        # Trigger phrases
└── references/               # Large libraries
    ├── characters.md        # 100 character templates
    ├── styles.md            # 60 photography styles
    ├── scenes.md            # 200+ scenes
    ├── outfits.md           # 200+ outfits
    ├── actions.md           # 100+ poses
    ├── expressions.md       # 50+ expressions
    ├── cameras.md           # 80+ camera setups
    └── multi-panel.md       # Grid / storyboard rules
```

## Installation (for Grok)

1. Clone or download this repository.
2. Place the folder in your Grok skills directory (`.grok/skills/image-prompt-writer`).
3. The skill will automatically trigger on relevant prompts.

## License

Personal use. Optimized for Grok + MiniMax image generation workflows.
