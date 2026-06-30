---
title: Take Profit
status: draft
audience: client
category: Trading Basics
region: global
language: en
owner: Compliance
reviewer:
last_reviewed:
effective_from: 2026-05-29
source_type: official
ai_allowed: false
risk_level: low
version: "1"
---
# Take Profit

## Simple explanation

A Take Profit (often abbreviated TP) is a pending instruction that automatically **closes** an open position when the market moves in your favour to a specified price. Where [[Stop Loss]] caps losses, Take Profit locks in gains — it's a pre-committed decision to exit a winning trade at a level you've defined, before greed or hope causes you to overstay.

A trader using a Take Profit is making a deal with their future self: *if my trade reaches this profit level, I take the win and walk away*. The Take Profit prevents the all-too-common pattern of watching a winning trade reverse into a loss.

## How Take Profit works

When you open a position, you attach a Take Profit at a price level on the *winning* side of the entry:

- **[[Long Position]] (you bought):** Take Profit is placed *above* your entry price. If the market rises to that level, the position closes at a profit.
- **[[Short Position]] (you sold):** Take Profit is placed *below* your entry price. If the market falls to that level, the position closes at a profit.

The Take Profit waits dormant alongside the [[Stop Loss]]. The position remains open until either the market hits one of the two levels, you manually close, or external events (such as [[Stop Out]]) intervene.

## Worked example

You open a long EUR/USD position at 1.1000 with a Stop Loss at 1.0970 and a Take Profit at 1.1060:

- Entry: 1.1000 (Long)
- Stop Loss: 1.0970 (30 pips risk = \$300 max loss on 1 lot)
- Take Profit: 1.1060 (60 pips reward = \$600 profit on 1 lot)
- Risk-to-reward ratio: 1:2

You've pre-committed to two outcomes: either you lose \$300, or you make \$600. The market chooses which.

## Take Profit and risk-to-reward ratio

The relationship between Stop Loss distance and Take Profit distance defines a trade's **risk-to-reward ratio** (R:R). This ratio matters more than win rate for long-term trading viability.

| Risk:Reward | Implication |
|---|---|
| 1:1 | Need >50% win rate to be profitable |
| 1:2 | Profitable at ~33% win rate or better |
| 1:3 | Profitable at ~25% win rate or better |
| 1:5 | Profitable at ~17% win rate or better |

A trader with a 40% win rate using 1:3 R:R is more profitable than a trader with a 70% win rate using 1:1 R:R. **Take Profit placement is what makes high-R:R trading possible** — without an automatic exit at the profit target, traders tend to close winners too early (taking small gains) and let losers run (taking large losses), inverting the math.

## Where to place a Take Profit

Common approaches:

**Technical placement:** Set TP at a key resistance level (for longs) or support level (for shorts), where the market has previously reversed. Logic: the market is likely to stall at known levels, so take profit before that happens.

**Risk-multiple placement:** Set TP at a fixed multiple of the Stop Loss distance. If SL is 30 pips, TP is 60 pips (2× SL) for 1:2 R:R, or 90 pips for 1:3.

**Volatility-based placement:** Use Average True Range. A 3× ATR Take Profit adjusts to instrument volatility — wider profit targets in trending markets, tighter in choppy ones.

**Round-number placement:** Many traders use round numbers (1.1000, 1.1050, 1.1100) as TP levels because these often act as psychological support/resistance.

**Trail-and-extend:** Set an initial TP, and if the market reaches that level, move the TP further while tightening the SL — effectively a manual trailing strategy.

Many professional traders **use both technical and R:R logic together:** find a technically meaningful TP level, then confirm it gives at least 1:2 R:R from the planned Stop Loss. If not, the trade doesn't meet criteria — skip it.

## What Take Profit is NOT

### 1. A guarantee of fill at the exact price

