---
title: Ask
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
 **Ask**

## Simple explanation

The Ask is the **higher** of the two prices quoted for any tradable instrument. It is the price at which you can **buy**.

OPO defines Ask in the Client Agreement Appendix A as:

> The higher price in the Quote being the price at which the Client may buy.

## How Ask fits into a quote

Every instrument is always quoted with two prices simultaneously:

| Price | What it means | Used when you |
|---|---|---|
| [[Bid]] | The lower price | **Sell** (close a long position or open a short) |
| [[Ask]] | The higher price | **Buy** (open a long position or close a short) |

Example for EUR/USD: `1.10005 / 1.10018`
- Bid = 1.10005 (sell here)
- Ask = 1.10018 (buy here)
- [[Spread]] = 1.3 pips

The Ask is always higher than the Bid. The gap between them is the [[Spread]] — the broker's primary revenue mechanism on most trades.

## When you interact with Ask

You're trading against the Ask in three situations:

**1. Opening a buy (long) position.** You're buying the instrument to enter the trade, so your entry price is the Ask.

**2. Closing a sell (short) position.** You opened at the Bid; you close by buying back, so the exit price is the Ask.

**3. Setting a Buy Limit or Buy Stop order.** Pending buy orders trigger based on the Ask price reaching the requested level.

This is why a short position shows an immediate paper loss when opened — you entered at the Bid, but the platform shows the position's current value at the Ask. The position must move at least one full spread in your favour before it breaks even.

## Ask vs Bid — quick reference

The simplest mnemonic: **B for Buy = the higher price (Ask), S for Sell = the lower price (Bid)** is *wrong*. The correct mapping is:

- **B**id is the **B**ottom price → you **S**ell here
- **A**sk is **A**bove → you bu**Y** here

Another way to remember: the broker "asks" you to pay more (the higher price) to buy. The broker "bids" less (the lower price) when buying from you.

## Source

- OPO Client Agreement v10, Appendix A (Ask definition)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction terms apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm which price (Bid, Ask, midpoint) is the default chart source on MT4, MT5, cTrader, and OpoTrade

## Related topics

- [[Bid]]
- [[Spread]]
- [[Quote]]
- [[Long Position]]
- [[Short Position]]
- [[Pip]]
- [[Pending Order]]