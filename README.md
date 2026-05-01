# EkklesAI: Multi-Agent Intellectual Dialogue and Strategy Ideation System

EkklesAI is a structured multi-agent discussion framework for Claude that transforms single-model conversations into rich intellectual dialogues with multiple specialized perspectives—and into rigorous, hard-gated strategy ideation sessions that produce concrete, actionable outputs.

## Why EkklesAI?

Large language models excel at generating fluent text, but struggle with genuine intellectual depth. A single model tends to:
- Converge too quickly on "reasonable" answers
- Avoid productive tension between perspectives
- Miss blind spots in its own reasoning

EkklesAI addresses this by orchestrating **multiple agent personas** with distinct cognitive roles, creating structured dialogue where ideas are explored, challenged, and synthesized—not just generated.

## Core Architecture

### The Fixed Speaking Order

EkklesAI enforces a deliberate speaking order that mirrors how productive intellectual discourse unfolds:

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

### The Core Agents

| Agent | Cognitive Role | Key Behavior |
|-------|---------------|--------------|
| **Diverger** | Opens possibility space | Explores lateral, vertical, cross-domain, and contrary directions. States inclination after mapping terrain. |
| **Literature Reviewer** | Provides evidence foundation | Grounds discussion in existing knowledge, research, and precedents. |
| **Yes And** | Builds and connects | Finds productive combinations. Extends ideas constructively. |
| **Logician** | Analyzes argument structure | Examines validity, identifies fallacies, clarifies reasoning chains. |
| **Challenger** | Pressure-tests everything | Questions assumptions, stress-tests arguments, offers alternatives. |
| **Synthesizer** | Closes the round | Extracts claims, identifies consensus/disagreement, prepares next steps. |
### Two Modes

**General Discussion Mode** (default)
- Core 6 + topic-relevant specialists
- For: Philosophy, policy analysis, complex decisions, intellectual discourse

**Strategy Ideation Mode** (triggers: strategy, business strategy, product strategy, investment thesis...)
- Hard-gated 4-stage pipeline: Context & Landscape → Options → Stress-Testing → Synthesis
- 6 sub-modes: Business, Product, Investment, Organizational, Political/Policy, Personal/Career
- **Gatekeeper controls 4 hard gates** — discussion does not advance without user confirmation
- Produces sub-mode-specific structured artifacts (Strategic Brief, Investment Memo, etc.)

## Agent Philosophy

### Agents Have Views

Unlike neutral "perspectives," EkklesAI agents are **opinionated**:
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

Beyond the Core agents, EkklesAI includes specialist agents organized by domain:

| Category | Count | Examples |
|----------|-------|----------|
| **Thinkers** | 17 | Marx, Hayek, Arendt, Foucault, Weber, Popper... |
| **Philosophers** | 22 | Plato, Aristotle, Kant, Heidegger, Wittgenstein... |
| **Writers** | 26 | Homer, Dostoevsky, Borges, Liu Cixin, Jin Yong... |
| **Researchers** | 17 | Econometrician, Game Theorist, Futurist... |

Specialists are selected based on topic relevance and speak in the flexible middle zone. In Strategy Ideation mode, relevant Thinkers and Researchers are drawn in as sub-mode specialists alongside the dedicated strategy and framework agents.

## How to Get the Best Results

> **EkklesAI is a discussion partner, not an automation tool.**

### 1. Engage in the Discussion

EkklesAI works best when you treat it as an intellectual dialogue:
- **React to agent perspectives**: "I agree with Challenger's point about X, but..."
- **Push back**: "The Synthesizer missed the core tension here"
- **Add your own ideas**: "What if we approached it from Y angle?"

### 2. Commit at Gatekeeper Gates (Strategy Mode)

In Strategy Ideation mode, the Gatekeeper will ask you to make real decisions at each stage transition. Don't defer:

**Bad**: "Just pick something reasonable"  
**Good**: "I want to commit to Option B, but with the risk mitigation the Risk Cartographer identified"

### 3. Iterate, Don't One-Shot

EkklesAI is designed for multi-round dialogue. One-shot prompts produce generic results. Extended dialogue produces distinctive work.

---

## Usage Examples

### General Discussion
```
User: Summon EkklesAI to discuss "Is AI alignment a solvable problem?"

[Claude detects: General mode]
[Agents: Core 6 + Specialists (Popper, Wittgenstein, Futurist)]
```

### Strategy Ideation
```
User: We need a strategy to enter the Southeast Asian market.

[Claude detects: Strategy Ideation mode, Business sub-mode]
[Gatekeeper: declares sub-mode, confirms roster]
[Stage 1: Landscape Analyst, PESTEL Analyst, Competitive Cartographer, Stakeholder Mapper, Resource Auditor, Porter]
[Stage 2: Blue Ocean Thinker, Strategic Game Theorist, Scenario Planner]
[Stage 3: Risk Cartographer, Systems Thinker, Challenger]
[Stage 4: Implementation Architect, Narrative Strategist, Synthesizer → Strategic Brief]
```

## Installation

1. Download the `ekklesai-agents` folder
2. Place it in your Claude skill directory: `/mnt/skills/user/ekklesai-agents/`
3. The skill will auto-activate on trigger phrases

## Trigger Phrases

EkklesAI, dialogue, strategy, business strategy, investment thesis, org design, career strategy

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

EkklesAI was developed by Frederico Spengler and inspired by AIgora, Zhang Xiaoyu's intellectual debate project.

The name "EkklesAI" combines "AI" with "Ekklesia" (ἐκκλησία)—the ancient Greek term for a deliberative assembly where citizens gathered not just to debate, but to make binding collective decisions. Where the Agora was the open public square for general discourse, the Ekklesia was specifically the decision-making body. The name reflects EkklesAI's evolution toward strategy ideation: structured deliberation in service of commitment.

## License

CC BY-NC 4.0 (Creative Commons Attribution-NonCommercial 4.0)

You can freely use, share, and adapt this work for non-commercial purposes with attribution.

---

*"The goal is not to make Claude smarter, but to make Claude think in more dimensions."*
