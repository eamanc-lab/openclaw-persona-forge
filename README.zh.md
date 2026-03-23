[English](README.md) | 中文

# 锻造一只有灵魂的龙虾 —— OpenClaw 龙虾灵魂锻造炉 🦞🔨

<p align="center">
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/adam-claw-logo.png" width="280" alt="亚当（Adam）—— 龙虾族创世神" />
  <br/>
  <strong>Adam</strong> —— 龙虾族创世神，第一只被锻造的灵魂
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/everup.jpeg" width="150" alt="Everup" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/signal.jpeg" width="150" alt="Signal" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/syn.jpeg" width="150" alt="Syn" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/unseal.jpeg" width="150" alt="Unseal" />
  <br/>
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/guipu.jpeg" width="150" alt="归朴" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/qianliwuxian.jpeg" width="150" alt="千里无线" />
  <img src="https://raw.githubusercontent.com/eamanc-lab/openclaw-persona-forge/main/docs/wenheng.jpeg" width="150" alt="文衡" />
  <br/>
  <em>更多被锻造的灵魂 —— 每一只都独一无二，共享同一套复古未来主义基因</em>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <a href="https://claude.ai"><img src="https://img.shields.io/badge/Claude_Code-Skill-blueviolet" alt="Claude Code"></a>
  <a href="https://python.org"><img src="https://img.shields.io/badge/Python-3-blue.svg" alt="Python 3"></a>
</p>

---

**功能亮点：**

- 🎴 **800 万种组合抽卡** — 5 个维度真随机，每只龙虾独一无二
- 🎭 **6 步锻造流水线** — 从方向到 SOUL.md，全程结构化输出
- 🌏 **双 Skill 双文化** — 中文版（中式原型）+ 英文版（欧美原型）各自原生
- 🖼️ **统一头像风格** — 复古未来主义 × Pin-up × 充气 3D × 街机 UI
- 📦 **交付三件套** — SOUL.md + IDENTITY.md + 头像提示词，开箱即用
- 🤖 **可选自动生图** — 安装 baoyu-image-gen 后直接出图，无需复制提示词

---

## 为什么需要这个 Skill？

手写 SOUL.md 听起来简单，做起来难：
- 不知道从哪个维度切入角色
- 写出来的底线规则像企业守则，没有角色味
- 中英两套内容需要分别适配本土文化语境，而不是翻译

这个 Skill 把角色锻造拆成 6 步可复现的流水线，用抽卡引擎注入随机张力，用统一的视觉体系保证每只龙虾都"长得像一家人"。

---

## 双 Skill，一个锻造炉

本仓库包含两个独立的 Claude Code Skill —— 相同的 6 步锻造流水线，不同的文化调色板：

| Skill | 语言 | 文化语境 | ClawHub Slug |
|-------|------|---------|--------------|
| **openclaw-persona-forge** | 中文 | 中文文化原型、中式文学表达 | `openclaw-persona-forge` |
| **openclaw-soul-forge** | English | 欧美文化原型、英文原生语感 | `openclaw-soul-forge` |

---

## 快速上手

**第 1 步：** 克隆并链接
```bash
git clone https://github.com/eamanc-lab/openclaw-persona-forge.git
ln -s $(pwd)/openclaw-persona-forge/skills/openclaw-persona-forge ~/.claude/skills/openclaw-persona-forge
ln -s $(pwd)/openclaw-persona-forge/skills/openclaw-soul-forge ~/.claude/skills/openclaw-soul-forge
```

**第 2 步：** 在 Claude Code 中对话
```
帮我设计龙虾灵魂
```
或随机抽一张：
```
抽卡
```

**第 3 步：** 取走交付三件套 — SOUL.md + IDENTITY.md + 头像提示词

---

## 使用示例

```
用户：/openclaw-persona-forge 抽卡

Skill 输出：
🎴 抽卡结果
前世身份：前监狱长（权威者）
来当龙虾的原因：被迫（某次执法失职后的惩罚）
核心气质：严肃但偶尔漏出温柔
说话风格：每次拒绝都先叹气
特征道具：裂了一条缝的墨镜

────────────────────────────────
Step 2 · 身份张力
————————————————
前世管着几百号人，现在是别人盘子里的主角。
最深的矛盾：习惯了"规则就是规则"，
           却在夹缝里学会了"有时候规则是用来保护人的"。
...（完整 SOUL.md 输出）
```

---

## 6 步锻造流水线

```
Step 1  选方向 ────────→ 10 类 × 每类 4 个（共 40 个）/ 抽卡随机
Step 2  身份张力 ──────→ 前世身份 × 当下处境 × 内在矛盾
Step 3  底线规则 ──────→ 从身份推导，角色化语言表达
Step 4  名字 ──────────→ 3 个候选 + 命名策略分析
Step 5  头像 ──────────→ 统一风格提示词（+ 自动生图，如已安装 baoyu-image-gen）
Step 6  完整交付 ──────→ SOUL.md + IDENTITY.md + 头像提示词/图片
```

---

## 两种触发模式

| 模式 | 触发词 | 说明 |
|------|--------|------|
| **引导模式** | "帮我设计龙虾灵魂" | 从 10 类（共 40 个）方向中选择或混搭 |
| **抽卡模式** | "抽卡"、"随机"、"gacha" | 从 800 万种组合中真随机抽取 |

---

<details>
<summary>目录结构</summary>

```
openclaw-forge/
├── skills/
│   ├── openclaw-persona-forge/         # 中文版
│   │   ├── SKILL.md                    #   主技能定义
│   │   ├── gacha.py                    #   抽卡引擎（800 万种组合）
│   │   ├── gacha.sh                    #   薄壳脚本
│   │   └── references/                 #   分步指南
│   └── openclaw-soul-forge/            # English 版
│       ├── SKILL.md                    #   Main skill definition
│       ├── gacha.py                    #   Gacha engine (8M combinations)
│       ├── gacha.sh                    #   Shell wrapper
│       └── references/                 #   Step-by-step guides
├── docs/
│   └── adam-claw-logo.png              # 共享资源
├── README.md                           # English README
└── README.zh.md                        # 本文件
```

</details>

<details>
<summary>发布到 ClawHub</summary>

每个 Skill 独立发布：

```bash
# 发布中文版
npx clawhub@latest publish ./skills/openclaw-persona-forge \
  --slug openclaw-persona-forge --version <版本号> --changelog "<更新说明>"

# 发布英文版
npx clawhub@latest publish ./skills/openclaw-soul-forge \
  --slug openclaw-soul-forge --version <版本号> --changelog "<更新说明>"
```

</details>

---

## 前置条件

- **Python 3**：运行抽卡引擎
- **baoyu-image-gen skill**（可选）：自动生图，仓库：[github.com/JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)

---

## 致谢

头像自动生成能力由 **baoyu-image-gen** 提供，来自宝玉老师的开源 skill 合集：
感谢宝玉老师（[@JimLiu](https://github.com/JimLiu)）的开源贡献。

## License

MIT
