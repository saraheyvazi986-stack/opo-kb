---
title: Commission
status: draft
audience: client
category: Trading Basics
region: global
language: en
owner: Compliance
reviewer:
last_reviewed:
effective_from:
source_type: official
ai_allowed: false
risk_level: low
version: "1"
---
# Commission

## Simple explanation

Commission is a per-trade fee that OPO charges on certain account types, calculated based on the volume traded. Unlike [[Spread]] (which is embedded in the price and paid on every trade automatically), commission is a separate explicit charge debited from your account when you open and/or close a position.

Not all accounts charge commission. OPO uses commission only on accounts that offer raw or near-raw spreads — the commission replaces the broker's earnings that would otherwise come from a wider spread.

## How commission is calculated at OPO

OPO charges commission **per lot traded**, in USD. The published rates from the account pages:

| Account | Commission per lot |
|---|---|
| [[Standard Account]] | None |
| [[ECN Account]] | $6 per lot |
| [[ECN Pro Account]] | $4 per lot |
| [[Social Trade Account]] | None |
| [[Social Pro Account]] | $4 per lot |
| [[Black Account]] | None |
| [[cTrader ECN Account]] | $6 per lot |
| [[cTrader ECN Plus Account]] | $4 per lot |
| [[cTrader Copy Account]] | None |

**Important: the published rate is typically the round-turn commission** (entry plus exit combined), but some brokers quote it as per-side. OPO documentation does not explicitly clarify which model applies — this needs confirmation. If the rate is per-side, the actual cost of a complete trade is double the quoted figure.

## Where commission comes from contractually

The Client Agreement clause 9.1 states:

> The Client shall be obliged to pay OPO GROUP LLC. the commissions, charges and other costs set out in the Contracts Specifications.

And clause 9.2:

> OPO GROUP LLC. may vary commissions, charges, and other costs from time to time without prior Written Notice to the Client. All changes in commissions, charges and other costs are displayed on OPO GROUP LLC. Website and posting on the Website shall be considered due notice.

This means: OPO can change commission rates at any time, and posting on the website is sufficient notice. Traders should check current rates before relying on historical figures, especially before high-volume trading.

## A worked example — when commission beats spread

Consider a trader placing one full lot (100,000 units) of EUR/USD on OPO:

**Standard Account** (no commission, 1.8-pip spread):
- Spread cost: 1.8 pips × $10/pip = **$18**
- Commission: $0
- **Total round-turn cost: $18**

**ECN Account** ($6/lot commission, 0.8-pip spread):
- Spread cost: 0.8 pips × $10/pip = $8
- Commission: $6 (assuming round-turn)
- **Total round-turn cost: $14**

**ECN Pro Account** ($4/lot commission, 0.0-pip spread):
- Spread cost: 0.0 pips × $10/pip = $0 (best case)
- Commission: $4
- **Total round-turn cost: $4** (best case)

On a 1-lot EUR/USD trade, ECN Pro is dramatically cheaper than Standard — about 4× cheaper. **But this only matters if you're trading enough volume to amortize the $5,000 minimum deposit.** A trader making one trade per week saves $14 a week on ECN Pro vs Standard — about $728/year. That's worth it. A trader making one trade per month saves $14/month — about $168/year. That doesn't justify the higher account minimum.

## Commission on partial lots

Commission scales linearly with trade size. A 0.5-lot trade pays half the per-lot commission; a 0.1-lot trade pays one-tenth.

On ECN at $6/lot:
- 1.0 lot trade: $6 commission
- 0.5 lot trade: $3 commission
- 0.1 lot trade: $0.60 commission
- 0.01 lot trade (minimum): $0.06 commission

This is one reason small-account traders should use the [[Standard Account]] — the commission per trade is tiny but the spread cost is also proportionally small, and the spread-only model avoids the per-trade overhead of commission accounting.

## When commission is charged

Commission is typically deducted at the moment the trade is opened (or split between open and close, depending on the model). The Client Agreement clause 9.1 also notes:

> OPO GROUP LLC. will provide to the Client an itemized breakdown of the total commissions, costs, and charges at the request of the Client. These can be found inside the Client's personal area, My OPO GROUP LLC.

So traders can verify commission charges by checking their account's transaction history.

## Other commission-like charges to be aware of

Beyond per-trade commission, OPO has several other potential charges. These are not strictly "commission" but they affect the total cost of running a trading account:

- **Inactivity / dormant account fee** — $5 per month after 6 consecutive months of no trading activity (Client Agreement clauses 9.11, 27.13). See [[Dormant Account Policy]].
- **No-activity withdrawal fee** — 3% to 6% of withdrawal amount if a trader deposits, doesn't trade, then withdraws (Client Agreement clause 6.14). See [[Withdrawal Procedure]].
- **Currency conversion fees** — when depositing or withdrawing in a currency other than the account currency, OPO applies a conversion rate that includes an implicit fee. The Client Agreement clause 10.1 gives OPO discretion over the conversion rate.
- **Payment processor fees** — passed through from third parties (clause 3.7 of Withdrawal Conditions).
- **Swap charges** — overnight financing charges on positions held past 5pm New York time. See [[Swap]].
- **Triple swap on Fridays** — clause 9.13 of the Client Agreement: standard practice covering weekend financing in advance.

A trader's total cost is the sum of all of these, not just the per-trade commission.

## Risk warning

Commission is the cleaner, more transparent of the two primary cost models — it's an explicit number debited from the account, easy to verify and budget for. However, traders should remember that commission is *additive* to spread on ECN/Pro accounts, not a replacement. The total cost per trade is spread plus commission, and on high-volume strategies the commission alone can become a significant drag on returns. OPO can change commission rates without notice (clause 9.2 only requires website posting), so traders running long-term automated strategies should monitor for changes that could affect strategy economics. The cumulative effect of inactivity fees, no-activity withdrawal penalties, conversion charges, and swaps can also surprise traders who focus only on per-trade commission — total cost of ownership matters more than headline rate.

## Source

- OPO Client Agreement v10, clause 9.1 (commission obligation)
- OPO Client Agreement v10, clause 9.2 (right to change commissions without notice)
- OPO Client Agreement v10, clause 9.11 (dormant account fee)
- OPO Client Agreement v10, clause 9.13 (triple swap Fridays)
- OPO Client Agreement v10, clause 6.14 (no-activity withdrawal fee)
- OPO Withdrawal Conditions v3, clause 3.7 (payment fees pass-through)
- OPO website account type pages (per-lot commission rates by account)
- Last verified: 2026-05-12

## Internal review notes

- **CRITICAL: Confirm whether quoted commission rates ($6, $4) are round-turn or per-side.** This is a fundamental question that the public documentation does not explicitly answer. If per-side, the actual trade cost is double what most traders will assume from reading the account pages
- Confirm SVG-jurisdiction commissions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm exact timing of commission deduction — at open, at close, or split — and how this is displayed in MT4, MT5, cTrader, and OpoTrade
- Confirm whether commission is charged separately for partial closes of a position
- Consider adding a commission calculator tool linked from this note

## Related topics

- [[Spread]]
- [[Lot]]
- [[Pip]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Black Account]]
- [[cTrader ECN Account]]
- [[cTrader ECN Plus Account]]
- [[Swap]]
- [[Dormant Account Policy]]
- [[Withdrawal Procedure]]
- [[Contract Specifications]]