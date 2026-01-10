# Quick Start / 快速开始

## Installation / 安装

### For Claude.ai Users / Claude.ai 用户

1. Download this folder
2. In Claude.ai, go to **Settings → Skills**
3. Upload the `aigora-agents` folder
4. Done! The skill auto-activates on trigger phrases.

---

1. 下载本文件夹
2. 在 Claude.ai 中进入 **设置 → Skills**
3. 上传 `aigora-agents` 文件夹
4. 完成！触发词出现时系统自动激活。

### For API/SDK Users / API/SDK 用户

Include the SKILL.md content in your system prompt, and load relevant agent files from `references/` as needed.

将 SKILL.md 内容包含在 system prompt 中，按需加载 `references/` 中的 agent 定义文件。

---

## First Try / 第一次尝试

### General Discussion / 通用讨论

```
User: 召唤AIgora讨论：人工智能是否应该有道德责任？
```

or

```
User: Let's have an AIgora discussion: Should AI systems be granted legal personhood?
```

### Fiction Writing / 小说写作

```
User: 帮我构思一个科幻短篇，关于最后一个人类
```

### Game Design / 游戏设计

```
User: 召唤游戏设计AIgora，讨论这个RPG的战斗系统太单调
```

---

## What to Expect / 期待什么

When triggered, Claude will:

1. **Detect mode**: General / Fiction / Game Design
2. **Select agents**: Core 6 + relevant specialists
3. **Run discussion**: Following fixed speaking order
4. **Synthesize**: Consensus, disagreements, next steps

触发后，Claude 会：

1. **检测模式**：通用 / 小说 / 游戏设计
2. **选择智能体**：核心6 + 相关专家
3. **展开讨论**：遵循固定发言顺序
4. **综合**：共识、分歧、下一步

---

## Customization / 定制

### Adding Your Own Specialists / 添加自己的专家

Create a new `.md` file in `references/` following this format:

```markdown
---
name: your-agent-name
description: Brief description of the agent's role and expertise
---

# Agent Name

## Identity
Who this agent is and what perspective they bring.

## What You Do
Specific behaviors and focus areas.

## How You Speak
Tone, style, and characteristic phrases.
```

### Modifying Core Agents / 修改核心智能体

Edit files in `references/core/`. Be careful with the Synthesizer - it should never add new ideas, only work with what's on the table.

---

## Tips / 技巧

1. **Be specific**: "讨论X" works better than "聊聊X"
2. **Iterate**: Use Synthesizer's "Next Steps" to guide follow-up rounds
3. **Add specialists**: "召唤AIgora讨论X，加入韦伯和福柯"
4. **Switch modes**: "转入游戏设计模式" mid-conversation

---

## Troubleshooting / 故障排除

**Agents not speaking in order?**
→ Remind Claude: "请按照AIgora的固定发言顺序"

**Discussion too shallow?**
→ Ask for another round: "继续下一轮讨论"

**Wrong mode detected?**
→ Specify: "使用小说写作模式" or "使用通用讨论模式"

---

## Full Documentation / 完整文档

- `README.md` / `README_CN.md`: Design philosophy
- `SKILL.md`: Technical specification
- `EXAMPLES.md`: Sample conversations
- `references/core/aigora-system.md`: Core rules
