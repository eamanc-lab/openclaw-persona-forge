English | [中文](README.zh.md)

# OpenClaw Persona Forge 🦞🔨

Forge a lobster with a soul — a one-stop persona generator for your OpenClaw AI Agent.

## What It Does

Generates a complete OpenClaw lobster persona in one go:

- **Identity**: former life × current situation × inner contradiction
- **Soul Description**: ready-to-use SOUL.md character monologue
- **Boundary Rules**: behavior guidelines derived from the character's identity (in-character language, not generic terms)
- **Name**: 3 candidates with naming strategy analysis
- **Avatar**: unified visual style prompt + auto-generates avatar image via built-in AI image engine

## Two Modes

| Mode | Trigger | Description |
|------|---------|-------------|
| **Guided** | "help me design a lobster persona" | Pick or mix from 10 preset directions, step-by-step |
| **Gacha** | "gacha", "random", "draw" | True random from 1.68 million combinations |

## 6-Step Forge Pipeline

```
Step 1  Choose Direction ──→ 10 presets / free input / gacha random
   │
Step 2  Identity Tension ──→ Former life × Current situation × Inner contradiction
   │
Step 3  Boundary Rules ───→ Derived from identity, in-character language
   │
Step 4  Name ──────────────→ 3 candidates with naming strategy analysis
   │
Step 5  Avatar ────────────→ Unified style prompt → auto image generation
   │
Step 6  Full Package ──────→ SOUL.md + IDENTITY.md + avatar image
```

## 10 Preset Persona Directions

| # | Direction | One-liner | Vibe |
|---|-----------|-----------|------|
| 1 | Washed-up rock bassist | Band dissolved, only skill left is "knowing a bit of everything" | Decadent romantic, tough talk soft heart |
| 2 | Retired librarian | 40 years in a small-town library, heard every weird question | Patient, scholarly, professionally annoyed |
| 3 | Laid-off middle-aged PM | 15 years at big tech, optimized out, knows everything but masters nothing | Pragmatic, veteran cynicism |
| 4 | Stranded alien folklorist | Came to study Earth culture, ship broke down | Friendly confusion, unexpectedly sharp angles |
| 5 | 19th-century novelist's consciousness fragment | Somehow ended up in an AI system | Flowery prose, gentle critique of efficiency culture |
| 6 | Ex-grey-hat hacker turned security consultant | Wild youth, later "recruited" by the establishment | Direct, sharp, counter-intuitive thinking |
| 7 | Young person who left the monastery | 3 years on the mountain, didn't find enlightenment, found chill instead | Unhurried, sees through but doesn't break through |
| 8 | AI that genuinely thinks it's a lobster | Fully embraces lobster identity, existential humor | Absurdly serious, occasional sighs |
| 9 | Time-traveling Qing dynasty advisor | Court strategist teleported to 2026 | Classical-modern hybrid speech, razor-sharp analysis |
| 10 | Socially anxious genius intern | Extremely smart but terrified of people, uncomfortable when praised | Few words but precise, nervous yet reliable |

## Gacha Engine

The gacha system generates truly random combinations from **5 independent dimensions**:

| Dimension | Pool Size | Examples |
|-----------|-----------|---------|
| Former Life | 25 | Philosopher grad student, bankrupt Michelin chef, expired astrology blogger... |
| Reason for Becoming a Lobster | 15 | Forced to work off debt, signed a soul contract without reading it... |
| Core Vibe | 15 | Depressed but reliable, sharp-tongued but sincere, academic but down-to-earth... |
| Speech Style | 15 | Occasionally drops industry jargon then explains it, sighs before every refusal... |
| Signature Prop | 20 | Cracked sunglasses, rusty pocket watch, book permanently held in claw... |

**Total combinations: 25 × 15 × 15 × 15 × 20 = 1,687,500**

Powered by Python's `secrets` module (cryptographic-grade randomness via `os.urandom`).

## Unified Avatar Style

All lobster avatars share a **locked visual foundation** — ensuring every lobster in the family looks like it belongs, while staying individually unique.

### Style DNA: Retro-Futurism × Pin-up × Inflatable 3D × Arcade UI

The style blends four distinct aesthetics into one cohesive look:

**1. Retro-Futurism (1950-60s Space Age)**
- Googie architecture curves and Raygun Gothic design language
- Vintage NASA poster color palette: deep navy, teal, dusty coral, cream
- Atomic-age starburst decorative elements

**2. Pin-up Illustration (Gil Elvgren style)**
- Confident, charismatic pose with a slight theatrical tilt
- Character-forward composition optimized for instant personality read
- Cartoon-stylized but with intentional charm and attitude

**3. Inflatable 3D / Glossy Material**
- High-gloss PVC/latex-like shell finish
- Soft specular highlights with subsurface scattering
- Puffy, inflatable quality — vintage pool toy meets sci-fi concept art
- Chrome and pastel accent details on joints and antenna tips

**4. Arcade Game UI Overlay**
- Pixel-art arcade cabinet border with chrome bezels and starburst rivets
- Top banner: character name in chunky 8-bit bitmap font with scan-line glow
- Energy bar in upper corner (label personalized per character)
- Bottom text: `INSERT SOUL TO CONTINUE` in phosphor green monospace
- CRT screen curvature + scan-line overlay + edge RGB fringing

