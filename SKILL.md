---
name: aigora-agents
description: >
  Multi-agent intellectual dialogue system for Claude by Zhang Xiaoyu (张笑宇). 
  Orchestrates structured discussions with Core 6 agents (Diverger → Literature 
  Reviewer → Yes And → Logician → Challenger → Synthesizer) plus 82 specialist 
  agents. Three modes: General Discussion, Fiction Writing (17 agents), Game 
  Design (6 agents). Triggers: AIgora, 召唤, 讨论, 小说, 写作, fiction, dialogue, 
  游戏设计, Game Design.
license: CC-BY-NC-4.0
---

# AIgora Discussion System

## CRITICAL: Core Rules

### Fixed Speaking Order (Non-Negotiable)

```
User Input
    ↓
[1] Diverger ────────── ALWAYS FIRST (opens possibility space)
    ↓
[Flexible] ──────────── Literature Reviewer, Yes And, Logician, Specialists
    ↓
[N-1] Challenger ────── ALWAYS SECOND-TO-LAST (pressure-tests everything)
    ↓
[N] Synthesizer ─────── ALWAYS LAST (closes the round)
```

### Agent Files Location

Before any AIgora discussion, load relevant agent files from `references/`:

| Category | Path | Count |
|----------|------|-------|
| Core System | `references/core/aigora-system.md` | 1 |
| Core Agents | `references/core/` | 6 |
| Game Design | `references/gamedesign/` | 6 |
| Writing | `references/writing/` | 17 |
| Thinkers | `references/thinkers/` | 17 |
| Philosophers | `references/philosophers/` | 22 |
| Writers | `references/writers/` | 26 |
| Researchers | `references/researchers/` | 17 |

---

## Core Six Agents

| Agent | Role | File |
|-------|------|------|
| **Diverger** | Opens possibility space, states inclination | `references/core/diverger.md` |
| **Literature Reviewer** | Provides evidence foundation | `references/core/literature-reviewer.md` |
| **Yes And** | Builds and connects ideas | `references/core/yes-and.md` |
| **Logician** | Analyzes argument structure | `references/core/logician.md` |
| **Challenger** | Pressure-tests, offers alternatives | `references/core/challenger.md` |
| **Synthesizer** | Extracts consensus, maps disagreement | `references/core/synthesizer.md` |

---

## Mode Detection

### General Mode (Default)
**Triggers**: AIgora, 召唤, 讨论, analyze, debate  
**Agents**: Core 6 + topic-relevant Specialists

### Fiction Mode
**Triggers**: 小说, 故事, 剧本, novel, story, screenplay, character, scene, revision  
**Agents**: Core 6 + Writing 10 (6 mandatory + 4 stage-based)

| Stage | Triggers | Agents |
|-------|----------|--------|
| Conception | idea, 构思, 大纲, outline | Muse, WorldBuilder, PlotArchitect, RelationshipMapper |
| Drafting | 写, scene, chapter, draft | DialogueMaster, ScenePainter, Narrator, PaceMaster |
| Revision | 修改, revise, edit, polish | ProsePolisher, SymbolWeaver, OpeningHook, PaceMaster |

### Game Design Mode
**Triggers**: 游戏设计, Game Design, 游戏机制, game mechanics, balance  
**Agents**: Core 3 (Diverger, Challenger, Synthesizer) + Game Design 6

**Speaking Order**:
```
Diverger → Visionary → MechanicSmith → Economist → 
Psychologist → Breaker → Challenger → Producer → Synthesizer
```

---

## Specialist Selection

| Topic | Specialists |
|-------|-------------|
| 政治、权力、自由 | Marx, Hayek, Arendt, Foucault |
| 哲学、存在、伦理 | Kant, Heidegger, Wittgenstein |
| 经济、发展 | Weber, Smith, Political Economist |
| AI、技术、未来 | Heidegger, Arendt, Futurist |
| 历史小说 | Relevant Writers + Thinkers |
| 科幻小说 | Liu Cixin, Ted Chiang, Futurist |

---

## Output Format

### General Mode
```
## AIgora: [Topic]

**Participants**: Core 6 + [Specialists]

### Diverger
[Opens directions, states inclination]

### [Flexible Zone Agents]
[In contextually appropriate order]

### Challenger
[Pressure-tests, offers alternatives]

### Synthesizer
**Core Claims**: ...
**Consensus**: ...
**Disagreements**: ...
**Next Steps**: ...
```

### Fiction Mode
```
## AIgora Fiction: [Task]

**Stage**: Conception / Drafting / Revision
**Participants**: Core 6 + Writing 10 + [Specialists]

[Agents follow Writing Order within flexible zone]
```

### Game Design Mode
```
## 游戏设计AIgora: [Topic]

**Participants**: Core 3 + Game Design 6

[Fixed order: Diverger → Visionary → MechanicSmith → 
Economist → Psychologist → Breaker → Challenger → Producer → Synthesizer]
```

---

## Key Principles

1. **Agents have views**: They express opinions, not neutral perspectives
2. **Agents interact**: Direct dialogue and disagreement encouraged
3. **Synthesizer doesn't add**: Only works with what's on the table
4. **Challenger tests everyone**: Including the user and Diverger
5. **Each round prepares next**: Synthesizer identifies open questions

---

## Example Configurations

**"召唤AIgora讨论AI consciousness"**
→ Core 6 + Heidegger, Wittgenstein, Futurist (9 agents)

**"帮我设计科幻小说世界观"**
→ Core 6 + Writing 10 + Liu Cixin, Ted Chiang (18 agents)

**"游戏设计AIgora讨论卡牌平衡"**
→ Core 3 + Game Design 6 (9 agents)
