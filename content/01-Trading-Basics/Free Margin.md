---
title: Free Margin
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
# Free Margin

## Simple explanation

Free Margin is the amount of money in your account that is currently available to open new positions. It is the portion of your [[Equity]] that is **not** locked up as collateral for positions you already have open.

OPO defines Free Margin in the Client Agreement Appendix A as:

> Funds on the Trading Account, which may be used to open a position. It is calculated as Equity Less Necessary Margin.

Where "Used Margin" (the agreement calls it [[Necessary Margin]]) is the total margin currently locked up across all open positions.

## Example

Suppose:
- Equity: $1,050
- Open positions using $300 in margin
That $750 is what you can use to:
- Open additional positions (subject to having enough Free Margin to cover the new position's [[Initial Margin]])
- Withdraw from the account (subject to having no withdrawal-blocking conditions, see [[Withdrawal Procedure]])

## Why Free Margin matters

**Free Margin gates new trades.** The Client Agreement clause 12.3(j) states that one of the conditions for OPO to accept a trade request is: "when the Client opens a position, the Client shall have sufficient Free Margin to cover the Initial Margin requirement in respect of that Open Position." If Free Margin is insufficient, the order is rejected.

**Free Margin gates withdrawals.** Clause 15.3(c) states that withdrawals are processed only if "at the moment of payment, the Client's Free Margin exceeds the amount specified in the withdrawal instruction including all payment charges." A trader with $10,000 Balance but high used Margin may not be able to withdraw freely.

## What changes Free Margin

Free Margin moves whenever Equity or Used Margin changes:

| When this happens                                            | Free Margin moves                                              |
| ------------------------------------------------------------ | -------------------------------------------------------------- |
| Open positions move in your favour (unrealized profit grows) | ↑ Free Margin increases                                        |
| Open positions move against you (unrealized loss grows)      | ↓ Free Margin decreases                                        |
| You open a new position                                      | ↓ Free Margin decreases (by the new position's Initial Margin) |
| You close a position                                         | Free Margin adjusts by the closed P/L and releases the Margin  |
| You deposit funds                                            | ↑ Free Margin increases                                        |
| You withdraw funds                                           | ↓ Free Margin decreases                                        |
| OPO changes margin requirements                              | Free Margin can move up or down                                |
|                                                              |                                                                |

## Free Margin can go negative

If open positions move severely against the trader and unrealized loss exceeds Balance, Equity can drop below Used Margin. At that point Free Margin is negative — the trader cannot open new positions, and the account is heading toward [[Margin Call]] and [[Stop Out]].

OPO provides [[Negative Balance Protection]] for retail accounts (clause 15.8), meaning the trader cannot owe more than the deposit. But Free Margin going negative is the warning sign that automatic position closure is approaching.

## Risk warning

A trader who opens too many positions or positions that are too large can find Free Margin draining rapidly during volatile market movements. Because Free Margin determines whether a new order is accepted and whether a withdrawal can be processed, monitoring Free Margin in real time is essential for active traders. A common mistake is opening multiple correlated positions that all move in the same direction during a market event — when they all lose simultaneously, Free Margin collapses faster than a trader anticipates.

## Source

- OPO Client Agreement v10, Appendix A (Free Margin, Necessary Margin)
- OPO Client Agreement v10, clause 12.3(j) (Free Margin requirement for opening positions)
- OPO Client Agreement v10, clause 15.3(c) (Free Margin requirement for withdrawals)
- OPO Client Agreement v10, clause 15.8 (Negative balance protection)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split into region-specific notes when ASIC, FSCA, and Seychelles agreements are obtained
- Note: the Client Agreement uses "Free Margin" and "Necessary Margin" but trading platforms (MT4, MT5, cTrader) often display these as "Free Margin" and "Margin" without further qualification — confirm whether platform labelling matches the agreement's terminology

## Related topics

- [[Equity]]
- [[Margin]]
- [[Necessary Margin]]
- [[Initial Margin]]
- [[Margin Level]]
- [[Margin Call]]
- [[Stop Out]]
- [[Negative Balance Protection]]
- [[Withdrawal Procedure]]
