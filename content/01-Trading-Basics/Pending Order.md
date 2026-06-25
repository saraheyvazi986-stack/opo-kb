---
title: Pending Order
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
# Pending Order

## Simple explanation

A pending order is an instruction to OPO to open a position **automatically** when the market reaches a specified price — not now, but later, when conditions you've defined are met. The order sits dormant on the broker's server until the market price reaches your trigger level, at which point it converts into an active position.

OPO defines pending order in the Client Agreement Appendix A as:

> An instruction from the Customer to the Company to open a position once the price has reached the level of the Order.

## Why pending orders exist

A pending order solves three trader problems:

1. **Trading without watching screens.** You can set an entry plan, walk away, and have it execute automatically if your level hits.
2. **Disciplined entries.** Forcing yourself to pre-commit to a price prevents emotional "I'll just buy here, the market feels right" decisions.
3. **Strategy automation.** Algorithmic strategies (EAs on MetaTrader, cBots on cTrader) place pending orders as part of their logic.

## The four pending order types

OPO supports the four standard pending order types (Client Agreement clause 12.3(g) and Appendix A's definition of "Order"). The four types split along two dimensions: direction (buy or sell) and trigger style (limit or stop).

| Order type | Triggers when | Used to |
|---|---|---|
| **Buy Limit** | [[Ask]] drops to your level | Buy at a *better* (lower) price than now |
| **Sell Limit** | [[Bid]] rises to your level | Sell at a *better* (higher) price than now |
| **Buy Stop** | [[Ask]] rises to your level | Buy at a *worse* (higher) price than now — typically on breakout |
| **Sell Stop** | [[Bid]] drops to your level | Sell at a *worse* (lower) price than now — typically on breakdown |

## Limit vs Stop — the key distinction

The confusing part for new traders is the difference between **limit** and **stop** orders. They sound similar but mean opposite things.

**Limit orders** wait for the price to come *to you* at a better level:
- "Buy EUR/USD if it drops to 1.0950" → Buy Limit at 1.0950 (current price is higher)
- "Sell EUR/USD if it rises to 1.1100" → Sell Limit at 1.1100 (current price is lower)

**Stop orders** wait for the price to *break through* a level — momentum entries:
- "Buy EUR/USD if it breaks above 1.1100" → Buy Stop at 1.1100 (current price is lower)
- "Sell EUR/USD if it breaks below 1.0950" → Sell Stop at 1.0950 (current price is higher)

A practical way to remember: **limit = patience** (waiting for a good price), **stop = momentum** (entering when something happens).

## When pending orders are accepted (or rejected)

The Client Agreement clause 12.3 lists the conditions a pending order must meet to be accepted. Failure of any of these can cause rejection:

- Quote must be valid and not [[Error Quote (Spike)|spike-driven]]
- Internet connection must not have dropped before the broker received the instruction
- Order size must meet the minimum [[Lot Size 1]] for the instrument
- A [[Force Majeure]] event must not be active
- The trader has sufficient [[Free Margin]] to cover the [[Initial Margin]] when the order triggers
- OPO does not suspect money laundering, terrorist financing, or other criminal activity
- A court order or regulatory directive does not prohibit the trade
- OPO has not sent a notice of agreement termination

If any of these fail at the moment the trigger price hits, the order can be rejected or partially filled.

## How long pending orders stay active

Pending orders remain active until one of three things happens:
1. The trigger price is hit and the order executes
2. The trader manually cancels the order
3. OPO reaches the end of the order's set expiry (usually GTC — "Good Till Canceled" — or a specific date/time set by the trader)

The Client Agreement clause 12.6 gives OPO the right to delete cancelled pending orders that are older than 1 month from the trading account history:

> OPO GROUP LLC. has the right to delete any canceled Pending Orders older than 1 month from the Client's Trading Account history.

So if you cancel a pending order and later want to verify what level it was at, you have about a month before that history may disappear.

## Pending orders during volatile market moves

During fast markets, pending orders can be filled at significantly worse prices than the trigger level — see [[Slippage]]. This is most common with:

- **Stop orders during news events** — a Buy Stop placed at 1.1100 might fill at 1.1130 if a major news release causes a price gap upward through your level
- **Pending orders at illiquid market opens** — Monday morning gaps can fill weekend-pending orders at significantly different prices
- **Orders on volatile instruments** — crypto, exotic forex, and indices during major events all routinely produce slippage

Limit orders, in contrast, can sometimes fill at *better* than requested prices (rare, but possible), because they trigger when the price reaches the level and may execute at the exact level or slightly inside the spread.

## Pending orders and Stop Out

When OPO triggers [[Stop Out]] and closes your open positions, **pending orders are not automatically cancelled**. This is important: a trader who experiences Stop Out and forgets to clear their pending orders can have new positions opened automatically if the market moves to their pending trigger levels. The Stop Out closed the *open* positions but left the *future entry plans* in place.

Always review and cancel orphaned pending orders after a Stop Out event.

## Risk warning

Pending orders execute automatically — they don't ask permission and don't check whether market conditions have changed since you placed them. A Buy Limit placed before a weekend at a level just below current price might trigger Monday morning at a much worse price if the market gaps. A Buy Stop placed expecting a clean breakout might fill in the middle of a sudden news-driven spike. Traders using pending orders should understand that the trigger price is not the guaranteed fill price — [[Slippage]] can be substantial in fast markets. Traders should also routinely review their list of active pending orders, especially after market-moving events, to ensure plans set days or weeks ago still make sense for current conditions.

## Source

- OPO Client Agreement v10, Appendix A (Pending Order, Order, Order Level definitions)
- OPO Client Agreement v10, clause 12.3 (conditions for accepting orders)
- OPO Client Agreement v10, clause 12.6 (deletion of canceled orders older than 1 month)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm whether pending orders trigger on Bid, Ask, or last-traded price per instrument class — this varies by broker and the OPO Client Agreement doesn't fully specify. The standard convention is Buy orders trigger on Ask and Sell orders trigger on Bid, but should be verified
- Confirm pending order behaviour during weekend gaps, especially for crypto (which trades 24/7) versus forex (which has weekend gaps) — these behave differently
- Confirm OPO's typical slippage statistics during news events — actual data would help traders calibrate expectations
- Confirm what happens to active pending orders during a [[Force Majeure]] event

## Related topics

- [[Order]]
- [[Bid]]
- [[Ask]]
- [[Quote]]
- [[Slippage]]
- [[Lot]]
- [[Free Margin]]
- [[Initial Margin]]
- [[Stop Loss]]
- [[Take Profit]]
- [[Stop Out]]
- [[Force Majeure]]
- [[Error Quote (Spike)]]
- [[Open Position]]
- [[Long Position]]
- [[Short Position]]
- [[Contract Specifications]]