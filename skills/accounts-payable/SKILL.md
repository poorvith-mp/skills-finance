---
name: accounts-payable
last_reviewed: 2026-09-06
group: Accounting
description: >-
  Run payables: vendor payments, contractor invoices and recurring bills across fiat, crypto and
  stablecoin rails. Use when managing incoming vendor bills, payment approvals, or expense
  reports.
---

# Accounts Payable

Accounts payable is a working capital and fraud-prevention discipline. Managing payables requires strict three-way matching (purchase order, receiving report, vendor invoice), clear segregation of payment approval duties, and structured disbursement schedules across both traditional banking and modern digital/stablecoin rails.

## 1. The Three-Way Matching Protocol
Never disburse funds based on an isolated invoice. Validate three core documents before payment approval:
1. **Purchase Order (PO)**: Validates that the purchase was authorized with approved unit pricing.
2. **Receiving Report / Goods Receipt**: Confirms that goods or services were delivered and accepted.
3. **Vendor Invoice**: Verifies that billed quantities and rates match the PO and delivery receipt within a tight tolerance (typically <1% variance).

## 2. Payment Approval Matrix & Segregation of Duties
Prevent unauthorized disbursements through tiered approval thresholds:
- **Level 1 (Tier 1: < $2,500)**: Department manager approval.
- **Level 2 (Tier 2: $2,500 – $25,000)**: Department head + Financial Controller approval.
- **Level 3 (Tier 3: > $25,000)**: Chief Financial Officer (CFO) or CEO co-signature required.
- *Segregation of Duties Rule*: The person who enters a vendor into the ERP/accounting system must never have banking disbursement or check-signing authority.

## 3. Disbursement Rails (Fiat, ACH, Wire, Stablecoins)
- **Domestic ACH**: Batch processed bi-weekly (Tuesdays and Thursdays) to optimize cash float while avoiding late fees.
- **Commercial Credit Cards**: Used for recurring SaaS subscriptions to capture 1.5%–2.0% cash rebates and leverage 30-day interest-free float.
- **International Wires / Stablecoins (USDC)**: For cross-border engineering contractors and overseas vendors. Verify wallet addresses via micro-transaction test transfers before executing full invoice disbursements.

## 4. Vendor Onboarding & Year-End Compliance
- Collect IRS Form W-9 (US entities) or W-8BEN / W-8BEN-E (foreign contractors) prior to issuing the first payment.
- Track 1099-NEC non-employee compensation thresholds ($600+ annual cumulative payment).

## Critical Rules
1. Never pay an invoice directly from an email attachment without verifying the vendor's bank account details against the master vendor file.
2. Reconcile open AP subledger accounts against general ledger account 2000 (Accounts Payable) at every month-end close.
3. Maintain an audit log of all payment authorizations for at least 7 years.

## Verification Checklist
- [ ] Three-way match confirmed between PO, receiving slip, and vendor bill.
- [ ] Tax documentation (W-9 / W-8BEN) verified on file before disbursement.
- [ ] Approval signatures correspond to authorized tier thresholds.
- [ ] Payment schedule optimized for cash flow float without incurring vendor penalties.
- [ ] 1099-eligible disbursements tagged in accounting system.

## Anti-Patterns
- NEVER update vendor banking or routing details based solely on an email request without phone verification via a known number.
- NEVER disburse payment without an itemized invoice detailing services rendered.
- NEVER allow manual paper checks without dual-signature controls for transactions over $10,000.
