---
title: Short Position
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

# Short Position

## Simple explanation

A short position is a trade that profits when the price of the instrument **goes down**. You're "short" when you've sold the instrument first — without owning it — with the intention of buying it back later at a lower price. The profit comes from the difference between your higher selling price and your lower buying price.

OPO defines short position in the Client Agreement Appendix A as:

> A sell position that appreciates in value if market prices fall. In respect of Currency Pairs: selling the Base Currency against the Quote Currency.

## How CFD shorting works (without owning the asset)

In traditional stock trading, going short requires borrowing shares from a broker, selling them, then buying them back to return them — a complex process with borrowing fees and limits.

In CFD trading (which is how OPO operates), shorting is mechanically identical to going long, just in reverse. There's no actual borrowing or asset movement. You're entering a contract whose value moves opposite to the long contract. The Client Agreement clause 7.5 confirms:

> OPO GROUP LLC. shall not provide physical delivery of the Underlying Asset of an Instrument in relation to any Transaction.

This means: going short on EUR/USD doesn't require borrowing euros from anyone. You're entering a CFD contract that pays you if EUR/USD drops and costs you if it rises. The mechanics of execution are the same as for [[Long Position|long positions]].

## How a short position works

1. You sell the instrument at the [[Bid]] price (the lower price in the [[Quote]])
2. The position is open. Your unrealized profit or loss updates in real time as the market moves
3. You close the position by buying back at the [[Ask]] price (the higher price)
4. **Profit** = (Bid price at open – Ask price at close) × position size
5. If the close price is higher than the open price, you've made a loss instead

## Worked example

You sell 1 lot of EUR/USD when the quote is `1.10005 / 1.10018`:
- Entry price: 1.10005 (the [[Bid]])
- Trade direction: short

A few hours later, EUR/USD has fallen. The quote is now `1.09480 / 1.09493`:
- You close by buying at the [[Ask]]: 1.09493
- Movement: 1.10005 – 1.09493 = 0.00512 = **51.2 pips profit**
- Dollar profit on 1 lot: 51.2 × \$10/pip = **\$512**

As with long positions, the trade started at an immediate paper loss equal to the spread. The market had to move 1.3 pips downward just for the trade to break even.

## When traders go short

Traders go short when they believe:

- The instrument's price will fall — based on technical analysis, fundamentals, news, or strategy
- Trend-following strategy: the instrument is in a downtrend, and they expect the trend to continue
- Mean reversion: the instrument has risen too far, too fast, and is likely to fall back
- Hedging: a trader holding the underlying asset elsewhere wants to protect against a price drop by opening a short CFD position
- Carry trade: holding the position short earns positive [[Swap]] when the [[Quote Currency]] has a higher interest rate than the [[Base Currency]]

## Short positions and risk asymmetry

There's an asymmetry in short position risk that doesn't apply to long positions:

**Long position maximum loss:** the price can go to zero. A \$100 stock can lose at most \$100. Loss is bounded.

**Short position maximum loss:** the price can rise indefinitely. There's no theoretical cap on how high a price can go. A \$100 stock could rise to \$200, \$500, or higher — and a short position loses on the full move.

In practice, on a leveraged CFD account, this asymmetry is contained by [[Margin Call]] and [[Stop Out]] — OPO closes the position automatically before losses become catastrophic. But traders should understand the underlying mathematical asymmetry, because it manifests during fast adverse moves (short squeezes, major news spikes) where the broker may not be able to close positions before losses are substantial.

## Short positions and swap

Holding a short position past 5pm New York time triggers a [[Swap]] charge or credit, opposite in direction to long-position swap:

- If the [[Quote Currency]] has a higher interest rate than the [[Base Currency]], holding short earns positive swap (credit)
- If the Quote Currency has a lower interest rate, holding short pays negative swap (debit)

So if long is profitable to hold overnight on a given pair, short usually isn't, and vice versa.

On Friday rollovers, OPO charges triple swap to cover the weekend (Client Agreement clause 9.13).

## Short vs Long — quick comparison

| | [[Long Position]] | Short Position |
|---|---|---|
| Direction expected | Price up | Price down |
| Entry price | [[Ask]] (higher) | [[Bid]] (lower) |
| Exit price | [[Bid]] (lower) | [[Ask]] (higher) |
| Profit calculation | Close – Open | Open – Close |
| When to use | Bullish view | Bearish view |
| Maximum theoretical loss | Bounded (price to zero) | Unbounded (price can rise indefinitely) |
| Forex carry | Earns when Base rate > Quote rate | Earns when Quote rate > Base rate |

## Common misconceptions about shorting

**"I'm selling something I don't have — is that legal?"**
In CFD trading at OPO, you're not literally selling an asset. You're entering a derivative contract whose value tracks the instrument's price inverse to a long contract. This is normal, legal, and how almost all retail forex/CFD trading works.

**"I'll get a margin call faster on shorts."**
Margin requirements are identical for long and short positions on the same instrument and size. [[Margin Call]] triggers at the same [[Margin Level]] for both directions.

**"Shorting only works in falling markets."**
Shorting can also be a hedging tool in rising markets — a long-term holder of an asset can short the same asset as protection against short-term drawdowns, then close the short when the drawdown is over.

**"I should always pick a direction."**
The best decision is sometimes "no position." Trading is not about being long or short; it's about identifying high-probability setups and trading them with appropriate risk. Many professional traders sit out 80%+ of the time.

## Risk warning

Short positions carry the same leveraged-loss risk as long positions, with the additional consideration that the theoretical maximum loss is unbounded — although in practice [[Stop Out]] prevents this on retail accounts. Short positions are particularly vulnerable to "short squeeze" events where a quickly rising price forces many short positions to close simultaneously, accelerating the price rise further. These events can produce gap moves that jump past stop loss levels, executing trades at much worse prices than the trader intended. Traders new to shorting are recommended to start with very small position sizes (0.01–0.10 lots) on liquid instruments (EUR/USD, GBP/USD) and avoid shorting volatile or low-liquidity instruments until experienced. [[Negative Balance Protection]] (Client Agreement clause 15.8) limits final loss to the deposit on retail accounts, but the deposit itself can be entirely lost.

## Source

- OPO Client Agreement v10, Appendix A (Short Position, Base Currency, Quote Currency definitions)
- OPO Client Agreement v10, clause 7.5 (no physical delivery — confirms CFD-only execution)
- OPO Client Agreement v10, clause 9.13 (triple swap on Fridays)
- OPO Client Agreement v10, clause 15.8 (Negative balance protection)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm the swap direction matches OPO's actual calculation in practice (Quote-Base rate differential for short, not Base-Quote)
- Confirm whether OPO restricts shorting on any specific instruments during volatile conditions or near corporate actions (dividend dates for stocks, contract expiry for commodities). The Client Agreement clause 9.14 specifically addresses dividend adjustments for short positions on stocks and indices — this needs cross-reference
- Consider adding visual examples to explain short mechanics — this is consistently the more confusing direction for beginners

## Related topics

- [[Long Position]]
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
- [[Dividend Adjustments]]