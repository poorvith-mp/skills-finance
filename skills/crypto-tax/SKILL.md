---
name: crypto-tax
group: Tax
description: >-
  Calculate capital gains, DeFi yield, NFT trades and cross-chain activity under FIFO, LIFO or
  HIFO. Use when calculating capital gains, staking rewards, or DeFi tax lots.
---

# Crypto Tax

Digital asset taxation requires strict tracking of cost-basis lots, characterization of income versus capital gains, and compliance with statutory tax reporting (IRS Form 8949 and Schedule D). Crypto accounting demands rigorous distinction between capital asset disposals, DeFi yield generation, staking rewards, and bridge transfers.

## 1. Taxable Events vs. Non-Taxable Transfers

Categorize blockchain transactions accurately:
- **Non-Taxable Events (Zero Gain/Loss Realized)**:
  - Transferring cryptocurrency between personal self-custody wallets or centralized exchange accounts owned by the same entity.
  - Purchasing cryptocurrency with fiat currency (establishes initial cost basis).
  - Minting an NFT for personal collection without commercial trade.
- **Taxable Capital Asset Disposals (Form 8949)**:
  - Crypto-to-crypto trades (e.g. trading ETH for SOL, or swapping USDC for WBTC on Uniswap).
  - Spending cryptocurrency to purchase goods or services.
  - Selling cryptocurrency or NFTs for fiat currency (USD, EUR).
- **Taxable Ordinary Income (Schedule 1 / Schedule C)**:
  - Staking rewards and validation fees (taxable at fair market value at the exact timestamp received).
  - Mining rewards.
  - Token airdrops and hard-fork distributions upon establishing dominion and control.
  - Payroll or contractor compensation paid in cryptocurrency or stablecoins.

## 2. Cost-Basis Accounting Methodologies

Select an inventory valuation method and apply it consistently:
- **FIFO (First-In, First-Out)**: Default tax standard in most jurisdictions. Oldest acquired coins are treated as sold first. In a bull market, FIFO typically maximizes realized capital gains.
- **HIFO (Highest-In, First-Out)**: Specifically identifies and matches the highest purchase price lots against disposals, minimizing realized capital gains and maximizing tax efficiency.
- **LIFO (Last-In, First-Out)**: Matches the most recently acquired coins against sales.
- *Specific Identification Mandate*: To utilize HIFO, the taxpayer must be able to document specific lot identifiers (transaction hash, wallet address, timestamp, unit basis).

## 3. Mathematical Gain/Loss Calculation
For every disposal transaction:
$$\text{Capital Gain / Loss} = \text{Fair Market Value of Proceeds (USD)} - \text{Cost Basis (USD)} - \text{Transaction/Gas Fees (USD)}$$
- **Holding Period**:
  - *Short-Term Capital Gain*: Asset held for $\le 365$ days (taxed at ordinary income rates, up to 37% federal).
  - *Long-Term Capital Gain*: Asset held for $> 365$ days (taxed at preferential rates: 0%, 15%, or 20%).

## 4. Complex DeFi Transactions
- **Liquidity Pool (LP) Deposits**: Providing liquidity (e.g. ETH/USDC) where LP tokens are minted in exchange for deposited assets may trigger a taxable disposal under strict IRS interpretations. Document as taxable disposal unless conservative non-recognition guidance is formally established.
- **Gas Fees**:
  - Gas fees paid to facilitate a sale or swap deduct directly from proceeds or add to cost basis.
  - Gas fees paid for failed transactions are treated as non-deductible personal losses or investment expenses depending on corporate classification.

## Critical Rules
1. Never assume that trading one cryptocurrency for another is a non-taxable "like-kind exchange" (Section 1031 does not apply to digital assets).
2. Every staking reward and airdrop must be valued in fiat currency at the exact block timestamp it became claimable.
3. Keep complete on-chain wallet histories; missing acquisition cost basis defaults to $0.00, resulting in 100% taxable gains.

## Verification Checklist
- [ ] Complete transaction history exported across all centralized exchanges and self-custodial wallets.
- [ ] Cost-basis methodology (FIFO vs HIFO) applied consistently across all tax years.
- [ ] Capital gains segregated into short-term (<= 365 days) and long-term (> 365 days).
- [ ] Staking rewards, airdrops, and mining revenues categorized as ordinary income.
- [ ] IRS Form 8949 and Schedule D reconciled against aggregate gain/loss totals.

## Anti-Patterns
- NEVER fail to answer the digital asset question on IRS Form 1040/1120 affirmatively if trades occurred.
- NEVER rely on automated exchange 1099-DA/1099-MISC reports alone without cross-reconciling external on-chain wallets.
- NEVER ignore cross-chain bridge transactions; bridging without tracking cost basis breaks asset lineage and causes false capital gain calculations.
