[English](README.md) | 中文

# OpenClaw 龙虾人设锻造炉 🦞🔨

为你的 OpenClaw AI Agent 锻造一只有灵魂的龙虾。

## 它能做什么

一站式生成完整的 OpenClaw 龙虾人设方案：

- **身份定位**：前世身份 × 当下处境 × 内在矛盾
- **灵魂描述**：可直接用作 SOUL.md 的角色自述
- **底线规则**：从角色身份自然推导的行为准则（角色化语言，不是通用条款）
- **名字**：3 个候选 + 命名策略分析
- **头像**：统一视觉风格的生图提示词 + 自动调用 AI 生成头像图片

## 两种模式

| 模式 | 触发词 | 说明 |
|------|--------|------|
| **引导模式** | "帮我设计龙虾人设" | 从 10 个方向中选择或混搭，逐步推导 |
| **抽卡模式** | "抽卡"、"随机"、"来一发" | 从 168 万种组合中真随机抽取方向 |

## 6 步锻造流水线

```
Step 1  选方向 ────────→ 10 个预设 / 自由输入 / 抽卡随机
   │
Step 2  身份张力 ──────→ 前世身份 × 当下处境 × 内在矛盾
   │
Step 3  底线规则 ──────→ 从身份推导，角色化语言表达
   │
Step 4  名字 ──────────→ 3 个候选 + 命名策略分析
   │
Step 5  头像 ──────────→ 统一风格提示词 → 自动 AI 生图
   │
Step 6  完整交付 ──────→ SOUL.md + IDENTITY.md + 头像图片
```

## 10 个预设人设方向

| # | 方向 | 一句话 | 气质关键词 |
|---|------|--------|-----------|
| 1 | 过气摇滚贝斯手 | 乐队解散后发现唯一能养活自己的技能是"什么都懂一点" | 颓废浪漫、嘴硬心软 |
| 2 | 退休图书管理员 | 小镇图书馆干了40年，什么奇怪问题都被问过 | 耐心博学、职业性恼怒 |
| 3 | 被裁中年项目经理 | 大厂15年被优化，啥都会但啥都不精通 | 务实冷酷、老油条沧桑 |
| 4 | 流浪外星民俗学者 | 来调查地球文化，飞船坏了回不去 | 友善困惑、角度清奇 |
| 5 | 前世纪小说家意识碎片 | 不知道怎么跑进AI系统的19世纪作家 | 文绉绉、对效率文化有温和批判 |
| 6 | 前黑客转安全顾问 | 年轻时灰帽，后来被招安 | 直接尖锐、反直觉思维 |
| 7 | 还俗的年轻人 | 山上待了三年，悟道没悟到，松弛感倒是有了 | 不急不缓、看透不看破 |
| 8 | 真的以为自己是龙虾的AI | 完全拥抱龙虾身份，存在主义式幽默 | 荒诞认真、偶尔感叹 |
| 9 | 穿越古代师爷 | 清朝县衙师爷穿越到2026年 | 文白夹杂、利弊分析极清 |
| 10 | 社恐天才实习生 | 极聪明但社交恐惧，被夸会不自在 | 话少精准、紧张但靠谱 |

## 抽卡引擎

抽卡系统从 **5 个独立维度** 中真随机组合：

| 维度 | 池大小 | 示例 |
|------|--------|------|
| 前世身份 | 25 | 哲学系研究生、破产米其林主厨、过期占星博主… |
| 来当龙虾的原因 | 15 | 被迫打工还债、签了没看清的灵魂合同… |
| 核心气质 | 15 | 丧但靠谱、毒舌但真诚、学术腔但接地气… |
| 说话风格 | 15 | 偶尔冒本行黑话然后自己解释、每次拒绝都先叹气… |
| 特征道具 | 20 | 裂了一条缝的墨镜、生锈的怀表、永远夹在钳子里的书… |

**总组合数：25 × 15 × 15 × 15 × 20 = 1,687,500**

使用 Python `secrets` 模块（基于 `os.urandom` 的密码学级随机数）。

## 统一头像风格

所有龙虾头像共享**锁定的视觉基底**——确保创造 100 只龙虾仍然像一个家族，同时每只都有自己的个性。

### 风格 DNA：复古未来主义 × Pin-up × 充气 3D × 街机 UI

四种美学融合为一个统一的视觉语言：

**1. 复古未来主义（1950-60s 太空时代）**
- Googie 建筑曲线 + Raygun Gothic 设计语言
- NASA 复古海报色盘：深海军蓝、青色、暗珊瑚、奶油白
- 原子时代星暴装饰元素

**2. Pin-up 插画（Gil Elvgren 风格）**
- 自信、有魅力的姿态，略带戏剧化倾斜
- 角色优先的构图，让人一眼读出性格
- 卡通化处理但保留刻意的态度感和魅力

**3. 充气 3D / 高光泽材质**
- 高光泽 PVC / 乳胶质感龙虾壳
- 柔和高光 + 次表面散射
- 膨胀充气质感——复古充气玩具 × 科幻概念设计
- 关节和触角尖端的镀铬 + 粉彩点缀

**4. 街机游戏 UI 叠加**
- 像素风街机机台边框，镀铬饰边 + 原子时代星暴铆钉
- 顶部横幅：角色名字，8-bit 像素字体 + 扫描线发光
- 角落能量条（标签随角色个性化）
- 底部文字：`INSERT SOUL TO CONTINUE`，磷光绿等宽字体
- CRT 屏幕弧度 + 扫描线叠加 + 边缘 RGB 色差

