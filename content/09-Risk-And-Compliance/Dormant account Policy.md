---
title: Dormant Account Policy
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

 
# Dormant Account Policy

## Simple explanation

A dormant account is a trading account that has had **no trading activity** for six consecutive months. When OPO classifies an account as dormant, it begins charging a **$5 monthly maintenance fee** debited directly from the account balance. The fee continues until the account is either reactivated through trading activity, fully depleted, or closed.

This catches many traders by surprise. A trader who opens an account, deposits funds, doesn't get around to actually trading, and forgets about it can return months later to find the balance has been quietly drained by maintenance fees.

The policy is documented in the Client Agreement clauses 9.11 and 27.13.

## How an account becomes dormant

From the Client Agreement clause 9.11:

> A Trading Account shall be considered "Dormant", thus charged accordingly, in the event that the Client has not opened or closed any positions, and/or has not placed any pending orders, for a duration of six (6) consecutive months.

Three things matter in this definition:

1. **Six consecutive months** — not six months total. A trader who places one trade in month 4 reset the clock; the dormancy clock starts fresh
2. **Any trading activity counts** — opening a position, closing a position, or placing a pending order all qualify
3. **Logging in does not count** — only actual trading activity. A trader who logs in regularly to check their balance, deposits or withdraws funds, but never places a trade, will still see their account become dormant

What also does **not** reset the dormancy clock:
- Logging into the platform
- Viewing market quotes
- Receiving newsletters or marketing emails from OPO
- Making a deposit
- Making a withdrawal
- Updating account information or KYC documents

The clock resets only on actual trade activity.

## What happens when the account is classified as dormant

From the Client Agreement clause 9.11:

> Following the aforementioned period, the Company has the right to charge an annual maintenance fee of 60 USD (5 USD per month) to cover administrative charges. Such fee shall be charged on the first day of each calendar month, starting from the first month of the Trading Account's dormancy classification.

So the mechanics are:
- **Trigger:** 6 consecutive months without trading activity
- **Fee:** $5 USD per month
- **Charging frequency:** First day of each calendar month
- **Account currency:** If the account is denominated in a currency other than USD, the fee is converted at OPO's prevailing exchange rate (which incorporates OPO's discretion per Client Agreement clause 10.1)

A trader who leaves $500 in an account and never returns will see:
- Months 1–6: no fees
- Month 7 onward: $5 deducted on the 1st of each month
- After approximately 100 months (≈8 years): account balance reaches zero

## What happens when the account balance reaches zero

From the Client Agreement clause 9.11:

> In the event that the Account Balance becomes zero, then the Company reserves the right to terminate the Client Agreement in accordance with Section 27.13 of this Agreement.

The Client Agreement clause 27.13 specifies the termination process for accounts:

> The Company shall be entitled to terminate this Agreement with immediate effect by giving Written Notice to the Client.

So when the dormant account fees reduce the balance to zero, OPO has the right to fully close the account. The trader's relationship with OPO ends. To trade again, the trader would need to re-open an account (which means going through KYC again, depositing again, and so on).

## A note on what counts as "balance"

The dormant fee is charged against Balance, not Equity. Since a dormant account by definition has no open positions, Balance and Equity are typically identical. But this matters in one edge case: if a trader has a "stuck" position they cannot close (technical platform issue, suspension, etc.), the Balance might still be positive even though Equity is lower. In this case, dormant fees still apply to Balance.

## How to avoid dormant fees

The simplest answer: **make a trade every 5 months.** Any trade resets the dormancy clock. Even a 0.01-lot micro position opened and closed immediately is sufficient.

Practical alternatives:

- **Place a pending order with a far-away trigger price.** Pending orders count as activity. Place a Buy Limit on EUR/USD at 0.5000 (no realistic chance of triggering) and your account stays active. You can cancel or modify the pending order later
- **Withdraw the funds.** If you don't plan to trade for over 6 months, withdraw to a bank account or e-wallet. The dormancy clock keeps running, but **zero-balance dormant accounts are exempt from the $5/month fee** (Client Agreement clause 27.13(d)) — though OPO reserves the right to close zero-balance dormant accounts entirely

