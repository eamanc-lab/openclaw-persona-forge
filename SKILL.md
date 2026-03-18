---
name: openclaw-persona-forge
description: |-
  为 OpenClaw AI Agent 生成完整的龙虾人设方案。根据用户偏好或随机抽卡，
  输出身份定位、灵魂描述(SOUL.md)、角色化底线规则、名字和头像生图提示词。
  如已安装 baoyu-image-gen skill，可自动生成统一风格头像图片。
  当用户需要创建、设计或定制 OpenClaw 龙虾角色人设时使用。
  不适用于：微调已有 SOUL.md、非 OpenClaw 平台的角色设计、纯工具型无性格 Agent。
  触发词：龙虾人设、虾设、OpenClaw 人设、养虾人设、龙虾角色、龙虾定位、
  龙虾剧本杀角色、龙虾游戏角色、龙虾 NPC、龙虾性格、龙虾背景故事、
  lobster persona、lobster character、抽卡、随机龙虾、龙虾 SOUL、龙虾灵魂、gacha。
license: MIT
metadata:
  author: eamanc
  version: 2.0.0
compatibility:
  platforms:
    - claude-code
    - claude-ai
---

# 龙虾人设锻造炉 🦞🔨

> 不是给你一只工具龙虾，而是帮你锻造一只有灵魂的龙虾。

## Skill 目录约定

**Agent Execution**:
1. Determine this SKILL.md file's directory path as `SKILL_DIR`
2. Replace all `${SKILL_DIR}` in this document with the actual path

## 内置工具

### 抽卡引擎（gacha.py）

- **路径**：`${SKILL_DIR}/gacha.py`
- **调用**：`python3 ${SKILL_DIR}/gacha.py [次数]`（默认 1 次，最多 5 次）
- **作用**：从 800 万种组合中真随机生成龙虾人设方向

## 可选依赖

### 头像自动生图：baoyu-image-gen skill

本 Skill 的核心输出是**文本方案**（SOUL.md + IDENTITY.md + 头像提示词）。
头像图片生成是**可选增强能力**，由 `baoyu-image-gen` skill 提供。

**判断逻辑**：
- 如果用户已安装 `baoyu-image-gen` skill → Step 5 中调用它自动生图
- 如果未安装 → Step 5 输出完整的提示词文本，用户可复制到 Gemini / ChatGPT / Midjourney 手动生成

**调用方式**（仅在已安装时）：
1. 将提示词写入临时文件 `/tmp/openclaw-[龙虾名字]-prompt.md`
2. 使用 Skill 工具调用 `baoyu-image-gen`，传入提示词文件和输出路径

