---
title: Floating Profit Loss
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
# Floating Profit/Loss

## Simple explanation

Floating Profit/Loss (often abbreviated Floating P/L) is the **unrealized** profit or loss on your currently open positions, calculated continuously based on current market prices. It is the live, second-by-second answer to the question: "if I closed all my open positions right now, how much would I gain or lose?"

OPO defines floating profit/loss in the Client Agreement Appendix A as:

> Current profit/loss on Open Positions calculated at the current Quotes.

It's called "floating" because it moves — the number changes every time market prices move, which can be many times per second. Until a position closes, its profit or loss is purely paper.

## How Floating P/L is calculated

For a single position:

**Long position:**
Floating P/L = (Current Bid – Open Ask price) × Position size × Pip value factor

**Short position:**
Floating P/L = (Open Bid price – Current Ask) × Position size × Pip value factor

The key insight: even immediately after opening a position, your Floating P/L is slightly negative. You opened a long at the [[Ask]] (the higher price), but the platform marks it at the current [[Bid]] (the lower price). The difference is exactly the [[Spread]]. This is why every trade starts with a small paper loss.

For multiple positions, total Floating P/L is the sum of all individual positions' P/L.

## Floating P/L is what drives Equity

[[Equity]] is calculated from Balance plus Floating P/L:

Equity = Balance + Floating Profit – Floating Loss

This is the live, real-time account valuation. While [[Balance]] only updates when positions close, Equity updates continuously with Floating P/L. This is also why:

- [[Free Margin]] = Equity – [[Necessary Margin]] — also updates continuously
- [[Margin Level]] = (Equity ÷ Necessary Margin) × 100% — also updates continuously
- [[Margin Call]] and [[Stop Out]] trigger based on Equity (driven by Floating P/L), not Balance

So when traders ask "why did I get a margin call when my account had \$5,000?" — the answer is that the \$5,000 was [[Balance]]; their Equity (Balance plus negative Floating P/L from open positions) was much lower.

## When Floating P/L is realized

Floating P/L becomes **realized** (added to Balance) the moment a position closes. At that point:

- The position transitions from [[Open Position]] to [[Completed Transaction]]
- The final P/L (which equals the Floating P/L at the moment of closure, minus any [[Spread]] and [[Commission]] effects) is added to [[Balance]]
- The position no longer contributes to Floating P/L

Until then, Floating P/L is just a paper number — accurate, but not money in your pocket.

## Floating P/L vs realized P/L

A trader who consistently shows positive Floating P/L but rarely closes positions has not actually made money — they have an unrealized paper profit. The market can erase that paper profit in seconds during a reversal, and there's no recovery once it's gone. Some traders fall into the trap of:

1. Opening winning positions
2. Watching Floating P/L grow
3. Refusing to close because "it might go higher"
4. Watching Floating P/L collapse on a reversal
5. Refusing to close at a loss because "it might recover"
6. Eventually getting [[Stop Out|stopped out]] with much worse results than if they'd taken the original profit

The discipline to convert Floating P/L into realized P/L at planned levels — using [[Take Profit]] orders — is one of the foundational skills of profitable trading.

## Floating P/L during overnight holds

For positions held past 5pm New York time:

- Floating P/L includes the current market valuation
- Accrued [[Swap]] charges are typically added to Balance at rollover, not held as floating
- The next day's Floating P/L starts from a slightly different base than when you went to sleep

So a trader holding a position overnight should expect to see:
- A different Floating P/L than expected from market moves alone
- A small [[Balance]] adjustment from accrued Swap
- The combined effect on Equity

## Risk warning

Floating P/L feels real but isn't realized until positions close. A trader looking at \$1,000 of positive Floating P/L and feeling like they've "won" hasn't actually made anything — the market can reverse and erase the gain before they exit. Conversely, traders looking at \$500 of negative Floating P/L and refusing to close because "it's not a real loss yet" are deluding themselves — the loss is real, just not yet recorded. Treating Floating P/L the same as realized P/L for psychological purposes — being equally willing to close winners and accept losses — is a core discipline. Setting [[Take Profit]] and [[Stop Loss]] orders converts emotional decisions into pre-committed ones, which is how professionals manage the gap between floating and realized P/L.

## Source

- OPO Client Agreement v10, Appendix A (Floating Profit/Loss, Equity definitions)
- OPO Client Agreement v10, clause 6.8 (P/L deposited on closing transaction)
- OPO Client Agreement v10, clause 7.5 (P/L withdrawn from Trading Account when closed)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm that Floating P/L calculations are consistent across MT4, MT5, cTrader, and OpoTrade — small differences in how swap and commission are factored into displayed Floating P/L can cause confusion
- Confirm timing — does Floating P/L update tick-by-tick or with each platform refresh? This varies by platform configuration

## Related topics

- [[Equity]]
- [[Balance]]
- [[Open Position]]
- [[Completed Transaction]]
- [[Free Margin]]
- [[Margin Level]]
- [[Margin Call]]
- [[Stop Out]]
- [[Take Profit]]
- [[Stop Loss]]
- [[Spread]]
- [[Commission]]
- [[Swap]]
- [[Bid]]
- [[Ask]]
- [[Quote]]


