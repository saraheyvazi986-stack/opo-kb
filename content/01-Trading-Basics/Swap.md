---
title: Swap
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
# Swap

## Simple explanation

A Swap is the overnight interest charge or credit applied to any position held open past the daily rollover time (typically 5pm New York time / 17:00 EST). It exists because, in the underlying market, leveraged positions involve effectively borrowing one currency to hold another — and the interest rate differential between the two currencies has to be settled daily.

Swap can be **positive** (you receive money for holding the position overnight) or **negative** (you pay money). Whether it's positive or negative depends on the interest rate differential of the two currencies in the pair, and on whether you're [[Long Position|long]] or [[Short Position|short]].

The Client Agreement does not formally define "Swap" in Appendix A, but treats it operationally throughout — most explicitly in clause 9.13.

## How swap is calculated

The general formula (industry standard) for forex swap:

In practice, OPO publishes specific swap rates per instrument in the Contract Specifications, and traders should consult those rather than calculating manually. Rates can change daily based on interbank lending rates.

For a Long EUR/USD position:
- Base currency: EUR
- Quote currency: USD
- If EUR interest rate > USD interest rate → positive swap (you earn)
- If USD interest rate > EUR interest rate → negative swap (you pay)

For a Short EUR/USD position, the direction reverses — you're effectively short EUR and long USD, so the swap direction flips.

## OPO's swap timing

The Client Agreement clause 9.13 is explicit on the schedule:

> From Monday to Thursday Swaps are calculated once. On Friday swaps are calculated in triple size. Exceptions apply, please refer to Contract Specifications for more information.

So the schedule is:

| Day of week (rollover at 17:00 NY) | Swap charged |
|---|---|
| Monday → Tuesday | 1× swap |
| Tuesday → Wednesday | 1× swap |
| Wednesday → Thursday | 1× swap |
| Thursday → Friday | 1× swap |
| **Friday → Saturday** | **3× swap** (covers Friday + Saturday + Sunday) |
| Saturday → Sunday | No swap (market closed) |
| Sunday → Monday | No swap (market closed) |

**Important:** The Client Agreement clause 9.13 specifies that triple swap is applied on the **Friday** rollover, covering Friday, Saturday, and Sunday. Traders should be aware of this when holding positions into the weekend.

## Swap and trading strategy

Different trading styles interact with swap very differently:

**Day traders** (open and close within the same day): no swap charges. Position is closed before 17:00 NY rollover.

**Swing traders** (hold for days to weeks): substantial swap exposure. A position held 14 days could pay or receive 16 days of swap (counting the triple-on-Friday). This can be significant.

**Position traders** (hold for weeks to months): swap becomes a major cost or revenue stream. A negative-swap trade held 3 months can lose more to swap than to spread + commission combined.

**Carry traders** specifically target positive-swap positions, accepting smaller price-move profits in exchange for steady overnight income. This is a real strategy in forex.

## A worked example of swap accumulation

Suppose a trader holds a 1-lot Long AUD/USD position at a time when:
- AUD interest rate: 4.0%
- USD interest rate: 5.0%
- Differential: AUD pays 1% less than USD

A Long AUD/USD position is effectively *borrowing USD to hold AUD*, so the trader pays the differential. The approximate daily swap charge:

Over 30 days (counting one extra triple-Friday): approximately \$90 in swap charges. This is per lot — at 10 lots, \$900. At 100 lots, \$9,000. For position traders holding negative-swap pairs, this is a quiet but substantial drag.

The same position held *short* (Short AUD/USD = effectively long USD, short AUD) would earn approximately \$2.74/day in positive swap.

## Swap on non-forex instruments

OPO applies swap charges to all leveraged instruments, not just forex:

