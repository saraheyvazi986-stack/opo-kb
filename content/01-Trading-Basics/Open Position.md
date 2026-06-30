---
title: Open Position
status: draft
audience: client
category: Trading Basics
region: global
language: en
owner: Compliance
reviewer:
last_reviewed:
effective_from: 2026-05-30
source_type: official
ai_allowed: false
risk_level: low
version: "1"
---
# Open Position

## Simple explanation

An Open Position is a trade that has been entered but not yet closed. From the moment you buy or sell an instrument until the moment that same instrument is sold or bought back at the equivalent size, the position is "open" — it exists on your account, it ties up [[Margin]], and its value moves continuously with the market.

OPO defines open position in the Client Agreement Appendix A as:

> A Long Position or a Short Position which is not a Completed Transaction.

In plain terms: an open position is half a trade. You've taken one side (buy or sell), but you haven't yet taken the opposite side to close it out.

## What an open position looks like on your account

Every open position contributes to four account metrics in real time:

- **[[Equity]]** — adjusts continuously with the position's [[Floating Profit/Loss]]
- **Used [[Margin]]** — locks up Initial Margin while the position is open
- **[[Free Margin]]** — reduced by the position's used Margin
- **[[Margin Level]]** — moves as Equity changes relative to used Margin

This is why open positions feel "active" in a way that completed trades don't. A completed trade is settled history; an open position is a live exposure that needs monitoring.

## How a position opens and closes

The lifecycle is a chain of well-defined events:

1. **Order placement** — the trader sends a request (market order, pending order, or instruction from an Expert Advisor)
2. **Position opening** — OPO accepts the order and creates the open position. [[Margin]] is locked
3. **Position is open** — [[Floating Profit/Loss]] moves with market price; [[Equity]], [[Free Margin]], and [[Margin Level]] update tick by tick
4. **Position closing** — either by trader manual close, [[Take Profit]] hit, [[Stop Loss]] hit, [[Stop Out]] forced closure, or expiry
5. **[[Completed Transaction]]** — the position is now settled history; Margin is released; final P/L is added to [[Balance]]

Until step 4 happens, the position is "open" and the trader has continuing exposure.

## Matched Positions

The Client Agreement defines a special case where a trader holds both a long and a short of the same instrument at the same time:

> "Matched Positions" shall mean long and Short Positions of the same Transaction Size opened on the Trading Account for the same Instrument.

For example: a trader holds 2 lots long EUR/USD and 2 lots short EUR/USD simultaneously. From a pure market-exposure perspective, these offset each other — the trader has effectively no directional risk on those 4 lots combined.

OPO recognises this and uses a lower [[Hedged Margin]] requirement for matched positions than for two independent same-direction positions. The exact reduction is defined per-instrument in the Contract Specifications.

**Why traders use matched positions:** to "park" a trade idea temporarily (locking in current P/L while keeping both exits available), or as a hedging tool. The strategy has trade-offs — you're still paying [[Spread]] and [[Commission]] on both legs, and Wednesday [[Swap]] charges apply to each side independently.

## What you can do with an open position

While a position is open, the trader can:

- **Close part of it** — partial close, reducing the position size
- **Close all of it** — full close
- **Add to it** — increase the position size by opening another in the same direction
- **Hedge it** — open an offsetting position of the same size (creating matched positions)
- **Modify Stop Loss or Take Profit** — change the auto-close trigger levels
- **Add Trailing Stop** — convert a fixed SL into a trailing one
- **Do nothing** — let the position sit (subject to [[Swap]] charges and the risk of adverse moves)

## Open positions and account events

Several events affect all open positions on an account simultaneously:

- **[[Margin Call]] / [[Stop Out]]** — when account [[Margin Level]] drops too low, OPO forcibly closes positions starting with the largest loser
- **[[Force Majeure]]** — OPO has the right to close any or all open positions at prices it considers appropriate (Client Agreement clause 26.2)
- **Document expiry / Close-Only mode** — if KYC documents lapse and aren't renewed within 15 days, the account enters Close-Only mode: no new positions can be opened, but existing ones can still be closed (clauses 20.6–20.9)
- **Termination of the agreement** — open positions must be settled before the account fully closes (clause 20.3)

## Risk warning

An open position is a live exposure. Unlike completed transactions which are settled and final, open positions can move significantly between when you check your account and when you next look. A position that's \$50 in profit when you go to bed can be hundreds of dollars in loss when you wake up, especially during weekend gaps for instruments that trade through weekends (crypto) or Monday-morning gaps for forex. Traders holding positions overnight, over weekends, or through major news events should size positions accordingly — assume the position can move 2–5× its normal range during these windows. The combination of leverage and open-position drift is the primary cause of unexpected account losses for new traders.

## Source

- OPO Client Agreement v10, Appendix A (Open Position, Matched Positions, Long Position, Short Position definitions)
- OPO Client Agreement v10, clause 26.2 (right to close positions during Force Majeure)
- OPO Client Agreement v10, clauses 20.6–20.9 (Close-Only Mode for expired documents)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm matched position margin reduction percentages per instrument — these should be in Contract Specifications but are not currently summarized for traders in a single place
- Confirm behaviour of open positions during weekend gaps — specifically whether stop losses are honoured at weekend-gap prices or wait for actual Monday open
- Confirm whether all platforms (MT4, MT5, cTrader, OpoTrade) display floating P/L identically — small differences in how unrealized P/L is calculated can cause confusion across platforms

## Related topics

- [[Long Position]]
- [[Short Position]]
- [[Completed Transaction]]
- [[Floating Profit/Loss]]
- [[Margin]]
- [[Hedged Margin]]
- [[Equity]]
- [[Free Margin]]
- [[Margin Level]]
- [[Margin Call]]
- [[Stop Out]]
- [[Stop Loss]]
- [[Take Profit]]
- [[Swap]]
- [[Force Majeure]]
- [[Order]]
- [[Pending Order]]
- [[Transaction Size]]
- [[Spread]]
- [[Commission]]