---
title: Quote
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
# Quote

## Simple explanation

A quote is the pair of prices — Bid and Ask — that OPO shows you for an instrument at any given moment. It is the broker's offer to buy from you (at the [[Bid]]) and sell to you (at the [[Ask]]). The gap between these two prices is the [[Spread]].

OPO defines quote in the Client Agreement Appendix A as:

> The information of the current price for a specific Instrument, in the form of the Bid and Ask prices.

## Anatomy of a quote

A typical EUR/USD quote on OPO looks like this:

- **Bid (1.10005)** — the price at which you can sell EUR/USD right now
- **Ask (1.10018)** — the price at which you can buy EUR/USD right now
- **Spread (1.3 pips)** — the gap between them

Both prices update continuously as the market moves. Most modern platforms update quotes multiple times per second.

## Where quotes come from

The Client Agreement clause 11.5 explains that quotes are derived from market sources:

> The Client is entitled to Market Data which are data produced directly by an Exchange and/or Liquidity Provider and/or Price Feeder, to be able to give Orders for Transactions...

In plain terms: OPO aggregates pricing from interbank liquidity providers, exchanges, and other price feeders, then shows you the combined best-available Bid and Ask. The quote you see is OPO's pricing — not raw market data — because the broker may add a markup, particularly on non-ECN accounts.

## Quotes vs Indicative Quotes

The Client Agreement distinguishes between an actionable quote and an "Indicative Quote." From Appendix A:

> "Indicative Quote" shall mean a Quote at which OPO GROUP LLC. has the right not to accept any Instructions or execute any Orders.

This means: under certain conditions (low liquidity, abnormal market conditions, technical issues), the displayed price may be **informational only** — OPO may decline to actually trade at that price. Indicative quotes are most common during:

- Pre-market or after-hours trading on certain instruments
- The first few seconds after a major news release
- [[Force Majeure]] or abnormal market conditions
- Quote source disruptions

In normal market conditions, the quote you see is actionable. The Indicative Quote provision exists for the broker's protection during unusual events.

## When quotes can change without notice

The Client Agreement clause 11.4 gives OPO broad rights to adjust the [[Spread]] component of quotes:

> OPO GROUP LLC. specifies Spread for each Instrument in the Contract Specifications. OPO GROUP LLC. is entitled to change Spreads without prior Written Notice to the Client subject to the Terms of Business. Otherwise, OPO GROUP LLC. shall notify the Client not less than 7 (seven) calendar days prior to any changes in Spreads.

So under normal conditions, spread changes require 7 days' notice. Under "Terms of Business" exception conditions (volatility, news, liquidity events), the broker can widen the spread immediately.

## What a quote does NOT do

Two important limitations from the Client Agreement clause 7.6:

**1. A quote is not investment advice.** Seeing a quote doesn't mean OPO is recommending the trade. The quote exists so you can make your own decision.

**2. A quote may differ from the actual execution price.** Clause 11.5(b) is explicit:

> Any Order that the Client gives to the Company constitutes an irrevocable instruction to the Company to proceed with the Transaction on the Client's behalf. In addition, any price quoted in the Market Data may differ from the execution price the Client obtains.

This is normal — between the moment you see a price and the moment your order reaches the broker's server, the market may have moved. The actual fill might be at a slightly worse (or better) price. See [[Slippage]] for what happens when this happens at scale.

## Error quotes and spikes

The Client Agreement defines two specific kinds of bad quotes that OPO can void:

**[[Error Quote]]** — a quote received by the platform due to a system or technical error.

**[[Error Quote (Spike)]]** — an Error Quote with the following characteristics (Appendix A):
- A significant [[Price Gap]]
- The price rebounds with another Price Gap shortly after
- No rapid price movements occurred before it
- No major economic news was released around the time
- The price diverges significantly from market pricing

When an Error Quote (Spike) is detected, OPO has the right to delete it from the server and treat any trades executed at that price as void. This protects both the broker and other traders from manipulation or technical glitches.

This is also why the Client Agreement clause 17.17 states that complaints about profits made from temporary excess Free Margin gained through Spike-priced trades are not accepted — those profits are nullified retroactively.

## Quotes during news and rollover

Two predictable times when quotes behave unusually:

**Major news releases** (NFP, central bank decisions, CPI): spreads widen dramatically — sometimes 5–10× normal — and execution becomes unpredictable for the first 5–30 seconds. Quotes during this window may be Indicative.

**Rollover** (around 5pm New York time): spreads widen briefly as liquidity providers reset for the new trading day. Most trading platforms show this as a quote freeze or visible spread spike. Quotes shown during rollover may not be actionable.

## Risk warning

The quote you see on screen is not a guarantee of execution price. In normal conditions, the gap between displayed and executed price is small (sub-pip), but during volatile or low-liquidity periods, [[Slippage]] can be significant. Stop Loss orders placed in fast markets may execute at much worse prices than the requested level. Traders should never assume the quoted price equals the executable price, especially when trading around news events, during rollover, or on instruments with thin liquidity (exotic forex, illiquid stocks, smaller cryptocurrencies).

## Source

- OPO Client Agreement v10, Appendix A (Quote, Indicative Quote, Error Quote, Error Quote (Spike), Quotes Base, Quotes Flow definitions)
- OPO Client Agreement v10, clause 11.4 (right to change spreads)
- OPO Client Agreement v10, clause 11.5 (market data and execution price)
- OPO Client Agreement v10, clause 7.6 (quotes are not investment advice)
- OPO Client Agreement v10, clause 17.17 (Spike-derived profits voided)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm OPO's liquidity providers — these aren't disclosed in the Client Agreement but are sometimes published in regulatory filings, and traders increasingly ask about LP relationships
- Confirm the typical magnitude of slippage during news events on OPO — actual data would be more useful than the generic warning
- Consider documenting the Indicative Quote conditions more explicitly than the agreement does — when exactly does a quote become indicative

## Related topics

- [[Bid]]
- [[Ask]]
- [[Spread]]
- [[Pip]]
- [[Slippage]]
- [[Error Quote]]
- [[Error Quote (Spike)]]
- [[Price Gap]]
- [[Force Majeure]]
- [[Abnormal Market Conditions]]
- [[Market Data]]
- [[Order]]
- [[Pending Order]]