---
title: Bid
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
# Bid

## Simple explanation

The Bid is the **lower** of the two prices quoted for any tradable instrument. It is the price at which you can **sell**.

OPO defines Bid in the Client Agreement Appendix A as:

> The lower price in the Quote being the price at which the Client may sell.

## How Bid fits into a quote

Every instrument is always quoted with two prices simultaneously:

| Price | What it means | Used when you |
|---|---|---|
| [[Bid]] | The lower price | **Sell** (close a long position or open a short) |
| [[Ask]] | The higher price | **Buy** (open a long position or close a short) |

Example for EUR/USD: `1.10005 / 1.10018`
- Bid = 1.10005 (sell here)
- Ask = 1.10018 (buy here)
- [[Spread]] = 1.3 pips

The Bid is always lower than the Ask. The gap between them is the spread, which is how OPO and the broader market earn revenue on each trade.

## When you interact with Bid

You're trading against the Bid in three situations:

**1. Opening a sell (short) position.** You're selling the instrument to enter the trade, so your entry price is the Bid.

**2. Closing a buy (long) position.** You opened at the Ask; you close by selling, so the exit price is the Bid.

**3. Setting a Sell Limit or Sell Stop order.** Pending sell orders trigger based on the Bid price reaching the requested level.

This is why a long position shows an immediate paper loss when opened — you entered at the Ask, but the platform shows the position's current value at the Bid. The position must move at least one full spread in your favour before it breaks even.

## Bid in practice

When traders look at a price chart, the line drawn is usually the Bid price — because charts traditionally represent "the current market" from a seller's perspective. The Ask line, if shown, sits slightly above. Most platforms allow toggling chart price source (Bid, Ask, or midpoint) in the settings.

## Source

- OPO Client Agreement v10, Appendix A (Bid definition)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction terms apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm which price (Bid, Ask, midpoint) is the default chart source on MT4, MT5, cTrader, and OpoTrade — this affects how traders read their charts

## Related topics

- [[Ask]]
- [[Spread]]
- [[Quote]]
- [[Long Position]]
- [[Short Position]]
- [[Pip]]
- [[Pending Order]]