---
title: Hedged Margin
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
# Hedged Margin

## Simple explanation

Hedged Margin is a reduced [[Margin]] requirement that applies when a trader holds matched [[Long Position|long]] and [[Short Position|short]] positions on the same instrument simultaneously. Because the two positions offset each other's directional risk, OPO requires less margin to maintain them than two independent same-direction positions would need.

OPO defines hedged margin in the Client Agreement Appendix A as:

> The margin required by OPO GROUP LLC. sufficient to open and maintain Matched Positions. The details for each Instrument are in the Contract Specifications.

## The concept of matched positions

OPO defines [[Matched Positions]] in Appendix A:

> Long and Short Positions of the same Transaction Size opened on the Trading Account for the same Instrument.

In plain terms: if you're holding 2 lots long EUR/USD AND 2 lots short EUR/USD at the same time, those 2 lots are "matched." The market exposure cancels out — if EUR/USD rises 50 pips, you make $1,000 on the long and lose $1,000 on the short. Net market P/L: zero.

Since there's no net market exposure on the matched portion, the broker accepts lower collateral requirements.

## A worked example

Suppose the standard [[Initial Margin]] for 1 lot of EUR/USD at 1:100 leverage is $1,100. A trader holds:

- 2 lots long EUR/USD
- 2 lots short EUR/USD

| Scenario | Margin required |
|---|---|
| Without hedged margin treatment | 4 lots × $1,100 = $4,400 |
| With hedged margin (matched 2 lots each way) | Significantly less — typically 25%–50% of the unhedged figure |

The exact reduction is defined per-instrument in the Contract Specifications. Standard industry practice is to charge 25%–50% of the normal margin on the matched portion, with full margin on any unmatched excess.

## Why traders use hedged positions

Three main reasons:

**1. Parking a trade temporarily.** A trader who is uncertain whether to close a position can open an offsetting position to "freeze" current P/L. The matched positions don't gain or lose from further market moves, but both close-orders remain available.

**2. Hedging against weekend or news risk.** A trader holding a long position into a weekend or major news event can open a short to neutralize directional risk through the event, then close one leg afterward.

**3. Strategy-driven offsetting.** Some grid trading and mean-reversion strategies intentionally accumulate matched positions as part of their logic.

## Caveats and trade-offs

Hedging via matched positions is not free:

- **Spread is paid twice.** Both legs (long and short) cross the [[Spread]] at entry, and both pay it again at exit. For a 2-lot hedged pair on a 1.8-pip spread, that's $72 in spread cost ($36 per leg × 2 legs).
- **[[Commission]] applies to both legs.** On a $6/lot ECN account, two 1-lot legs cost $12 in commission, not $6.
- **[[Swap]] is charged on both legs independently.** This is the most surprising cost. On each daily rollover, both legs incur their respective swap charges. A pair where one leg has positive swap and the other has negative swap will not net out — the trader pays both.
- **Friday triple-swap applies to both legs.** So holding a hedged position through Friday night can be substantially more expensive than expected.

The Client Agreement clause 9.13 confirms: swap is calculated independently on each open position, not netted across hedged pairs.

## Hedged Margin vs Initial Margin

| | [[Initial Margin]] | Hedged Margin |
|---|---|---|
| When applies | Opening a single-direction position | Opening matching opposite-direction positions |
| Per-trade or aggregate | Per new trade | On the matched portion across two trades |
| Magnitude | Standard | Reduced (typically 25%–50% of standard) |

## Source

- OPO Client Agreement v10, Appendix A (Hedged Margin, Matched Positions definitions)
- OPO Client Agreement v10, clauses 14.1, 14.2 (margin requirements for opening positions)
- OPO Client Agreement v10, clause 9.13 (swap charged per position)
- OPO Contract Specifications (per-instrument hedged margin requirements)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- **Confirm exact hedged margin percentages** per instrument category — this is not currently published in a single accessible location, and traders need to know it for hedging strategy decisions
- Confirm whether MT4, MT5, cTrader, and OpoTrade all calculate hedged margin identically — some platforms compute differently
- Document whether OPO restricts certain hedging strategies (some brokers limit "grid trading" with extensive matched positions)

## Related topics

- [[Margin]]
- [[Initial Margin]]
- [[Necessary Margin]]
- [[Free Margin]]
- [[Matched Positions]]
- [[Long Position]]
- [[Short Position]]
- [[Open Position]]
- [[Swap]]
- [[Spread]]
- [[Commission]]
- [[Transaction Size]]
- [[Contract Specifications]]