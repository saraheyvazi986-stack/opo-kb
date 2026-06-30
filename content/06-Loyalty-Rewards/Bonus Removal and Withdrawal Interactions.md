---
title: Bonus Removal and Withdrawal Interactions
status: draft
audience: client
category: Loyalty-Rewards
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



# Bonus Removal and Withdrawal Interactions

## Simple explanation

A bonus at OPO is conditional credit, not unconditional cash. There are multiple specific conditions under which an active bonus is removed from your account, and several scenarios where the interaction between a bonus and a withdrawal becomes complicated. Understanding these mechanics before you accept a bonus — and certainly before you request a withdrawal during a bonus period — is essential.

This note covers the removal triggers, the withdrawal interactions, and what happens to associated trading profits when bonuses are removed.

The mechanics are governed by the **OPO Bonus Programs document**, with cross-references to multiple Client Agreement clauses.

## The five categories of bonus removal triggers

A bonus can be removed for any of the following reasons. Each category is described in detail below:

1. **Equity-reaches-deposit threshold** — the bonus's main risk-management trigger
2. **Voluntary withdrawal** — the trader chooses to withdraw deposited funds
3. **Expiry without meeting volume requirement** — time runs out
4. **Abuse or misconduct finding** — disciplinary removal
5. **Other operational triggers** — dormancy, account changes, broker discretion

## Trigger 1: Equity reaches the deposit amount

This is the most common and surprising removal trigger. The Bonus Programs document clause 2.6 states:

> The Bonus will be removed if the Client's account Equity reaches the amount of the deposit. The Bonus will also be removed if the Client suffers losses equal to the amount deposited.

What this means in practice:

Suppose a trader deposits \$1,000 and receives a \$500 bonus. Their starting state:
- Deposit: \$1,000
- Bonus: \$500
- Total Equity: \$1,500

If trading losses bring Equity down to \$1,000 (matching the original deposit), **the bonus is removed**.

After bonus removal:
- Deposit Balance: \$1,000 (theoretical maximum — but Equity is also \$1,000 now)
- Bonus: \$0 (removed)
- Total Equity: \$1,000

The trader still has their original deposit. They've lost the bonus.

This is intentional — the bonus serves as a "first-loss" buffer. The broker effectively offers the bonus credit as risk capital, and when losses consume that buffer, the bonus disappears and the trader's own capital is at risk going forward.

**Why this catches traders by surprise:** when a trader sees \$1,500 in Equity after deposit + bonus, they often size positions based on the \$1,500 figure. A loss that reduces Equity by \$500 — bringing it to \$1,000 — feels like a loss of bonus only. But it also triggers complete removal of the remaining bonus structure. The trader now faces their next trade with \$1,000 (real capital) and no bonus buffer.

**Practical implication for risk management:** position size based on deposited capital, not bonus-inflated equity. If you have \$1,000 deposit + \$500 bonus, treat the trading capital as \$1,000 for risk-management purposes. The \$500 bonus is the "free shot" — losing it costs nothing real, but it goes away entirely once losses match the deposit amount.

## Trigger 2: Voluntary withdrawal

The interaction between withdrawals and active bonuses is the second most common source of trader confusion. The Bonus Programs document and [[Withdrawal Procedure]] together establish the rules.

### Withdrawing deposited funds while bonus is active

When a trader requests a withdrawal of deposited funds (not yet converted bonus credit), the typical outcomes:

| Withdrawal type | Effect on active bonus |
|---|---|
| Full deposit withdrawal | Bonus removed entirely |
| Partial deposit withdrawal | Bonus reduced proportionally OR removed entirely (depends on specific bonus terms) |
| Withdrawal of converted bonus (volume requirement met) | Bonus already converted; no removal issue |
| Withdrawal of profits earned during bonus period | Profits typically withdrawable; bonus credit treatment varies |

The Bonus Programs document is somewhat inconsistent on partial-withdrawal handling — some bonus types support proportional reduction, others remove the entire bonus on any partial withdrawal. The specific bonus terms must be consulted.

