---
name: image-prompt-writer
description: "Generate detailed, ready-to-use image prompts for MiniMax image-01 or similar models. Use when the user asks for image prompts, says '换', '随便', '继续', or provides short ideas for photos of women with specific styles, nudity levels, or scenes."
type: workflow
lifecycle: active
---

# Image Prompt Writer — Detailed MiniMax Prompts

Generate one continuous paragraph of rich image prompt text (target ~1500 Chinese characters) following strict structure. Output only the prompt text, no commentary.

## Core Rules

**Fixed (unless user overrides):**
- Sexy dressed (性感穿衣): revealing but clothed (low-cut, short, lace, silk, etc.), not fully nude unless explicitly requested.
- Japanese-style high-definition natural light: golden soft light, sharp clean, no film grain, no bloom.
- Looking at the camera with natural expression.
- High artistic quality.

**Changeable on "换" / "随便" / "继续":**
- Person (from character templates or blend)
- Scene, action, pose, angle, camera position, time of day, weather
- Photography style (from style pool)
- Foreground/background details

**Real people:** Allowed to use real names (e.g., 王楚然). Describe accurately + visible traits.

**Length:** 1400–1600 characters preferred. Single paragraph, flowing Chinese.

**Structure (must include):**
1. Anchor sentence (overall look + viewpoint)
2. Subject details (age, face, eyes, hair, skin, build, expression, pose frozen moment)
3. Outfit details (fabric, cut, how it sits)
4. Scene (place, time, weather, FG/MG/BG)
5. Composition & camera (shot size, height, position, lens feel)
6. Light & color (key light direction, shadow/highlight hue, exposure anchor, palette)
7. Style & medium finish

## Workflow

1. Check user input for overrides (nudity level, specific style, specific person).
2. If "换"/"随便"/"继续": pick new person from templates (or blend 2), new style from pool, new scene/action.
3. Write the single paragraph prompt following structure.
4. For multi-panel (九宫格 etc.): follow multi-panel rule in references.

## References

- Character templates: `references/characters.md` (100 templates, blendable)
- Style pool: `references/styles.md` (60 high-def artistic styles)
- Scene library: `references/scenes.md` (200+)
- Outfit library: `references/outfits.md` (200+ sexy dressed)
- Action/pose library: `references/actions.md` (100+)
- Expression library: `references/expressions.md` (50+)
- Camera & composition: `references/cameras.md` (80+)
- Multi-panel: `references/multi-panel.md`

On every "换"/"随便"/"继续": randomly select from each library above to ensure variety in person, style, scene, outfit, action, expression, camera.

When user specifies a real name, use it directly + matching visual traits from public knowledge.
