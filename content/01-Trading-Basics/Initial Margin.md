---
title: Initial Margin
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
# Initial Margin

## Simple explanation

Initial Margin is the [[Margin]] amount required to **open** a new position. It is the collateral OPO locks up at the moment you enter a trade. Until you close the position, that amount sits in "used Margin" and is not available for new trades or withdrawals.

OPO defines initial margin in the Client Agreement Appendix A as:

> The margin required by OPO GROUP LLC. to open a position. The details for each Instrument are in the Contract Specifications.

## How Initial Margin is calculated

For a leveraged position:

Example: opening 1 lot of EUR/USD at 1.1000 on 1:100 leverage:

So opening this position locks \$1,100 of [[Free Margin]] as Initial Margin. If your account had \$5,000 of Free Margin before opening, it now has \$3,900 available for new trades.

Exact margin requirements per instrument are defined in OPO's Contract Specifications and may differ from this formula based on leverage tier, account type, and instrument category.

## Initial Margin gate at order placement

The Client Agreement clause 12.3(j) makes Initial Margin a hard gate for new orders:

> when the Client opens a position, the Client shall have sufficient Free Margin to cover the Initial Margin requirement in respect of that Open Position;

If [[Free Margin]] is insufficient to cover the Initial Margin requirement, the order is rejected before it executes. The trader sees the rejection in the platform with an error like "Not enough money" or "Insufficient funds."

## Initial Margin vs [[Necessary Margin]]

These two terms are sometimes confused:

| | Initial Margin | Necessary Margin |
|---|---|---|
| Used when | Opening a new position | Maintaining an open position |
| Defined per | New trade | Currently open trades |
| Static or dynamic | Set at order placement | Can fluctuate with margin requirement changes |

For a single trade with no requirement changes, Initial Margin and the Necessary Margin for that trade are typically the same number. The distinction matters when OPO increases margin requirements mid-trade (Client Agreement clause 14.5 allows this): the position keeps running, but the Necessary Margin requirement for it may increase, eating into [[Free Margin]].

## How Initial Margin changes with leverage

| Leverage | Initial Margin for 1 lot EUR/USD |
|---|---|
| 1:30 | \$3,667 |
| 1:100 | \$1,100 |
| 1:200 | \$550 |
| 1:500 | \$220 |
| 1:1000 | \$110 |
| 1:2000 | \$55 |

Higher leverage means smaller Initial Margin — which means more positions can be opened from the same account balance. This is the appeal and the danger of high leverage simultaneously. See [[Leverage]] for the full picture.

## Source

- OPO Client Agreement v10, Appendix A (Initial Margin definition)
- OPO Client Agreement v10, clause 12.3(j) (Free Margin required to cover Initial Margin)
- OPO Client Agreement v10, clause 14.5 (margin requirements can change mid-trade)
- OPO Contract Specifications (per-instrument margin requirements)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm Initial Margin formula applies consistently across MT4, MT5, cTrader, and OpoTrade
- Confirm whether Initial Margin for cryptocurrencies differs from forex (the dynamic leverage table suggests it does — typically much higher margin requirement)

## Related topics

- [[Margin]]
- [[Necessary Margin]]
- [[Hedged Margin]]
- [[Free Margin]]
- [[Leverage]]
- [[Equity]]
- [[Margin Level]]
- [[Open Position]]
- [[Order]]
- [[Lot]]
- [[Contract Specifications]]