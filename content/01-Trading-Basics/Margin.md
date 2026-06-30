---
title: Margin
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

# Margin

## Simple explanation

Margin is the deposit you must hold in your trading account to open and maintain a leveraged position. It is not a fee or a cost — it is collateral that secures the position. When you close the position, the margin is released back into your available balance, adjusted for any profit or loss on the trade.

OPO defines margin in the Client Agreement as "the necessary guarantee funds to maintain Open Positions, as determined in the Contract Specifications for each Instrument" (Appendix A).

## Why margin exists

When a trader uses [[Leverage]] (for example, 1:100), they control a position much larger than the cash they have deposited. The broker is effectively allowing the trader to trade on borrowed buying power. Margin is the trader's collateral — the amount the broker requires the trader to put up against the borrowed exposure. If the position moves against the trader, the margin absorbs the loss; if the loss approaches the margin amount, the broker is forced to close the position to prevent further losses.

## Two types of margin OPO distinguishes

The Client Agreement (clause 14) and Appendix A define two specific margin types:

### Initial Margin

The margin required to **open** a position. Calculated based on the trade size, leverage, and the instrument's Contract Specifications. When a trader places an order, [[Free Margin]] must be sufficient to cover the Initial Margin requirement (Client Agreement clause 12.3(j)) or the order is rejected.

### Hedged Margin

The margin required to maintain **matched positions** — for example, a 2-lot long position and a 2-lot short position on the same instrument. Because the two positions offset each other's market exposure, the Hedged Margin is typically lower than the Initial Margin for two independent positions of the same size. The exact value is defined per instrument in the Contract Specifications.

## How margin connects to your account

Margin is one of five interlocking concepts on every trader's account screen:

- [[Balance]] — total cash in the account from deposits, withdrawals, and closed trades
- [[Equity]] — Balance plus or minus profit/loss on open positions in real time
- **Margin (used)** — the portion of Equity locked up as collateral for open positions
- [[Free Margin]] — the portion of Equity available to open new positions (Equity minus used Margin)
- [[Margin Level]] — Equity as a percentage of used Margin (the key risk metric)

When Margin Level drops too low, OPO is contractually entitled to close positions automatically — see [[Margin Call]] and [[Stop Out]].

## How margin is calculated

The exact formula depends on the instrument, but the general structure is:

For example, opening a 1-lot EUR/USD position (100,000 EUR) at a price of 1.10, on 1:500 leverage:
So \$220 of the trader's Free Margin is locked as Initial Margin for that one position. The remaining Free Margin is available for further positions.

For exact margin requirements per instrument, traders should consult the Contract Specifications on the OPO website or inside their trading platform.

## Margin currency conversion

If the instrument is denominated in a different currency than the trader's account, OPO converts the margin requirement into the account currency at the prevailing exchange rate (Client Agreement clauses 10.1, 14.9). Traders trading non-USD instruments on a USD account should be aware that the converted margin requirement can fluctuate with exchange rate movements.

## When margin requirements can change

The Client Agreement gives OPO the right to change margin requirements in several scenarios:

- With **3 business days' written notice** under normal market conditions (clause 14.3)
- **Without notice** during a [[Force Majeure]] event (clause 14.4)
- **Without notice** during exceptional market conditions including abnormal volatility, low liquidity, market disruptions, trading halts, pricing anomalies, or geopolitical events (clause 14.12)

When margin requirements are increased, the new requirement applies to both new positions and positions already open (clause 14.5). This means a trader holding open positions could find their used Margin recalculated upward without warning during volatile conditions, potentially reducing Free Margin or triggering margin pressure.

## Your responsibilities as a trader

The Client Agreement explicitly places several responsibilities on the trader (clauses 14.1, 14.7, 14.8):

- **Understanding how margin is calculated** is the trader's responsibility, not the broker's
- **Notifying OPO** as soon as the trader believes they will be unable to meet a margin payment
- **OPO is not obliged to make margin calls** — see [[Margin Call]]. Traders cannot rely on receiving a warning before automatic position closure
- **Monitoring the account** — OPO is not liable for any failure to contact a trader about margin levels

## Risk warning

Trading on margin amplifies both potential gains and potential losses. A small adverse move in the market can result in losses that exceed the deposited margin, though OPO provides [[Negative Balance Protection]] for retail accounts (Client Agreement clause 15.8). Traders should understand exactly how margin is calculated for their chosen instruments before placing trades, and should never deposit funds they cannot afford to lose. Margin requirements can be changed by OPO with limited or no notice in certain conditions, which can put pressure on open positions unexpectedly.

## Source

- OPO Client Agreement v10, clause 14 (Margin Requirements) and Appendix A (Margin, Initial Margin, Hedged Margin, Necessary Margin definitions)
- OPO Contract Specifications (instrument-by-instrument margin requirements)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split into region-specific notes when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm the worked-example calculation is the actual formula OPO uses (it's the industry-standard formula but should be cross-checked with operations)
- Confirm Contract Specifications are accessible to clients pre-account-opening, or only after login
- Confirm whether Hedged Margin applies the same way on cTrader-family accounts as on MetaTrader-family accounts

## Related topics

- [[Leverage]]
- [[Equity]]
- [[Balance]]
- [[Free Margin]]
- [[Margin Level]]
- [[Margin Call]]
- [[Stop Out]]
- [[Negative Balance Protection]]
- [[Force Majeure]]
- [[Initial Margin]]
- [[Hedged Margin]]
- [[Necessary Margin]]
- [[Contract Specifications]]