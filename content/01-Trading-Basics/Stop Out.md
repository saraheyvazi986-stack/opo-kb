---
title: Stop Out
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
# Stop Out

## Simple explanation

Stop Out is the level at which OPO automatically closes your open positions to prevent further losses. At OPO, Stop Out triggers when your [[Margin Level]] reaches 20%. This action requires no consent from the trader and may happen without any prior warning.

Stop Out is not a service or a feature — it is a contractual right that the broker exercises to protect itself, and indirectly to protect the trader from owing more than their deposit.

## The Stop Out threshold at OPO

The Client Agreement clause 14.6 grants OPO the right to close positions automatically when Equity drops below a threshold determined by account type. The published Stop Out level across all OPO account types is **20%**.

This means: when your Margin Level reaches 20%, OPO's systems begin closing your open positions automatically, starting with the most loss-making position, until Margin Level recovers above 20% or all positions are closed.

## How Stop Out actually works

Stop Out is not a single event — it's a process:

1. **Margin Level reaches 20%.** Trigger condition met.
2. **System identifies the largest losing position.** Usually the most heavily unrealized-loss position.
3. **That position is closed at the current market price.** Closure happens immediately and may incur additional slippage in fast markets.
4. **Margin Level is recalculated.** If still below 20%, the next position is closed.
5. **Process repeats** until Margin Level is above 20% or no open positions remain.

This means a Stop Out event can result in **multiple positions being closed in rapid succession**, not just one. A trader with five open positions can find all five closed within a few seconds if the market is moving fast enough.

## Why Stop Out triggers without warning

The Client Agreement clause 14.6 explicitly removes any obligation on OPO to notify the trader before closing positions:

> ...without the consent of the Client or any prior Written Notice...

Combined with clause 14.8 ("OPO GROUP LLC. is not obliged to make margin calls"), this means a trader can go from healthy account to fully closed-out positions with no prior communication from the broker at any stage. This is not a customer-service failure — it is the contractual structure.

## The chain leading to Stop Out

Stop Out is the end of a sequence that the trader can see coming if monitoring [[Margin Level]]:

| Margin Level | State |
|---|---|
| Above 100% | Healthy |
| 80% to 100% | Approaching margin call |
| 80% | [[Margin Call]] threshold |
| 20% to 80% | Margin call zone — trader can still act |
| 20% | **Stop Out triggers — broker takes over** |

Once Stop Out triggers, the trader loses the ability to choose which positions to keep. The system decides, starting with the largest losing position.

## Stop Out and Negative Balance Protection

Even after Stop Out closes all positions, in extreme cases the final Balance can be negative — for example, during a major news event where prices gap through the Stop Out level faster than the system can close positions. The Client Agreement clause 15.8 provides [[Negative Balance Protection]] for retail accounts:

> OPO GROUP LLC. ensures that losses will not exceed the total available funds per Clients' OPO GROUP LLC. trading account(s) (negative balance protection).

This means the trader cannot end up owing OPO money beyond the deposit. The negative balance is reset to zero by OPO, except in cases where clause 16.6 applies — if the trader created the negative balance through illicit methods.

## What the trader should do to avoid Stop Out

Stop Out is preventable through risk management:

- **Use position sizes appropriate to account balance** — a \$500 account placing 1-lot trades on most instruments will reach Stop Out quickly
- **Watch [[Margin Level]] continuously**, not Balance
- **Set Stop Loss orders** — these close losing trades at a level the trader chooses, rather than waiting for the broker to act
- **Avoid opening positions immediately before high-volatility events** — economic news releases, market opens, weekends, gold market breaks
- **Avoid stacking correlated positions** — if all positions lose at once, Margin Level collapses fast
- **Add funds before Margin Level is critical**, not after

## What happens to pending orders during Stop Out

When Stop Out triggers, **only open positions** are closed automatically. Pending orders (limits, stops, take-profits) generally remain in place unless the trader has set them as part of the closed positions. After Stop Out, traders should review their pending order list — orphaned pending orders from closed positions can produce unexpected re-entries if not cancelled.

## Risk warning

Stop Out is the broker's last line of defence against an account going negative. It is automatic, immediate, and final. Traders who experience Stop Out typically lose a significant portion of their deposit in one cascading event — multiple positions closing at the worst possible moment, often at unfavourable prices due to slippage in fast markets. The single best protection against Stop Out is **not letting Margin Level approach the trigger** in the first place. Active risk management, appropriate position sizing, and continuous monitoring during open positions are the trader's responsibility under the Client Agreement.

## Source

- OPO Client Agreement v10, clause 14.6 (right to close positions when Equity falls below threshold)
- OPO Client Agreement v10, clause 14.8 (broker not obliged to make margin calls)
- OPO Client Agreement v10, clause 15.8 (Negative balance protection)
- OPO Client Agreement v10, clause 16.6 (negative balance not pursued except for illicit methods)
- OPO website account type pages (20% Stop Out level)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction terms apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- The 20% threshold appears on the OPO website but not explicitly in the Client Agreement — recommend adding to the Contract Specifications referenced by the agreement
- Confirm Stop Out behaviour is consistent across MT4, MT5, cTrader, and OpoTrade — each platform may handle the closure sequence slightly differently
- Confirm what happens to pending orders during Stop Out across each platform — this is a real trader question and the behaviour may differ by platform

## Related topics

- [[Margin]]
- [[Margin Level]]
- [[Margin Call]]
- [[Equity]]
- [[Free Margin]]
- [[Negative Balance Protection]]
- [[Leverage]]
- [[Stop Loss]]
- [[Slippage]]
- [[Leverage Adjustment Policy]]