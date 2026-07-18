# skills-finance

Claude / Agent **skills** library by **Poorvith M P**.

- Version: **v0.2**
- Last updated: **July 2026**
- License: **MIT**
- Skills in this repo: **9**

Part of the **[open-claude-skills](https://github.com/prvthmpcypher/open-claude-skills)** multi-repo hub.

## Install

### Claude Code
```bash
# copy one skill
cp -R skills/<skill-id> ~/.claude/skills/<skill-id>
# or project-local
cp -R skills/<skill-id> .claude/skills/<skill-id>
```

### Claude.ai
Zip a single `skills/<skill-id>` folder and upload via **Settings → Capabilities → Skills**.

## Skill index

| Skill ID | Title |
|----------|-------|
| `bookkeeper-and-controller` | Bookkeeper & Controller |
| `budget-expense-auditor` | Budget & Expense Auditor |
| `cap-table-fundraising-modeler` | Cap Table & Fundraising Modeler |
| `crypto-tax-specialist` | Crypto Tax Specialist |
| `financial-analyst` | Financial Analyst |
| `fp-and-a-analyst` | FP&A Analyst |
| `insurance-actuary-analyst` | Insurance & Actuarial Analyst |
| `investment-researcher` | Investment Researcher |
| `tax-strategist` | Tax Strategist |

## Structure

Each skill follows skill-creator conventions:

```text
skills/<skill-id>/
├── SKILL.md
├── references/NOTE.md   # empty tips for future progressive disclosure
└── assets/NOTE.md       # empty tips for future templates
```

## Author

Copyright (c) 2026 Poorvith M P
Follow the build: [@poorvith_mp](https://x.com/poorvith_mp)