- **Indices (CFD on S&P 500, NASDAQ, etc.)** — swap based on the index's underlying interest rate environment
- **Commodities (gold, silver, oil, gas)** — swap based on storage/carry costs of the underlying
- **Stocks (CFD)** — swap based on the broker's cost of funding the position
- **Cryptocurrencies** — swap based on funding rates in the underlying spot/perpetual markets

These can be quite different from forex swaps. Crypto swap rates in particular can be highly volatile, with daily rates sometimes exceeding 0.1% — which annualizes to 36%+ on a held position.

For exact swap rates per instrument, traders should consult the Contract Specifications inside their trading platform.

## Dividend adjustments — related but separate

The Client Agreement clause 9.14 introduces a related but distinct concept for stock and index CFDs: dividend adjustments. When the underlying stock or index pays a dividend:

- **Long positions** receive a credit equal to the dividend (at OPO's discretion based on internal policies)
- **Short positions** are debited an amount equal to the dividend

This is separate from swap — it's a one-time adjustment on the ex-dividend date, not an overnight rollover charge. Traders holding stock CFDs across dividend dates should be aware of this. Position-holding requirements may apply: typically positions must be open for 24–48 hours before and after the ex-dividend date to qualify.

## How to minimize negative swap

Practical actions:

1. **Close positions before rollover.** If you're a day trader anyway, no swap.
2. **Choose the direction that earns positive swap.** For carry strategies, this is the primary consideration.
3. **Avoid known-negative-swap instruments** for multi-day holds. Some exotic pairs have crushing negative swap on both sides.
4. **Consider a [[Swap Free]] account** if you cannot avoid overnight positions and want to avoid swap entirely.
5. **Check swap rates before every trade**, especially for unfamiliar instruments — rates change.

## Risk warning

Swap is the most under-monitored cost in retail trading. A trader focused on entry and exit price can lose substantial amounts to swap over weeks or months without realising the cumulative cost. For position traders, swap can exceed all other trading costs combined. The Friday triple-swap is a particular surprise for new traders — a position that pays \$5/day in negative swap suddenly costs \$15 on Friday night, and traders who don't anticipate this can find their [[Margin Level]] dropping unexpectedly into [[Margin Call]] territory. Swap rates can also change without notice based on interbank conditions — a trade entered with positive swap can later become negative-swap if rate differentials shift. Always check current swap rates before placing trades you intend to hold overnight.

## Source

- OPO Client Agreement v10, clause 9.13 (Friday triple swap)
- OPO Client Agreement v10, clause 9.14 (dividend adjustments for CFDs)
- OPO Contract Specifications (per-instrument swap rates)
- Note: "Swap" is not formally defined in the Client Agreement Appendix A despite being operationally referenced. This note draws from industry-standard definitions
- Last verified: 2026-05-12

## Internal review notes

- **Swap is not defined in the OPO Client Agreement Appendix A.** Like Pip, Stop Loss, and Take Profit, this is a fundamental term used operationally but not formally defined. Recommend adding to the next agreement revision
- Confirm SVG-jurisdiction conventions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm whether OPO publishes swap rates in real time or as static daily figures
- Confirm timing of swap calculation — is it precisely at 17:00 NY, or per OPO server time (which may differ)
- Confirm how swap is displayed in MT4 vs MT5 vs cTrader vs OpoTrade — labelling differences can confuse traders
- The Client Agreement clause 9.13 states Friday for triple swap. Industry convention is typically Wednesday. Confirm with operations which day OPO actually applies the triple swap charge.
- Confirm the exact dividend adjustment policy mentioned in clause 9.14 — what's the "minimum holding period" and which instruments are affected

## Related topics

- [[Swap Free]]
- [[Long Position]]
- [[Short Position]]
- [[Open Position]]
- [[Completed Transaction]]
- [[Balance]]
- [[Base Currency]]
- [[Quote Currency]]
- [[Lot]]
- [[Margin Level]]
- [[Margin Call]]
- [[Dividend Adjustments]]
- [[Carry Trade]]
- [[Contract Specifications]]