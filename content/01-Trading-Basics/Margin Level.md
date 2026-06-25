---
title: Margin Level
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
# Margin Level

## Simple explanation

Margin Level is the single most important risk number on your trading account. It's the ratio of your [[Equity]] to your used Margin, expressed as a percentage. OPO uses this number to decide when to issue a [[Margin Call]] and when to forcibly close your positions at [[Stop Out]].

OPO defines Margin Level in the Client Agreement Appendix A as:

> The percentage Equity to Necessary Margin ratio. It is calculated as (Equity / Necessary Margin) × 100%.

When you have no open positions, the formula returns infinity (you have Equity but zero used Margin). Most trading platforms display this as no Margin Level value or as "∞". The moment you open a position, Margin Level becomes a real number.

## Worked example

Suppose:
- Equity: $1,050
- Used Margin: $300

A 350% Margin Level means you have 3.5 times more Equity than the broker requires to keep your positions open. You're well clear of margin pressure.

If your positions then move against you and Equity drops to $400:

You're approaching the danger zone. Margin Call may be imminent.

If Equity drops to $250:
You're below 100% — your Equity is no longer enough to cover the margin required by your open positions. Stop Out is imminent or already executing.

## Margin Level thresholds at OPO

The Client Agreement (clause 14.6) gives OPO the right to close positions automatically when Equity is below a certain threshold "depending on the account type." Across OPO's account types, the published thresholds are:

| Threshold | Value | What happens |
|---|---|---|
| [[Margin Call]] | 80% | Warning level — the broker may notify the trader, though is not obliged to |
| [[Stop Out]] | 20% | Forced closure level — the broker closes positions automatically without consent or warning |

These thresholds apply across all OPO account types — Standard, ECN, ECN Pro, Social Trade, Social Pro, Black, and the cTrader-family accounts.

**Important from the Client Agreement clause 14.8:** "OPO GROUP LLC. is not obliged to make margin calls for the Client. OPO GROUP LLC. is not liable to the Client for any failure by OPO GROUP LLC. to contact or attempt to contact the Client." Traders cannot rely on receiving the 80% Margin Call warning — they may go directly from healthy to Stop Out if market movement is fast enough.

## What moves Margin Level

Margin Level moves whenever Equity or used Margin changes:

| Event                             | Effect on Margin Level |
| --------------------------------- | ---------------------------------------------------------------------------- |
| Open positions gain value         | ↑ Margin Level increases |
| Open positions lose value         | ↓ Margin Level decreases |
| Open a new position               | ↓ Margin Level decreases (used Margin grows) |
| Close a winning position          | ↑ Margin Level increases (used Margin shrinks, Equity locked in) |
| Close a losing position           | ↑ Margin Level usually increases (used Margin shrinks more than Equity does) |
| Deposit funds                     | ↑ Margin Level increases |
| Withdraw funds                    | ↓ Margin Level decreases |
| OPO increases margin requirements | ↓ Margin Level decreases (without you doing anything) |

## How to protect Margin Level

Practical actions traders can take if Margin Level is falling:

- **Close losing positions** — reduces used Margin and stops the bleeding
- **Reduce position size on existing trades** (partial close) — frees Margin
- **Add funds** — increases Equity directly
- **Avoid opening new positions** — each new position increases used Margin further
- **Avoid opening correlated positions** — if multiple positions all lose at once, Margin Level collapses fast

## Risk warning

Margin Level is the number that determines whether your positions get closed by the broker automatically. A trader who isn't watching Margin Level can be Stopped Out without warning, especially during high-volatility events like major economic news releases, market opens after weekends, or low-liquidity periods. The Client Agreement specifically lists scenarios (clause 14.11) where OPO adjusts leverage and margin around news events — these adjustments can cause Margin Level to drop suddenly even on positions that haven't moved much. Active traders should watch Margin Level continuously during volatile sessions, not Balance.

## Source

- OPO Client Agreement v10, Appendix A (Margin Level definition; note the source contains a typo: "Ragin Level" — flagged for legal correction)
- OPO Client Agreement v10, clause 14.6 (forced closure based on Equity)
- OPO Client Agreement v10, clause 14.8 (broker not obliged to issue margin calls)
- OPO Client Agreement v10, clause 14.11 (leverage adjustment policy)
- OPO website (Margin Call 80% / Stop Out 20% across account types)
- Last verified: 2026-05-12

## Internal review notes

- Source page typo: Client Agreement Appendix A contains the entry "Ragin Level" instead of "Margin Level" — pass to legal for correction in next agreement revision
- Confirm SVG-jurisdiction definitions apply globally, or split into region-specific notes when ASIC, FSCA, and Seychelles agreements are obtained
- The 80% Margin Call and 20% Stop Out thresholds come from the OPO website's account-type pages, not the Client Agreement itself (the agreement only says "certain rate depending on the account type"). Confirm these are documented in the Contract Specifications

## Related topics

- [[Equity]]
- [[Margin]]
- [[Free Margin]]
- [[Necessary Margin]]
- [[Margin Call]]
- [[Stop Out]]
- [[Leverage]]
- [[Open Position]]
- [[Floating Profit/Loss]]
- [[Negative Balance Protection]]
- [[Leverage Adjustment Policy]]


