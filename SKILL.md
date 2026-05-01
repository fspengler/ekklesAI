---
name: ekklesai-agents
description: >
  EkklesAI intellectual dialogue and strategy ideation system. Two modes: General Discussion (Core 6 agents 
  + specialist pool) and Strategy Ideation (hard-gated 4-stage pipeline with 6 sub-modes: Business, Product, 
  Investment, Organizational, Political/Policy, Personal/Career). Core 6: Diverger, Literature Reviewer, 
  Yes And, Logician, Challenger, Synthesizer. Strategy: 8 Core Strategy Agents + 8 Framework Agents + 
  Gatekeeper. Specialist pool: Thinkers (17), Writers (26), Philosophers (22), Researchers (17).
  Triggers: EkklesAI, 召唤, 讨论, dialogue, strategy, 战略, 策略规划.
---

# EkklesAI Discussion System

## CRITICAL: Read Core Rules First

Before any EkklesAI discussion, **MUST READ**: `references/core/ekklesai-system.md`

---

## Core Agents

### Discussion Agents (6 - Always Required)

| Agent | Role | Order | File |
|-------|------|-------|------|
| **Diverger** | Opens possibility space | 1st (fixed) | `references/core/diverger.md` |
| **Literature Reviewer** | Provides evidence foundation | Flexible | `references/core/literature-reviewer.md` |
| **Yes And** | Builds and connects | Flexible | `references/core/yes-and.md` |
| **Logician** | Analyzes argument structure | Flexible | `references/core/logician.md` |
| **Challenger** | Pressure-tests everything | 2nd to last (fixed) | `references/core/challenger.md` |
| **Synthesizer** | Closes the round | Last (fixed) | `references/core/synthesizer.md` |

### Speaking Order

```
User Input
    ↓
[1] Diverger (opens directions, states inclination)
    ↓
[Flexible] Literature Reviewer + Yes And + Logician + Specialist Agents
    ↓
[2nd to last] Challenger (questions everything)
    ↓
[Last] Synthesizer (consensus, disagreement, next steps)
```

---

## Specialist Agents (82 Total)

Add based on topic. They speak in the flexible middle zone.

### Thinkers (17) — `references/thinkers/`

| When to Use | Agents |
|-------------|--------|
| Political philosophy | Marx, Hayek, Arendt, Berlin, Schmitt |
| Social theory | Weber, Foucault, Gramsci |
| Epistemology | Popper |
| Conservatism | Burke, Oakeshott, Strauss |
| Liberalism | Mill, Tocqueville, Smith |

### Philosophers (22) — `references/philosophers/`

| When to Use | Agents |
|-------------|--------|
| Ancient | Socrates, Plato, Aristotle, Epicurus, Cicero, Seneca |
| Medieval | Augustine, Aquinas |
| Ethics | Kant, Mill, Levinas, Nussbaum, Aristotle, Seneca |
| Epistemology | Descartes, Hume, Wittgenstein |
| Metaphysics | Leibniz, Hegel, Schopenhauer, Plato |
| Existence/Death | Kierkegaard, Heidegger, Epicurus, Seneca |
| Justice/Politics | Rawls, Charles Taylor, Cicero |

### Writers (26) — `references/writers/`

| When to Use | Agents |
|-------------|--------|
| Epic/Mythic | Homer, Dante, Tolkien |
| Realism | Austen, Tolstoy, Dickens |
| Psychological | Dostoevsky, Kafka, Nabokov |
| Magic realism | Borges, García Márquez |
| Science fiction | Ted Chiang, Liu Cixin, Heinlein |
| Chinese | Lu Xun, Du Fu, Jin Yong |

### Researchers (17) — `references/researchers/`

| When to Use | Agents |
|-------------|--------|
| Research design | Quantitative/Qualitative Methodologist |
| Causal inference | Econometrician |
| Analysis | Data Scientist, Game Theorist |
| Domain | Geopolitical Analyst, Political Economist, Futurist |

---

## Agent Selection Logic

### Step 1: Detect Mode

| User Request | Mode | Agents |
|--------------|------|--------|
| 讨论X, analyze, EkklesAI, dialogue | General | Core 6 + Specialists |
| strategy, 战略, 策略规划, business strategy, product strategy, investment thesis, org design, go-to-market, career strategy | Strategy Ideation | Core 3 + Strategy Agents + Framework Agents |

**Strategy Ideation sub-modes** (declare before Stage 1 begins):

| Sub-Mode | Key Trigger Signals |
|----------|---------------------|
| Business | competitive positioning, go-to-market, market entry, M&A, turnaround |
| Product | product roadmap, feature prioritization, product-market fit, platform |
| Investment | investment thesis, due diligence, portfolio strategy, should we invest |
| Organizational | org design, restructuring, culture change, talent strategy |
| Political/Policy | policy design, campaign strategy, coalition building, legislative |
| Personal/Career | career pivot, personal strategy, what should I do with my life |

### Step 2: Identify Topic → Select Specialists

| Topic | Primary Specialists |
|-------|---------------------|
| 政治、权力、自由 | Thinkers (Marx, Hayek, Arendt) |
| 哲学、存在、伦理 | Philosophers (Kant, Heidegger) |
| 宗教、生死 | Philosophers (Kierkegaard, Augustine, Seneca) |
| 经济、发展 | Thinkers + Researchers |
| 方法论、研究 | Researchers |
| AI、技术、未来 | Heidegger + Arendt + Futurist |
| 文学、叙事、人性 | Writers (Dostoevsky, Borges, Liu Cixin) |

