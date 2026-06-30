---
title: Long Position
status: draft
audience: client
category: Trading Basics
region: global
language: en
owner:
reviewer:
last_reviewed:
effective_from: 2026-05-29
source_type: official
ai_allowed: false
risk_level: low
version: "1"
---

# Long Position

## Simple explanation

A long position is a trade that profits when the price of the instrument **goes up**. You're "long" when you've bought the instrument — you own it, in CFD terms, and you want the market to rise so you can sell it back at a higher price.

OPO defines long position in the Client Agreement Appendix A as:

> A buy position that appreciates in value if market prices increase. In respect of Currency Pairs: buying the Base Currency against the Quote Currency.

## How a long position works

A long trade follows a simple sequence:

1. You buy the instrument at the [[Ask]] price (the higher price in the [[Quote]])
2. The position is open. Your unrealized profit or loss updates in real time as the market moves
3. You close the position by selling at the [[Bid]] price (the lower price)
4. **Profit** = (Bid price at close – Ask price at open) × position size
5. If the close price is lower than the open price, you've made a loss instead

## Worked example

You buy 1 lot of EUR/USD when the quote is `1.10005 / 1.10018`:
- Entry price: 1.10018 (the [[Ask]])
- Trade direction: long

A few hours later, EUR/USD has risen. The quote is now `1.10523 / 1.10535`:
- You close by selling at the [[Bid]]: 1.10523
- Movement: 1.10523 – 1.10018 = 0.00505 = **50.5 pips profit**
- Dollar profit on 1 lot: 50.5 × \$10/pip = **\$505**

Note that the trade *started* at an immediate paper loss equal to the spread. The market had to move at least 1.3 pips upward just for the trade to break even — see [[Spread]] for why.

## When traders go long

Long is the default direction. Traders go long when they believe:

- The instrument's price will rise — based on technical analysis, fundamentals, news, or strategy
- Trend-following strategy: the instrument is in an uptrend, and they expect the trend to continue
- Mean reversion: the instrument has dropped too far, too fast, and is likely to rebound
- Carry trade: holding the position long earns positive [[Swap]] (interest) overnight

Long is also the natural fit for instruments where shorting is restricted, complicated, or carries higher costs — although on OPO's CFD platform, shorting any instrument is as easy as going long.

## Long positions and market exposure

When you open a long position with [[Leverage]], you control much more of the instrument than your [[Margin]] alone would buy:

- \$1,000 margin at 1:100 leverage = \$100,000 of EUR/USD exposure (1 lot)
- A 1% rise in EUR/USD produces \$1,000 profit
- A 1% fall produces \$1,000 loss — wiping out the margin

The full exposure determines profit and loss, not just the margin. This is why position sizing matters more than direction — being right about direction with a too-large lot still produces large losses on small adverse moves.

## Long positions and swap

Holding a long position past the rollover time (5pm New York time) triggers a [[Swap]] charge or credit, depending on the interest rate differential between the two currencies (for forex) or the holding cost of the instrument (for CFDs).

- If the [[Base Currency]] has a higher interest rate than the [[Quote Currency]], holding long earns positive swap (credit)
- If the Base Currency has a lower interest rate, holding long pays negative swap (debit)

On Friday rollovers, OPO charges triple swap to cover the weekend (Client Agreement clause 9.13).

Swap-eligible accounts at OPO include all account types. Swap-free options are available with conditions (see [[Swap Free]]).

## Long vs Short — quick comparison

| | Long Position | [[Short Position]] |
|---|---|---|
| Direction expected | Price up | Price down |
| Entry price | [[Ask]] (higher) | [[Bid]] (lower) |
| Exit price | [[Bid]] (lower) | [[Ask]] (higher) |
| Profit calculation | Close – Open | Open – Close |
| When to use | Bullish view | Bearish view |
| Forex carry | Earns when Base rate > Quote rate | Earns when Quote rate > Base rate |

## Risk warning

Going long does not limit your downside to your initial margin in all market conditions. With leverage, an adverse move can quickly exceed the margin and trigger [[Margin Call]] and [[Stop Out]]. OPO provides [[Negative Balance Protection]] for retail accounts (Client Agreement clause 15.8), so a trader cannot end up owing more than their deposit — but the deposit itself can be lost. Long positions are particularly vulnerable to sudden adverse moves during overnight gaps (price moves between sessions), low-liquidity periods, and major economic news events when spreads widen and execution becomes unpredictable.

## Source

- OPO Client Agreement v10, Appendix A (Long Position, Base Currency, Quote Currency definitions)
- OPO Client Agreement v10, clause 9.13 (triple swap on Fridays)
- OPO Client Agreement v10, clause 15.8 (Negative balance protection)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm OPO's swap rollover time across all platforms (MT4, MT5, cTrader, OpoTrade) — industry standard is 5pm New York, but platforms can differ
- Confirm the carry-trade direction (long earns when Base rate > Quote rate) matches OPO's swap calculation in practice
- Consider adding visual examples or animations to explain long mechanics — this is one of the foundational concepts that beginners struggle with

## Related topics

- [[Short Position]]
- [[Bid]]
- [[Ask]]
- [[Spread]]
- [[Pip]]
- [[Lot]]
- [[Margin]]
- [[Leverage]]
- [[Swap]]
- [[Swap Free]]
- [[Margin Call]]
- [[Stop Out]]
- [[Negative Balance Protection]]
- [[Quote]]
- [[Base Currency]]
- [[Quote Currency]]
- [[Open Position]]
- [[Completed Transaction]]