Like [[Stop Loss]] and other pending instructions, a Take Profit is a *trigger* — when the market reaches the level, OPO attempts to close the position at the current market price. In normal conditions this matches the TP level closely. During volatile fast markets, the fill can be at a *better* price (positive slippage, since you're closing a winner) or, occasionally, at a worse price if the market gaps through the level then reverses.

The Client Agreement clause 17.21 specifically addresses TP triggering after dispute resolution:

> Once the dispute has been resolved the OPO GROUP LLC. has the right to trigger the Stop Loss or Take Profit in the chronological order in which they would have been triggered if the Stop Out had not been executed.

So Take Profit triggers retroactively after disputed trades are resolved — meaning the broker honours valid TP triggers even when the position was technically held in dispute resolution.

### 2. A reason to take small profits

Some traders set tight Take Profits (10–15 pips) to "lock in something" on every trade. This pattern is profitable only with very high win rates and tight Stop Losses — and most retail traders cannot sustain those win rates. The combination of "small TPs + standard SLs" produces a negative-expectancy strategy where occasional losses overwhelm many small wins.

Better discipline: take fewer trades with higher-quality setups and bigger TPs, not many trades with small TPs.

### 3. A substitute for trade management

A pre-set Take Profit is a static target — it doesn't know if the market has changed. If a major news event during your trade has invalidated your original thesis, the TP doesn't adjust. Active traders may manually move TPs or close positions early when conditions change, even if the original target hasn't been reached.

## Take Profit and Trailing Stop together

Some traders use the [[Stop Loss|Trailing Stop]] feature instead of a fixed Take Profit — letting the position run as long as the market keeps moving favourably, and closing only when the market reverses by a specified amount. This is mathematically different from a fixed TP:

| Approach | Outcome on a winning trade |
|---|---|
| Fixed TP only | Position closes at TP level — clean profit |
| Trailing Stop only | Position runs until market reverses — captures more of trending moves but exits at a lower price than the peak |
| Both together | Position closes at TP if reached, or at trailing stop if market reverses first |

There is no universally better approach. Trending strategies favour trailing stops; mean-reversion strategies favour fixed TPs.

## Risk warning

Take Profit, like Stop Loss, executes automatically without checking whether market conditions still make sense. A fixed TP set days ago may execute during a news event that has invalidated the original trade thesis — closing the position for a small profit when, had the trader been watching, they could have closed earlier (or held longer) based on the new information. Traders should review pending Take Profit levels regularly, especially on positions held through significant news events or over weekends. The Client Agreement makes no explicit guarantees about Take Profit execution price — like all order types, the trigger creates an instruction to close at market, not a guarantee of exact-price fill. Take Profit is the *easy* discipline tool — it's pleasant to set a profit target. The hard discipline is setting an appropriate [[Stop Loss]] alongside it and respecting the loss when it triggers.

## Source

- OPO Client Agreement v10, clause 17.21 (Take Profit triggering after dispute resolution)
- Note: Take Profit is not formally defined in the Client Agreement Appendix A despite being operationally referenced. This note draws from industry-standard definitions
- Last verified: 2026-05-12

## Internal review notes

- **Take Profit is not defined in the OPO Client Agreement Appendix A.** Like Stop Loss and Pip, this is a fundamental term used throughout but not formally defined. Recommend adding to the next agreement revision alongside Stop Loss and Pip
- Confirm SVG-jurisdiction conventions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm Take Profit trigger price (does it trigger on Ask for long TPs and Bid for short TPs, as is industry standard for closing trades?)
- Confirm typical slippage statistics on Take Profit fills during normal vs volatile conditions
- Consider whether OPO should publish suggested TP placement guidance — the absence of such guidance leaves traders to learn risk-reward concepts from third-party sources

## Related topics

- [[Stop Loss]]
- [[Pending Order]]
- [[Long Position]]
- [[Short Position]]
- [[Open Position]]
- [[Slippage]]
- [[Pip]]
- [[Lot]]
- [[Bid]]
- [[Ask]]
- [[Trailing Stop]]
- [[Force Majeure]]
- [[Margin Level]]
- [[Stop Out]]