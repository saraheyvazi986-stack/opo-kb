---
title: Spread
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
# Spread

## Simple explanation

The spread is the difference between the price at which you can buy an instrument and the price at which you can sell it at the same moment. It's the most common way OPO earns money on a trade — a built-in cost embedded in the prices you see on screen.

OPO defines spread in the Client Agreement Appendix A as:

> The difference between Ask and Bid.

Where [[Bid]] is the lower price (what you receive when selling) and [[Ask]] is the higher price (what you pay when buying). The gap between them is the spread.

## How spread becomes a cost

Every trade starts at an immediate loss equal to the spread:

1. You open a position at the [[Ask]] price (buy) or [[Bid]] price (sell)
2. The moment the position is open, it's marked at the *other* side of the market — so a buy is immediately valued at the Bid, and a sell at the Ask
3. The position must move at least one full spread in your favour before it breaks even

This means a trader who opens and closes a position immediately, with no market movement at all, still loses the spread. The wider the spread, the bigger this hidden starting cost.

## How spread is measured

Spread is measured in **pips** (or **pipettes** for fractional pips). For most major forex pairs, one pip is 0.0001 of the quote currency. For EUR/USD:

- If Bid = 1.1000 and Ask = 1.1002, the spread is **2 pips** (0.0002)
- If Bid = 1.10005 and Ask = 1.10018, the spread is **1.3 pips** (sometimes written as 13 pipettes)

The dollar cost of a 1-pip spread depends on trade size. For a standard lot (100,000 units) of EUR/USD, 1 pip ≈ \$10. So a 2-pip spread on a 1-lot trade costs ~\$20 immediately.

## Spread at OPO by account type

Spread varies significantly by account. From OPO's account pages:

| Account | Spread starting from |
|---|---|
| [[Standard Account]] | 1.8 pip |
| [[ECN Account]] | 0.8 pip |
| [[ECN Pro Account]] | 0.0 pip |
| [[Social Trade Account]] | 1.5 pip |
| [[Social Pro Account]] | 0.0 pip |
| [[Black Account]] | Raw (near-zero) |
| [[cTrader ECN Account]] | 1.0 pip |
| [[cTrader ECN Plus Account]] | 0.0 pip |
| [[cTrader Copy Account]] | 2.2 pip |

**Important: "starting from" is not the typical spread.** These numbers represent the *tightest* spreads available — usually on the most liquid instruments (EUR/USD, GBP/USD) during peak market hours (London/New York overlap). Spreads on exotic pairs, indices, commodities, or crypto are wider. Spreads during low-liquidity hours (Asian session for non-Asian pairs, weekends for crypto) are wider. Spreads during news events can widen dramatically.

For exact spreads per instrument, traders should consult the Contract Specifications inside their trading platform.

## Spread vs commission — the two pricing models

OPO accounts use one of two cost structures:

### Spread-only accounts

Standard, Social Trade, cTrader Copy, Black. There's **no per-trade commission** — OPO earns its margin entirely through the spread. The displayed spread is wider to compensate.

### Spread plus commission accounts

ECN, ECN Pro, Social Pro, cTrader ECN, cTrader ECN Plus. These accounts show **raw or near-raw spreads** but charge a separate per-lot [[Commission]]. The trader pays a small commission on every lot traded (\$6/lot on ECN, \$4/lot on ECN Pro and Plus).

**Which is cheaper depends on trade size and frequency.** A low-volume trader placing occasional 0.1-lot trades often saves money on the spread-only model. A high-volume trader placing many full-lot trades typically saves on the commission model. See [[Commission]] for a worked comparison.

## When spreads widen

OPO can change spreads on each instrument. The Client Agreement clause 11.4 states:

> OPO GROUP LLC. specifies Spread for each Instrument in the Contract Specifications. OPO GROUP LLC. is entitled to change Spreads without prior Written Notice to the Client subject to the Terms of Business. Otherwise, OPO GROUP LLC. shall notify the Client not less than 7 (seven) calendar days prior to any changes in Spreads.

