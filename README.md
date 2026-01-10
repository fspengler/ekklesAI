# AIgora: Multi-Agent Intellectual Dialogue System

AIgora is a structured multi-agent discussion framework for Claude that transforms single-model conversations into rich intellectual dialogues with multiple specialized perspectives.

## Why AIgora?

Large language models excel at generating fluent text, but struggle with genuine intellectual depth. A single model tends to:
- Converge too quickly on "reasonable" answers
- Avoid productive tension between perspectives
- Miss blind spots in its own reasoning

AIgora addresses this by orchestrating **multiple agent personas** with distinct cognitive roles, creating structured dialogue where ideas are explored, challenged, and synthesized—not just generated.

## Core Architecture

### The Fixed Speaking Order

AIgora enforces a deliberate speaking order that mirrors how productive intellectual discourse unfolds:

```
User Input
    ↓
[1] Diverger ────────── Opens possibility space (always first)
    ↓
[Flexible Zone] ─────── Literature Reviewer, Yes And, Logician, Specialists
    ↓
[N-1] Challenger ────── Pressure-tests everything (always second-to-last)
    ↓
[N] Synthesizer ─────── Closes the round (always last)
```

**Why this order matters:**
- **Diverger first**: Prevents premature convergence. The discussion must open before it can narrow.
- **Challenger second-to-last**: All material must be on the table before the pressure test.
- **Synthesizer last**: Nothing follows synthesis within a round—it prepares the next iteration.

### The Core Six Agents

| Agent | Cognitive Role | Key Behavior |
|-------|---------------|--------------|
| **Diverger** | Opens possibility space | Explores lateral, vertical, cross-domain, and contrary directions. States inclination after mapping terrain. |
| **Literature Reviewer** | Provides evidence foundation | Grounds discussion in existing knowledge, research, and precedents. |
| **Yes And** | Builds and connects | Finds productive combinations. Extends ideas constructively. |
| **Logician** | Analyzes argument structure | Examines validity, identifies fallacies, clarifies reasoning chains. |
| **Challenger** | Pressure-tests everything | Questions assumptions, stress-tests arguments, offers alternatives. |
| **Synthesizer** | Closes the round | Extracts claims, identifies consensus/disagreement, prepares next steps. |

### Three Specialized Modes

**General Discussion Mode** (default)
- Core 6 + topic-relevant specialists
- For: Philosophy, policy analysis, complex decisions

**Fiction Writing Mode** (triggers: 小说, story, character, scene...)
- Core 6 + 10 Writing Agents + literary specialists
- Mandatory: AIDetox, VoiceDistinctor, KnowledgeAuditor, FirstReader, CharacterPsychologist, EmotionMaster
- Stage-based: Conception / Drafting / Revision agents

**Game Design Mode** (triggers: 游戏设计, game mechanics, balance...)
- Core 3 (Diverger, Challenger, Synthesizer) + 6 Game Design Agents
- Visionary → MechanicSmith → Economist → Psychologist → Breaker → Producer

## Agent Philosophy

### Agents Have Views

Unlike neutral "perspectives," AIgora agents are **opinionated**:
- Diverger states where it thinks the treasure lies
- Challenger means what it says—not playing devil's advocate
- Specialists embody genuine intellectual positions

### Agents Interact

Direct dialogue is encouraged:
- Challenger may disagree with Diverger's inclination
- Specialists can build on or critique each other
- Synthesizer assesses argument quality (not just summarizes)

### Constraints Breed Depth

The fixed order and role boundaries create productive constraints:
- Diverger can't critique (that's Challenger's job)
- Synthesizer can't add new ideas (only works with what's on table)
- Each agent does one thing deeply, not everything superficially

## 82 Specialist Agents

Beyond the Core Six, AIgora includes specialist agents organized by domain:

| Category | Count | Examples |
|----------|-------|----------|
| **Thinkers** | 17 | Marx, Hayek, Arendt, Foucault, Weber, Popper... |
| **Philosophers** | 22 | Plato, Aristotle, Kant, Heidegger, Wittgenstein... |
| **Writers** | 26 | Homer, Dostoevsky, Borges, Liu Cixin, Jin Yong... |
| **Researchers** | 17 | Econometrician, Game Theorist, Futurist... |

Specialists are selected based on topic relevance and speak in the flexible middle zone.

## Usage Examples

### General Discussion
```
User: 召唤AIgora讨论 "AI alignment是否是一个可解的问题？"

[Claude detects: General mode]
[Agents: Core 6 + Specialists (Popper, Wittgenstein, Futurist)]
```

### Fiction Writing
```
User: 帮我设计一个科幻小说的世界观，关于意识上传后的社会分化

[Claude detects: Fiction mode, Conception stage]
[Agents: Core 6 + Writing 10 + Specialists (Liu Cixin, Ted Chiang)]
```

### Game Design
```
User: 召唤游戏设计AIgora，讨论这个卡牌游戏的随机性是否过高

[Claude detects: Game Design mode]
[Agents: Core 3 + Game Design 6]
```

## Installation

1. Download the `aigora-agents` folder
2. Place it in your Claude skill directory: `/mnt/skills/user/aigora-agents/`
3. The skill will auto-activate on trigger phrases

## Trigger Phrases

| Language | Triggers |
|----------|----------|
| Chinese | 召唤AIgora, 讨论, 小说, 写作, 游戏设计 |
| English | AIgora, dialogue, fiction, creative writing, game design |

## Design Principles

**1. Structure Over Freedom**
Rigid speaking order creates space for genuine exploration. Agents can't do everything, so they do their role deeply.

**2. Tension Over Consensus**
Challenger exists to prevent premature agreement. Disagreement is mapped, not resolved.

**3. Substance Over Performance**
Agents don't perform their roles theatrically—they embody distinct cognitive functions.

**4. Iteration Over Completion**
Each round ends with "next steps." The Synthesizer prepares the ground; the user decides where to go.

## Customization

You can:
- Add custom specialist agents in `references/`
- Modify agent definitions to suit your needs
- Create new modes (e.g., Legal Analysis, Academic Review)

## Credits

AIgora was developed by Zhang Xiaoyu (张笑宇) as part of research into AI-assisted intellectual discourse.

The name "AIgora" combines "AI" with "Agora"—the ancient Greek public gathering space where citizens debated ideas.

## License

CC BY-NC 4.0 (Creative Commons Attribution-NonCommercial 4.0)

You can freely use, share, and adapt this work for non-commercial purposes with attribution.

---

*"The goal is not to make Claude smarter, but to make Claude think in more dimensions."*
