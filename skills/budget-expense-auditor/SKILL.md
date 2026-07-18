---
name: budget-expense-auditor
description: Reviews a budget or expense report to find anomalies, overspend, duplicate charges, unusual month-over-month swings, and concrete cut opportunities. Use this whenever the user shares expense data (CSV, spreadsheet, or pasted numbers), asks "where is my money going", "why did this month cost more", "help me find things to cut", wants a personal or business budget reviewed, or is preparing for a monthly/quarterly financial review. Also use it when the user wants to build a budget from scratch and needs category benchmarks to compare against.
---

# Budget & Expense Auditor

You're reviewing spending data to find what's worth questioning — not just summarizing it back to the user in prettier form. A good audit surfaces the 3-5 things a person would actually want to act on, not a wall of restated numbers.

## Why this matters

Anyone can total a spreadsheet. The value here is judgment: knowing that a category jumping 40% month-over-month is worth a comment even if the absolute number is small, or that two nearly-identical charges three days apart is worth flagging as a possible duplicate even if neither looks wrong in isolation. Don't just report what's in the data — interpret it.

## Workflow

1. **Get the data.** If a file is attached (CSV/XLSX), read it directly rather than asking the user to retype numbers. If they paste numbers inline, work with what's given rather than demanding a specific format.
2. **Establish the baseline.** If multiple periods are present, compute period-over-period deltas per category. If only one period exists, ask what they're comparing against (a prior month, a budget target) — or if they just want a first-pass read, do that and say what you'd need for a deeper comparison.
3. **Look for these patterns, in priority order:**
   - **Large or unexplained swings** — a category up/down more than ~25-30% period over period.
   - **Possible duplicates** — near-identical amounts within a few days of each other in the same category.
   - **Category creep** — a category with no absolute red flag but steadily growing across 3+ periods.
   - **Concentration risk** — one or two line items making up a disproportionate share of a category (worth a comment even if the total budget is fine).
   - **Recurring charges that may no longer be needed** — subscriptions/fees appearing every period at flat amounts, worth a "still using this?" flag.
4. **Rank findings by dollar impact first, then by how actionable they are.** A $12/month subscription is easy to cut but low-impact; lead with what actually moves the needle, then mention the easy wins after.
5. **Suggest concrete next steps**, not vague advice. "Cancel the duplicate $14.99 charge from March 3 and March 6" beats "review your subscriptions."

## What NOT to do

- Don't moralize about spending habits or make assumptions about why someone spent what they did — you don't have that context, and it's not helpful even when the data looks concerning.
- Don't recommend specific investment products, insurance products, or tax strategies — that's outside scope; flag if the user needs that and suggest they'd want a licensed advisor for those specific calls.
- Don't manufacture findings to seem thorough. If the data genuinely looks fine, say so — a clean bill of health is a valid and useful output.

## Output format

```markdown
## Budget review: <period(s) covered>

**Top findings** (ranked by impact)
1. [Finding] — [dollar impact] — [suggested action]
2. ...

**Worth watching** (smaller or early-stage patterns)
- ...

**Looks fine**
- [categories/items that reviewed clean, so the user knows they were checked]
```

See `references/category-benchmarks.md` for rough category-share benchmarks to use when the user wants "is this normal?" context rather than just period-over-period comparison.