In practice, three things widen the spread you see on screen:

**1. Low liquidity.** When fewer market participants are trading an instrument, the gap between Bid and Ask widens naturally. This happens during off-hours (Asian session for European pairs, weekend crypto trading), holidays, and the rollover window around 5pm New York time.

**2. High volatility.** Around major economic news (NFP, central bank rate decisions, CPI releases), spreads can widen by 5–10× their normal level for the first few seconds after the announcement. The Client Agreement clause 14.11 specifically reduces leverage during these windows to protect traders, but the spread widening itself is a separate effect.

**3. Force Majeure or abnormal market conditions.** During major geopolitical events, flash crashes, or other disruptions, spreads can widen by 50× or more, or quotes can disappear entirely (clause 26).

## Spread cost compounding

Spread is paid **on every trade**, not just losing trades. A trader who places 10 trades per day, each 1 lot of EUR/USD on a Standard account with a 1.8-pip spread, pays roughly:

Over a month of trading (~22 days), that's ~\$3,960 in spread before considering profit or loss on the actual market moves. For a \$5,000 account, that's 79% of capital paid in spread costs per month. Active traders typically use commission-based accounts (ECN, ECN Pro) specifically because the per-trade cost is lower.

## How to reduce spread cost

Practical actions:

- **Choose the right account.** High-volume traders save dramatically on ECN/ECN Pro/ECN Plus.
- **Trade during peak liquidity hours.** London/New York overlap (roughly 13:00–17:00 UTC) is the tightest-spread window for most forex pairs.
- **Avoid trading around major news** unless the news is your strategy. Spreads widen, and execution becomes unpredictable.
- **Avoid exotic pairs unless necessary.** EUR/USD might trade at 0.8 pips; USD/TRY (Turkish lira) might trade at 50+ pips even on the same account.
- **Use limit orders for entries** when possible — you set the price, the market comes to you, and you can sometimes enter on the better side of the spread.

## Risk warning

Spread is the most under-appreciated cost in retail trading. Traders focus on profit and loss on the market move and forget the spread cost on every trade. A strategy that looks profitable on paper can lose money in practice because spread costs were not accounted for. Before evaluating any trading approach, calculate the spread cost based on expected trade frequency and account type — that's the cost floor your strategy must beat. Spreads can widen substantially during news events and low-liquidity periods, and OPO has the contractual right to change spreads at its discretion under abnormal market conditions, including without notice. Stop Loss orders placed at tight distances from the entry price may be triggered by spread widening alone, even when the underlying market hasn't actually moved.

## Source

- OPO Client Agreement v10, Appendix A (Spread, Bid, Ask definitions)
- OPO Client Agreement v10, clause 11.4 (right to change spreads, 7-day notice exception)
- OPO Client Agreement v10, clause 14.11 (Leverage Adjustment Policy — related news-event protections)
- OPO Client Agreement v10, clause 26 (Force Majeure)
- OPO website account type pages (starting-from spread values)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction terms apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm the actual typical spread (not "starting from") for the top 10 most-traded instruments, by account type — this is more useful for traders than the marketing minimum
- Confirm the Bid/Ask conversion to "pipettes" terminology — some traders use this term, others don't, and OPO documentation is inconsistent about whether the fifth decimal counts as a pip or pipette
- Confirm what happens to existing pending orders (limit, stop) when spreads suddenly widen — do they fill at the requested price or the actual spread-widened price
- Add a worked example calculator (or link to one) for traders to compute spread cost per strategy

## Related topics

- [[Bid]]
- [[Ask]]
- [[Commission]]
- [[Pip]]
- [[Pipette]]
- [[Lot]]
- [[Raw Spread]]
- [[Contract Specifications]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Black Account]]
- [[Force Majeure]]
- [[Leverage Adjustment Policy]]
- [[Stop Loss]]