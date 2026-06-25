---
title: Lot Size
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
# Lot Size

## Simple explanation

Lot Size is the number of units of an instrument contained in **one standard [[Lot]]**. It defines what "1 lot" actually means for each tradable instrument — and that meaning varies by instrument class.

OPO defines lot size in the Client Agreement Appendix A as:

> The number of shares, underlying assets or units of Base Currency, or troy oz. of Precious Metal in one Lot defined in the Contract Specifications.

In plain terms: Lot Size is *what's inside* one lot. Lot Size for EUR/USD is 100,000 EUR. Lot Size for gold is 100 troy ounces. The specific number depends on the instrument.

## Standard Lot Sizes at OPO

From industry standard practice and OPO's Contract Specifications:

| Instrument class | 1 standard lot |
|---|---|
| Forex (most pairs) | 100,000 units of the [[Base Currency]] |
| Gold (XAU/USD) | 100 troy ounces |
| Silver (XAG/USD) | 5,000 troy ounces |
| Indices (e.g. S&P 500) | Typically 1 contract |
| Commodities (oil, gas) | Varies by instrument |
| Cryptocurrencies | Typically 1 unit of base crypto |
| Stocks (CFDs) | Typically 1 share |

Exact Lot Size per instrument is published in OPO's Contract Specifications, accessible inside the trading platform or via the website.

## Why Lot Size matters

Lot Size is the conversion factor between two ways of expressing a trade:

- **Trader's mental model:** "I want to trade 2 lots of EUR/USD"
- **Market reality:** 200,000 EUR is moving

This conversion shapes every downstream calculation:

- **[[Transaction Size]]** = Lots × Lot Size
- **[[Pip]] value** depends on Lot Size for the specific instrument
- **[[Margin]] requirements** scale with Transaction Size (and therefore Lot Size)
- **[[Spread]] and [[Commission]] costs** are typically quoted per lot — but the dollar impact varies by Lot Size

## Why Lot Size varies by instrument

Different instruments have different natural unit sizes:

- **Forex pairs** trade in millions or hundreds of thousands of units — making 100,000 a sensible "lot" size
- **Gold** trades in much smaller absolute quantities by weight — 100 ounces is a manageable lot
- **Crypto** can be highly priced (BTC at $50,000) — making 1 unit a reasonable lot
- **Stocks** trade in single-share increments — 1 share per lot reflects the underlying market

The conventions are inherited from the underlying spot, futures, and OTC markets. OPO respects them so that traders moving between brokers find familiar lot definitions.

## Lot Size vs Lot — the distinction

These two terms are often confused:

| | [[Lot]] | Lot Size |
|---|---|---|
| What it is | The unit of trade measurement | The quantity inside one Lot |
| Example value | 1.0, 0.5, 0.01 | 100,000 EUR; 100 troy oz; 1 contract |
| Set by | The trader (in lot count) | The broker/instrument convention |
| Changes per trade | Yes (trade size choice) | No (fixed per instrument) |

A trader chooses how many [[Lot|Lots]] to trade. The Lot Size is fixed by the broker and instrument convention.

## Source

- OPO Client Agreement v10, Appendix A (Lot Size, Base Currency, Precious Metal definitions)
- OPO Contract Specifications (per-instrument Lot Size)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction Lot Size conventions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Document the Lot Size for each major instrument category in a single accessible reference — currently scattered across Contract Specifications
- Confirm whether OPO uses any non-standard Lot Size conventions on specific instruments (some brokers use 10,000-unit "mini lots" as the standard for low-balance accounts)

## Related topics

- [[Lot]]
- [[Transaction Size]]
- [[Base Currency]]
- [[Pip]]
- [[Margin]]
- [[Initial Margin]]
- [[Spread]]
- [[Commission]]
- [[Contract Specifications]]