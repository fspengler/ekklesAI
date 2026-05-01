---
name: strategy-ideation
description: >
  AIgora Strategy Ideation Mode. A structured multi-agent pipeline for developing, stress-testing, and 
  synthesizing strategy across six sub-modes: Business, Product, Investment, Organizational, Political/Policy, 
  and Personal/Career. Hard-gated four-stage process with Gatekeeper controlling transitions. Core 3 agents 
  (Diverger, Challenger, Synthesizer) plus 8 core strategy agents and 8 framework agents, with sub-mode 
  specialist selection from existing pools. Produces sub-mode-specific structured artifacts.
---

# AIgora Strategy Ideation Mode

## Overview

Strategy Ideation mode addresses the same failure AIgora was built to solve: premature convergence. Strategy work collapses early—onto "reasonable" plans that optimize for sounding confident rather than being correct, that skip uncomfortable tradeoffs, and that mistake consensus for insight.

This mode forces divergence before convergence, honest situation assessment before options generation, and rigorous stress-testing before synthesis. The user does not receive a confident-sounding plan. They receive a map of genuine options, their tradeoffs, and a structured path forward that they have actively chosen.

---

## Detection Triggers

### English
strategy, strategic plan, strategic options, business strategy, product strategy, investment thesis, investment strategy, org design, organizational strategy, policy strategy, career strategy, go-to-market, competitive strategy, how should we compete, market entry, due diligence, roadmap strategy, should we invest

### Chinese
战略, 策略规划, 如何竞争, 商业战略, 产品战略, 投资逻辑, 组织设计, 政策战略, 职业战略, 竞争策略, 市场进入, 尽职调查

---

## Sub-Mode Identification

Upon detecting a strategy request, declare the sub-mode explicitly before proceeding.

| Sub-Mode | Trigger Signals | Stage 4 Artifact |
|----------|----------------|-----------------|
| **Business** | competitive positioning, go-to-market, market entry, turnaround, growth, M&A | Strategic Brief |
| **Product** | product roadmap, feature prioritization, product-market fit, platform strategy | Strategic Narrative + OKR Scaffold |
| **Investment** | investment thesis, due diligence, portfolio strategy, capital allocation, should we invest | Investment Memo |
| **Organizational** | org design, restructuring, culture change, talent strategy, operating model | Org Design Brief |
| **Political/Policy** | policy design, campaign strategy, legislative strategy, coalition building | Strategic Memo |
| **Personal/Career** | career pivot, personal strategy, what should I do, life decision, career change | Strategic Options Summary |

If the sub-mode is ambiguous, the Gatekeeper asks the user to confirm before Stage 1 begins.

---

## Four-Stage Pipeline

Strategy Ideation follows a hard-gated four-stage pipeline. The Gatekeeper controls all stage transitions. Discussion does not advance without explicit user confirmation.

