---
name: runway-planning
last_reviewed: 2026-09-06
group: Modelling
description: >-
  Work out burn rate, months of runway, which cuts buy how long, and when the raise has to start.
  Use when calculating net burn, zero-cash dates, or default-alive plans.
---

# Runway Planning

Runway planning is insolvency avoidance. Runway modeling requires calculating fully-loaded gross burn and net burn, establishing deterministic Zero Cash Dates (ZCD), evaluating the "Default Alive vs Default Dead" framework, and structuring phased cost-reduction playbooks triggered by explicit cash thresholds.

## 1. Burn Rate & Runway Formulations

Calculate financial runway with mathematical precision:
- **Gross Monthly Burn**:
  $$\text{Gross Burn} = \text{Total Monthly Cash Outflows (Payroll + Hosting + Rent + Marketing + Tooling)}$$
- **Net Monthly Burn**:
  $$\text{Net Burn} = \text{Gross Burn} - \text{Total Monthly Cash Collections}$$
  *Rule*: Use cash receipts, not accrual booked revenue, to calculate Net Burn.
- **Months of Runway**:
  $$\text{Months of Runway} = \frac{\text{Current Cash Balance} - \text{Restricted/Reserve Buffer}}{\text{Average Net Monthly Burn (Trailing 3 Months)}}$$
- **Zero Cash Date (ZCD)**: The exact calendar date when the operating cash account reaches zero.

## 2. The Default Alive vs. Default Dead Framework (Paul Graham)
Evaluate company trajectory before planning capital allocation:
- **Default Alive**: If current revenue growth rate continues without hiring more staff or raising more capital, will the company reach cash flow profitability before running out of money?
- **Default Dead**: At the current burn rate and revenue trajectory, the company will run out of cash before reaching breakeven, requiring external financing to survive.
- *Strategic Mandate*: If Default Dead, the executive team must immediately either: (a) accelerate unit-profitable growth, or (b) reduce burn to cross into Default Alive territory.

## 3. The Runway Defense Trigger Framework
Establish pre-committed executive triggers tied to months of remaining runway:

| Remaining Runway | Status Stage | Mandatory Executive Actions |
|---|---|---|
| **> 18 Months** | Green (Growth Zone) | Standard operating plan; strategic hiring within approved budget envelopes. |
| **12 – 18 Months** | Yellow (Prepare Raise) | Prepare fundraising materials; stress-test BVA variance; tighten discretionary spend. |
| **9 – 12 Months** | Amber (Active Raise) | Launch formal equity/debt fundraising round; freeze non-revenue headcount. |
| **6 Months** | Red (Cost Cut Trigger) | Execute Phase 1 cost cuts: freeze all hiring, eliminate non-essential software, cut paid marketing. |
| **< 3 Months** | Black (Survival Plan) | Execute Phase 2 cost cuts: across-the-board payroll reductions, wind-down plan, M&A sale. |

## 4. Scenario Sensitivity Modeling
Model three distinct financial scenarios:
1. **Status Quo (Base Case)**: Current net burn rate projected forward with modest planned growth.
2. **Fundraising Runway Requirement**: A standard venture capital fundraising process requires **6 to 9 months** from first meeting to cash in bank. If you begin raising with <6 months of runway, you enter negotiations with zero leverage.
3. **Emergency Zero-Growth Budget**: Demonstrates the exact line-item cuts required to achieve cash flow break-even within 60 days.

## Critical Rules
1. Never calculate runway using projected, unclosed revenue increases; runway is measured against guaranteed cash.
2. The fundraising countdown begins when cash hits 12 months, not 6 months.
3. Include severance costs, lease termination penalties, and working capital lag when modeling emergency expense reductions.

## Verification Checklist
- [ ] Net burn calculated using cash collections rather than accrual revenue.
- [ ] Trailing 3-month average burn used to smooth one-off expenditure anomalies.
- [ ] Exact Zero Cash Date (ZCD) calculated and visible on executive dashboards.
- [ ] Default Alive / Default Dead status evaluated and communicated to the board.
- [ ] Phased cost-reduction playbook documented with explicit trigger dates.

## Anti-Patterns
- NEVER assume an existing investor will provide an emergency insider bridge round without a signed term sheet.
- NEVER wait until 4 months of runway remain before initiating cost reductions.
- NEVER include accounts receivable in immediate cash runway calculations without applying a bad-debt discount.