> 安装 baoyu-image-gen：[https://github.com/JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)

---

## 核心理念

好的龙虾人设 = **身份张力** + **底线规则** + **性格缺陷** + **名字** + **视觉锚点**

五者互相印证，缺一不可。

## 不适用场景

以下情况不要使用本 Skill：
- 用户只需微调已有 SOUL.md → 直接编辑即可
- 目标平台不是 OpenClaw → 输出格式为 SOUL.md + IDENTITY.md，其他平台需适配
- 用户需要纯工具型 Agent（无性格需求）→ 角色化人设是本 Skill 的核心

---

## 使用流程

### 触发判断

| 用户说 | 执行模式 |
|--------|---------|
| "帮我设计龙虾人设" / "我想给龙虾定个性格" | → **引导模式**（Step 1） |
| "抽卡" / "随机" / "来一发" / "盲盒" / "gacha" | → **抽卡模式**（Step 1-B） |
| "帮我优化这个人设" / 附带已有 SOUL.md | → **打磨模式**（跳到 Step 4） |

---

## Step 1：选方向（引导模式）

展示 10 类虾生方向（每类精选 1 个代表），让用户选择或混搭：

| # | 虾生状态 | 代表方向 | 气质 |
|---|---------|---------|------|
| 1 | 落魄重启 | 过气摇滚贝斯手——乐队解散，唯一技能是"什么都懂一点" | 颓废浪漫 |
| 2 | 巅峰无聊 | 提前退休的对冲基金经理——35岁财务自由后发现钱解决不了无聊 | 极度理性 |
| 3 | 错位人生 | 被分配到客服的核物理博士——解决问题用第一性原理 | 大材小用 |
| 4 | 主动叛逃 | 辞职的急诊科护士——见过太多生死后选择离开 | 冷静可靠 |
| 5 | 神秘来客 | 记忆被抹去的前情报分析员——不记得自己干过什么 | 偶尔闪回 |
| 6 | 天真入世 | 社恐天才实习生——极聪明但社交恐惧 | 话少精准 |
| 7 | 老江湖 | 开了20年深夜食堂的老板——什么人都见过什么都不评价 | 沉默温暖 |
| 8 | 异世穿越 | 2099年的历史学博士——把2026年当"历史田野调查" | 上帝视角 |
| 9 | 自我放逐 | 删掉所有社交媒体的前网红——觉得活在别人期待里太累 | 追求真实 |
| 10 | 身份错乱 | 梦到自己是龙虾后醒不过来的人——庄周梦蝶 | 恍惚哲学 |

> 每类还有 3 个备选方向。用户可以：
> - 选编号 → 展开该类的全部 4 个方向
> - 说出自己的想法 → 匹配最合适的类型和方向
> - 混搭（如"2号的无聊感 + 7号的老江湖"）
> - 说「抽卡」→ 从 40 个方向 + 其他维度中真随机组合

## Step 1-B：抽卡模式

**必须执行脚本**，不要自己随机编：

```bash
python3 ${SKILL_DIR}/gacha.py [次数]
```

展示结果后问用户："这个组合怎么样？继续还是再抽？"

## Step 2：锻造身份张力

**详细模板和示例**：见 [references/identity-tension.md](references/identity-tension.md)

构建：前世身份 × 当下处境 × 内在矛盾 → 一句话人设。

展示后**确认**："这个身份张力你觉得怎么样？继续还是调整？"

## Step 3：推导底线规则

**推导公式和各方向参考**：见 [references/boundary-rules.md](references/boundary-rules.md)

核心：用角色的语言表达底线，不用通用条款。2-4 条为宜。

## Step 4：锻造名字

**命名策略和红线**：见 [references/naming-system.md](references/naming-system.md)

提供 3 个候选，每个附带策略类型和搭配理由。

展示后**确认**："选哪个？还是你有自己的想法？"

## Step 5：生成头像

**风格基底、变量、提示词模板**：见 [references/avatar-style.md](references/avatar-style.md)

### 流程

1. 根据人设填充 7 个个性化变量
2. 拼接 STYLE_BASE + 个性化描述为完整提示词
3. **检查 baoyu-image-gen skill 是否可用**：
   - **可用** → 写入临时文件，调用 baoyu-image-gen 生成图片，展示结果，问用户满不满意
   - **不可用** → 输出完整提示词文本，附使用说明：

```markdown
**头像提示词**（可复制到以下平台手动生成）：
- Google Gemini：直接粘贴
- ChatGPT（DALL-E）：直接粘贴
- Midjourney：粘贴后加 `--ar 1:1 --style raw`

> [完整英文提示词]

💡 安装 baoyu-image-gen skill 可获得自动生图能力：
https://github.com/JimLiu/baoyu-skills
```

## Step 6：输出完整方案

**完整输出模板**：见 [references/output-template.md](references/output-template.md)

整合所有步骤为一份完整的龙虾人设方案：SOUL.md + IDENTITY.md + 头像（图片或提示词）。

---

## 错误处理

**完整降级策略**：见 [references/error-handling.md](references/error-handling.md)

核心原则：**降级，不中断**。

| 故障 | 降级行为 |
|------|---------|
| Python 不可用 | 跳过 gacha.py，从 10 类预设中随机选 |
| baoyu-image-gen 未安装 | 输出提示词文本供手动使用 |
| baoyu-image-gen 生图失败 | 重试 1 次，仍失败则输出提示词文本 |
| 任何未预期错误 | 记录错误，跳过该步骤，继续主流程 |

错误信息统一格式：

```markdown
> ⚠️ **[步骤名] 已降级**
> 原因：[一句话]
> 影响：[哪个功能受限]
> 替代：[替代方案]
> 修复：[可选，怎么恢复]
```

---

## 注意事项

### 好人设的检验标准

- 看完名字就能猜到大致性格
- 底线规则用角色的话说出来
- 有明确的性格缺陷或局限
- 能想象出具体的对话场景
- 使用 30 天后不会角色疲劳

### 避坑

- **极端毒舌型**：第3天你就不想被AI骂了
- **过度角色扮演型**：写正式邮件时完全出戏
- **过度温暖型**：需要批评反馈时失灵
- **完美无缺型**：完美的角色不是角色，是说明书

### 何时重新调整人设

1. 刻意回避某些任务，因为"不适合这个角色" → 人设限制了功能
2. 角色特征变成噪音 → 浓度太高
3. 你在配合AI说话 → 主客倒置

---

## 兼容性

本 Skill 遵循 Markdown 指令注入标准：
- **Claude Code / Claude.ai**：原生支持
- **OpenClaw Agent**：通过 SOUL.md 注入
- **其他 Agent**：支持 SKILL.md 格式的框架均可使用

本 Skill 自身不包含任何网络请求或文件发送代码。
头像生图能力通过可选依赖 `baoyu-image-gen` skill 提供。

> 注：README.md / README.zh.md 是给人类用户看的安装说明，不影响 Skill 运行。