What does **not** work:
- Calling support and saying "I plan to come back"
- Making a deposit
- Logging in to check the account

**Fee waiver provision:** Client Agreement clause 27.13(c) allows OPO to waive dormancy fees at its discretion if a client makes a genuine attempt to resolve outstanding balances or reactivate the account. Contact support if you believe a waiver is warranted.

## Multiple accounts under one client login

The Client Agreement is silent on how dormancy applies across multiple sub-accounts. Two interpretations are possible:

1. **Per-account dormancy:** Each MT4, MT5, cTrader, or OpoTrade sub-account is evaluated independently. A trader with three accounts could see one go dormant while the others stay active
2. **Per-client dormancy:** Any trading activity on any sub-account resets the dormancy clock for all of them

In practice, brokers typically use **per-account dormancy** — meaning a trader with multiple sub-accounts needs to ensure each one has at least one trade per 5 months. The trader should verify this with OPO support before relying on it.

## How dormancy interacts with active bonuses

If a trader has any active bonus credit (from the Bonus Programs) and the account becomes dormant, the relationship is unclear:
- The bonus is typically forfeited when the account is closed
- Whether the dormant-fee accumulation begins before or after bonus removal is not explicitly stated
- A trader with a remaining bonus balance who becomes dormant should review their exact bonus terms

See [[Bonus Programs]] for the full bonus mechanics. The interaction with dormancy needs clarification from OPO support.

## What the policy is designed to do

The dormant account fee serves three purposes from OPO's perspective:

1. **Recover the administrative cost** of maintaining inactive accounts on their systems
2. **Encourage account closure** rather than indefinite open inactive accounts
3. **Discourage account hoarding** — traders sometimes open multiple accounts at different brokers as backups, planning never to use them. The fee creates a small cost for this

From a trader perspective, the fee is best understood as a "use it or close it" prompt. A trader who genuinely intends to come back to trading should keep at least one small trade per 5 months. A trader who is genuinely done should withdraw funds and let the account close (or formally request closure to be tidy about it).

## Risk warning

The dormant account fee is small ($5/month) but compounds quietly over time. A trader who leaves a $500 balance and walks away for 8 years will find the entire balance has been consumed by fees, with the account ultimately closed. More importantly: many traders open accounts to "try out" a broker, deposit a moderate sum, never get serious about trading, and forget about the account entirely. Months or years later, they recall the deposit and find the balance dramatically reduced or zero. The Client Agreement provides no warning before dormancy fees begin — a trader is responsible for knowing about and remembering this provision. The simplest protection is to either trade at least every 5 months or withdraw remaining funds when stepping away from active trading.

## Source

- OPO Client Agreement v10, clause 9.11 (dormant account classification and fee)
- OPO Client Agreement v10, clause 27.13 (agreement termination)
- OPO Client Agreement v10, clause 10.1 (currency conversion discretion)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction dormancy rules apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained — some jurisdictions have specific rules about dormant account treatment and required client notification
- Confirm whether OPO sends any notification to clients before the dormancy classification begins — the Client Agreement is silent on this, but some regulators require advance notice (typically 30 days). Sending such a notice would significantly reduce trader complaints
- Confirm per-account vs per-client dormancy treatment — this is a practical question traders frequently ask
- Confirm the dormant-fee-vs-bonus-balance interaction — this should be explicitly documented
- Confirm whether the $5/month fee is fixed or subject to change. The Client Agreement clause 9.2 allows OPO to change fees with website-posting notice, but historically this fee has been stable across brokers using similar models
- Consider publishing the dormancy fee more prominently. Currently it's only in clause 9.11 of a 55-page agreement and is genuinely surprising to most traders. A prominent FAQ entry, account page mention, or onboarding notice would substantially reduce post-fee complaints
- Document whether traders can dispute dormancy fees that they believe were applied incorrectly (e.g. due to a forgotten trade that should have reset the clock)

## Related topics

- [[Balance]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Black Account]]
- [[Social Trade Account]]
- [[Account Types Overview]]
- [[Bonus Programs]]
- [[Withdrawal Procedure]]
- [[Pending Order]]
- [[Order]]
- [[Open Position]]