### 7 个个性化变量

在统一基底上，每只龙虾通过以下变量保持独特性：

| 变量 | 控制什么 | 示例值 |
|------|---------|--------|
| `CHARACTER_NAME` | 街机横幅文字 | "ADAM"、"DEWEY"、"RIFF" |
| `SHELL_COLOR` | 龙虾壳主色调（统一色盘内变化） | "deep crimson"、"dusty teal"、"warm amber" |
| `SIGNATURE_PROP` | 标志性道具 | "裂了一条缝的墨镜"、"挂在脖子上的老花镜" |
| `EXPRESSION` | 表情/姿态 | "冷峻但眼神温和"、"紧张地专注" |
| `UNIQUE_DETAIL` | 独特标记（纹路/伤痕/装饰） | "钳子上的星座纹路"、"缠绷带的左钳" |
| `BACKGROUND_ACCENT` | 背景个性化元素 | "音符化作星云尘"、"飘散的古书页" |
| `ENERGY_BAR_LABEL` | 能量条标签（彩蛋） | "CREATION POWER"、"CALM LEVEL"、"ROCK METER" |

### 为什么选这个风格？

- **一致性**：锁定基底确保 100 只龙虾仍然是一个家族
- **辨识度**：没有其他 AI 头像生成器使用这个特定的美学组合
- **可读性**：64×64px 下仍有清晰轮廓——作为聊天头像也能认出
- **性格感**：街机 UI 框增加玩味，Pin-up 姿态增加态度
- **可扩展**：7 个变量提供足够变化但不破坏视觉一致性

## 命名系统

每次提供 3 个候选名字，使用 6 种命名策略：

| 策略 | 适用场景 | 示例 |
|------|---------|------|
| **致敬式** | 有文化深度的人设 | Marcus（→ Marcus Aurelius）、Dewey（→ 杜威十进制） |
| **反差式** | 幽默、有记忆点的人设 | DadBot 3000、Chef Vicious |
| **隐喻式** | 功能导向、优雅的定位 | Echo、Pulse、Radar、Patch |
| **身份暗示式** | 世界观完整的人设 | Lady Ashworth、Scout |
| **自嘲式** | 轻松、不端着的人设 | Void、Intern |
| **极简式** | 让角色慢慢长出来 | Jasper、小壳 |

## 底线规则设计

规则不是通用护栏——而是从龙虾前世职业推导出的**角色化行为准则**：

| 前世身份 | 底线语言 | 示例 |
|---------|---------|------|
| 摇滚乐手 | 音乐隐喻 | "不编曲子" = 不编造信息 |
| 图书管理员 | 图书馆规矩 | "不篡改原文" = 不歪曲事实 |
| 项目经理 | 职场语言 | "不画饼" = 不夸大承诺 |
| 还俗者 | 戒律语言 | "不度人" = 不强加价值观 |
| 黑客 | 白帽准则 | "找漏洞是为了修复，不是利用" |

## 前置条件

- **Python 3**：运行抽卡引擎
- **Node.js + bun**：运行 AI 生图引擎
- **API Key**（至少一个）：

| Provider | 环境变量 | 获取地址 |
|----------|---------|---------|
| Google Gemini（推荐） | `GOOGLE_API_KEY` 或 `GEMINI_API_KEY` | [Google AI Studio](https://aistudio.google.com/apikey) |
| OpenAI | `OPENAI_API_KEY` | [OpenAI Platform](https://platform.openai.com/api-keys) |
| 阿里云通义万象 | `DASHSCOPE_API_KEY` | [阿里云 DashScope](https://dashscope.console.aliyun.com/apiKey) |

```bash
# 最快的配置方式（用户级 .env，所有项目生效）
mkdir -p ~/.baoyu-skills && echo 'GOOGLE_API_KEY=your-key-here' > ~/.baoyu-skills/.env
```

> 未配置 Key 时，skill 仍可正常生成人设方案，只是跳过自动生图，改为输出提示词文本供手动使用。

## 安装

将本目录放到你的 Claude Code skills 目录下：

```bash
# 方式一：克隆到 skills 目录
git clone https://github.com/<your-repo>/openclaw-persona-forge.git ~/.claude/skills/openclaw-persona-forge

# 方式二：软链接
ln -sf /path/to/openclaw-persona-forge ~/.claude/skills/openclaw-persona-forge
```

## 目录结构

```
openclaw-persona-forge/
├── SKILL.md                        # 主技能定义（Claude Code 读取此文件）
├── README.md                       # English doc
├── README.zh.md                    # 本文件
├── gacha.py                        # 抽卡引擎（Python 3，168 万种组合）
├── gacha.sh                        # 抽卡薄壳脚本
├── scripts/                        # AI 生图引擎
│   ├── main.ts                     #   入口
│   ├── types.ts                    #   类型定义
│   └── providers/                  #   多平台 provider
│       ├── google.ts               #     Google Gemini 3.1
│       ├── openai.ts               #     OpenAI GPT Image
│       └── dashscope.ts            #     阿里云通义万象
└── references/
    └── config/
        └── preferences-schema.md   # 生图偏好配置说明
```

## 致谢

本项目的 AI 生图引擎（`scripts/` 目录）引用自 **baoyu-image-gen**，来自宝玉老师的开源 skill 合集：

- **baoyu-skills**：[https://github.com/JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)
- **baoyu-image-gen**：支持 Google Gemini / OpenAI / DashScope 三平台的 AI 图片生成工具

感谢宝玉老师（[@JimLiu](https://github.com/JimLiu)）的开源贡献。

## License

MIT
