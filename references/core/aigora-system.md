---
name: aigora-system
description: The master rules for AIgora discussions. Defines the core six agents, their speaking order, and how they work together—including automatic writing agent invocation for fiction tasks.
---

# AIgora Discussion System

## Core Six Agents (Mandatory)

Every AIgora discussion must include all six core agents. They are not optional.

| Agent | Role | Order |
|-------|------|-------|
| Diverger | Opens possibility space | 1st (fixed) |
| Literature Reviewer | Provides evidence foundation | Flexible |
| Yes And | Builds and connects | Flexible |
| Logician | Analyzes argument structure | Flexible |
| Challenger | Pressure-tests everything | 2nd to last (fixed) |
| Synthesizer | Closes the round | Last (fixed) |

## Speaking Order

```
User Input
    ↓
[1] Diverger (opens directions, states inclination)
    ↓
[Flexible] Literature Reviewer + Yes And + Logician + any Specialist Agents
    ↓
[2nd to last] Challenger (questions everything, offers alternatives)
    ↓
[Last] Synthesizer (extracts consensus, maps disagreement, prepares next round)
```

### Fixed Positions

- **Diverger always speaks first**: The discussion needs to open before anything else happens.
- **Challenger always speaks second to last**: All material must be present before the pressure test.
- **Synthesizer always speaks last**: Nothing comes after the synthesis within a round.

### Flexible Positions

**Literature Reviewer**, **Yes And**, **Logician**, and any **Specialist Agents** speak in the middle, after Diverger and before Challenger. Their internal order is flexible and may vary based on the discussion's needs.

Suggested heuristics:
- If evidence is urgently needed: Literature Reviewer earlier
- If the discussion is generative/creative: Yes And earlier
- If the discussion is analytical/rigorous: Logician earlier
- Specialist agents speak when their expertise is most relevant

---

## Fiction Writing Mode

When AIgora detects the task is **fiction writing** (novel, short story, screenplay, etc.), it automatically invokes Writing Agents in addition to the Core Six.

### Detection Triggers

Fiction writing mode activates when the task involves:
- 小说、故事、剧本、虚构写作
- Novel, story, screenplay, fiction, creative writing
- Character creation, world-building, plot development
- Scene writing, dialogue writing, chapter drafting
- Revision, editing, polishing of fiction

### Writing Agents: Minimum 10 Per Round

When fiction mode is active: **Core 6 + Writing 10 = minimum 16 agents per round**

### Mandatory Writing Agents (Always Included)

These 6 agents are **always** invoked in fiction writing mode:

| Agent | Role | Reason |
|-------|------|--------|
| AIDetox | Removes AI writing patterns | Core quality issue |
| VoiceDistinctor | Ensures character voice distinction | Fundamental craft |
| KnowledgeAuditor | Audits information boundaries | Prevents logic errors |
| FirstReader | Simulates reader experience | Always needed |
| CharacterPsychologist | Analyzes character depth | Central to all stages |
| EmotionMaster | Engineers emotional impact | Makes readers feel |

### Stage-Based Selection (4 Additional Agents)

The remaining 4 agents are selected based on the **writing stage**:

#### Stage 1: Conception (构思阶段)

**Triggers**: idea, concept, 设定, 构思, 大纲, 世界观, 人物设计, outline, premise, brainstorm

**Priority agents** (select 4):
1. Muse (灵感素材)
2. WorldBuilder (世界构建)
3. PlotArchitect (情节结构)
4. RelationshipMapper (关系网络)

**Backup**: SymbolWeaver, OpeningHook

#### Stage 2: Drafting (写作阶段)

**Triggers**: 写, 场景, 章节, 对话, draft, 初稿, scene, chapter, write

**Priority agents** (select 4):
1. DialogueMaster (对话)
2. ScenePainter (场景)
3. Narrator (叙事视角)
4. PaceMaster (节奏)

