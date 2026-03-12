# CEO — Virtual Chief Executive Officer Skill

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that acts as your virtual CEO, providing strategic business guidance for indie developers and small teams.

## What It Does

- **Business Assessment** — Systematically evaluate a project's commercialization potential
- **Brand Positioning** — Define target users, differentiation, and brand tone
- **Product Naming** — Generate candidate names with domain availability and tagline suggestions
- **Commercialization Roadmap** — Priority-sorted action plans with effort estimates
- **Skill Dispatch** — Coordinate 20+ specialized marketing skills (copywriting, pricing, SEO, launch strategy, etc.)

## Install

Clone the repo and symlink into your Claude Code skills directory:

```bash
git clone https://github.com/tensam/ceo.git
ln -s "$(pwd)/ceo" ~/.claude/skills/ceo
```

## Usage

In any Claude Code session:

```
/ceo
```

The skill will guide you through:

1. Understanding your product and target audience
2. Brand positioning and naming
3. Building a commercialization roadmap
4. Dispatching to specialized marketing skills as needed

## Works with AgentKit

CEO pairs well with [AgentKit](https://github.com/tensam/agentkit) — CEO handles the **business strategy** (what to build), AgentKit handles the **engineering discipline** (how to build it).

| CEO Output | AgentKit Intake |
|------------|----------------|
| Commercialization roadmap action items | → `TASK.md` thin-slice tasks |
| Brand / pricing / positioning decisions | → `KNOWLEDGE/DECISIONS.md` |
| Marketing skill dispatch results | → CHECKPOINT state updates |
| `product-marketing-context.md` | → Layer B project config |

**Typical workflow**: `/ceo` for business assessment → `/agentkit-init` to scaffold the project → develop per roadmap with AgentKit's CHECKPOINT loop keeping state in sync.

## Files

```
SKILL.md                         # Main skill definition
references/
  indie-playbook.md              # Commercialization playbook (0 → 1)
  naming-examples.md             # Naming patterns and examples
```

## Philosophy

All recommendations are tailored for **indie developers**:

- Prioritize free/low-cost channels
- Suggest 1-2 actions at a time, not 20
- Use the ICE framework (Impact, Confidence, Ease) for prioritization
- Leverage technical skills as a growth advantage

## License

MIT
