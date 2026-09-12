---
name: budgeting
last_reviewed: 2026-09-06
group: Accounting
description: >-
  Build the budget, run rolling forecasts, and explain budget-versus-actual variance and expense
  anomalies. Use when creating annual operating budgets, departmental spend, or variance.
---

# Budgeting

Budgeting is resource allocation against strategic hypotheses, not an accounting compliance exercise. Operating budgets must establish departmental spend envelopes, forecast cash runway under variable revenue trajectories, and institute rolling 4+8 and 9+3 variance reviews to catch expense anomalies before they threaten liquidity.

## 1. Operating Budget Architecture

Deconstruct company expenses into three structural layers:
- **Headcount Costs (typically 70%–80% of tech OpEx)**: Model fully-loaded payroll (base salary + employer payroll taxes + healthcare + 401(k) match + hardware/SaaS seat stipends). Use a 1.20x–1.25x multiplier on base salaries.
- **Direct Variable COGS**: Cloud compute, database storage, payment processing, third-party API token costs. Model directly as a percentage of revenue or active user volume.
- **Fixed & Discretionary OpEx**: Office rent, legal/accounting retainers, travel and entertainment (T&E), software tooling.

## 2. Rolling Forecast Models (4+8, 9+3)
Static annual budgets become obsolete within 90 days. Implement rolling forecasts:
- **4+8 Forecast**: 4 months of closed historical actuals + 8 months of updated forward projections.
- **Scenario Sensitivities**:
  - *Base Case*: Budgeted target revenue growth (e.g. +40% YoY).
  - *Conservative Case*: Flat net new bookings; headcount freeze; extends runway by 6 months.
  - *Downside / Stress Test Case*: 20% revenue contraction; immediate elimination of discretionary spend.

## 3. Budget-vs-Actual (BVA) Variance Analysis
Review departmental performance on the 10th of every month:
$$\text{Variance (\%)} = \frac{\text{Actual Spend} - \text{Budgeted Spend}}{\text{Budgeted Spend}} \times 100$$
- **Variance Thresholds**:
  - *Favorable Variance (< 0% for expenses)*: Spend below budget; verify if due to delayed hiring or efficiency.
  - *Unfavorable Variance (> +5% or > $5,000)*: Requires written department lead variance explanation and corrective remediation plan.

## 4. Departmental Budget Allocations

| Department | Typical % of Total OpEx | Primary Budget Drivers | Key Performance Metric |
|---|---|---|---|
| **R&D / Engineering** | 45% – 55% | Engineering headcount, cloud infrastructure, AI compute | Features shipped, system uptime, cloud cost/MAU |
| **Sales & Marketing** | 25% – 35% | Quota-carrying reps, digital media spend, conferences | CAC, Pipeline generated, Magic Number |
| **G&A (Ops, Legal, Fin)** | 10% – 15% | Legal counsel, accounting audit, insurance, executive team | Month-end close speed, compliance certifications |

## Critical Rules
1. Never budget revenue without tying it to pipeline conversion rates and sales headcount productivity caps.
2. Every new full-time headcount addition must have an assigned requisition ID and fully-loaded financial model approval.
3. Budget owners are accountable for gross dollar ceilings; savings in one line item cannot be diverted to unapproved software subscriptions without CFO sign-off.

## Verification Checklist
- [ ] Fully-loaded headcount multiplier (1.20x–1.25x) applied to all projected salaries.
- [ ] Variable COGS tied dynamically to revenue projections.
- [ ] Monthly BVA variance reports generated with written management explanations.
- [ ] Downside stress-test scenario guarantees minimum 12 months cash runway.
- [ ] Capital expenditure (CapEx) separated from operational expenditure (OpEx).

## Anti-Patterns
- NEVER create an annual budget that remains untouched for 12 months despite material market shifts.
- NEVER rely on straight-line revenue growth assumptions without accounting for sales rep ramp time (typically 3–6 months).
- NEVER treat projected cost savings from unhired roles as permanent financial buffer.
