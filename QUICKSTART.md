# Quick Start

## Installation

### For Claude.ai Users

1. Download this folder
2. In Claude.ai, go to **Settings → Skills**
3. Upload the `ekklesai-agents` folder
4. Done! The skill auto-activates on trigger phrases.

### For API/SDK Users

Include the SKILL.md content in your system prompt, and load relevant agent files from `references/` as needed.

---

## First Try

### General Discussion

```
User: Let's have an EkklesAI discussion: Should AI systems be granted legal personhood?
```

### Strategy Ideation

```
User: We need a strategy to enter the Southeast Asian market.
```

or

```
User: Help me build a product strategy — our Q3 roadmap needs a rethink.
```

---

## What to Expect

When triggered, Claude will:

1. **Detect mode**: General Discussion / Strategy Ideation
2. **Select agents**: Core 6 + relevant specialists (General) or strategy pipeline agents (Strategy)
3. **Run discussion**: Following fixed speaking order
4. **Synthesize**: Consensus, disagreements, next steps — or a structured artifact (Strategy mode)

---

## Customization

### Adding Your Own Specialists

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

### Modifying Core Agents

Edit files in `references/core/`. Be careful with the Synthesizer - it should never add new ideas, only work with what's on the table.

---

## Tips

1. **Be specific**: "Discuss X" works better than vague prompts
2. **Iterate**: Use Synthesizer's "Next Steps" to guide follow-up rounds
3. **Add specialists**: "Summon EkklesAI to discuss X, add Weber and Foucault"
4. **Switch to strategy**: "Let's run this as a strategy ideation session" mid-conversation

---

## Troubleshooting

**Agents not speaking in order?**
→ Remind Claude: "Please follow EkklesAI's fixed speaking order"

**Discussion too shallow?**
→ Ask for another round: "Continue to the next round"

**Wrong mode detected?**
→ Specify: "Use strategy ideation mode" or "Use general discussion mode"

---

## Full Documentation

- `README.md`: Design philosophy
- `SKILL.md`: Technical specification
- `EXAMPLES.md`: Sample conversations
- `references/core/ekklesai-system.md`: Core rules
