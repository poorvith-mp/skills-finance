---
name: bookkeeping
group: Accounting
description: >-
  Run day-to-day accounting: reconciliations, month-end close, journal entries and internal
  controls. Use when reconciling bank accounts, chart of accounts, or ledger entries.
---

# Bookkeeping

Bookkeeping is the foundation of financial veracity. Reliable accounting requires double-entry rigor, adherence to the accrual principle (ASC 606 / matching principle), structured Chart of Accounts (COA) taxonomy, and disciplined month-end close checklists.

## 1. Chart of Accounts (COA) Taxonomy
Organize accounts in a standard five-digit hierarchical numbering schema:
- **10000 – 19999 Assets**: 10100 Operating Cash, 10200 Treasury MMF, 11000 Accounts Receivable, 12000 Prepaid Expenses.
- **20000 – 29999 Liabilities**: 20100 Accounts Payable, 21000 Accrued Expenses, 22000 Deferred Revenue (Unearned).
- **30000 – 39999 Equity**: 30100 Common Stock, 30200 Additional Paid-in Capital (APIC), 30300 Retained Earnings.
- **40000 – 49999 Revenue**: 40100 SaaS Subscription Revenue, 40200 Professional Services, 40300 Refunds/Discounts.
- **50000 – 59999 Cost of Goods Sold (COGS)**: 50100 Cloud Hosting (AWS/GCP), 50200 Payment Gateway Fees (Stripe), 50300 Customer Support Salaries.
- **60000 – 69999 Operating Expenses (OpEx)**: 61000 R&D Salaries, 62000 Sales & Marketing, 63000 G&A (Legal, Accounting, Rent).

## 2. Double-Entry Journal Entry Discipline
Every transaction must satisfy the fundamental balance sheet equation:
$$\text{Assets} = \text{Liabilities} + \text{Equity}$$

### Example: SaaS Customer Annual Prepayment ($12,000 on Jan 1)
- **Initial Cash Receipt (Jan 1)**:
  - Debit: `10100 Operating Cash` $12,000 (Asset increases)
  - Credit: `22000 Deferred Revenue` $12,000 (Liability increases)
- **Monthly Revenue Recognition (Jan 31)**:
  - Debit: `22000 Deferred Revenue` $1,000 (Liability decreases)
  - Credit: `40100 SaaS Subscription Revenue` $1,000 (Revenue increases)

## 3. Month-End Close Checklist (Target: Day +5)
Execute the close systematically across 5 working days:
- **Day 1**: Reconcile all bank, credit card, and payment processor accounts (Stripe clearing balance vs bank deposits).
- **Day 2**: Reconcile Accounts Receivable and post bad debt allowances.
- **Day 3**: Reconcile Accounts Payable, review unbilled purchase orders, and record vendor accruals.
- **Day 4**: Post prepaid expense amortizations (insurance, annual SaaS tooling) and depreciation schedules.
- **Day 5**: Run Trial Balance verification; review P&L variances against previous month; lock accounting period.

## Critical Rules
1. Never mix cash-basis reporting with accrual revenue recognition; recognize revenue in the period performance obligations are satisfied.
2. Every balance sheet account must have a supporting reconciliation schedule matching the trial balance to the cent.
3. Once an accounting period is locked, never post retrospective adjustments directly to that period; record prior-period adjustments via current period journal entries.

## Verification Checklist
- [ ] Bank and credit card accounts reconciled to official institution statements.
- [ ] Stripe / payment gateway clearing accounts balance to zero after in-transit transfers.
- [ ] Deferred revenue schedule ties directly to active customer contract terms.
- [ ] Prepaid expenses amortized according to benefit period.
- [ ] General ledger debit and credit totals balance exactly.

## Anti-Patterns
- NEVER book customer annual upfront payments directly as immediate revenue.
- NEVER categorize expenses into generic "Miscellaneous" or "Ask My Accountant" buckets past month-end close.
- NEVER leave personal founder expenses commingled with corporate operating bank accounts.
