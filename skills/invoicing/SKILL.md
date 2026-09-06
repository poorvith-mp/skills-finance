---
name: invoicing
group: Accounting
description: >-
  Draft invoices, payment schedules and receivables with tax lines, payment terms and late-fee
  policy. Use when generating client invoices, payment terms, or chasing collections.
---

# Invoicing

Invoicing is working capital acceleration and cash collection governance. A professional invoicing process requires legally binding contract references, explicit payment terms, automated dunning cadences, compliant tax line items (VAT, GST, Sales Tax), and early payment incentive structures.

## 1. Statutory Invoice Requirements & Structure
Every commercial invoice must contain mandatory legal and accounting metadata:
1. **Unique Invoice Identifier**: Sequential, tamper-proof numbering schema (e.g. `INV-2026-0042`). Never duplicate invoice numbers.
2. **Entity & Tax Metadata**:
   - Issuer legal entity name, physical address, business tax ID (EIN / VAT ID / GSTIN).
   - Customer legal entity name, billing address, and AP contact email.
3. **Contractual Cross-Reference**: Linked Master Services Agreement (MSA), Statement of Work (SOW), or client Purchase Order (PO) number.
4. **Itemized Billing Ledger**:
   - Description of deliverables/services rendered.
   - Units, billable hours, or milestone phase.
   - Unit price, line item subtotal, applicable statutory tax percentage, and total amount due.
5. **Clear Remittance Instructions**: Bank wire routing/SWIFT details, ACH payment link, or credit card portal.

## 2. Payment Terms & Early Settlement Incentives
- **Standard Payment Terms**:
  - *Due Upon Receipt*: Standard for software self-serve and digital products.
  - *Net 30*: Enterprise commercial baseline. Payment due 30 calendar days from invoice date.
  - *Net 60 / Net 90*: Avoid unless contract value justifies financing the client's working capital.
- **Dynamic Early Settlement Discounts (e.g. 2/10 Net 30)**:
  - Offer a 2% discount if paid within 10 days; full amount due in 30 days.
  - *Mathematical Equivalence*: An annualized return of ~36.7% for the client, dramatically accelerating cash collection.

## 3. Automated Dunning & Collections Escalation Cadence
Systematize overdue receivables collections to prevent aged bad debt:

```
Day -5:   [Courtesy Notification] Upcoming invoice payment reminder with PDF attachment
Day 0:    [Due Date] Formal invoice due notification with direct payment link
Day +7:   [First Reminder] Polite follow-up requesting payment confirmation or remittance date
Day +15:  [Second Notice] Formal past-due notice; notification of pending late fees (1.5%/month)
Day +30:  [Service Suspension Warning] Account escalation; immediate notification of service pause
Day +45:  [Service Interruption] Access paused; account transferred to collections management
```

## 4. Sales Tax, VAT, and Reverse Charge Mechanics
- **US Sales Tax**: Determine state nexus (economic nexus thresholds typically $100,000 in sales or 200 transactions). Software-as-a-Service taxability varies by state.
- **EU/UK VAT**: Include customer VAT registration number for B2B cross-border transactions. Apply **Reverse Charge Mechanism** where applicable: "VAT reverse charge: customer liable for VAT pursuant to Article 196 of Council Directive 2006/112/EC."

## Critical Rules
1. Never deliver bespoke enterprise work without referencing an approved PO or signed SOW on the invoice.
2. All invoices must specify the currency ISO code (USD, EUR, GBP) to eliminate foreign exchange ambiguity.
3. Send invoices directly to the designated Accounts Payable department, not solely to the project champion.

## Verification Checklist
- [ ] Unique sequential invoice number assigned and logged in accounting software.
- [ ] Customer PO or contract SOW number referenced accurately.
- [ ] Statutory entity names, addresses, and tax IDs displayed.
- [ ] Subtotal, applicable taxes, and total due calculate accurately.
- [ ] Payment instructions (ACH, Wire, SWIFT/IBAN, Credit Card link) verified.

## Anti-Patterns
- NEVER wait until the end of the month to issue invoices for milestones completed weeks earlier.
- NEVER accept verbal payment term extensions without assessing interest penalties.
- NEVER write off aged receivables without documented collections escalation attempts.
