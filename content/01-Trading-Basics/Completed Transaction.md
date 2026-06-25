---
title: Completed Transaction
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

# Completed Transaction

## Simple explanation

A Completed Transaction is a trade that has finished — both the opening side (buy or sell) and the closing side (the opposite) have executed. The trade is settled history. Its final profit or loss has been added to your account [[Balance]], and the [[Margin]] it tied up is released.

OPO defines completed transaction in the Client Agreement Appendix A as:

> Two counter deals of the same size in different directions (opening a position and closing the position): buying and then selling or selling and then buying.

In plain terms: one buy + one matching sell = one completed transaction. The position is closed, the books are settled, and what's left is a record in your trading history.

## The lifecycle

A completed transaction is the final state of a trade:

The transition from [[Open Position]] to Completed Transaction happens the instant the closing side executes. At that moment:

- The position disappears from "open trades" and appears in trade history
- Final profit or loss is calculated and added to [[Balance]]
- Used [[Margin]] for that position is released back into [[Free Margin]]
- Any [[Swap]] charges accrued during the open period are also debited from Balance
- [[Floating Profit/Loss]] for that position is no longer relevant

## What appears in your completed transaction history

For each completed transaction, your platform records:

- **Open time** and **Close time**
- **Instrument** (e.g. EUR/USD)
- **Direction** (Buy or Sell)
- **[[Lot]] size**
- **Open price** and **Close price**
- **[[Stop Loss]] and [[Take Profit]] levels** (if used)
- **[[Swap]] charges accrued**
- **[[Commission]] charged** (if applicable)
- **Final profit or loss in account currency**

This history is the trader's primary record-keeping resource — it's the data used to analyze strategy performance, calculate win rates, and identify which instruments or times of day produced the best results.

## How long completed transactions are kept

The Client Agreement clause 12.10 specifies a minimum retention period:

> OPO GROUP LLC. hereby confirms that all Client records and/or trading and non-Trading activity, current and/or past and/or archived shall be maintained for at least five (5) years after the termination of the business relationship with the Client and as per applicable legislative requirements.

So OPO keeps records for at least 5 years. However, the Client Agreement also allows the broker to **archive** older history within the platform:

> The Client understands, confirms, and accepts herein that any and/or all of his/her trading account history in MetaTrader 4 and MetaTrader 5 Platforms may at any time and without prior written consent and/or notice to the Client, further be archived by OPO GROUP LLC. to a single summarized line in the respective MetaTrader 4 trading account, where such trading account history records exceed a timeframe of one (1) month.

In plain terms: completed transactions older than 1 month may be compressed into a summarized line in the trading platform itself, though the full records remain accessible through the OPO dashboard/client portal (clauses 12.8 and 12.9).

**Practical implication:** if you want detailed records of trades older than a month, retrieve them via the client portal rather than the trading platform. Active traders are recommended to export their trade history regularly to maintain their own records.

## Completed transactions vs Open Positions — the key distinction

| | [[Open Position]] | Completed Transaction |
|---|---|---|
| State | Active, unsettled | Settled history |
| Affects [[Equity]] | Yes — via [[Floating Profit/Loss]] | No (already added to [[Balance]]) |
| Affects [[Free Margin]] | Yes — locks Margin | No (Margin released) |
| Affects [[Margin Level]] | Yes | No |
| Can be modified | Yes (close, partial close, change SL/TP) | No (history is fixed) |
| Subject to [[Margin Call]] / [[Stop Out]] | Yes | No |
| Subject to [[Swap]] charges | Yes (overnight) | No (already settled) |

Once a transaction completes, it has no further effect on the account except its contribution to the final [[Balance]].

## Why completed transactions matter for analysis

For strategy review and improvement, completed transactions are everything. Common metrics traders calculate from completed transaction history:

- **Win rate** — percentage of completed trades that closed in profit
- **Average win vs average loss** — informs effective risk-to-reward ratio
- **Total P/L by instrument** — which instruments produced gains, which produced losses
- **P/L by time of day / day of week** — when does the strategy work best
- **Drawdown** — worst sequence of consecutive losses
- **Profit factor** — total wins divided by total losses (above 1.0 is profitable; 1.5+ is healthy)

Without good trade record-keeping, traders cannot improve. Exporting completed transaction history regularly is one of the highest-value habits a developing trader can build.

## Risk warning

Completed transaction history is fixed once recorded, but during a [[Stop Out]] event or [[Force Majeure]], OPO can complete transactions at prices significantly different from what the trader anticipated. The history will accurately record these executions, but the trader's account balance will reflect actual closures, not expected ones. Traders reviewing their history after major events should not assume that losing trades represent "bad strategy" — sometimes they represent involuntary forced closure during fast markets. Distinguishing between strategy-driven losses and event-driven losses is critical for accurate strategy assessment.

## Source

- OPO Client Agreement v10, Appendix A (Completed Transaction, Transaction definitions)
- OPO Client Agreement v10, clause 12.7 (trade history archiving after 1 month)
- OPO Client Agreement v10, clauses 12.8 and 12.9 (accessibility of archived history)
- OPO Client Agreement v10, clause 12.10 (5-year minimum retention)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction retention requirements apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained (data retention requirements often vary by jurisdiction)
- Confirm whether the 1-month archive applies to MT5, cTrader, and OpoTrade in addition to MT4 (clause 12.7 explicitly mentions only MT4 and MT5)
- Confirm whether traders can export complete history beyond what's shown in-platform, and what export formats are supported
- Consider documenting recommended trade-history backup practice for traders

## Related topics

- [[Open Position]]
- [[Long Position]]
- [[Short Position]]
- [[Balance]]
- [[Equity]]
- [[Floating Profit/Loss]]
- [[Margin]]
- [[Free Margin]]
- [[Swap]]
- [[Commission]]
- [[Spread]]
- [[Transaction]]
- [[Transaction Size]]
- [[Stop Loss]]
- [[Take Profit]]
- [[Stop Out]]