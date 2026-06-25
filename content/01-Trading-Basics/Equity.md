---
title: Equity
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
# Equity

## Simple explanation

Equity is the real-time value of your trading account if all your open positions were closed right now at current market prices. It's the most important number on your account screen because it's what OPO uses to make automatic decisions about your account — including [[Margin Call]] and [[Stop Out]].

OPO defines Equity in the Client Agreement Appendix A as:

> Balance + Floating Profit – Floating Loss

## The formula in plain language

- **[[Balance]]** is the cash in your account from completed trades, deposits, and withdrawals. It does not move when an open position's market price changes.
- **Floating Profit/Loss** is the running profit or loss on all your currently open positions, recalculated tick by tick as market prices move.

Add unrealized profit to Balance, subtract unrealized loss, and you have Equity.

## Example

Suppose your account shows:
- Balance: $1,000
- One open position currently showing $80 in unrealized profit
- One open position currently showing $30 in unrealized loss
If both trades were closed at this moment, your Balance would become $1,050 and your Equity would equal that same $1,050. Until the positions close, Equity is a snapshot of "what your account is worth right now" — and it moves constantly.

## Why Equity matters

Equity drives every automatic risk decision on your account:

- **Free Margin is calculated from Equity**, not Balance. See [[Free Margin]].
- **Margin Level is calculated from Equity**, not Balance. See [[Margin Level]].
- **Stop Out is triggered based on Equity**, not Balance. The Client Agreement clause 14.6 states OPO "is entitled to close the Client's Open Positions without the consent of the Client or any prior Written Notice if the Equity is less than certain rate depending on the account type."

This is the key insight: a trader can have $10,000 of Balance but only $200 of Equity if their open positions are deep in unrealized loss. The broker acts on the $200, not the $10,000.

## Equity vs Balance — why they differ

| | Balance | Equity |
|---|---|---|
| Includes closed trades | ✓ | ✓ |
| Includes open trade P/L | ✗ | ✓ |
| Moves in real time | ✗ | ✓ |
| Used for risk decisions | ✗ | ✓ |
| Used for withdrawal eligibility | Indirectly | Directly (via Free Margin) |

When you have no open positions, Equity equals Balance. The moment you open a position, they diverge.

## Risk warning

Because Equity changes in real time with market movements, a trader monitoring only Balance can miss serious account risk. A losing open position eats into Equity without changing Balance until the position is closed. By the time Equity drops to [[Stop Out]] level, OPO will close positions automatically with no warning. Active traders should watch Equity, not Balance.

## Source

- OPO Client Agreement v10, Appendix A (definition of Equity, Balance, Floating Profit/Loss)
- OPO Client Agreement v10, clause 14.6 (Equity-based position closure)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split into region-specific notes when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm whether OPO platforms display "Equity" consistently across MT4, MT5, cTrader, and OpoTrade

## Related topics

- [[Balance]]
- [[Free Margin]]
- [[Margin]]
- [[Margin Level]]
- [[Margin Call]]
- [[Stop Out]]
- [[Floating Profit/Loss]]
- [[Open Position]]
- [[Completed Transaction]]