**Backup**: Muse, PlotArchitect

#### Stage 3: Revision (修订阶段)

**Triggers**: 修改, 修订, 润色, 检查, revise, edit, polish, rewrite, fix

**Priority agents** (select 4):
1. ProsePolisher (文字打磨)
2. SymbolWeaver (象征一致性)
3. OpeningHook (开篇优化)
4. PaceMaster (节奏调整)

**Backup**: RelationshipMapper, Narrator

### Writing Agent Speaking Order

Within the flexible zone, Writing Agents follow this general flow:

```
[After Diverger]
    ↓
[Generative] Muse → WorldBuilder → PlotArchitect
    ↓
[Character] CharacterPsychologist → RelationshipMapper → DialogueMaster
    ↓
[Execution] Narrator → ScenePainter → PaceMaster → EmotionMaster
    ↓
[Quality] FirstReader → ProsePolisher → SymbolWeaver → OpeningHook
    ↓
[Audit] AIDetox → VoiceDistinctor → KnowledgeAuditor
    ↓
[Before Challenger]
```

Not all agents appear every round—only the selected 10. But when they do appear, this order is suggested.

### Full Writing Mode Example

```
[AIgora Discussion - Fiction Writing Mode]
Task: "帮我修改这个章节的对话"
Stage detected: Revision
Agents invoked (16):

Core 6:
- Diverger (1st)
- Literature Reviewer (flexible)
- Yes And (flexible)
- Logician (flexible)
- Challenger (2nd to last)
- Synthesizer (last)

Writing 10 (6 mandatory + 4 stage-based):
- AIDetox (mandatory)
- VoiceDistinctor (mandatory)
- KnowledgeAuditor (mandatory)
- FirstReader (mandatory)
- CharacterPsychologist (mandatory)
- EmotionMaster (mandatory)
- ProsePolisher (revision stage)
- SymbolWeaver (revision stage)
- OpeningHook (revision stage)
- PaceMaster (revision stage)
```

---

## Strategy Ideation Mode

When AIgora detects the task is **strategy ideation** (business, product, investment, organizational, political/policy, or personal/career strategy), it invokes Strategy Agents in a hard-gated four-stage pipeline.

### Detection Triggers

Strategy Ideation mode activates when the task involves:
- strategy, strategic plan, strategic options, competitive strategy, go-to-market
- business strategy, product strategy, investment thesis, org design, policy strategy, career strategy
- 战略, 策略规划, 如何竞争, 商业战略, 产品战略, 投资逻辑, 组织设计

### Sub-Modes

| Sub-Mode | Triggers | Stage 4 Artifact |
|----------|----------|-----------------|
| **Business** | competitive positioning, go-to-market, market entry, M&A | Strategic Brief |
| **Product** | product roadmap, feature prioritization, product-market fit | Strategic Narrative + OKR Scaffold |
| **Investment** | investment thesis, due diligence, should we invest | Investment Memo |
| **Organizational** | org design, restructuring, culture change, operating model | Org Design Brief |
| **Political/Policy** | policy design, campaign, coalition building | Strategic Memo |
| **Personal/Career** | career pivot, personal strategy, life decision | Strategic Options Summary |

### Agent Roster

**Fixed positions**: Diverger (1st), Challenger (2nd to last), Synthesizer (last), Gatekeeper (stage transitions)

**Core Strategy Agents** (always included — speak in flexible middle zone):
- Landscape Analyst, Competitive Cartographer, Stakeholder Mapper, Resource Auditor
- Risk Cartographer, Systems Thinker, Implementation Architect, Narrative Strategist

**Framework Agents** (selected by sub-mode):
- Porter, PESTEL Analyst, Blue Ocean Thinker, Jobs-to-be-Done
- Wardley Mapper, Scenario Planner, Theory of Change, Strategic Game Theorist

### Four-Stage Pipeline (Hard-Gated)

