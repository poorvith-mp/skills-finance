---
name: cap-table
group: Modelling
description: >-
  Model cap tables, dilution scenarios, waterfalls and round structures — SAFE, convertible notes,
  priced. Use when modeling founder equity, SAFEs, option pools, or dilution waterfalls.
---

# Cap Table

The capitalization table models economic ownership, governance rights, and liquidation economics. Accurately managing a cap table requires modeling fully-diluted share counts, calculating post-money vs pre-money SAFEs, configuring employee equity option pools, and structuring preferred share liquidation waterfalls.

## 1. Share Counts: Issued vs. Fully-Diluted
Distinguish between voting shares and total diluted shares:
- **Issued & Outstanding**: Common stock held by founders, early employees, and exercised shares.
- **Fully-Diluted Shares (FD)**:
  $$\text{Fully-Diluted Shares} = \text{Issued Common} + \text{Unexercised Options Granted} + \text{Unallocated Option Pool} + \text{Convertible Securities}$$
  *Rule*: Always use the fully-diluted share count when calculating per-share price and percentage ownership.

## 2. SAFE Conversion Mechanics (Valuation Cap & Discount)
Simple Agreements for Future Equity (SAFEs) convert into preferred stock upon a qualified priced equity financing:
- **Pre-Money SAFE Conversion Price**:
  $$\text{Conversion Price} = \min\left( \frac{\text{Valuation Cap}}{\text{Pre-Money Fully-Diluted Shares}}, \text{Priced Round Price} \times (1 - \text{Discount Rate}) \right)$$
- **Post-Money SAFE Ownership (Y Combinator Standard)**:
  $$\text{Investor Ownership \%} = \frac{\text{Investment Amount}}{\text{Post-Money Valuation Cap}}$$
  *Note*: Post-money SAFEs dilute existing common shareholders with mathematical certainty, but do not dilute other post-money SAFE holders until the priced round.

## 3. Option Pool Shuffle Mechanics
Lead investors in priced rounds frequently demand an unallocated option pool (typically 10%–15% post-financing):
- **Investor Preference (Pre-Money Option Pool Shuffle)**: The option pool is created/expanded *before* the investor's cash goes in, forcing 100% of the dilution onto the existing founders and common holders.
- **Founder Counter**: Negotiate the pool size based on a hiring plan for the next 12–18 months (e.g. 7% instead of a generic 15%), or negotiate a post-money option pool expansion where all shareholders share dilution proportionally.

## 4. Liquidation Waterfall Architecture
In an exit or liquidity event, proceeds are distributed according to security preference:
1. **Seniority Tier**: Senior debt -> Convertible notes -> Preferred equity holders -> Common shareholders.
2. **Preference Multiple**: 1x Non-Participating Preferred is the venture standard.
   - *Non-Participating*: Investor takes the greater of: (a) 1x original investment amount, or (b) their pro-rata common share of total exit proceeds.
   - *Participating (Founder Anti-Pattern)*: Investor gets 1x investment back FIRST, AND ALSO shares pro-rata in the remaining proceeds ("double dipping").

## 5. Sample Cap Table Summary

| Shareholder Class | Shares Held | % Issued & Outstanding | % Fully-Diluted | Liquidation Preference |
|---|---|---|---|---|
| Founders (Common) | 6,000,000 | 66.7% | 60.0% | None (Pari-passu common) |
| Early Employees (Vested Options) | 1,000,000 | 11.1% | 10.0% | None |
| Unallocated Option Pool | 1,000,000 | 0.0% | 10.0% | None |
| Seed Investors (Series Seed Preferred) | 2,000,000 | 22.2% | 20.0% | 1x Non-Participating ($2.0M) |
| **Total** | **10,000,000** | **100.0%** | **100.0%** | **$2,000,000** |

## Critical Rules
1. Never accept participating preferred shares in a venture term sheet unless in a distressed recapitalization.
2. Always calculate dilution using a post-money capitalization model that accounts for all outstanding SAFEs and promissory notes.
3. Model option pool expansions against an explicit hiring roadmap to avoid giving away unneeded founder equity.

## Verification Checklist
- [ ] Share counts tie out across common, vested/unvested options, and preferred classes.
- [ ] SAFE conversion formulas verified (valuation cap, discount rate, and MFN clauses).
- [ ] Pre-money vs post-money option pool dilution modeled accurately.
- [ ] 1x non-participating liquidation preference confirmed in term sheet review.
- [ ] Section 83(b) elections confirmed filed within 30 days of equity grants.

## Anti-Patterns
- NEVER promise percentage ownership in an offer letter; grant an explicit number of option shares.
- NEVER stack multiple un-capped SAFEs without modeling the catastrophic founder dilution at the priced round.
- NEVER grant equity without a standard 4-year vesting schedule with a 1-year cliff.
