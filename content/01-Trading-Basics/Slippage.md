---
title: Slippage
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
# Slippage

## Simple explanation

Slippage is the difference between the price you **expected** when placing an order and the price at which the order **actually executed**. It happens because market prices can move in the milliseconds between your order being placed and being filled — especially during fast markets.

Slippage can be **negative** (you got a worse price than expected — most common) or **positive** (you got a better price than expected — less common, but real).

The Client Agreement does not formally define slippage in Appendix A, but addresses it operationally in clause 16.3(j):

> OPO GROUP LLC. will not be liable for any loss or expense incurred by the Client in connection with, or directly or indirectly arising from: [...] (j) Slippage;

So slippage is recognized as a real phenomenon in the agreement, and OPO disclaims liability for losses caused by it.

## How slippage happens

A trader sees EUR/USD quoted at 1.10018 / 1.10005. They place a market order to buy 1 lot.

In the **~50 milliseconds** between clicking "buy" and the order reaching OPO's server:
- The market moves
- A new quote arrives: 1.10025 / 1.10012
- OPO fills the order at the new Ask: 1.10025

Result: the trader expected to pay 1.10018, but paid 1.10025. That's **0.7 pips of negative slippage** — costing approximately $7 on a 1-lot trade.

In calm markets, slippage is usually sub-pip and barely noticeable. In fast markets, it can be many pips.

## When slippage is worst

Three predictable conditions produce significant slippage:

### 1. Major economic news releases

Non-Farm Payrolls, central bank rate decisions, CPI releases, GDP announcements — within the first 5–30 seconds of release, spreads widen, liquidity drops, and slippage on market orders can be 5–50 pips on instruments that normally have tight execution.

This is why the Client Agreement clause 14.11 specifically reduces leverage around these events: not to protect against slippage directly, but because slippage during news can produce losses that exceed normal margin assumptions.

### 2. Market opens after closures

The Monday morning forex open (Sunday 5pm NY) often features **gap slippage** — instruments open at prices different from where they closed Friday. Stop Loss and Pending Orders placed before the close can fill at significantly worse prices on Monday's first tick.

Crypto markets, which trade 24/7, see similar gaps after low-liquidity weekend hours when major news breaks during quiet times.

### 3. Force Majeure and abnormal market conditions

During flash crashes, geopolitical events, central bank interventions, or other disruptions, spreads can widen by 50× or more, quotes can disappear briefly, and slippage can be catastrophic. The Client Agreement clause 26 covers these conditions.

## Slippage on different order types

| Order type | Slippage direction | Typical magnitude |
|---|---|---|
| Market order (buy/sell now) | Either, typically negative | Sub-pip in normal markets; pips in fast markets |
| Buy Stop / Sell Stop | Negative (price has moved past your trigger) | Can be significant during news |
| Buy Limit / Sell Limit | Often zero or positive (price came to you) | Rarely substantial |
| Stop Loss | Negative (the loss-side trigger fires when price moves against you) | Can be very large during gaps |
| Take Profit | Often zero or positive | Rarely substantial |

Stop Losses are particularly vulnerable to slippage because they typically trigger when the market is moving fast and against the trader — exactly when liquidity is poor and prices are moving in jumps.

## What OPO does and doesn't do about slippage

**What OPO does:**
- Provides ECN and ECN Pro accounts with tighter spreads and faster execution, reducing typical slippage
- Reduces leverage around predictable high-volatility events (clause 14.11) to limit catastrophic outcomes
- Honours executed prices as final (clause 11.5(b)): once an order fills, the price stands

**What OPO does not do:**
- Guarantee execution at the quoted price (clause 11.5(b))
- Offer "no slippage" guarantees on standard accounts
- Refund losses caused by slippage (clause 16.3(j))

Some brokers offer "Guaranteed Stop Loss" features that explicitly cap slippage — OPO's standard account pages do not appear to advertise this, but it should be confirmed with support.

## How to reduce slippage exposure

Practical actions:

- **Trade during peak liquidity hours.** London/New York overlap (roughly 13:00–17:00 UTC) has the deepest market and smallest typical slippage.
- **Avoid trading the first 30 seconds after major news.** Wait for spreads to normalize before entering.
- **Use Limit orders for entries when possible.** Limits cannot have negative slippage on entry — only positive (or no fill at all).
- **Don't place Stop Losses too tightly during volatile sessions.** A 5-pip stop on a fast market can be triggered by spread widening alone, with no actual price movement against you.
- **Be aware of weekend gaps.** Don't hold positions over the weekend if a 100-pip Monday gap would create unacceptable loss.
- **Choose appropriate account type.** ECN and ECN Pro accounts typically have less slippage than Standard accounts due to direct market access execution.

## Slippage and strategy testing

Strategies backtested on historical data often produce wildly different live results because backtests **don't model slippage** accurately. A strategy that appears to make 50 pips per trade in backtests may actually make 35 pips live, because each trade loses 1.5 pips on entry and exit slippage.

Active traders evaluating strategies should:
1. Run strategies on demo for at least a month before going live, to see realistic slippage
2. Subtract estimated slippage from backtest results before judging strategy viability
3. Recognize that backtest slippage assumptions are often optimistic

## Risk warning

Slippage is one of the largest hidden costs in retail trading. A trader may run a strategy assuming "perfect" entry and exit prices, then find live performance significantly worse due to accumulated slippage on every trade. Stop Loss orders are particularly affected — during gap events, a Stop Loss intended to cap losses at $50 can result in actual losses of $200 or more because the market jumped through the trigger level. OPO's Client Agreement explicitly disclaims liability for losses caused by slippage (clause 16.3(j)), placing the burden of slippage risk entirely on the trader. The best protection is conservative position sizing — choosing lot sizes so that worst-case slippage still produces acceptable dollar losses.

## Source

- OPO Client Agreement v10, clause 16.3(j) (non-liability for slippage)
- OPO Client Agreement v10, clause 11.5(b) (quote price may differ from execution price)
- OPO Client Agreement v10, clause 14.11 (Leverage Adjustment Policy around news)
- OPO Client Agreement v10, clause 26 (Force Majeure)
- Note: "Slippage" is not formally defined in the Client Agreement Appendix A despite being operationally referenced. This note draws from industry-standard definitions
- Last verified: 2026-05-12

## Internal review notes

- **Slippage is not defined in the OPO Client Agreement Appendix A.** Recommend adding to the next agreement revision alongside Pip, Stop Loss, Take Profit, and Swap
- Confirm SVG-jurisdiction conventions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Document actual slippage statistics by account type and instrument — typical, P95, and P99 slippage during normal and news conditions. This is the kind of operational data that builds trader trust
- Confirm whether OPO offers Guaranteed Stop Loss on any account type
- Confirm whether ECN/ECN Pro accounts genuinely produce less slippage than Standard (this is widely claimed by brokers but not always true in practice)

## Related topics

- [[Quote]]
- [[Bid]]
- [[Ask]]
- [[Spread]]
- [[Pip]]
- [[Pending Order]]
- [[Stop Loss]]
- [[Take Profit]]
- [[Order]]
- [[Lot]]
- [[Force Majeure]]
- [[Leverage Adjustment Policy]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Black Account]]