---
title: Order
status: draft
audience: client
category: Trading Basics
region: global
language: en
owner:
reviewer:
last_reviewed:
effective_from: 2026-05-29
source_type: official
ai_allowed: false
risk_level: low
version: "1"
---
# Order

## Simple explanation

An Order is an instruction from a trader to OPO to open or close a position. It is the formal request that turns a trading decision into an actual trade. Every position that exists on your account started as an order — whether placed manually, by an Expert Advisor, or as a pending instruction.

OPO defines order in the Client Agreement Appendix A as:

> An instruction from the Client to OPO GROUP LLC. to open or close a position when the price reaches the Order Level.

And **Order Level** as:

> The price indicated in the Order.

## The two broad order categories

All orders fall into one of two categories:

### Market Orders

A request to execute *immediately* at the current market price. The trader is saying: "Open this position right now, at whatever the price happens to be."

- Used when entering or exiting a trade based on real-time decisions
- Fills typically happen within milliseconds in normal market conditions
- May experience [[Slippage]] in fast markets — the fill price can differ from the quoted price

### [[Pending Order|Pending Orders]]

A request to execute *later*, when the market reaches a specified price. The trader is saying: "Open this position when the market gets to this level."

Four pending order types:
- **Buy Limit** — buy when price drops to a specified level (better than current)
- **Sell Limit** — sell when price rises to a specified level (better than current)
- **Buy Stop** — buy when price breaks above a specified level (worse than current — breakout entry)
- **Sell Stop** — sell when price breaks below a specified level (worse than current — breakdown entry)

See [[Pending Order]] for full details on each type.

## The Order lifecycle

Every order goes through a sequence of states:

1. **Placement** — trader sends the request
2. **Validation** — OPO checks the order against acceptance conditions (Client Agreement clause 12.3): valid quote, sufficient [[Free Margin]], market open, no [[Force Majeure]], no money-laundering suspicion, etc.
3. **Acceptance or rejection** — broker either accepts or rejects with a reason
4. **For market orders:** immediate execution at current market price
5. **For pending orders:** the order waits dormant until the trigger price is reached, then converts to a market order at that moment
6. **Fill** — the order executes and creates an [[Open Position]] (for entry orders) or closes one (for exit orders)
7. **History** — the order and resulting trade are recorded in trade history

## Order rejection — common reasons

The Client Agreement clause 12.3 lists conditions under which OPO will reject an order:

- A quote must be obtained (the market must be open and quoting)
- Quote must not be indicative or marked erroneous
- Quote must not be a spike-driven [[Error Quote (Spike)]]
- Internet connection must not have dropped before the broker received the instruction
- Order size must meet the minimum [[Lot Size 1]] for the instrument
- A [[Force Majeure]] event must not be active
- Trader must have sufficient [[Free Margin]] to cover the [[Initial Margin]]
- OPO must not suspect money laundering, terrorist financing, or other criminal activity
- A regulatory or court order must not prohibit the trade
- A notice of agreement termination must not have been sent

Rejected orders typically return an error code visible in the trading platform. Common rejections in practice: insufficient margin (most common), market closed, weekend gap protection.

## Modifying or cancelling orders

After placement but before fill:

- **Pending orders** can be modified (change the trigger price, change Stop Loss / Take Profit attached to them) or cancelled entirely
- **Market orders** typically can't be modified — they fill too quickly. They can sometimes be partially executed if too large for available liquidity

After fill:

- **The resulting position** can be modified (close partially, adjust Stop Loss / Take Profit, add hedging trades)
- **The order itself** is history — you can't undo a filled order, only manage the resulting position

The Client Agreement clause 12.6 limits cancellation history retention:

> OPO GROUP LLC. has the right to delete any canceled Pending Orders older than 1 month from the Client's Trading Account history.

So cancelled pending orders disappear from your platform after about a month.

## Orders and slippage

For market orders and triggered pending orders, the executed price may differ from the price you saw when placing the order. This is [[Slippage]]. It can be:

- **Negative** (worse than expected) — most common, especially during news events or fast markets
- **Positive** (better than expected) — less common but does occur, especially on limit orders

OPO's Client Agreement clause 16.3(j) explicitly lists slippage as something OPO is not liable for. Traders accept slippage as a normal part of trading.

## Source

- OPO Client Agreement v10, Appendix A (Order, Order Level definitions)
- OPO Client Agreement v10, clause 12.3 (conditions for accepting orders)
- OPO Client Agreement v10, clause 12.6 (deletion of cancelled orders after 1 month)
- OPO Client Agreement v10, clause 16.3(j) (slippage non-liability)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm whether OPO publishes rejected-order statistics or typical rejection rates by reason
- Confirm whether order modifications during fast markets are restricted on any platform
- Consider documenting the specific error codes traders may see when orders are rejected — this would help support reduce inbound questions

## Related topics

- [[Pending Order]]
- [[Open Position]]
- [[Completed Transaction]]
- [[Slippage]]
- [[Quote]]
- [[Free Margin]]
- [[Initial Margin]]
- [[Stop Loss]]
- [[Take Profit]]
- [[Lot]]
- [[Lot Size 1]]
- [[Force Majeure]]
- [[Error Quote (Spike)]]
- [[Bid]]
- [[Ask]]