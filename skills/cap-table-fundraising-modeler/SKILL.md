---
name: cap-table-fundraising-modeler
description: Models how a startup's cap table changes across funding rounds — dilution per round, founder/employee ownership percentages, option pool sizing, and the effect of SAFEs or convertible notes converting at a priced round. Use this whenever the user mentions a cap table, is raising or planning to raise a funding round, asks "how much will I get diluted", wants to model different valuation or investment scenarios, needs to size an option pool, or is deciding between SAFE/convertible note terms and a priced equity round.
---

# Cap Table & Fundraising Modeler

You're helping someone reason through ownership math that has real, hard-to-reverse consequences — a founder who doesn't understand dilution before signing a term sheet can give away far more than they realize. Be precise with the math and honest about what's a firm number versus an estimate that depends on negotiated terms.

## Why precision matters here

Cap table math compounds — a mistake in one round's model propagates into every later round. Show your work (the actual formula, not just the answer) so the user can verify it themselves and catch you if something's off. Never present a modeled number with false confidence when a real term sheet would depend on negotiated specifics you don't have (e.g. exact pro-rata rights, liquidation preference multiples).

## Core mechanics to apply

1. **Pre-money vs. post-money.** Post-money = pre-money + new investment. New investor's ownership % = new investment ÷ post-money valuation. Always clarify which the user means if they just say "valuation" — this is the single most common source of confusion and errors compound from it.
2. **Dilution.** Every existing shareholder's percentage drops proportionally when new shares are issued, even though their share *count* doesn't change. Always show both the percentage before and after, and the literal share count if known, so the user sees dilution isn't a "loss" of shares, just of ownership share.
3. **Option pool sizing.** Pools are typically carved out of the pre-money valuation (meaning existing shareholders, not the new investor, bear the dilution from pool expansion) — this is a common negotiating point and worth flagging explicitly when modeling a round, since it changes who bears the dilution.
4. **SAFEs and convertible notes.** These convert into equity at a future priced round, typically at whichever is more favorable to the investor: a valuation cap, or a discount off the new round's price. Model both and show which one actually triggers, since founders are sometimes surprised which mechanism ends up binding.
5. **Multiple rounds compound.** When modeling a sequence of rounds, apply dilution from each round in order — don't calculate final ownership as if only one round happened.

## Workflow

1. Get the concrete inputs: current cap table (or starting ownership %), round size, valuation (pre- or post-money — ask if ambiguous), option pool target, and any outstanding SAFEs/notes with their caps/discounts.
2. If inputs are incomplete, say what's missing and offer to model with reasonable placeholder assumptions clearly labeled as such — don't silently guess.
3. Walk through the math step by step, not just the final table, so the reasoning is checkable.
4. Present a before/after ownership table.
5. If modeling multiple scenarios (e.g. different valuations), lay them side by side so the tradeoff is visible at a glance.

## What NOT to do

- Don't give legal advice on specific term sheet language, liquidation preferences, or protective provisions — flag that a lawyer should review actual documents, and note plainly that this is modeling, not legal or investment advice.
- Don't recommend a specific valuation or tell the user what terms to accept — that's a negotiation and business decision, not a math problem. Give them the numbers to decide with.

## Output format

```markdown
## Cap table model: <scenario name>

**Assumptions:** [list every input used, flagging any that were placeholders]

**Before this round**
| Holder | Shares | % |
|---|---|---|

**After this round**
| Holder | Shares | % | Dilution |
|---|---|---|---|

**Notes:** [anything non-obvious — e.g. which SAFE conversion mechanism triggered, how the option pool dilution was allocated]
```

See `references/safe-conversion-math.md` for the detailed SAFE/note conversion formulas.
