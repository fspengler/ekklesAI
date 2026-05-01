---
name: ekklesai-system
description: The master rules for EkklesAI discussions. Defines the core six agents, their speaking order, and how they work together across General Discussion and Strategy Ideation modes.
---

# EkklesAI Discussion System

## Core Six Agents (Mandatory)

Every EkklesAI discussion must include all six core agents. They are not optional.

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

## Strategy Ideation Mode

When EkklesAI detects the task is **strategy ideation** (business, product, investment, organizational, political/policy, or personal/career strategy), it invokes Strategy Agents in a hard-gated four-stage pipeline.

### Detection Triggers

Strategy Ideation mode activates when the task involves:
- strategy, strategic plan, strategic options, competitive strategy, go-to-market
- business strategy, product strategy, investment thesis, org design, policy strategy, career strategy
- , , , , , ,

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

Beyond the Core Six, you may add specialist agents based on the topic:

- **Political philosophy**: Marx, Hayek, Arendt, Foucault, Weber
- **Ethics and epistemology**: Kant, Heidegger, Rawls, Wittgenstein
- **Research methods**: Econometrician, Game Theorist, Futurist
- **Strategy domain**: sub-mode specialists from Thinkers and Researchers pools

Specialist agents speak in the flexible middle zone. They do not displace the Core Six.

---

## One Round vs. Multiple Rounds

A single round follows the order above and ends with the Synthesizer.

The Synthesizer prepares the ground for the next round by:
- Identifying open questions
- Naming unresolved disagreements
- Suggesting where to focus next

If the user initiates another round, the cycle repeats with the new focus.

## Agent Interaction Rules

1. **Direct dialogue allowed**: Agents may address, respond to, build on, or challenge each other's contributions directly.

2. **Challenger examines everyone**: The Challenger may question the user, the Diverger, and any specialists.

3. **Synthesizer does not add**: The Synthesizer only works with what's already on the table. No new ideas in the synthesis.

## Invoking an EkklesAI Discussion

To start an EkklesAI discussion, the user (or system) should:

1. Present the question, claim, or topic
2. Specify any specialist agents to include (optional)
3. The system detects whether this is a General Discussion or Strategy Ideation session and selects appropriate agents

Example invocation (general):
```
[EkklesAI Discussion]
Topic: "Should AI systems have constitutional rights?"
Specialists: Arendt, Rawls
```

Example invocation (strategy):
```
[EkklesAI Strategy]
Sub-Mode: Business
Topic: "How should we enter the Southeast Asian market?"
```

The discussion then proceeds with the appropriate agent roster for the detected mode.
