---
title: Base Currency
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
# Base Currency

## Simple explanation

The Base Currency is the **first** currency in a currency pair. It's the currency you're effectively buying when you go [[Long Position|long]] the pair, and selling when you go [[Short Position|short]].

OPO defines base currency in the Client Agreement Appendix A as:

> The first currency in the Currency Pair against which the Client buys or sells the Quote Currency.

## How to identify the Base Currency

Every forex pair is written as `BASE/QUOTE`. The Base is on the left, the Quote is on the right:

| Pair | Base Currency | [[Quote Currency]] |
|---|---|---|
| EUR/USD | EUR (Euro) | USD (US Dollar) |
| GBP/USD | GBP (British Pound) | USD (US Dollar) |
| USD/JPY | USD (US Dollar) | JPY (Japanese Yen) |
| AUD/CAD | AUD (Australian Dollar) | CAD (Canadian Dollar) |
| XAU/USD | XAU (Gold, one troy ounce) | USD (US Dollar) |

## What the Base Currency means in practice

When you see a price quote like EUR/USD at 1.1000, that means:
- **1 EUR = 1.1000 USD**
- The Base Currency is EUR
- The Quote Currency is USD
- The number 1.1000 represents how many units of USD it takes to buy 1 unit of EUR

When you go long EUR/USD, you are effectively buying EUR and selling USD. When you go short EUR/USD, you are selling EUR and buying USD.

## Base Currency and trade size

The standard [[Lot]] size in forex is defined in units of the Base Currency:

- 1 lot of EUR/USD = 100,000 EUR (not 100,000 USD)
- 1 lot of GBP/USD = 100,000 GBP
- 1 lot of USD/JPY = 100,000 USD

This matters because the **actual dollar value of one lot** depends on the Base Currency's exchange rate to USD. A 1-lot GBP/USD position is worth more in USD terms than a 1-lot EUR/USD position when GBP/USD trades higher than EUR/USD.

## Base Currency and swap direction

Whether [[Swap]] is positive or negative for a position depends on the interest rate differential between Base and Quote currencies:

- **Long position:** earns positive swap if Base Currency interest rate > Quote Currency interest rate
- **Short position:** earns positive swap if Quote Currency interest rate > Base Currency interest rate

This is why some traders specifically target pairs where the Base Currency has a much higher interest rate than the Quote — they earn substantial overnight swap simply by holding the position long. See [[Swap]] for the full mechanics.

## Source

- OPO Client Agreement v10, Appendix A (Base Currency definition)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained

## Related topics

- [[Quote Currency]]
- [[Quote]]
- [[Bid]]
- [[Ask]]
- [[Long Position]]
- [[Short Position]]
- [[Lot]]
- [[Lot Size 1]]
- [[Swap]]
- [[Spread]]
- [[Pip]]
