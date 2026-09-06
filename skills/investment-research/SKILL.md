---
name: investment-research
group: Investing
description: >-
  Run market analysis, due diligence, valuation and portfolio review across asset classes. Use
  when evaluating public equities, earnings calls, or 10-K filings.
---

# Investment Research

Investment research requires rigorous fundamental analysis, accounting forensics, competitive moat assessment, and valuation modeling. Analyzing public equities, corporate filings, or private venture opportunities demands deconstructing SEC filings (10-K, 10-Q), evaluating management capital allocation track records, and modeling investment returns with explicit margin-of-safety parameters.

## 1. SEC Filing Deconstruction & Forensic Accounting

Inspect audited financial statements for earnings quality:
- **Form 10-K (Annual) & Form 10-Q (Quarterly)**:
  - *Item 1 (Business)*: Moat analysis, customer concentration risks, supplier dependencies.
  - *Item 7 (Management's Discussion & Analysis - MD&A)*: Organic growth vs acquisition growth, pricing power, headwinds.
  - *Item 8 (Financial Statements & Notes)*: Revenue recognition policies, off-balance-sheet commitments, stock-based compensation (SBC), pending litigation.
- **Quality of Earnings Signals**:
  - *Accruals Anomaly*: High Net Income accompanied by declining Operating Cash Flow indicates aggressive revenue recognition.
  - *Stock-Based Compensation Dilution*: Treat SBC as a real cash expense; add back dilution to share counts.
  - *Goodwill Impairments*: Historical track record of M&A write-downs signals poor capital allocation.

## 2. Competitive Moat Assessment (Porter & Helmer Frameworks)
Evaluate structural competitive barriers:
- **Network Effects**: Value increases quadratically with user additions (Metcalfe's Law).
- **Switching Costs**: Cost to migrate to an alternative exceeds the expected savings (mission-critical enterprise software).
- **Scale Economies**: Declining marginal cost curve creating an insurmountable pricing advantage.
- **Counter-Positioning**: Incumbents cannot copy the new business model without cannibalizing their core revenue stream.

## 3. Financial Ratio & DuPont ROE Decomposition
Deconstruct Return on Equity (ROE) into operational efficiency, asset productivity, and leverage:
$$\text{ROE} = \left( \frac{\text{Net Income}}{\text{Revenue}} \right) \times \left( \frac{\text{Revenue}}{\text{Total Assets}} \right) \times \left( \frac{\text{Total Assets}}{\text{Shareholders' Equity}} \right)$$
- **Net Profit Margin**: Operating discipline and pricing power.
- **Asset Turnover**: Capital efficiency.
- **Equity Multiplier**: Degree of financial leverage.

## 4. Valuation Multiples & Margin of Safety

| Valuation Metric | Formula | Best Used For | Warning Threshold |
|---|---|---|---|
| **EV / NTM EBITDA** | $\frac{\text{Enterprise Value}}{\text{Next 12M Projected EBITDA}}$ | Capital-intensive, profitable businesses | Multiple > 2x peer historical median |
| **EV / NTM Sales** | $\frac{\text{Enterprise Value}}{\text{Next 12M Projected Revenue}}$ | High-growth, pre-profit SaaS | Multiple > 15x without >40% growth |
| **Free Cash Flow Yield** | $\frac{\text{FCF per Share}}{\text{Market Share Price}}$ | Mature, cash-generating companies | Yield < Risk-free 10-Yr Treasury rate |
| **P/E to Growth (PEG)** | $\frac{\text{P/E Ratio}}{\text{Projected EPS Growth Rate}}$ | Growth at a reasonable price (GARP) | PEG > 2.0x |

## Critical Rules
1. Never value a growth company on gross revenue alone without accounting for stock-based compensation dilution.
2. Always adjust EBITDA for capitalized software development costs and recurring maintenance CapEx.
3. Every investment recommendation must state the specific falsification criteria: what verifiable milestone or metric degradation would invalidate the thesis.

## Verification Checklist
- [ ] 10-K financial statement notes reviewed for contingent liabilities and revenue recognition rules.
- [ ] Operating cash flow reconciled against net income to identify non-cash earnings inflation.
- [ ] Historical dilution modeled including outstanding stock option pools and RSUs.
- [ ] Valuation checked across multiple methodologies (DCF, historical multiples, sum-of-the-parts).
- [ ] Falsification criteria and downside bear-case scenario documented.

## Anti-Patterns
- NEVER rely on management-adjusted EBITDA figures that exclude regular, recurring cash expenses.
- NEVER initiate an investment position without an explicit target entry valuation incorporating a margin of safety.
- NEVER confuse high revenue growth with competitive moat; evaluate customer churn and pricing power.
