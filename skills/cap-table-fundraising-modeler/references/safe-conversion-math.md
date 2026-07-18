# SAFE / convertible note conversion math

## Valuation cap conversion
Conversion price = Valuation cap ÷ Fully-diluted shares outstanding (pre-money, pre-new-round)
Shares issued to SAFE holder = Investment amount ÷ Conversion price

## Discount conversion
Conversion price = New round price per share × (1 − discount %)
Shares issued to SAFE holder = Investment amount ÷ Conversion price

## Which one triggers
Whichever conversion price is *lower* is more favorable to the investor and is the one that actually applies — compute both and use the smaller resulting conversion price (i.e. the one that issues more shares to the SAFE holder), unless the specific instrument's terms say otherwise (some SAFEs are cap-only or discount-only).

## Post-money SAFEs (YC-style, post-2018)
These directly state the investor's ownership percentage on a post-money basis rather than requiring a share-count calculation — read the specific SAFE's terms carefully, since "post-money SAFE" and "pre-money SAFE" use meaningfully different math and are easy to conflate.

## Option pool shuffle
When a priced round includes an option pool expansion carved from pre-money, the pool dilution is borne by pre-round shareholders (founders + earlier investors), not the new investor — this is a standard but often underappreciated negotiating point worth surfacing explicitly in any round model.