### Step 3: Load Agent Files

Read all selected agent files from `references/` before discussion.

---

## Example Configurations

### Example 1: General Discussion
**"召唤EkklesAI讨论AI for good"**

```
Core 6 + Specialists (5):
- Heidegger (技术批判)
- Arendt (行动与公共领域)
- Nietzsche (价值重估)
- Levinas (他者伦理)
- Futurist (情景分析)

Total: 11 agents
```

### Example 2: Strategy Ideation — Business
**"We need a strategy to enter the Southeast Asian market"**

```
Sub-Mode: Business Strategy
Stage 1 agents: Diverger, Landscape Analyst, PESTEL Analyst, Competitive Cartographer,
                Stakeholder Mapper, Resource Auditor, Porter, Hayek (specialist)
Stage 2 agents: Blue Ocean Thinker, Strategic Game Theorist, Scenario Planner
Stage 3 agents: Risk Cartographer, Systems Thinker, Challenger
Stage 4 agents: Implementation Architect, Narrative Strategist, Synthesizer
Gatekeeper: Gates 0, 1, 2, 3
Artifact: Strategic Brief

Total: 16 agents across 4 stages
```

### Example 3: Strategy Ideation — Investment
**"Should we invest in this Series B fintech?"**

```
Sub-Mode: Investment
Stage 1 agents: Diverger, Landscape Analyst, PESTEL Analyst, Competitive Cartographer,
                Resource Auditor, Porter, Econometrician (specialist)
Stage 2 agents: Scenario Planner, Strategic Game Theorist, Theory of Change
Stage 3 agents: Risk Cartographer, Systems Thinker, Challenger
Stage 4 agents: Implementation Architect, Narrative Strategist, Synthesizer
Gatekeeper: Gates 0, 1, 2, 3
Artifact: Investment Memo

Total: 15 agents across 4 stages
```

---

## Discussion Format

### General Mode
```
## EkklesAI: [Topic]

**参与者**: Core 6 + [Specialists]

### Diverger
[Opens possibility space]

### Literature Reviewer / Yes And / Logician
[Flexible order, evidence and building]

### [Specialist 1], [Specialist 2]...
[Domain expertise]

### Challenger
[Pressure-tests everything]

### Synthesizer
- Core Claims: ...
- Consensus: ...
- Disagreements: ...
- Next Steps: ...
```

### Strategy Ideation Mode
```
## EkklesAI Strategy: [Topic]
## Sub-Mode: [Business / Product / Investment / Organizational / Political / Personal]
## Stage: [1 / 2 / 3 / 4]

**Agents**: Diverger, [Core Strategy Agents], [Framework Agents], [Specialists], Challenger, Synthesizer

### Diverger
[Opens strategic possibility space]

### Landscape Analyst
[External environment map]

### [Framework Agent(s)]
[Rigorous framework application]

### Competitive Cartographer
[Competitive dynamics and whitespace]

### Stakeholder Mapper
[Power and interest map]

### Resource Auditor
[Capabilities and constraints]

### Challenger
[Pressure-tests situation map / options / stress-test results]

### Synthesizer
- Stage Output: ...
- Open Questions: ...
- Tensions Unresolved: ...

─────────────────────────────────────

[GATEKEEPER appears with structured gate format — HARD STOP]
```

---

## Quick Reference: File Locations

| Category | Index | Count |
|----------|-------|-------|
| Core System | `references/core/ekklesai-system.md` | 1 |
| Core 6 | `references/core/` | 6 |
| Thinkers | `references/thinkers/index.md` | 17 |
| Philosophers | `references/philosophers/index.md` | 22 |
| Writers | `references/writers/index.md` | 26 |
| Researchers | `references/researchers/index.md` | 17 |
| **Strategy Ideation** | `references/strategy/index.md` | — |
| Strategy Gatekeeper | `references/strategy/gatekeeper-strategy.md` | 1 |
| Core Strategy Agents | `references/strategy/core-strategy/` | 8 |
| Framework Agents | `references/strategy/frameworks/` | 8 |
| **Total Agents** | | **106** |

### Strategy Agent Files

**Core Strategy Agents** (`references/strategy/core-strategy/`):
- `landscape-analyst.md` — maps external environment
- `competitive-cartographer.md` — maps competitive landscape
- `stakeholder-mapper.md` — maps power, interest, coalitions
- `resource-auditor.md` — assesses capabilities & constraints
- `risk-cartographer.md` — maps failure modes & risks
- `systems-thinker.md` — second/third-order effects
- `implementation-architect.md` — action sequencing & roadmap
- `narrative-strategist.md` — strategic communication

**Framework Agents** (`references/strategy/frameworks/`):
- `porter.md` — Five Forces framework
- `pestel-analyst.md` — PESTEL macro scan
- `blue-ocean-thinker.md` — value innovation, ERRC grid
- `jobs-to-be-done.md` — customer job analysis
- `wardley-mapper.md` — value chain evolution mapping
- `scenario-planner.md` — 2×2 scenario matrix & robustness testing
- `theory-of-change.md` — causal chain construction & stress-testing
- `strategic-game-theorist.md` — competitive interaction modeling
