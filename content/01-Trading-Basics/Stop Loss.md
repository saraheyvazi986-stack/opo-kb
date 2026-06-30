---
title: Stop Loss
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
# Stop Loss

## Simple explanation

A Stop Loss (often abbreviated SL) is a pending instruction that automatically **closes** an open position when the market moves against you to a specified price. It is the trader's primary risk-management tool — a pre-committed decision to cap losses at a level you choose, before emotion or hope can intervene.

A position without a Stop Loss is a position with unlimited downside (within the broker's [[Stop Out]] limit). A position with a Stop Loss is a position with a known, bounded maximum loss.

## How Stop Loss works

When you open a position, you attach a Stop Loss at a price level on the *losing* side of the entry:

- **[[Long Position]] (you bought):** Stop Loss is placed *below* your entry price. If the market falls to that level, the position closes at a loss.
- **[[Short Position]] (you sold):** Stop Loss is placed *above* your entry price. If the market rises to that level, the position closes at a loss.

The Stop Loss waits dormant. The position remains open until either: (a) the market hits the Stop Loss price and the position closes automatically, or (b) you close the position manually, or (c) the position hits a [[Take Profit]] level (if you also set one).

## Worked example

You open a long EUR/USD position at 1.1000 with a Stop Loss at 1.0970:

- Entry: 1.1000 (Long)
- Stop Loss: 1.0970 (30 pips below entry)
- Lot size: 1.0
- Maximum loss if SL triggers: 30 pips × \$10/pip = **\$300**

Whatever the market does, your loss on this trade is capped at approximately \$300 (assuming no slippage). Even if EUR/USD crashes 500 pips overnight, your loss stops at 30 pips. The Stop Loss is your circuit breaker.

## What Stop Loss is NOT

Three things Stop Loss does not do — and the Client Agreement is explicit about each:

### 1. A guarantee of exit price

The Client Agreement clause 16.3(n) explicitly states OPO is not liable for losses arising from:

> The Client relying in Stop Loss Orders;

This means: a Stop Loss is a triggering mechanism, not a guaranteed exit price. When the trigger fires, OPO attempts to close the position at the current market price — which can be significantly worse than the Stop Loss level during:

- **Price gaps** (Monday opens, post-news jumps, weekend crypto moves)
- **Fast markets** (news releases, flash crashes)
- **Low liquidity periods** (Asian session for European pairs, holidays)

A Stop Loss at 1.0970 can fill at 1.0950, 1.0900, or even worse if the market gaps through the level. This is called [[Slippage]].

### 2. An income source

A Stop Loss doesn't earn anything. Many beginners think "if my stop is hit, I lose, but if it's not, I win" — but a position can sit indefinitely below entry, slowly bleeding [[Swap]] charges, never triggering the SL, never reaching profitability. The Stop Loss is a defensive tool, not a strategy.

### 3. A substitute for position sizing

A trader using a 50-pip Stop Loss on a 10-lot trade has a \$5,000 maximum loss. A trader using a 50-pip Stop Loss on a 0.1-lot trade has a \$50 maximum loss. **The Stop Loss is in pips; the actual dollar risk is set by lot size**. See [[Lot]] for position-sizing math.

## Where to place a Stop Loss

There is no universally correct Stop Loss distance — it depends on strategy, instrument volatility, and risk tolerance. Common approaches:

**Technical placement:** Set the SL just beyond a key support/resistance level, swing low/high, or technical indicator (moving average, Bollinger band edge). The logic: if price breaks that level, the trade idea is invalidated.

**Volatility-based placement:** Use Average True Range (ATR) to set SL at a multiple of typical price movement. A 2× ATR stop adjusts to current volatility — wider stops in choppy markets, tighter in calm ones.

**Fixed-pip placement:** Always 30 pips below entry, for example. Simple but doesn't adapt to market conditions.

**Risk-based placement:** Calculate from the dollar amount you're willing to risk. If you'll risk \$50 on a trade at \$1/pip (0.1 lot), your SL must be within 50 pips of entry.

**Most professional traders combine technical and risk-based approaches:** find a technically valid SL level, calculate the dollar risk at that distance, and adjust lot size so the risk matches their per-trade rule (usually 1–2% of account).

## Trailing Stop Loss

A Trailing Stop is a Stop Loss that automatically adjusts in your favour as the market moves your way. For a long position:

- Initial Stop Loss: 1.0970 (30 pips below entry at 1.1000)
- Market rises to 1.1050. Trailing Stop tightens to 1.1020 (now 30 pips below current price)
- Market rises to 1.1100. Trailing Stop tightens to 1.1070
- Market reverses to 1.1071. Position closes — but at a \$700 profit, not a \$300 loss

The Trailing Stop locks in profits while still using the same "cap losses if the market reverses" logic.

**Caveat from Client Agreement clause 16.3(m):**

> The Client using Trailing Stop and/or Expert Adviser;

is listed as one of the items OPO is not liable for. Trailing Stops depend on platform connectivity and continuous price updates — if the platform disconnects briefly, the trail may not adjust, and the original SL applies.

## Stop Loss and Stop Out

These two have similar names and similar mechanics, but they serve different parties:

| | [[Stop Loss]] | [[Stop Out]]                  |
| ---------------------------- | ------------------------ | ----------------------------- |
| Who sets it | The trader | OPO (system, automatic)       |
| Per-position or account-wide | Per-position | Account-wide                  |
| Triggered by | Specific price level | [[Margin Level]] reaching 20% |
| Purpose | Trader's risk management | Broker's protection           |
| Avoidable | Yes (just don't set one) | No (contractual)              |

A trader using proper Stop Losses on every trade almost never reaches Stop Out — because their losses are capped well before [[Margin Level]] approaches 20%. Stop Out only triggers when traders run too many positions without stops, or with stops set so far away that several positions can lose simultaneously.

## Risk warning

A Stop Loss is the single most important risk management tool a trader has, but it is not foolproof. In fast markets, Stop Losses fill at worse prices than requested ([[Slippage]]) — sometimes dramatically worse. During price gaps (weekend opens, post-news jumps), the slippage can exceed the planned loss by a significant multiple. Traders should treat the Stop Loss as a typical cap on losses, not an absolute guarantee. Position sizing — choosing lot size so that even worst-case slippage stays within an acceptable dollar loss — is the necessary complement to a Stop Loss. A Stop Loss with too-large position size is not risk management; it is a hope that the market behaves normally. The Client Agreement explicitly disclaims OPO's liability for traders relying on Stop Loss orders (clause 16.3(n)) — the responsibility for setting appropriate stops and appropriate sizes belongs entirely to the trader.

## Source

- OPO Client Agreement v10, clause 16.3(n) (OPO not liable for Stop Loss reliance)
- OPO Client Agreement v10, clause 16.3(m) (OPO not liable for Trailing Stop / Expert Advisor)
- OPO Client Agreement v10, clause 17.21 (Stop Loss / Take Profit triggering after dispute resolution)
- Note: Stop Loss is not formally defined in the Client Agreement Appendix A despite being operationally referenced. This note draws from industry-standard definitions
- Last verified: 2026-05-12

## Internal review notes

- **Stop Loss is not defined in the OPO Client Agreement Appendix A.** Like Pip, this is a fundamental term used throughout but not formally defined. Recommend adding to the next agreement revision
- Confirm SVG-jurisdiction conventions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm Stop Loss trigger price (does it trigger on Bid for long SLs and Ask for short SLs, as is industry standard?)
- Confirm Trailing Stop behaviour during platform disconnections — does the trail freeze or revert to last server-known position
- Confirm typical Stop Loss slippage statistics on OPO during news events
- Consider documenting OPO's "Guaranteed Stop Loss" status — some brokers offer guaranteed stops as a premium feature; OPO's account pages don't appear to mention this, but should be confirmed for completeness

## Related topics

- [[Take Profit]]
- [[Pending Order]]
- [[Long Position]]
- [[Short Position]]
- [[Open Position]]
- [[Slippage]]
- [[Stop Out]]
- [[Margin Level]]
- [[Pip]]
- [[Lot]]
- [[Bid]]
- [[Ask]]
- [[Swap]]
- [[Expert Advisors]]
- [[Trailing Stop]]
- [[Force Majeure]]