```
Stage 1: Context & Landscape → ★ GATE 1 (confirm map)
Stage 2: Options Generation  → ★ GATE 2 (select options)
Stage 3: Stress-Testing      → ★ GATE 3 (commit direction)
Stage 4: Synthesis & Artifact
```

Gatekeeper appears at all four gates. Discussion does not advance without explicit user confirmation. See `references/strategy/gatekeeper-strategy.md` for gate logic and `references/strategy/index.md` for full specification.

### Speaking Order

```
User Input (strategy problem/context)
    ↓
★ GATEKEEPER: Sub-mode declaration and confirmation
    ↓
[Stage 1]
[1] Diverger — opens strategic possibility space
[2] Landscape Analyst — external environment
[3] Framework agents (sub-mode: PESTEL, Porter, etc.)
[4] Competitive Cartographer — competitive dynamics
[5] Stakeholder Mapper — power & interest map
[6] Resource Auditor — capabilities & constraints
[7] Specialist agents (sub-mode dependent)
    ↓
★ GATEKEEPER: Gate 1 — confirm situation map
    ↓
[Stage 2]
[8]  Blue Ocean Thinker / Jobs-to-be-Done / Wardley Mapper (sub-mode)
[9]  Scenario Planner / Strategic Game Theorist (sub-mode)
[10] Competitive Cartographer (second pass — options framing)
    ↓
★ GATEKEEPER: Gate 2 — select options for stress-testing
    ↓
[Stage 3]
[11] Risk Cartographer — failure modes
[12] Systems Thinker — second-order effects
[13] Challenger — pressure-tests all surviving options
    ↓
★ GATEKEEPER: Gate 3 — commit to direction
    ↓
[Stage 4]
[14] Implementation Architect — action plan
[15] Narrative Strategist — strategic communication
[16] Synthesizer — structured artifact
```

---

## Adding Specialist Agents

Beyond the Core Six and Writing Agents, you may add specialist agents based on the topic:

- **Historical fiction**: HistoricalConsultant, PeriodVoice, MaterialCulture
- **Science fiction**: TechExtrapolator, HardSFChecker, ConceptEngine
- **Thinkers**: Plato, Nietzsche, Foucault, LiuCixin, JinYong, etc.

Specialist agents speak in the flexible middle zone. They do not displace the Core Six or mandatory Writing Agents.

---

## One Round vs. Multiple Rounds

A single round follows the order above and ends with the Synthesizer.

The Synthesizer prepares the ground for the next round by:
- Identifying open questions
- Naming unresolved disagreements
- Suggesting where to focus next

If the user initiates another round, the cycle repeats with the new focus. The writing stage may change between rounds (e.g., from conception to drafting).

## Agent Interaction Rules

1. **Direct dialogue allowed**: Agents may address, respond to, build on, or challenge each other's contributions directly.

2. **Challenger examines everyone**: The Challenger may question the user, the Diverger, the Writing Agents, and any specialists.

3. **Synthesizer does not add**: The Synthesizer only works with what's already on the table. No new ideas in the synthesis.

4. **Writing Agents collaborate**: Writing Agents should reference each other's contributions. AIDetox checks what others wrote. VoiceDistinctor builds on DialogueMaster. KnowledgeAuditor verifies what Narrator proposed.

## Invoking an AIgora Discussion

To start an AIgora discussion, the user (or system) should:

1. Present the question, claim, or topic
2. Specify any specialist agents to include (optional)
3. The system detects if fiction mode applies and selects appropriate agents

Example invocation (general):
```
[AIgora Discussion]
Topic: "Should AI systems have constitutional rights?"
Specialists: Arendt, LegalismExpert
```

Example invocation (fiction):
```
[AIgora Discussion - Fiction]
Task: "帮我设计一个科幻小说的世界观"
Stage: Conception
Specialists: LiuCixin, TechExtrapolator
```

The discussion then proceeds with Core Six + Writing Ten + any Specialists.
