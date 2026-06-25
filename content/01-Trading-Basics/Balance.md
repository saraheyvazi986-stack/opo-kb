---
title: Balance
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
# Balance

## Simple explanation

Balance is the cash in your trading account that has actually been realized — money from deposits, money from closed trades, minus money from withdrawals and minus realized losses. Balance does **not** include the unrealized profit or loss of currently [[Open Position|open positions]].

OPO defines balance in the Client Agreement Appendix A as:

> The total financial result of all Completed Transactions and depositing/withdrawal operations on the Trading Account.

In plain terms: Balance is what your account would be worth if you closed nothing, withdrew nothing, and only counted what's already locked in.

## Balance vs Equity — the key distinction

This is the single most important distinction on a trading account:

| | Balance | [[Equity]] |
|---|---|---|
| Includes deposits and withdrawals | ✓ | ✓ |
| Includes closed trade P/L | ✓ | ✓ |
| Includes open trade P/L | ✗ | ✓ |
| Updates in real time | ✗ | ✓ |
| Used for risk decisions | ✗ | ✓ |

When you have no open positions, Balance and Equity are identical. The moment a position opens, they diverge — Equity moves with the market, Balance stays still until the position closes.

## What changes Balance

Balance moves at four specific moments:

1. **You deposit funds.** Balance increases immediately on settlement.
2. **You withdraw funds.** Balance decreases when the withdrawal is processed.
3. **A trade closes.** The final P/L from the [[Completed Transaction]] is added (or subtracted) from Balance, along with any [[Swap]] accrued and [[Commission]] charged.
4. **Account fees are debited.** Such as the dormant account fee (Client Agreement clause 9.11) or no-activity withdrawal charges (clause 6.14).

Between these moments, Balance is frozen. The market can move dramatically while you hold open positions, and Balance won't budge until those positions close.

## Why this matters

A trader looking at Balance thinks they have a certain amount. A trader looking at Equity sees what they actually have, accounting for live market positions. The two can differ wildly — a $10,000 Balance with three losing open positions might have an Equity of $6,000. The broker uses Equity (not Balance) for [[Margin Level]], [[Margin Call]], and [[Stop Out]] decisions.

**Practical rule:** Balance is for accounting. Equity is for risk management.

## Source

- OPO Client Agreement v10, Appendix A (Balance definition)
- OPO Client Agreement v10, clauses 9.11 and 6.14 (fee deductions affecting Balance)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm that all four account-change events (deposit, withdrawal, trade close, fee) display consistently across MT4, MT5, cTrader, and OpoTrade

## Related topics

- [[Equity]]
- [[Free Margin]]
- [[Margin Level]]
- [[Completed Transaction]]
- [[Open Position]]
- [[Floating Profit/Loss]]
- [[Swap]]
- [[Commission]]
- [[Dormant Account Policy]]
- [[Withdrawal Procedure]]