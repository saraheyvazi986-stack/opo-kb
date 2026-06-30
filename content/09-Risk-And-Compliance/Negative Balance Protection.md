---
title: Negative Balance Protection
status: draft
audience: client
category: Risk and Compliance
region: global
language: en
owner: Compliance
reviewer:
last_reviewed:
effective_from: 2026-06-22
source_type: official
ai_allowed: false
risk_level: low
version: "1"
---
# Negative Balance Protection

## Simple explanation

Negative Balance Protection is OPO's commitment that a retail client cannot lose more than the total funds in their trading account. If a position closes at a loss large enough to drive the account balance below zero — for example, during an extreme market move or a price gap — OPO absorbs the excess loss rather than pursuing the client for the difference.

The maximum a retail trader can lose is the deposit. Not more. This is a contractual guarantee, not a courtesy.

OPO establishes Negative Balance Protection in the Client Agreement clause 15.8:

> OPO GROUP LLC. ensures that losses will not exceed the total available funds per Clients' OPO GROUP LLC. trading account(s) (negative balance protection).

## Why this matters

Without Negative Balance Protection, leveraged CFD trading would carry potentially unlimited downside. A trader with \$1,000 in their account, using 1:500 leverage to control a \$500,000 position, could in theory lose far more than \$1,000 if the market moved violently against them — they would owe the broker the difference, possibly tens of thousands of dollars.

This actually happened in January 2015 when the Swiss National Bank removed the EUR/CHF peg. The pair moved hundreds of pips in seconds, and many traders worldwide ended up owing brokers amounts that exceeded their account balances by 10x, 100x, or more. Some brokers pursued these debts; some absorbed them; some went bankrupt because the losses cascaded back to them from clients who simply couldn't pay.

Negative Balance Protection eliminates this risk entirely for the trader. The worst-case scenario is the loss of the deposit — substantial, but bounded.

## How Negative Balance Protection works mechanically

The protection operates after a position has closed at a catastrophic loss. The sequence:

1. A position is open with significant size and leverage
2. A fast adverse market move occurs (gap, news event, flash crash, force majeure)
3. The position triggers [[Stop Out]] but the system cannot close it fast enough at the Stop Out level
4. The position closes at a price that produces a loss larger than the account balance
5. The account balance shows a **negative number** temporarily
6. OPO adjusts the balance back to **zero** as part of Negative Balance Protection
7. The trader's account remains active at zero — no debt, no liability

The trader sees the protection work in the trade history: a position closed with a loss recorded, balance dropped to negative briefly, then a "Negative Balance Protection" adjustment entry brings it back to zero.

## What the policy covers

Negative Balance Protection covers losses that arise from:

- Standard market movements during normal trading
- Fast adverse moves during high-volatility events (news, central bank decisions)
- Price gaps at market opens (Monday morning forex, post-news jumps)
- [[Force Majeure]] events as defined in the Client Agreement clause 26
- Cascading [[Stop Out]] sequences during fast markets
- Failures of OPO's own systems that prevent timely position closure

The principle is simple: the broker took the trade, the broker provided the leverage, the broker is responsible for the execution infrastructure. If those things produce a loss exceeding the deposit, the broker absorbs it.

## What the policy does NOT cover

The Client Agreement clause 16.6 introduces a narrow but important exception:

> In the event of a negative balance in a retail Client account, OPO GROUP LLC. will not file a claim against the Client for that amount, except in cases where the Client has used illicit methods to create it.

The phrase **"illicit methods to create it"** is the carve-out. If a trader deliberately exploits the broker's systems or markets — for example through:

- **Market abuse** as defined in Client Agreement clause 35 (arbitrage trading, picking/sniping, manipulating quotes, abusive strategies during volatile conditions)
- **Latency arbitrage** — exploiting price feed delays
- **Bonus arbitrage** — exploiting promotional credits in ways the Bonus Programs document prohibits
- **Erroneous order exploitation** — knowingly trading on quotes that the trader knows are erroneous
- **Money laundering, fraud, or other criminal activity** under Client Agreement clauses 24, 27.2, 35

then OPO reserves the right to:
- Withdraw the Negative Balance Protection
- Pursue the trader for the deficit
- Close the account
- Confiscate profits from the abusive activity
- Take legal action

This is consistent with how regulated brokers in major jurisdictions handle the same protection. The protection exists to shield ordinary trading losses, not to insure fraudulent activity.

## Retail clients only — not Professional or Eligible Counterparty

Negative Balance Protection in the Client Agreement clause 15.8 applies to **retail** trading accounts. The agreement also defines two other client categories:

- **Professional Client** — clients who meet specific financial sophistication thresholds and have explicitly opted into professional status
- **Eligible Counterparty** — institutional clients (banks, asset managers, regulated investment firms)