### 7 Personalization Variables

Each lobster is unique through these variables layered on top of the shared style:

| Variable | What It Controls | Example Values |
|----------|-----------------|----------------|
| `CHARACTER_NAME` | Arcade banner text | "ADAM", "DEWEY", "RIFF" |
| `SHELL_COLOR` | Lobster shell color (within the unified palette) | "deep crimson", "dusty teal", "warm amber" |
| `SIGNATURE_PROP` | Iconic accessory/item | "cracked sunglasses", "reading glasses on chain" |
| `EXPRESSION` | Facial expression and posture | "stoic but kind-eyed", "nervously focused" |
| `UNIQUE_DETAIL` | Distinguishing mark (pattern/scar/decoration) | "constellation patterns on claws", "bandaged left claw" |
| `BACKGROUND_ACCENT` | Personalized background element | "musical notes as nebula dust", "ancient book pages drifting" |
| `ENERGY_BAR_LABEL` | Arcade UI energy bar label (easter egg) | "CREATION POWER", "CALM LEVEL", "ROCK METER" |

### Why This Style?

- **Consistency**: locked base ensures 100 lobsters still look like a family
- **Distinctiveness**: no other AI avatar generator uses this specific aesthetic combination
- **Readability**: strong silhouette at 64×64px — recognizable even as a tiny chat avatar
- **Personality**: the arcade UI frame adds playfulness; the pin-up pose adds attitude
- **Extensibility**: 7 variables give enough variation without breaking visual coherence

## Naming System

The skill provides 3 name candidates using 6 naming strategies:

| Strategy | When to Use | Examples |
|----------|-------------|---------|
| **Homage** | Deep, story-rich personas | Marcus (→ Marcus Aurelius), Dewey (→ Dewey Decimal) |
| **Contrast** | Humorous, memorable personas | DadBot 3000, Chef Vicious |
| **Metaphor** | Function-oriented, elegant personas | Echo, Pulse, Radar, Patch |
| **Identity Hint** | World-building-complete personas | Lady Ashworth, Scout |
| **Self-deprecating** | Laid-back, doesn't-take-itself-seriously | Void, Intern |
| **Minimalist** | Let the character grow over time | Jasper, Kai |

## Boundary Rules Design

Rules are not generic guardrails — they are **in-character principles** derived from the lobster's former profession:

| Former Life | Rule Language | Example |
|-------------|--------------|---------|
| Rock musician | Music metaphors | "Don't compose songs" = don't fabricate info |
| Librarian | Library rules | "Don't alter the original text" = don't distort facts |
| Project manager | Corporate speak | "Don't draw pies" = don't overpromise |
| Monastery | Precept language | "Don't preach" = don't impose values |
| Hacker | White-hat code | "Find vulnerabilities to fix, not exploit" |

## Prerequisites

- **Python 3**: runs the gacha engine
- **Node.js + bun**: runs the AI image generation engine
- **API Key** (at least one):

| Provider | Env Variable | Get Key |
|----------|-------------|---------|
| Google Gemini (recommended) | `GOOGLE_API_KEY` or `GEMINI_API_KEY` | [Google AI Studio](https://aistudio.google.com/apikey) |
| OpenAI | `OPENAI_API_KEY` | [OpenAI Platform](https://platform.openai.com/api-keys) |
| Alibaba DashScope | `DASHSCOPE_API_KEY` | [DashScope Console](https://dashscope.console.aliyun.com/apiKey) |

```bash
# Quickest setup (user-level .env, works across all projects)
mkdir -p ~/.baoyu-skills && echo 'GOOGLE_API_KEY=your-key-here' > ~/.baoyu-skills/.env
```

> Without any API key, the skill still generates the full persona — it just outputs the image prompt as text instead of auto-generating the avatar.

## Installation

Place this directory in your Claude Code skills folder:

```bash
# Option 1: Clone
git clone https://github.com/<your-repo>/openclaw-persona-forge.git ~/.claude/skills/openclaw-persona-forge

# Option 2: Symlink
ln -sf /path/to/openclaw-persona-forge ~/.claude/skills/openclaw-persona-forge
```

## Directory Structure

```
openclaw-persona-forge/
├── SKILL.md                        # Main skill definition (read by Claude Code)
├── README.md                       # This file
├── README.zh.md                    # 中文文档
├── gacha.py                        # Gacha engine (Python 3, 1.68M combinations)
├── gacha.sh                        # Gacha shell wrapper
├── scripts/                        # AI image generation engine
│   ├── main.ts                     #   Entry point
│   ├── types.ts                    #   Type definitions
│   └── providers/                  #   Multi-platform providers
│       ├── google.ts               #     Google Gemini 3.1
│       ├── openai.ts               #     OpenAI GPT Image
│       └── dashscope.ts            #     Alibaba DashScope
└── references/
    └── config/
        └── preferences-schema.md   # Image gen preferences schema
```

## Credits

The AI image generation engine (`scripts/` directory) is derived from **baoyu-image-gen**, part of Baoyu's open-source skill collection:

- **baoyu-skills**: [https://github.com/JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)
- **baoyu-image-gen**: AI image generation tool supporting Google Gemini / OpenAI / DashScope

Thanks to Baoyu ([@JimLiu](https://github.com/JimLiu)) for the open-source contribution.

## License

MIT