### A worked example

A trader has:
- Deposit: \$2,000
- Bonus: \$1,000 (50% Welcome Bonus)
- Current Equity: \$3,200 (some profits accumulated)
- Volume requirement: 30% completed (not yet converted)

The trader requests a withdrawal of \$500 from their deposited funds.

**Possible outcomes depending on bonus terms:**

| Outcome | Result |
|---|---|
| Bonus removed entirely (most common) | Account: \$500 withdrawn, \$1,500 deposit + \$0 bonus + \$200 retained profit = \$1,700 Equity |
| Proportional reduction (less common) | Account: \$500 withdrawn, \$1,500 deposit + \$750 reduced bonus + \$200 retained profit = \$2,450 Equity |
| Bonus locked until full deposit re-paid (rare) | Withdrawal allowed, but bonus frozen pending re-deposit |

The trader cannot know in advance which outcome will apply without reading the specific bonus terms for the bonus they accepted.

### The deposit-method matching rule

The [[Withdrawal Procedure]] anti-money-laundering rule (Client Agreement clause 15.5) requires that withdrawals be processed back to the original deposit method. This creates an additional complication during bonus periods:

If a trader deposited via bank card and wants to withdraw via crypto, they must first withdraw to the bank card. But the act of starting a withdrawal — even before any funds actually arrive at the trader's payment method — typically triggers the bonus removal logic.

So a trader requesting a withdrawal route they prefer (crypto for speed) before the deposit-method-matching withdrawal is complete may forfeit the bonus without successfully completing the desired withdrawal.

## Trigger 3: Expiry without meeting volume requirement

If a bonus has a time limit (most do) and the trader fails to meet the volume requirement before the expiry date:

- Bonus credit is **removed**
- Trading profits earned **using deposited funds** are not affected
- Trading profits earned **using bonus credit** are typically removed alongside the bonus
- The trader retains deposited principal

The distinction between profits earned with deposited vs. bonus funds is often unclear in practice — OPO generally applies a proportional approach, but the specific bonus terms vary.

This is one reason traders should track their bonus expiry dates carefully and avoid accepting bonuses with timelines that don't match their realistic trading volume.

## Trigger 4: Abuse or misconduct finding

The Bonus Programs document and [[Market Abuse Policy]] together create severe consequences for traders found to engage in abusive behaviour around bonuses:

### Bonus-specific abuse

Behaviour that triggers bonus-specific abuse findings:
- Opening multiple accounts to claim the same bonus
- Coordinating with other traders to manipulate bonus volume requirements
- Using bonuses in patterns specifically designed to exploit the mechanics
- Engaging in trades specifically to inflate volume artificially
- Hedged-position patterns designed to accumulate volume without market risk

### Consequences of bonus abuse findings

| Consequence                                                               | Severity |
|---|---|
| Bonus credit immediate forfeiture                                         | Standard |
| Profits earned using bonus credit confiscated                             | Standard |
| Profits earned using deposited funds reviewed and potentially confiscated | Severe |
| Account placed in Close-Only Mode pending investigation                   | Standard |
| Permanent ban from future OPO bonus programs                              | Standard |
| Account termination under [[Market Abuse Policy]]                         | Severe |
| Refusal of withdrawal requests for disputed funds                         | Severe |
| Loss of [[Negative Balance Protection]] under "illicit methods" exception | Catastrophic |

The combination of severe consequences — confiscation of profits, potential account closure, loss of NBP — means that traders identified for bonus abuse can lose dramatically more than the bonus itself.

### Detection mechanisms

OPO monitors for bonus abuse through:

- KYC data matching across accounts
- IP address and device fingerprinting
- Payment method matching
- Trading pattern analysis (correlation of trades across multiple accounts)
- Anomaly detection on volume patterns
- Manual compliance review of suspicious accounts

Sophisticated abuse schemes are typically detected — both immediately and retroactively. A trader who appears to have successfully extracted bonus value through abusive patterns may face consequences months later as detection systems improve.

