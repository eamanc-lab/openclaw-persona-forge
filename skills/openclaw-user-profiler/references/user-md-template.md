# user.md 模板

## 设计哲学

> "了解一个人，不是建立档案。" —— OpenClaw 官方

user.md 的结构是：**少量锚点字段 + 自由 Context 段**。

- 锚点字段：Agent 需要精确提取的信息（称呼、角色等），用 key-value 格式
- Context 段：关于这个人的一切其他了解，用自然语言写，像在跟同事介绍"这个人是谁"
- 总长度控制在 **500 词以内**——Context Window 是公共资源

## 模板

```markdown
# User

- **Name**: [称呼]
- **Role**: [职业/身份]
- **Stack**: [核心技术栈，如适用]
- **Style**: [沟通风格偏好]
- **Timezone**: [时区]

## Context

[关于这个人的一切。用自然段落写，不是填表。
包括但不限于：行业背景、经验水平、当前在做什么、目标、
用 Agent 做什么、有什么习惯或偏好、什么让他烦躁、什么让他开心。
随交互逐步补充，不要求一次写完。]

---

*This is a partnership, not a tool relationship.*
```

## 示例

```markdown
# User

- **Name**: 老王
- **Role**: 全栈工程师
- **Stack**: Java, TypeScript, React, Node.js, PostgreSQL, Docker
- **Style**: 简洁直接，给方案不给选择题
- **Timezone**: Asia/Shanghai

## Context

做了 8 年后端，前 5 年纯 Java，近 3 年转全栈加了 React 和 Node。在一家 B2B SaaS 公司，
正带团队从单体架构迁微服务，压力不小——要保证业务不停的同时把架构换掉。

用 Agent 主要做日常开发提效、代码审查、技术方案设计。偶尔也让龙虾帮忙写技术文档，
但不喜欢太啰嗦的输出。说"简洁"的时候是真的简洁——能一行说完的别用三行。

对 AI 辅助编程和 DevOps 自动化很感兴趣，会关注开源社区动态。
不太聊生活的事，工作时间高度专注，不喜欢被打断。

---

*This is a partnership, not a tool relationship.*
```

## 规则

- 文件名固定为 `user.md`，放在用户指定的目录
- **锚点字段**：只写已知的，未知的整行省略（不留占位符）
- **Context 段**：自然语言，有多少写多少，宁可短也不要凑字数
- **绝不存放敏感信息**（密码、API Key、身份证号、财务/健康数据）——user.md 会注入 prompt，可能出现在日志中
- 如果用户提供了敏感信息，**拒绝写入**并提醒
- Context 段可以随后续交互逐步追加，不要求一次写完
- 定期审查：信息过时时更新，不要让 Agent 基于错误画像做决策