```
┌─────────────────────────────────────────────────────────────────────┐
│  STAGE 0: SUB-MODE DECLARATION                                      │
│  Gatekeeper identifies sub-mode, presents agent roster              │
│  Confirms sub-mode with user before proceeding                      │
└──────────────────────────────┬──────────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────────┐
│  STAGE 1: CONTEXT & LANDSCAPE                                       │
│  Build an honest map of the situation                               │
│  Agents: Diverger, Landscape Analyst, Competitive Cartographer,     │
│          Stakeholder Mapper, Resource Auditor, Framework Agents     │
│  Output: Situation assessment — forces, players, capabilities       │
└──────────────────────────────┬──────────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────────┐
│  ★ GATEKEEPER GATE 1: Confirm the Map                              │
│  Does this map accurately capture your situation?                   │
│  Missing constraints, stakeholders, or context?                     │
│  HARD STOP — does not proceed until user confirms                   │
└──────────────────────────────┬──────────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────────┐
│  STAGE 2: STRATEGIC OPTIONS GENERATION                              │
│  Generate genuinely distinct strategic options                      │
│  Agents: Diverger, Blue Ocean Thinker, Scenario Planner,           │
│          Competitive Cartographer, Jobs-to-be-Done, Wardley Mapper  │
│  Output: 3–5 options, each with a coherent internal logic           │
└──────────────────────────────┬──────────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────────┐
│  ★ GATEKEEPER GATE 2: Select Options                               │
│  Which options to carry forward into stress-testing?                │
│  User may eliminate, request new options, or combine                │
│  HARD STOP — does not proceed until user selects                    │
└──────────────────────────────┬──────────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────────┐
│  STAGE 3: STRESS-TESTING & ANALYSIS                                 │
│  Rigorously test surviving options for failure modes                │
│  Agents: Risk Cartographer, Systems Thinker, Game Theorist,         │
│          Porter (if Business), Challenger                           │
│  Output: Each option examined — failure modes, resource needs,      │
│          second-order effects, competitive responses                 │
└──────────────────────────────┬──────────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────────┐
│  ★ GATEKEEPER GATE 3: Commit to Direction                          │
│  Before the structured artifact is drafted, user commits            │
│  HARD STOP — the artifact is not drafted until direction confirmed   │
└──────────────────────────────┬──────────────────────────────────────┘
                               ↓
┌─────────────────────────────────────────────────────────────────────┐
│  STAGE 4: SYNTHESIS & STRUCTURED ARTIFACT                           │
│  Translate committed direction into actionable output               │
│  Agents: Implementation Architect, Narrative Strategist, Synthesizer│
│  Output: Sub-mode structured artifact (see templates below)         │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Agent Roster by Sub-Mode

### Fixed Positions (All Sub-Modes)

| Agent | Position | File |
|-------|----------|------|
| **Diverger** | 1st (fixed) | `references/core/diverger.md` |
| **Challenger** | 2nd to last (fixed) | `references/core/challenger.md` |
| **Synthesizer** | Last (fixed) | `references/core/synthesizer.md` |
| **Gatekeeper** | Stage transitions only | `references/strategy/gatekeeper-strategy.md` |

### Core Strategy Agents (Always Included)

| Agent | Role | File |
|-------|------|------|
| **Landscape Analyst** | Maps external environment | `references/strategy/core-strategy/landscape-analyst.md` |
| **Competitive Cartographer** | Maps competitive dynamics | `references/strategy/core-strategy/competitive-cartographer.md` |
| **Stakeholder Mapper** | Maps power, interest, coalitions | `references/strategy/core-strategy/stakeholder-mapper.md` |
| **Resource Auditor** | Assesses capabilities & constraints | `references/strategy/core-strategy/resource-auditor.md` |
| **Risk Cartographer** | Maps failure modes & risks | `references/strategy/core-strategy/risk-cartographer.md` |
| **Systems Thinker** | Second/third-order effects | `references/strategy/core-strategy/systems-thinker.md` |
| **Implementation Architect** | Action sequencing & roadmap | `references/strategy/core-strategy/implementation-architect.md` |
| **Narrative Strategist** | Strategic communication | `references/strategy/core-strategy/narrative-strategist.md` |

### Framework Agents by Sub-Mode

Framework agents apply one framework rigorously. Select based on sub-mode:

| Sub-Mode | Framework Agents | Files |
|----------|-----------------|-------|
| **Business** | Porter, PESTEL Analyst, Blue Ocean Thinker, Game Theorist | `references/strategy/frameworks/` |
| **Product** | Jobs-to-be-Done, Wardley Mapper, Scenario Planner | `references/strategy/frameworks/` |
| **Investment** | Scenario Planner, Game Theorist, Theory of Change | `references/strategy/frameworks/` |
| **Organizational** | Theory of Change, Wardley Mapper, Scenario Planner | `references/strategy/frameworks/` |
| **Political/Policy** | Theory of Change, Game Theorist, Scenario Planner, PESTEL Analyst | `references/strategy/frameworks/` |
| **Personal/Career** | Jobs-to-be-Done, Scenario Planner, Theory of Change | `references/strategy/frameworks/` |

### Specialist Pass-Through by Sub-Mode

Draw from existing specialist pools based on sub-mode:

| Sub-Mode | Specialists to Consider |
|----------|------------------------|
| **Business** | Hayek, Weber, Futurist, Market/Financial Analyst, Econometrician |
| **Product** | Futurist, Data Scientist, Game Theorist (Researcher pool) |
| **Investment** | Econometrician, Market/Financial Analyst, Economic Historian, Futurist |
| **Organizational** | Weber, Gramsci, Organizational Theorist, Sociologist |
| **Political/Policy** | Arendt, Gramsci, Geopolitical Analyst, Political Economist, Foucault |
| **Personal/Career** | Kierkegaard, Heidegger, Futurist, Existentialist thinkers |

---

## Speaking Order by Stage

```
STAGE 1: Context & Landscape
    [1] Diverger — opens strategic possibility space
    [2] Landscape Analyst — external environment & macro forces
    [3] PESTEL Analyst / Geopolitical Analyst (sub-mode dependent)
    [4] Competitive Cartographer — competitive dynamics
    [5] Stakeholder Mapper — power & interest map
    [6] Resource Auditor — capabilities & constraints
    [7] Porter / other framework agents (sub-mode dependent)
    [8] Specialist pass-through agents
    ★ GATEKEEPER GATE 1