Professional Clients and Eligible Counterparties **do not automatically receive Negative Balance Protection.** The Client Agreement places professional and eligible counterparty clients under different protections, including the Title Transfer Collateral Arrangement (TTCA — clause 6.15) which can leave the client as an unsecured creditor in the event of broker insolvency.

This is one of several important reasons most retail traders should **decline** any offer to upgrade to Professional Client status. The trade-offs are:

| | Retail Client | Professional Client |
|---|---|---|
| Negative Balance Protection | Yes (clause 15.8) | Not automatic |
| Title Transfer Collateral Arrangement | No | Can apply (clause 6.15) |
| Maximum leverage | Standard tier or High Leverage tier | Sometimes higher |
| Regulatory protections | Full retail-tier protections | Reduced — professional is deemed to understand the risks |

The Client Agreement clause 4.5 makes the default explicit: *"The Client will be categorized and treated by OPO GROUP LLC. as a Retail Client unless otherwise expressly specified by OPO GROUP LLC."* So retail status is the default — and for most traders, the right one to keep.

See [[Client Categorization]] for full details on the differences.

## Account-level, not position-level

A subtle but important point: Negative Balance Protection applies at the **account level**, not per-position. The relevant phrase from clause 15.8 is "per Clients' trading account(s)."

This means:
- If you have multiple positions, total losses across all of them cannot exceed your account balance
- If you have multiple trading accounts under one client login, each account is protected separately
- Internal transfers between accounts can complicate the calculation — see Client Agreement clause 13.3, which lets OPO use funds in any of your accounts to settle obligations on a deficit account

## What traders should still do

Negative Balance Protection is a safety net, not a license to take excessive risk. The protection caps your downside at the deposit, but **losing the entire deposit is still a catastrophic outcome.** Active risk management remains essential:

- Set appropriate [[Stop Loss]] orders on every position
- Use position sizing that limits per-trade risk to 1-2% of account
- Avoid stacking correlated positions that could all lose simultaneously
- Watch [[Margin Level]] continuously, not [[Balance]]
- Don't hold leveraged positions through major news events without considering reduced position size
- Don't assume Negative Balance Protection will save you from poor risk management — it only saves you from losing *more than* the deposit, not from losing the deposit itself

## Risk warning

Negative Balance Protection is a meaningful retail-trader safeguard, but traders should not let it create a false sense of security. The protection ensures that you cannot owe OPO money beyond your deposit — but the deposit itself can be entirely wiped out by a single catastrophic event, especially with high leverage and large position sizes. The protection also does not apply to losses generated through abusive trading practices, market abuse, or other "illicit methods" as defined in Client Agreement clause 16.6 — and OPO has broad discretion in determining what constitutes such activity. The most important protection for a trader is appropriate position sizing combined with disciplined Stop Loss usage. Negative Balance Protection is the safety net beneath these primary protections; it should never be the primary protection itself.

## Source

- OPO Client Agreement v10, clause 15.8 (Negative Balance Protection definition)
- OPO Client Agreement v10, clause 16.6 (illicit methods exception)
- OPO Client Agreement v10, clause 4 (Client Categorization — Retail, Professional, Eligible Counterparty)
- OPO Client Agreement v10, clause 4.5 (default Retail status)
- OPO Client Agreement v10, clause 6.15 (Title Transfer Collateral Arrangement)
- OPO Client Agreement v10, clause 13.3 (multi-account settlement)
- OPO Client Agreement v10, clause 35 (Market Abuse)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction Negative Balance Protection applies globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. **Note:** ASIC mandates Negative Balance Protection for retail clients under ASIC regulations, so the ASIC version may differ in specificity even if the substantive protection is the same
- Confirm that the per-account interpretation of clause 15.8 is OPO's actual operational practice — specifically, what happens to multi-account clients when one account goes negative
- Document the typical timeframe in which negative balance is corrected to zero (immediate, end of day, T+1) — this is the kind of operational detail traders ask about
- Clarify the boundary of "illicit methods" in clause 16.6. The current language is broad and could create disputes — concrete examples in client-facing documentation would reduce trader confusion
- Confirm how Negative Balance Protection interacts with the Bonus Programs document — specifically clause 2.6 of Bonus Programs ("The Bonus will be removed if... The Client suffers losses equal to the amount deposited") which suggests bonus removal can produce a balance scenario that intersects with Negative Balance Protection rules
- Consider publishing the protection more prominently on the OPO website. Currently it's buried in clause 15.8 of a 55-page agreement — many traders don't know they have it

## Related topics

- [[Margin]]
- [[Free Margin]]
- [[Equity]]
- [[Balance]]
- [[Stop Out]]
- [[Margin Call]]
- [[Margin Level]]
- [[Leverage]]
- [[Stop Loss]]
- [[Long Position]]
- [[Short Position]]
- [[Open Position]]
- [[Force Majeure]]
- [[Market Abuse Policy]]
- [[Client Categorization]]
- [[Title Transfer Collateral Arrangement]]
- [[Bonus Programs]]
