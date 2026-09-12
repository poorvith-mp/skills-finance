---
name: tax-strategy
last_reviewed: 2026-09-06
group: Tax
description: >-
  Plan entity structure, transfer pricing, credits and multi-jurisdiction compliance. Use when
  planning corporate R&D tax credits, QSBS, or depreciation.
---

# Tax Strategy

Corporate tax strategy is legal liability optimization and statutory compliance. Strategic tax planning requires optimizing corporate entity structures, claiming research and development (R&D) payroll tax credits, managing Qualified Small Business Stock (QSBS) eligibility, and complying with multi-state and international tax nexus.

## 1. Entity Architecture & Structural Selection
- **Delaware C-Corporation**: The non-negotiable standard for venture-backed technology companies. Required for institutional equity financing, equity incentive plans (stock options), and QSBS eligibility.
- **LLC / Pass-Through Entity**: Best for bootstrapped businesses, consultancies, or real estate holding companies where operating profits and losses pass directly to individual member tax returns (Schedule K-1).
- **83(b) Election**: Mandatory for founders and early employees receiving unvested restricted stock. Must be signed and filed with the IRS within **30 calendar days** of stock grant. Failure to file triggers catastrophic ordinary income tax on equity value appreciation as shares vest.

## 2. Federal R&D Tax Credit (IRC Section 41 & Section 3111(f))
Early-stage technology companies can monetize R&D tax credits immediately against payroll taxes even if currently unprofitable:
- **Qualified Research Activities (QRA)**: Software engineering, architecture design, algorithmic development, and complex technical prototyping satisfy the IRS four-part test.
- **Payroll Tax Offset**: Eligible startup businesses (<$5M in gross receipts for the tax year, with no gross receipts older than 5 years) can elect to apply up to **$500,000 annually** of federal R&D tax credits directly against the employer portion of FICA payroll tax.

## 3. Qualified Small Business Stock (QSBS - IRC Section 1202)
Section 1202 allows founders and early investors to exclude up to 100% of federal capital gains tax upon the sale of stock:
- **Eligibility Criteria**:
  - Stock must be acquired directly from an active domestic C-Corporation at original issuance.
  - Aggregate gross assets of the corporation must not exceed $50 million at all times before and immediately after issuance.
  - The stock must be held for a minimum of **5 continuous years**.
- **Tax Exclusion Ceiling**: Exclude up to **$10 million** in capital gains, or **10x the taxpayer's aggregate adjusted basis** in the stock, whichever is greater.

## 4. Multi-State Economic Nexus & Sales Tax (Wayfair Doctrine)
Operating a remote-first software business creates tax liabilities across multiple jurisdictions:
- **State Corporate Income Tax Nexus**: Establishing remote employees, physical offices, or high revenue in a state creates income tax filing obligations.
- **Sales & Use Tax Nexus**: Software-as-a-Service taxability varies drastically by state (e.g. New York and Texas tax SaaS; California does not tax purely downloaded/cloud SaaS without custom tangible property). Register and automate state tax collection via tools like Anrok or Stripe Tax.

## Critical Rules
1. Every founder receiving restricted stock must file an IRS Section 83(b) election via certified mail with tracking within 30 days of grant.
2. Never treat software engineering salaries as non-R&D without evaluating the Section 41 payroll tax credit offset.
3. Comply with IRC Section 174 capitalization requirements for domestic and international software development expenditures.

## Verification Checklist
- [ ] Section 83(b) election forms and certified mail receipts archived for all equity founders.
- [ ] C-Corporation qualifying criteria verified for QSBS Section 1202 status.
- [ ] Software engineering expenses documented under the IRC Section 41 four-part test for R&D tax credits.
- [ ] State economic nexus monitored for remote employee payroll withholding and SaaS sales tax.
- [ ] Transfer pricing documentation in place for any foreign subsidiary engineering entities.

## Anti-Patterns
- NEVER miss the 30-day postmark deadline for Section 83(b) elections; the IRS does not grant relief for late filings.
- NEVER assume digital software sales are exempt from state sales tax without reviewing economic nexus thresholds.
- NEVER mix personal deductible expenses into corporate tax returns without explicit business justification.