## Trigger 5: Other operational triggers

Several other situations can result in bonus removal:

### Account dormancy

The [[Dormant Account Policy]] (6 months of no trading) typically results in bonus removal. The specific timing isn't documented in the Client Agreement — typically the bonus is removed when the dormancy classification activates, alongside the \$5/month maintenance fee accrual.

### KYC issues and Close-Only Mode

When an account enters [[Document Expiry / Close-Only Mode]] due to expired documents, active bonuses are typically removed during the period. The trader cannot trade, cannot meet volume requirements, and cannot benefit from the bonus. Even after document renewal, the removed bonus is typically not restored.

### Account categorization changes

A trader upgrading from Retail to Professional Client (see [[Client Categorization]]) may find that:
- Existing Retail-targeted bonuses are removed
- New Professional-tier bonus options may become available
- The transition itself may trigger bonus removal regardless of new eligibility

### Account closure

A trader who closes their account (whether voluntarily or by OPO termination) forfeits any active bonus credit and any profits associated with that bonus that haven't been converted.

### Leverage tier changes

Moving from a standard-leverage account to a high-leverage account (which is excluded from bonuses per the Bonus Programs document clause 2.3) automatically removes any active bonus.

### Broker discretion

The Bonus Programs document grants OPO broad discretion to remove bonuses at its judgment. Common discretionary scenarios:

- Suspicious activity patterns not rising to formal abuse findings
- Compliance investigations even when no determination is made
- Risk management responses to extreme market events
- General OPO commercial decisions

The trader cannot easily predict or prevent discretionary removal beyond avoiding patterns that look suspicious.

## What happens to profits when a bonus is removed

This is the area where bonus mechanics affect trader outcomes most directly. The general framework:

### Profits earned using bonus credit

Profits that arose from trading the bonus credit (the additional buying power the bonus provided) are typically:

- Removed alongside the bonus if the bonus is removed for "first-loss" or equity-threshold reasons
- Removed if the bonus is removed for abuse findings
- Retained if the bonus is removed due to voluntary withdrawal of deposited funds (depending on terms)
- Retained if the bonus expires after volume conversion is complete

The specific behaviour varies by bonus type. The general principle: profits from bonus credit are conditional on the bonus successfully completing its conversion.

### Profits earned using deposited funds

Profits earned through trading with the trader's own deposited capital are generally:

- Retained when the bonus is removed for routine reasons
- Subject to review and potential confiscation in abuse cases
- Generally protected unless the trader is found to have committed abuse

The line between "bonus profits" and "deposit profits" can be unclear in practice. OPO typically applies a proportional approach — if a position was opened with 60% deposited funds and 40% bonus credit, profits are allocated 60/40. But the specific calculation method isn't always transparent.

## What this means for trader strategy

Practical implications for how to think about a bonus:

1. **Treat the bonus as conditional, not real money.** Until conversion is complete, the bonus is not your capital
2. **Size positions based on deposited capital, not bonus-inflated equity.** This protects against the "Equity reaches deposit" trigger
3. **Plan withdrawal needs before accepting a bonus.** If you might need to withdraw funds during the bonus period, calculate whether you can afford to forfeit the bonus
4. **Track expiry dates.** Set calendar reminders for the volume-requirement deadline
5. **Don't increase position sizes to chase volume.** This typically destroys profitability and exposes the trader to greater drawdowns
6. **Avoid behaviours that look like abuse, even if not intentional.** Multiple accounts, coordinated trading, rapid hedged positions, volume specifically targeted at bonus thresholds — all flag detection systems
7. **Don't trade through Close-Only Mode or KYC issues hoping the bonus will restore.** Removed bonuses are typically permanently removed
8. **Take profits when you have them.** Profits earned during a bonus period that haven't yet been converted to withdrawable status are at risk until the volume requirement is fully met

## Risk warning

