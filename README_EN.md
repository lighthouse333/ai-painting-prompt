# AI Painting Prompt Generator

A Claude Code skill based on the *Parametric Description Template for Female Portraits*. Describe a character in natural language, and it generates a complete 28-dimension AI painting prompt as a formatted `.docx` file.

## Quick Start

1. Clone this repo
2. Open the project directory in Claude Code
3. Type `/ai-painting-prompt <character description>`

```
/ai-painting-prompt A 25-year-old woman with a cool, aloof elegance, long hair, simple office wear, sitting by a café window in autumn afternoon light
```

## Workflow

1. **Requirement Gathering** — Extract age, temperament, makeup, body type, outfit, scene, etc. from user input; ask about any missing details
2. **Trend Research** — When keywords like "latest" or "trending" appear, search for current trends (2026)
3. **28-Dimension Fill** — Populate every dimension per the template, no skipping
4. **Word Document Generation** — Produce a formatted `.docx` via python-docx
5. **Summary Output** — Display a character overview table and file path

## The 28 Dimensions

| # | Dimension | Details |
|---|-----------|---------|
| 1 | Basic Info | Age perception, identity, overall temperament, style keywords |
| 2 | Head & Face Shape | Head shape, face shape, facial proportions, contour, cheeks |
| 3 | Facial Features | Eyes (shape/lid/spacing/lashes/gaze), brows, nose, mouth, ears |
| 4 | Distinctive Features | Moles, freckles, dimples + S/A/B priority tiers |
| 5 | Skin | Skin tone, texture, realism requirements |
| 6 | Hair | Length, style, color, texture, parting, bangs, flyaways, accessories |
| 7 | Body Contour & Proportions | Silhouette, shoulder-hip ratio, torso/leg proportions, posture |
| 8 | Chest & Upper Body | Chest width/depth, side profile, presentation under clothing |
| 9 | Waist & Abdomen | Waist width, waist-hip lines, abdominal contour |
| 10 | Hips & Buttocks | Hip width, pelvic contour, gluteal contour, waist-hip transition |
| 11 | Thighs | Thickness, length, lines, transition to hips/knees |
| 12 | Calves | Length, contour, calf muscle, ankle definition |
| 13 | Leg Proportions | Thigh-calf ratio, leg-torso ratio, muscle visibility |
| 14 | Neck, Shoulders & Posture | Neck, collarbone, shoulders, shoulder line, back |
| 15 | Arms & Hands | Arm thickness, hand posture, anatomical accuracy |
| 16 | Clothing | Tops, bottoms, footwear, fit, color, fabric, pattern |
| 17 | Makeup | Base, eye makeup, blush, contour, lip, overall look |
| 18 | Accessories | Glasses, earrings, necklace, watch — minimalist principle |
| 19 | Expression & Mood | Eyes & brows, gaze, mouth corners, final emotion |
| 20 | Pose & Action | Head, body, shoulders, hands |
| 21 | Photography & Composition | Angle, lens, framing, camera height, composition, aspect ratio |
| 22 | Lighting | Source, direction, quality |
| 23 | Background & Environment | Scene, style, depth of field |
| 24 | Color & Image Quality | Color temperature, saturation, contrast, sharpness, style |
| 25 | Consistency Priority | S-tier (immutable) / A-tier (preserve) / B-tier (adaptable) |
| 26 | Strictly Forbidden | Face/body/makeup/clothing/expression/image prohibitions |
| 27 | Core Summary | A single continuous paragraph — ready-to-use positive prompt |
| 28 | Negative Constraints | Ready-to-use negative prompt |

## Core Principles

- **Photorealistic** — Real women as subjects; no over-beautification, no "AI face", no plastic skin
- **28-Dimension Coverage** — Every dimension must be filled; no skipping
- **S/A/B Priority** — Facial features (S) never altered; hair/skin/body (A) preserved as much as possible; clothing/scene (B) adaptable
- **Forbidden List** — Plastic skin, over-smoothing, anime-style, distorted anatomy always included
- **Timeliness** — Real-time trend search whenever "latest" or "trending" is mentioned

## File Structure

```
.
├── .claude/
│   └── commands/
│       └── ai-painting-prompt.md   # Claude Code slash command definition
├── CLAUDE.md                       # Project instructions (fallback)
├── 女性人物肖像参数化描写模板.md     # 28-dimension reference template (Chinese)
├── generate_prompt.py              # docx generation script (reference)
├── README.md                       # Documentation (Chinese)
├── README_EN.md                    # Documentation (English)
└── .gitignore
```

## Dependency

Python environment required for `.docx` generation:

```bash
pip install python-docx
```

## License

MIT
