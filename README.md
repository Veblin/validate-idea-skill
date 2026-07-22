# Validate Idea (Multi-Expert Adversarial Review)

A Claude Code skill that runs 5 parallel expert agents to stress-test a business/product idea before committing time.

## How It Works

```
User describes idea
      │
      ▼
┌─ Main Agent ─────────────────────────────────────┐
│ 1. Gather input (5 clarifying questions)           │
│ 2. Launch 5 experts in parallel                    │
│ 3. Cross-validate findings → Verdict               │
└─────────────────────────────────────────────────┘
      │         │         │         │         │
      ▼         ▼         ▼         ▼         ▼
  🎯 RAT     👂 Mom    🔍 Competitor 💰 Investor 🧪 Value Prop
  Hunter    Test       Exhauster    Inquisitor  Stress Tester
```

## The 5 Experts

| Expert | Framework | Focus |
|--------|-----------|-------|
| 🎯 RAT Hunter | Riskiest Assumption Test | Identify top 3 fatal assumptions + design ≤2wk / ≤$100 validation experiments |
| 👂 Mom Test Interrogator | *The Mom Test* by Rob Fitzpatrick | Write interview questions that probe past behavior, never mentioning your product |
| 🔍 Competitor Exhauster | Exhaustive multi-layer search | Direct, indirect, alternative, platform risk, AI substitution — no such thing as no competition |
| 💰 Investor Inquisitor | Angel investor due diligence | Painkiller vs. vitamin, timing, moat dynamics, unit economics, founder-fit |
| 🧪 Value Prop Stress Tester | *Value Proposition Design* by Osterwalder | Jobs-Pains-Gains breakdown + 10 critical pass/fail questions |

## Verdicts

| Verdict | Meaning |
|:-------:|---------|
| 🟢 **Pursue** | Highest-risk assumption identified with a concrete validation experiment |
| 🟡 **Narrow** | Cut scope to a specific segment or feature, then re-test |
| 🔴 **Kill** | Fatal flaw found — do not pursue this direction |

## Install

```bash
mkdir -p ~/.claude/skills/validate-idea
cp SKILL.md ~/.claude/skills/validate-idea/SKILL.md
```

## Usage

```
/validate-idea
```

Or just describe your idea — Claude will ask clarifying questions before launching the experts.

## Language Support

The skill automatically matches the user's language. Write in Chinese, get responses in Chinese. Write in English, get responses in English.

## Credits

Inspired by:
- **Riskiest Assumption Test (RAT)** — find what kills you fastest
- **The Mom Test** by Rob Fitzpatrick — how to talk to customers without lying to yourself
- **Value Proposition Design** by Alexander Osterwalder — Jobs-Pains-Gains framework
- **Angel investing due diligence** — the questions investors actually ask before writing checks
