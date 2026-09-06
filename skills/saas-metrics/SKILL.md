---
name: saas-metrics
group: Modelling
description: >-
  Track MRR, ARR, cohort revenue, net revenue retention, and recognise revenue on the right
  period. Use when tracking ARR/MRR, Net Revenue Retention, CAC payback, or churn.
---

# SaaS Metrics

Software-as-a-Service economics are defined by recurring revenue retention and cohort velocity. Managing SaaS operations requires tracking Annual/Monthly Recurring Revenue (ARR/MRR) movements, calculating Net Revenue Retention (NRR), applying ASC 606 revenue recognition, and benchmarking against the Rule of 40.

## 1. The ARR / MRR Waterfall Architecture

Recurring revenue must be decomposed into five discrete, reconcilable movements:
$$\text{Ending ARR} = \text{Beginning ARR} + \text{New ARR} + \text{Expansion ARR} - \text{Contraction ARR} - \text{Churned ARR}$$

- **New ARR**: Revenue from newly closed customer accounts.
- **Expansion ARR**: Additional revenue from existing accounts (seat expansions, tier upgrades, cross-sells).
- **Contraction ARR**: Revenue lost from existing customers downgrading tiers or reducing seats without fully churning.
- **Churned ARR**: Total revenue lost from customers cancelling contracts completely.

## 2. Retention Metrics: NRR vs. GRR
Retention is the single greatest predictor of software enterprise valuation:

### A. Net Revenue Retention (NRR)
Measures the percentage of recurring revenue retained from an existing cohort over a 12-month period, including expansion:
$$\text{NRR} = \frac{\text{Starting ARR} + \text{Expansion} - \text{Contraction} - \text{Churn}}{\text{Starting ARR}} \times 100$$
- *Benchmark*:
  - `< 100%`: Leaky bucket; company must constantly acquire new logos just to stay flat.
  - `105% – 115%`: Solid B2B mid-market software health.
  - `> 125%`: World-class enterprise expansion engine (Snowflake, Datadog cohort tier).

### B. Gross Revenue Retention (GRR)
Measures retained revenue excluding expansion; caps out at 100%:
$$\text{GRR} = \frac{\text{Starting ARR} - \text{Contraction} - \text{Churn}}{\text{Starting ARR}} \times 100$$
- *Benchmark*: High-performing enterprise SaaS maintains GRR `> 90%` (B2B) or `> 80%` (SMB).

## 3. Revenue Recognition Discipline (ASC 606 / IFRS 15)
Recognize revenue when performance obligations are satisfied, not when invoiced:
- **Contract Billing vs Revenue**: A $120,000 annual upfront contract signed on Jan 1 is invoiced and collected immediately.
  - Cash Balance increases by $120,000 on Jan 1.
  - Deferred Revenue Liability increases by $120,000 on Jan 1.
  - Recognized Revenue is booked at $10,000 per month across each of the 12 calendar months.

## 4. The Rule of 40 & Magic Number
- **The Rule of 40**: A SaaS company's combined growth rate and profit margin should equal or exceed 40%:
  $$\text{Rule of 40 Score} = \text{Year-over-Year ARR Growth Rate (\%)} + \text{Free Cash Flow Margin (\%)} $$
  *Score > 40%* represents top-quartile operational efficiency.
- **SaaS Magic Number (Sales Efficiency)**:
  $$\text{Magic Number} = \frac{(\text{Quarterly ARR}_t - \text{Quarterly ARR}_{t-1}) \times 4}{\text{Quarterly Sales \& Marketing Expense}_{t-1}}$$
  - *< 0.75x*: Sales efficiency lagging; do not accelerate go-to-market spend.
  - *> 1.0x*: Exceptional sales efficiency; pour capital into customer acquisition.

## Critical Rules
1. Never include one-time professional services or setup fees inside ARR or MRR calculations.
2. Calculate churn based on annualized revenue (revenue churn), not solely customer count (logo churn).
3. Do not count contracted but unlaunched accounts as live ARR; recognize ARR only upon service provisioning.

## Verification Checklist
- [ ] ARR waterfall reconciles: Beginning + New + Expansion - Contraction - Churn == Ending.
- [ ] One-off services and non-recurring fees excluded from MRR/ARR totals.
- [ ] Net Revenue Retention (NRR) and Gross Revenue Retention (GRR) tracked across monthly cohorts.
- [ ] ASC 606 revenue recognition matches monthly performance obligation schedules.
- [ ] Rule of 40 and Sales Magic Number calculated quarterly.

## Anti-Patterns
- NEVER report Bookings as Revenue; bookings are future commitments, revenue is earned performance.
- NEVER offset customer churn by adding new customer acquisition in the same line item; report churn explicitly.
- NEVER calculate NRR without tracking the exact same customer cohort across a full 12-month period.
