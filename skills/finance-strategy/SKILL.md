---
name: finance-strategy
last_reviewed: 2026-09-06
group: Modelling
description: >-
  Set capital allocation, treasury policy, M&A finance, investor relations and board reporting.
  Use when structuring capital allocation, debt vs equity, or treasury.
---

# Finance Strategy

Financial strategy is capital allocation to maximize Risk-Adjusted Return on Invested Capital (ROIC). A strategic finance function aligns capital structure (equity, venture debt, credit lines), manages corporate treasury liquidity across risk-free yield curves, governs M&A capital deployment, and communicates transparent operational metrics to the Board of Directors.

## 1. Capital Allocation & Cost of Capital (WACC)

Deploy capital where projected ROIC exceeds the Weighted Average Cost of Capital (WACC):
$$\text{WACC} = \left(\frac{E}{V} \times R_e\right) + \left(\frac{D}{V} \times R_d \times (1 - T)\right)$$
- $E$: Market value of equity; $D$: Market value of debt; $V = E + D$.
- $R_e$: Cost of equity (calculated via CAPM: $R_f + \beta \times (R_m - R_f)$).
- $R_d$: Pre-tax cost of debt; $T$: Corporate tax rate.
- *Strategic Rule*: If expected return on a growth initiative or acquisition is less than WACC, executing the project destroys shareholder value.

## 2. Debt vs. Equity Financing Decision Matrix
- **Equity (Venture Capital / Growth Equity)**:
  - *Best for*: High-uncertainty R&D, early market expansion, negative cash flow operations.
  - *Cost*: Highly expensive (permanent dilution of ownership), but zero debt service default risk.
- **Venture Debt / Term Loans**:
  - *Best for*: Extending runway between equity rounds when milestones are within clear sight; funding predictable ARR expansion.
  - *Terms*: Typically 20%–35% of recent equity round; requires warrants (1%–3% coverage); covenants on minimum cash and ARR growth.
- **Asset-Backed / Revolving Credit Facility**:
  - *Best for*: Working capital cycles, accounts receivable financing, inventory bridge.

## 3. Corporate Treasury & Liquidity Policy
Structure cash reserves across three liquidity tiers to balance safety and yield:
- **Tier 1 (Operating Liquidity - 30 to 60 Days)**: Checking/sweep accounts at top-tier financial institutions. Zero capital risk, instant liquidity.
- **Tier 2 (Reserve Liquidity - 3 to 12 Months)**: High-yield institutional money market funds (Treasury-only) or direct short-term US Treasury Bills (30–90 day maturities). Yield capture with same-day or T+1 liquidity.
- **Tier 3 (Strategic Capital - 12+ Months)**: Laddered US Treasuries (up to 12 months duration). Zero credit risk; held-to-maturity to avoid mark-to-market interest rate volatility.
- *Counterparty Risk Constraint*: Never hold more than 25% of corporate cash in an uninsured single institution beyond FDIC limits without automated sweep architecture.

## 4. Board Reporting & Investor Relations Cadence
Every quarterly board deck must lead with four standardized financial scorecards:
1. **Executive Scorecard**: Cash balance, Net Burn, Months of Runway, ARR, ARR Growth YoY, Gross Margin, Rule of 40.
2. **Bridge Analysis (Waterfall)**: ARR bridge showing Opening ARR + New Bookings + Expansion - Contraction - Churn = Closing ARR.
3. **P&L vs Budget**: Actual performance versus approved board plan with variance commentary.
4. **Hiring & Capital Requisitions**: Planned headcount vs actual additions.

## Critical Rules
1. Never take on debt with restrictive financial covenants that can trigger premature technical default during a market downturn.
2. Maintain a minimum of 6 months of cash reserves in Tier 1 and Tier 2 liquidity at all times.
3. Board presentations must report GAAP revenue alongside non-GAAP metrics with clear reconciliation schedules.

## Verification Checklist
- [ ] Treasury policy defines counterparty diversification and maximum maturity limits.
- [ ] Capital allocation decisions supported by hurdle rate and ROIC vs WACC analysis.
- [ ] Debt covenants monitored monthly to ensure compliance buffer >20%.
- [ ] Board reporting pack reconciles with closed financial statements.
- [ ] Investor updates published on a disciplined monthly or quarterly schedule.

## Anti-Patterns
- NEVER use high-risk yield-farming or speculative credit investments for corporate operating treasury.
- NEVER borrow venture debt to fund an unproven product hypothesis without clear unit-economic payback.
- NEVER present optimistic forward projections to the Board without disclosing key operating risks.
