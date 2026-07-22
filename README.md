# Validate Idea / 想法拷问（多专家版）

A Claude Code skill that runs 5 parallel expert agents to stress-test a business/product idea before committing time.

## How it works

```
User describes idea
      │
      ▼
┌─ Main Agent ─────────────────────────────────────┐
│ 1. Gather input (5 questions)                      │
│ 2. Launch 5 experts in parallel                    │
│ 3. Cross-validate → Verdict                        │
└─────────────────────────────────────────────────┘
      │         │         │         │         │
      ▼         ▼         ▼         ▼         ▼
  🎯 RAT     👂 Mom    🔍 竞品   💰 投资人  🧪 价值主张
  Hunter    Test      穷举师   质询官   拷问官
```

## 5 Experts

| Expert | Framework | Focus |
|--------|-----------|-------|
| 🎯 RAT Hunter | Riskiest Assumption Test | Find top 3 fatal assumptions + design ≤$100/≤2wk experiments |
| 👂 Mom Test Interrogator | Rob Fitzpatrick's The Mom Test | Write interview questions that don't mention your product |
| 🔍 Competitor Exhauster | Exhaustive search | Direct/indirect/alternative/platform/AI — no such thing as no competition |
| 💰 Investor Inquisitor | Angel investor lens | Painkiller vs vitamin, timing, moat, unit economics, founder fit |
| 🧪 VP Stress Tester | Value Proposition Design | Jobs-Pains-Gains + 10 critical questions |

## Verdicts

- 🟢 **Go** — Highest-risk assumption identified, with a concrete test
- 🟡 **Narrow** — Cut scope to a specific segment, retest
- 🔴 **Kill** — Fatal flaw found, don't pursue

## Install

Copy `SKILL.md` to `~/.claude/skills/validate-idea/SKILL.md`

## Usage

```
/validate-idea
```

Or describe your idea and Claude will ask clarifying questions before launching the experts.

## Credits

Inspired by:
- Riskiest Assumption Test (RAT)
- Rob Fitzpatrick's *The Mom Test*
- Alexander Osterwalder's *Value Proposition Design*
- Angel investing due diligence frameworks
