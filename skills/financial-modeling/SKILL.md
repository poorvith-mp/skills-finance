---
name: financial-modeling
group: Modelling
description: >-
  Build models, forecasts, valuations and scenario analyses from raw data. Use when building
  three-statement models, DCF valuations, or pro formas.
---

# Financial Modeling

A financial model is an inspectable simulation of corporate operating reality. Dynamic financial modeling requires building integrated Three-Statement Models (Income Statement, Balance Sheet, Cash Flow Statement) linked via deterministic mathematical schedules, Discounted Cash Flow (DCF) valuations, and multi-variable scenario matrices.

## 1. Integrated Three-Statement Model Architecture

The three statements must link dynamically without circular reference errors:

```
[Income Statement]
  Revenue - COGS = Gross Profit
  Gross Profit - OpEx = EBITDA
  EBITDA - D&A = Operating Income (EBIT)
  EBIT - Interest - Taxes = Net Income ────────┐
                                               │
┌──────────────────────────────────────────────┘
▼
[Cash Flow Statement]
  Operating: Net Income + D&A - Change in Working Capital
  Investing: - Capital Expenditures (CapEx) ──┐
  Financing: Debt Issuance/Repayment + Equity │
  Net Change in Cash = Operating + Investing + Financing ──┐
                                                           │
┌──────────────────────────────────────────────────────────┘
▼
[Balance Sheet]
  Assets: Cash (from CFS), Accounts Receivable, PP&E (from CapEx/D&A schedule)
  Liabilities: Accounts Payable, Deferred Revenue, Debt
  Equity: Common Stock + Retained Earnings (Prior Retained Earnings + Net Income)
  Balance Check: Assets - (Liabilities + Equity) === $0.00
```

## 2. Working Capital & Supporting Schedules
Do not hardcode balance sheet line items; calculate them via operational driver schedules:
- **Accounts Receivable (AR)**: $\text{AR} = \frac{\text{Days Sales Outstanding (DSO)}}{365} \times \text{Revenue}$
- **Accounts Payable (AP)**: $\text{AP} = \frac{\text{Days Payable Outstanding (DPO)}}{365} \times \text{COGS}$
- **Depreciation Schedule**: Straight-line depreciation based on asset useful life:
  $$\text{Depreciation} = \frac{\text{Historical Cost} - \text{Salvage Value}}{\text{Useful Life (Years)}}$$

## 3. Discounted Cash Flow (DCF) Valuation Engine

Calculate enterprise value by discounting projected Free Cash Flow to Firm (FCFF):
$$\text{FCFF} = \text{EBIT} \times (1 - T) + \text{D&A} - \text{CapEx} - \Delta\text{Net Working Capital}$$
$$\text{Enterprise Value} = \sum_{t=1}^{n} \frac{\text{FCFF}_t}{(1 + \text{WACC})^t} + \frac{\text{Terminal Value}}{(1 + \text{WACC})^n}$$

### Terminal Value Formulations
1. **Gordon Growth Model**:
   $$\text{Terminal Value} = \frac{\text{FCFF}_{n} \times (1 + g)}{\text{WACC} - g}$$
   *Rule*: Long-term perpetual growth rate $g$ must not exceed projected long-term GDP growth (typically 2.0%–3.0%).
2. **Exit Multiple Method**:
   $$\text{Terminal Value} = \text{EBITDA}_n \times \text{Target Industry Multiple}$$

## 4. Model Integrity & Color Coding Standards
Enforce universal financial modeling formatting standards:
- **Blue Text**: Hardcoded historical inputs and user-adjustable assumptions.
- **Black Text**: Dynamic formulas and mathematical calculations.
- **Green Text**: Internal cross-sheet links and dependencies.
- **Red Text**: External workbook references and critical error flags.

## Critical Rules
1. The balance sheet must balance mathematically ($Assets - Liabilities - Equity = 0$) across every historical and forecast period.
2. Never hardcode numbers directly inside calculation formulas (e.g. `=B12*1.05`); place assumptions in dedicated input cells.
3. Every dynamic financial model must include automated error-check flags on every sheet.

## Verification Checklist
- [ ] Three statements dynamically linked; zero circular references.
- [ ] Balance check formula verifies Assets == Liabilities + Equity for all periods.
- [ ] Working capital schedules drive AR, AP, and deferred revenue movements.
- [ ] Discount rate (WACC) and terminal growth assumptions documented with sources.
- [ ] Sensitivity table models revenue growth against gross margin variations.

## Anti-Patterns
- NEVER use Excel circular calculation modes to resolve interest expense loops; use an average cash/debt balance schedule.
- NEVER hardcode forward balance sheet cash; cash must flow strictly from the Cash Flow Statement.
- NEVER build a model without an audit sheet verifying formula consistency.