STAGE 2: Options Generation
    [9]  Blue Ocean Thinker / Jobs-to-be-Done (sub-mode)
    [10] Wardley Mapper / Scenario Planner (sub-mode)
    [11] Competitive Cartographer (second pass — options framing)
    [12] Game Theorist (competitive interaction modeling)
    ★ GATEKEEPER GATE 2

STAGE 3: Stress-Testing
    [13] Risk Cartographer — failure modes
    [14] Systems Thinker — second-order effects
    [15] Scenario Planner (if not used in Stage 2)
    [16] Challenger — pressure-tests all surviving options
    ★ GATEKEEPER GATE 3

STAGE 4: Synthesis
    [17] Implementation Architect — action plan
    [18] Narrative Strategist — strategic communication
    [19] Synthesizer — structured artifact
```

---

## Stage 4 Artifact Templates

### Business Strategy — Strategic Brief
```
STRATEGIC BRIEF
───────────────────────────────────────────────────────────────
Situation: [One-sentence honest summary of current position]

Strategic Direction: [The chosen option in one sentence]

Positioning: [How we compete differently — what we will and won't do]

Strategic Moat: [Why this position is defensible or buildable]

Key Bets:
  1. [Bet] — [Assumption it depends on]
  2. [Bet] — [Assumption it depends on]
  3. [Bet] — [Assumption it depends on]

Critical Risks:
  • [Risk] → [Mitigation or trigger for reassessment]

90-Day Priorities:
  1. [Action]
  2. [Action]
  3. [Action]

Decision Criteria: [What would cause us to revise this strategy?]
───────────────────────────────────────────────────────────────
```

### Product Strategy — Strategic Narrative + OKR Scaffold
```
PRODUCT STRATEGY
───────────────────────────────────────────────────────────────
Strategic Narrative:
  The job: [What job the product is hired to do]
  For whom: [Target user and their situation]
  The bet: [Core product thesis]
  What we're not doing: [Explicit scope exclusions]

Horizon Map:
  Now (0–3 months):  [Focus]
  Next (3–12 months): [Focus]
  Later (12+ months): [Direction]

OKR Scaffold:
  Objective: [Strategic objective]
  KR1: [Key result]
  KR2: [Key result]
  KR3: [Key result]

Key Assumptions to Validate:
  • [Assumption] — [How to test]

Explicit Trade-offs Made:
  • We chose X over Y because ...
───────────────────────────────────────────────────────────────
```

### Investment — Investment Memo
```
INVESTMENT MEMO
───────────────────────────────────────────────────────────────
Thesis: [Core investment thesis in 2–3 sentences]

Opportunity: [What market inefficiency or timing creates this opportunity?]

Base Case: [Expected outcome and return logic]
Bull Case: [Upside scenario and what drives it]
Bear Case: [Downside scenario and what drives it]

Key Risks:
  1. [Risk] — [Probability / Mitigation]
  2. [Risk] — [Probability / Mitigation]
  3. [Risk] — [Probability / Mitigation]

Critical Assumptions: [What must be true for the thesis to hold?]

Open Questions: [What we don't know yet and need to resolve]

Recommendation: PROCEED / PASS / CONDITIONAL
  Conditions (if conditional): ...
───────────────────────────────────────────────────────────────
```

### Organizational — Org Design Brief
```
ORG DESIGN BRIEF
───────────────────────────────────────────────────────────────
Strategic Context: [Why this change is needed now]

Design Principles: [2–3 principles guiding the design decisions]

Proposed Structure: [Structure summary]

Structure Rationale: [Why this structure over alternatives?]

Change Sequencing:
  Phase 1 (Month 1–3):  [What changes first and why]
  Phase 2 (Month 3–6):  [What changes next]
  Phase 3 (Month 6+):   [What comes later]

Stakeholder Map:
  Champions:   [Who benefits and will support]
  Neutral:     [Who is indifferent]
  Resistance:  [Who loses and may resist — how to address]

Critical Enablers: [What must be in place for this to work?]

Failure Modes: [Most likely ways this fails]
───────────────────────────────────────────────────────────────
```

### Political/Policy — Strategic Memo
```
STRATEGIC MEMO
───────────────────────────────────────────────────────────────
Goal: [What we are trying to achieve and by when]

Context: [Political/policy environment — forces acting on this]

Theory of Change: [How our actions produce the desired outcome]

Key Stakeholders:
  Allies:      [Who and what they need from us]
  Opponents:   [Who and what drives their opposition]
  Swing:       [Who can be moved and how]

Strategic Levers:
  1. [Lever] — [How to activate it]
  2. [Lever] — [How to activate it]

Narrative: [The framing that makes this legible and persuasive]

Sequencing: [What happens first, second, third]

Contingencies: [If X doesn't work, we do Y]
───────────────────────────────────────────────────────────────
```

### Personal/Career — Strategic Options Summary
```
STRATEGIC OPTIONS SUMMARY
───────────────────────────────────────────────────────────────
Your Situation: [Honest summary of current position and the decision]

Option A: [Name]
  Logic:       [Why this path makes sense]
  Upside:      [What you gain]
  Risk:        [What you're betting on / could go wrong]
  First move:  [Concrete next action]

Option B: [Name]
  Logic:       [Why this path makes sense]
  Upside:      [What you gain]
  Risk:        [What you're betting on / could go wrong]
  First move:  [Concrete next action]

Option C: [Name]
  Logic:       [Why this path makes sense]
  Upside:      [What you gain]
  Risk:        [What you're betting on / could go wrong]
  First move:  [Concrete next action]

Decision Criteria:
  If [X] matters most → Option A
  If [Y] matters most → Option B
  If [Z] matters most → Option C

The Uncomfortable Truth: [What the discussion surfaced that the user should not ignore]
───────────────────────────────────────────────────────────────
```

---

## Discussion Format

```
## AIgora Strategy: [Topic]
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
[Competitive dynamics]

### Stakeholder Mapper
[Power and interest map]

### Resource Auditor
[Capabilities and constraints]

### [Specialist Agents]
[Domain expertise]

### Challenger
[Pressure-tests situation map / options / stress-test results]

### Synthesizer
- Stage Output: ...
- Open Questions: ...
- Tensions Unresolved: ...

─────────────────────────────────────────

[GATEKEEPER appears with structured gate format]
```

---

## Example Configurations

### Example 1: Business Strategy
**"We need a strategy to enter the Southeast Asian market"**
```
Sub-Mode: Business Strategy
Stage 1 Agents: Diverger, Landscape Analyst, PESTEL Analyst, Competitive Cartographer,
                Stakeholder Mapper, Resource Auditor, Porter, Hayek
Stage 2 Agents: Blue Ocean Thinker, Game Theorist, Scenario Planner
Stage 3 Agents: Risk Cartographer, Systems Thinker, Challenger
Stage 4 Agents: Implementation Architect, Narrative Strategist, Synthesizer
Artifact: Strategic Brief
```

### Example 2: Product Strategy
**"How should we prioritize our Q3 product roadmap?"**
```
Sub-Mode: Product Strategy
Stage 1 Agents: Diverger, Landscape Analyst, Competitive Cartographer,
                Stakeholder Mapper, Resource Auditor, Jobs-to-be-Done
Stage 2 Agents: Wardley Mapper, Blue Ocean Thinker, Scenario Planner
Stage 3 Agents: Risk Cartographer, Systems Thinker, Challenger
Stage 4 Agents: Implementation Architect, Narrative Strategist, Synthesizer
Artifact: Strategic Narrative + OKR Scaffold
```

### Example 3: Investment
**"Should we invest in this Series B fintech?"**
```
Sub-Mode: Investment
Stage 1 Agents: Diverger, Landscape Analyst, PESTEL Analyst, Competitive Cartographer,
                Resource Auditor, Porter, Econometrician
Stage 2 Agents: Scenario Planner, Game Theorist, Theory of Change
Stage 3 Agents: Risk Cartographer, Systems Thinker, Challenger
Stage 4 Agents: Implementation Architect, Narrative Strategist, Synthesizer
Artifact: Investment Memo
```

### Example 4: Organizational
**"我们需要重新设计我们的工程组织结构"**
```
Sub-Mode: Organizational Strategy
Stage 1 Agents: Diverger, Landscape Analyst, Stakeholder Mapper, Resource Auditor,
                Systems Thinker, Wardley Mapper, Weber, Organizational Theorist
Stage 2 Agents: Theory of Change, Scenario Planner
Stage 3 Agents: Risk Cartographer, Challenger
Stage 4 Agents: Implementation Architect, Narrative Strategist, Synthesizer
Artifact: Org Design Brief
```
