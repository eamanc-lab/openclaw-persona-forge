English | [中文](README.zh.md)

# OpenClaw Forge — Generate Deep AI Personas with Cultural Soul

<p align="center">
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/adam-claw-logo.png" width="280" alt="Adam — The Lobster Creator God" />
  <br/>
  <strong>Adam</strong> — The Lobster Creator God, the first soul forged
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/everup.jpeg" width="150" alt="Everup" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/signal.png" width="150" alt="Signal" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/syn.jpeg" width="150" alt="Syn" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/unseal.jpeg" width="150" alt="Unseal" />
  <br/>
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/guipu.jpeg" width="150" alt="Guipu" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/qianliwuxian.png" width="150" alt="Qian Li Wu Xian" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/wenheng.jpeg" width="150" alt="Wenheng" />
  <br/>
  <em>More souls forged by this skill — each one unique, all sharing the same retro-futuristic DNA</em>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <a href="https://claude.ai"><img src="https://img.shields.io/badge/Claude_Code-Skill-blueviolet" alt="Claude Code Skill"></a>
  <a href="https://python.org"><img src="https://img.shields.io/badge/Python-3-blue.svg" alt="Python 3"></a>
</p>

Stop hand-writing character docs. Tell Claude one phrase — get a complete lobster soul with identity tension, boundary rules, a name, and a cohesive avatar prompt. Three skills: two culturally-tuned soul forges (8M gacha combinations each), plus a user profiler that writes user.md and recommends Skills by role.

---

## Why This Exists

Designing a convincing AI persona from scratch is slow and inconsistent. Most people write a paragraph of traits and call it a soul — but real character depth requires **identity tension** (former life vs. current situation), **in-character rules** (not generic guardrails), and a **visual identity** that locks the style.

OpenClaw Forge structures all of that into a repeatable 6-step pipeline, with two cultural variants so your lobster speaks in the right register — Chinese literary references or English-native Western archetypes.

---

## Highlights

- **Two cultural palettes** — Chinese archetypes (CN) and Western archetypes (EN), pick the one that fits your audience
- **6-step forge pipeline** — guided flow from direction → identity → rules → name → avatar → full package
- **8,000,000 gacha combinations** — 5 dimensions, true random, one command to pull a soul
- **Identity tension by design** — every persona gets a former life, current situation, and inner contradiction
- **In-character boundary rules** — behavior limits written in the character's own voice, not boilerplate
- **Unified avatar style** — Retro-Futurism × Pin-up × Inflatable 3D × Arcade UI, locked across all lobsters
- **Auto image gen** — plug in baoyu-image-gen and the avatar prompt becomes a real image
- **User profiler** — chat-based intake → user.md so your lobster actually remembers who you are
- **Role-based Skill recommendations** — 42 roles × curated Skill catalog, three-level inheritance

---

## Quick Start

**Step 1 — Install the skill**

```bash
git clone https://github.com/eamanc-lab/openclaw-persona-forge.git
ln -s $(pwd)/openclaw-persona-forge/skills/openclaw-persona-forge ~/.claude/skills/openclaw-persona-forge
ln -s $(pwd)/openclaw-persona-forge/skills/openclaw-soul-forge ~/.claude/skills/openclaw-soul-forge
ln -s $(pwd)/openclaw-persona-forge/skills/openclaw-user-profiler ~/.claude/skills/openclaw-user-profiler
```

**Step 2 — Start Claude Code in your project**

```bash
claude
```

**Step 3 — Forge a soul**

```
# Guided mode
help me design a lobster soul

# Gacha mode (random)
gacha
```

---

## Usage Example

**Gacha pull output:**

```
Drawing from the gacha pool...

Former Life:  Veteran game designer, shipped 12 titles, burnt out at 40
Reason:       Voluntary exit — needed to feel something again
Core Vibe:    Sardonic but sincere
Speech Style: Sighs before every refusal, food metaphors for everything
Signature Prop: A cracked pair of sunglasses she never takes off

─────────────────────────────────────
SOUL PACKAGE
─────────────────────────────────────

Name candidates:
  1. Vera Ash  — "ash" carries burnout + phoenix; crisp and memorable
  2. Cleo Salt — salt: preserved, sharp, a little bitter
  3. Nox       — single-word, anonymous, suits someone done with being known

Identity:
  Vera spent two decades building worlds for other people to escape into.
  Now she's the one who needs escaping. She didn't quit — she dissolved.
  The contradiction she carries: she's the best at making things feel alive,
  but she herself feels nothing.

SOUL.md ready. IDENTITY.md ready. Avatar prompt ready.
```

---

## Three Skills, One Forge