The combination of triggers that can cause bonus removal — equity thresholds, withdrawal interactions, expiry, abuse findings, dormancy, KYC issues, account changes, broker discretion — means that maintaining a bonus through to successful conversion requires both careful risk management and continuous attention to account state. The "Equity reaches deposit" trigger is particularly insidious because it operates automatically without warning at the moment Equity touches the threshold. Profits earned during a bonus period exist in a state of uncertainty until the volume requirement is fully met — they can be lost alongside the bonus in many removal scenarios. Bonus abuse findings can result in confiscation of profits, account closure, and loss of [[Negative Balance Protection]], producing total losses dramatically larger than the bonus value. The safest approach is to accept bonuses only when the volume requirement is comfortably achievable in your normal trading rhythm, to size positions as if the bonus didn't exist (protecting against the equity-threshold trigger), to avoid any behaviour patterns that could be classified as abuse, and to never accept a bonus where you might need to withdraw funds before volume conversion is complete.

## Source

- OPO Bonus Programs document, clause 2.6 (Equity reaches deposit triggers removal)
- OPO Bonus Programs document (general removal and withdrawal interaction provisions)
- OPO Bonus Programs document, clause 2.11 (1:500 leverage cap)
- OPO Bonus Programs document, clause 9.4 (Seychelles governing law)
- OPO Client Agreement v10, clause 15 (Withdrawal Procedure)
- OPO Client Agreement v10, clause 15.5 (deposit-method matching)
- OPO Client Agreement v10, clause 15.8 (Negative Balance Protection)
- OPO Client Agreement v10, clause 16.6 (illicit methods exception)
- OPO Client Agreement v10, clause 35 (Market Abuse Policy)
- OPO Client Agreement v10, clause 9.11 (dormant account fee)
- OPO Client Agreement v10, clauses 20.6–20.9 (Document Expiry / Close-Only Mode)
- OPO Client Agreement v10, clause 4 (Client Categorization)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG/Seychelles jurisdictional bonus removal applies globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. The governing-law inconsistency between the Bonus Programs document (Seychelles) and Client Agreement (SVG) is particularly relevant for removal disputes — the jurisdiction for dispute resolution affects practical outcomes
- Document the **specific equity-threshold removal mechanics** more precisely — is it the instantaneous Equity touch, the daily review, end-of-trading-session review? The Bonus Programs document clause 2.6 doesn't specify
- Document the **specific behaviour on partial withdrawals** for each bonus type — currently inconsistent across bonus terms
- Document the **specific profit-allocation method** when both bonus credit and deposited funds contribute to a trade — proportional, FIFO, LIFO, or some other approach
- Document the **complete list of dormancy-triggering and bonus-removal sequence** — when exactly during the 6-month dormancy timeline does the bonus get removed
- Document the **appeals process specifically for bonus removal decisions**, beyond general [[Complaints Procedure]]
- Document **historical cases where bonuses were removed by discretion** (anonymized) to give traders insight into what kinds of patterns trigger discretionary action
- Clarify the **interaction between bonus removal and Negative Balance Protection during fast adverse moves** — if losses are accumulating rapidly during a market event, does the bonus removal complete before NBP triggers, or vice versa, and what's the practical outcome for the trader
- Consider whether the OPO dashboard should display **active bonus status and approaching removal triggers** more prominently — traders frequently aren't aware their bonus is about to be removed

## Related topics

- [[Bonus Programs Overview]]
- [[Bonus Conversion and Volume Requirements]]
- [[Bonus Eligibility and Restrictions]]
- [[Withdrawal Procedure]]
- [[Negative Balance Protection]]
- [[Market Abuse Policy]]
- [[Dormant Account Policy]]
- [[Document Expiry / Close-Only Mode]]
- [[Client Categorization]]
- [[Complaints Procedure]]
- [[Leverage]]
- [[Leverage Adjustment Policy]]
- [[Equity]]
- [[Balance]]
- [[Free Margin]]
- [[Margin Level]]
- [[Stop Out]]
- [[Open Position]]
- [[Completed Transaction]][]()