| Skill | Purpose | ClawHub |
|-------|---------|--------|
| **openclaw-persona-forge** | Forge a lobster soul — Chinese cultural archetypes | [Install](https://clawhub.ai/eamanc-lab/openclaw-persona-forge) |
| **openclaw-soul-forge** | Forge a lobster soul — Western cultural archetypes | [Install](https://clawhub.ai/eamanc-lab/openclaw-soul-forge) |
| **openclaw-user-profiler** | Build user.md + recommend Skills by role | [Install](https://clawhub.ai/eamanc-lab/openclaw-user-profiler) |

The forge skills produce **SOUL.md** + **IDENTITY.md** + **avatar prompt**. The profiler produces **user.md** and recommends Skills from a catalog of 42 roles.

---

## 6-Step Forge Pipeline

```
Step 1  Choose Direction ──→ 10 categories × 4 each (40 total) / gacha random
Step 2  Identity Tension ──→ Former life × Current situation × Inner contradiction
Step 3  Boundary Rules ───→ Derived from identity, in-character language
Step 4  Name ─────────────→ 3 candidates with naming strategy analysis
Step 5  Avatar ────────────→ Unified style prompt (+ auto gen if baoyu-image-gen installed)
Step 6  Full Package ──────→ SOUL.md + IDENTITY.md + avatar prompt/image
```

---

## Two Modes

| Mode | Trigger | Description |
|------|---------|-------------|
| **Guided** | "help me design a lobster soul" | Pick or mix from 10 categories (40 directions), step-by-step |
| **Gacha** | "gacha", "random", "draw" | True random from 8,000,000 combinations |

---

## Gacha Engine

**5 dimensions × true random = 8,000,000 combinations** (per skill)

| Dimension | Pool | Examples |
|-----------|------|---------|
| Former Life | 40 | 10 life-state categories |
| Reason | 20 | Forced / voluntary / mysterious / accidental |
| Core Vibe | 20 | "Burnt out but dependable", "sardonic but sincere" |
| Speech Style | 20 | "Sighs before every refusal", "food metaphors for everything" |
| Signature Prop | 25 | "Cracked sunglasses", "four-string travel guitar" |

---

## Unified Avatar Style

All lobster avatars share a locked visual foundation: **Retro-Futurism × Pin-up × Inflatable 3D × Arcade UI**

- 1950–60s Space Age aesthetics, Googie curves, Raygun Gothic
- Gil Elvgren-style pin-up composition
- High-gloss PVC / inflatable 3D rendering with subsurface scattering
- Pixel-art arcade UI overlay (name banner, energy bar, CRT scan lines)
- 7 personalization variables keep each lobster unique within the family style

---

## Optional: Auto Image Generation

Both skills output **avatar prompts as text** by default. Install **baoyu-image-gen** to generate the image automatically:

- **Repository**: [github.com/JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)

---

<details>
<summary>Directory Structure</summary>

```
openclaw-forge/
├── skills/
│   ├── openclaw-persona-forge/         # Chinese version
│   │   ├── SKILL.md                    #   Main skill definition
│   │   ├── gacha.py                    #   Gacha engine (8M combinations)
│   │   ├── gacha.sh                    #   Shell wrapper
│   │   └── references/                 #   Step-by-step guides
│   ├── openclaw-soul-forge/            # English version
│   │   ├── SKILL.md                    #   Main skill definition
│   │   ├── gacha.py                    #   Gacha engine (8M combinations)
│   │   ├── gacha.sh                    #   Shell wrapper
│   │   └── references/                 #   Step-by-step guides
│   └── openclaw-user-profiler/        # User profiler + Skill recommender
│       ├── SKILL.md                    #   Main skill definition
│       └── references/                 #   Intake guide, template, role catalog
├── docs/
│   └── adam-claw-logo.png              # Shared assets
├── README.md                           # This file (English)
└── README.zh.md                        # Chinese README
```

</details>

<details>
<summary>Publishing to ClawHub</summary>

Each skill is published independently:

```bash
# Publish Chinese version
npx clawhub@latest publish ./skills/openclaw-persona-forge \
  --slug openclaw-persona-forge --version <ver> --changelog "<notes>"

# Publish English version
npx clawhub@latest publish ./skills/openclaw-soul-forge \
  --slug openclaw-soul-forge --version <ver> --changelog "<notes>"

# Publish user profiler
npx clawhub@latest publish ./skills/openclaw-user-profiler \
  --slug openclaw-user-profiler --version <ver> --changelog "<notes>"
```

</details>

---

## Credits

Avatar auto-generation powered by **baoyu-image-gen** from Baoyu's open-source skill collection.

Thanks to Baoyu ([@JimLiu](https://github.com/JimLiu)) for the open-source contribution — [github.com/JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills).

---

## License

MIT

<!--
Recommended GitHub topics:
claude-code, claude-code-skill, ai-persona, character-design, gacha, lobster, openclaw, soul-generator, ai-agent, retro-futurism
-->
