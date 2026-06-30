---
title: Bonus Program Overview
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

# Bonus Programs Overview

## Simple explanation

OPO offers promotional bonus credits to traders who meet specific eligibility criteria. A bonus is **not the same as cash you deposited** — it's a credit added to your trading account that increases your buying power and potential profit, but is subject to specific rules about how it can be converted to withdrawable money, when it can be removed, and what trading behaviour around it is acceptable.

The bonus structure is one of the most common sources of trader confusion and complaints at any broker, including OPO. The terms are technical, the interactions with other policies are complex, and the consequences of misunderstanding can include losing the bonus, losing trading profits, or having the account flagged for [[Market Abuse Policy|abuse]].

The bonus structure is governed by the **OPO Bonus Programs document**, with cross-references to the Client Agreement.

## Important upfront: the governing-law issue

Before describing the bonus structure, one critical legal point to flag.

The **Bonus Programs document specifies Seychelles governing law** in clause 9.4. The **Client Agreement specifies SVG (Saint Vincent and the Grenadines) governing law** in clause 28.

This is a meaningful inconsistency:

| Document                 | Governing law |
| ------------------------ | ------------- |
| OPO Client Agreement v10 | SVG           |
| OPO Bonus Programs       | Seychelles    |

The practical implications are unclear. If a dispute arises specifically about a bonus, do Seychelles laws apply, or SVG laws? If a dispute crosses both areas, which governs? OPO has not publicly clarified this.

This has been flagged for compliance resolution. Traders should be aware that:
- Bonus-related disputes may face additional jurisdictional complexity compared to other disputes
- The [[Complaints Procedure]] in the Client Agreement may not directly apply to pure bonus disputes
- Any escalation of bonus disputes should clarify which jurisdiction's law applies

This is not a reason to avoid bonuses entirely, but it's something traders should know exists.

## What a bonus actually is

A bonus is **credit** added to your trading account that you can use to open positions. It has three important characteristics:

1. **It increases your available trading capital** — your [[Free Margin]] becomes larger
2. **It is NOT immediately withdrawable** — bonus credit cannot be taken out as cash until specific volume requirements are met (see [[Bonus Conversion and Volume Requirements]])
3. **It can be removed under specific conditions** — bonuses are conditional, not unconditional gifts (see [[Bonus Removal and Withdrawal Interactions]])

A typical bonus structure:

| Deposit | Bonus % | Bonus credit added | New trading capital |
|---|---|---|---|
| \$1,000 | 50% | \$500 | \$1,500 |
| \$5,000 | 100% | \$5,000 | \$10,000 |

The trader sees the bonus credit reflected in their [[Balance]] or as a separate bonus balance. They can use this capital to open positions just like real deposited funds. But the bonus comes with strings attached.

## How bonus credit interacts with your account

When you have an active bonus, several things happen to your account state:

### Balance display

OPO may display Balance as a single combined figure (deposit + bonus) or as two separate figures (Deposit Balance + Bonus Balance). The specific display depends on the platform and account type. Either way, the trader needs to know how much of their displayed Balance is actually theirs vs. broker credit.

### Margin and risk

For [[Margin]] calculations, both deposited funds and bonus credit count as part of [[Equity]] and [[Free Margin]]. This means:

- You can use bonus credit to open positions
- Bonus credit absorbs losses just like deposited funds
- [[Margin Level]] is calculated using total Equity, regardless of source

This is the appeal of bonuses — they expand your usable capital. But it's also the trap: losses on bonus-funded positions feel less painful than losses on deposited funds, leading some traders to take risks they wouldn't otherwise take.

### Withdrawal behaviour

When you request a withdrawal, the rules differ depending on what you're withdrawing:

- **Withdrawing deposited funds while bonus is active:** typically removes the bonus proportionally or entirely. See [[Bonus Removal and Withdrawal Interactions]]
- **Withdrawing converted bonus** (bonus credit that has met volume requirements and been converted to withdrawable status): treated as regular funds
- **Withdrawing unconverted bonus credit:** generally not possible — bonus credit cannot be withdrawn until conversion is complete

## The fundamental rule: bonuses are conditional

The most important thing to understand about OPO bonuses (and bonuses at any broker) is that they are **conditional credit, not unconditional money**. The conditions typically include:

1. **Volume requirements** — you must trade a specific number of lots before the bonus can be converted to withdrawable cash. This is the "turnover" requirement and is often the most restrictive condition
2. **Time limits** — bonuses sometimes have an expiry date by which volume must be reached
3. **Account type restrictions** — some account types (notably [[High Leverage Account]]s) are excluded from bonuses entirely
4. **Leverage restrictions** — the Bonus Programs document clause 2.11 specifies a maximum 1:500 leverage cap on any account with active bonus credit
5. **Trading behaviour restrictions** — abusive trading patterns trigger bonus removal
6. **Withdrawal restrictions** — withdrawing deposited funds typically forfeits the active bonus
7. **Bonus cap** — per clause 2.5, the maximum bonus amount is USD 2,000–2,500 depending on the promotion, cumulative across all of a client's accounts
8. **Stop Out equity exclusion** — per clause 2.12, bonus credit is excluded from equity during [[Stop Out]] calculations. This means Stop Out triggers based on your deposited funds, not the inflated bonus-inclusive balance

A trader who treats a bonus as "free money" without understanding these conditions will frequently lose either the bonus, the associated profits, or both.

## How OPO bonuses interact with other policies

The bonus structure interacts with multiple other policies in ways that traders should understand:

### Interaction with Negative Balance Protection

[[Negative Balance Protection]] applies to Retail Clients (Client Agreement clause 15.8). But the Bonus Programs document clause 2.6 introduces a complication:

> The Bonus will be removed if the Client's account Equity reaches the amount of the deposit. The Bonus will also be removed if the Client suffers losses equal to the amount deposited.

This intersects with NBP in a subtle way:

- If a trader's losses reach the amount deposited, the bonus is removed
- Once the bonus is removed, only the deposited amount can be lost further before NBP applies
- So the trader is protected from total catastrophic loss, but the bonus serves as a "first loss" buffer that absorbs adverse moves before the trader's own capital is at risk

In practice this means: bonus credit makes it look like you have more capital, but the broker's downside protection (NBP) only covers your deposited amount. The bonus is the first money to disappear in bad scenarios.

### Interaction with Market Abuse Policy

The [[Market Abuse Policy]] clause 35 applies to all clients including those with active bonuses. But the Bonus Programs document adds specific anti-abuse provisions targeting bonus-related schemes:

- Opening multiple accounts to claim the same bonus
- Coordinating with other traders to manipulate bonus volume requirements
- Using bonuses in patterns specifically designed to extract maximum value with minimum legitimate trading

A finding of bonus-specific abuse can result in:
- Bonus credit forfeiture
- Profits from bonus-funded trades forfeiture
- Account termination under Market Abuse Policy
- Permanent ban from future OPO bonus programs

### Interaction with Withdrawal Procedure

The [[Withdrawal Procedure]] interacts with active bonuses in ways many traders find surprising:

- Withdrawing deposited funds while a bonus is active typically removes the bonus
- The exact removal mechanism (proportional, full, or threshold-based) depends on the specific bonus terms
- Some bonuses are forfeited entirely on any deposit withdrawal
- The [[Withdrawal Procedure]] no-activity penalty (3-6% for deposit-then-withdraw without trading) may stack with bonus forfeiture

A trader who deposits, receives a bonus, doesn't trade much, then withdraws can face:
1. Bonus removal
2. No-activity penalty
3. Possible flagging for bonus abuse

The combination is particularly punitive.

### Interaction with Dormant Account Policy

If a trader has active bonus credit and the account becomes dormant (no trading for 6 months per [[Dormant Account Policy]]), the interaction is unclear:

- The dormant account fee (\$5/month) begins
- The bonus is typically removed when the account becomes dormant, but exact timing is not specified
- A trader with \$500 deposit + \$500 bonus who becomes dormant may find: bonus removed, \$500 deposit slowly drained by fees, account eventually closed

### Interaction with Leverage Adjustment Policy

The Bonus Programs document clause 2.11 caps leverage at 1:500 for accounts with active bonuses. This means:

- High Leverage account holders cannot have active bonuses (their leverage is dynamic up to 1:2000)
- Standard accounts at 1:1000 or 1:2000 are NOT eligible for bonuses (or must drop to 1:500 if they want to be)
- The [[Leverage Adjustment Policy]]'s scheduled and discretionary leverage reductions still apply normally — bonuses don't protect against them

## What bonuses are typically offered at OPO

The Bonus Programs document covers multiple bonus types. The specific types currently available may change — traders should consult the current promotions page on the OPO website. Common bonus categories:

| Bonus type | Trigger | Typical structure |
|---|---|---|
| Welcome / First Deposit | New client makes first deposit | Percentage of deposit, e.g. 50-100% |
| Deposit Bonus | Existing client makes additional deposit | Often smaller percentage than Welcome |
| Cashback | Trading volume reaches thresholds | Percentage of spread/commission returned |
| Referral / Affiliate | Trader refers another active trader | Per-referral payment |
| Contest / Promotion | Time-limited campaigns | Variable |

Each specific bonus has its own detailed terms. The general framework described in this note applies to all of them; the specifics vary.

## What traders should do before accepting a bonus

The bonus is optional — traders can decline. Practical guidance:

1. **Read the specific bonus terms in full.** Volume requirements, expiry dates, withdrawal interactions. Don't accept based on the headline percentage alone
2. **Calculate the volume requirement.** If the bonus requires 5 lots per \$1 of bonus to convert, ask: is that achievable for your trading style and timeframe?
3. **Confirm your account type and leverage are bonus-eligible.** High Leverage accounts and 1:1000+ leverage accounts may not qualify
4. **Plan for the withdrawal interaction.** If you might need to withdraw funds during the bonus period, calculate the cost of bonus forfeiture
5. **Don't increase position sizes based on the bonus.** Sizing positions to risk a fixed percentage of your *deposited* capital remains the safer approach
6. **Don't engage in bonus-arbitrage strategies.** Strategies designed to extract maximum bonus value will be flagged
7. **Decline if uncertain.** A bonus you don't fully understand is a trap, not an opportunity

## Risk warning

Bonuses are the single largest source of trader-broker disputes across the entire industry. The reasons are consistent: traders accept bonuses without understanding the volume requirements; traders attempt to withdraw funds during an active bonus period and lose the bonus; traders increase position sizes because the bonus makes their account look larger; traders engage in trading patterns the broker classifies as abusive. The Bonus Programs document gives OPO broad discretion to remove bonuses, confiscate associated profits, and terminate accounts for behaviour deemed abusive — and OPO is the initial judge of what constitutes abuse. The governing-law inconsistency between the Bonus Programs document (Seychelles) and Client Agreement (SVG) creates additional complexity for dispute resolution. Traders should treat any bonus as a conditional offer with significant strings attached, read all terms before accepting, and decline if the terms are unclear or if the volume requirements don't fit their trading style. Trading without a bonus is not worse than trading with a poorly-understood bonus — it's often better.

## Source

- OPO Bonus Programs document (all clauses)
- OPO Bonus Programs document, clause 2.6 (bonus removal on equity reaching deposit)
- OPO Bonus Programs document, clause 2.11 (1:500 maximum leverage with bonus)
- OPO Bonus Programs document, clause 9.4 (Seychelles governing law)
- OPO Client Agreement v10, clause 28 (SVG governing law)
- OPO Client Agreement v10, clause 15.8 (Negative Balance Protection)
- OPO Client Agreement v10, clause 35 (Market Abuse Policy)
- Last verified: 2026-05-12

## Internal review notes

- **CRITICAL: Governing law inconsistency.** The Bonus Programs document specifies Seychelles governing law (clause 9.4) while the Client Agreement specifies SVG (clause 28). These documents should be reconciled — either the Bonus Programs document should be amended to specify SVG law, or the relationship between the two documents should be explicitly documented. This is a real legal-jurisdiction issue that affects how bonus disputes would be resolved
- Confirm SVG-jurisdiction bonus rules apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. ASIC and other major regulators have specific bonus restrictions (some prohibit bonuses to retail clients entirely)
- Document the specific bonus types currently active at OPO — Welcome, Deposit, Cashback, Referral, others. Currently this is on the website but not consistently documented in legal documents
- Document specific volume requirements per bonus type — currently these vary by promotion and aren't centralized
- Document the specific bonus removal triggers more precisely — when exactly does "Client's account Equity reaches the amount of the deposit" trigger the removal? Is it at the moment Equity touches that level, or at a daily review? This affects how traders manage risk
- Clarify the interaction between bonus removal and Negative Balance Protection — the current language creates ambiguity about whether the bonus serves as "first loss" protection or whether it's separate from NBP
- Document the appeals process for bonus removal decisions — particularly when the trader disputes that abuse occurred
- Document whether bonus credits can be partially converted (e.g. half the volume requirement met) or only fully converted
- Document the time horizon for volume requirements — bonuses with multi-year volume requirements are effectively unconvertible for most traders
- Consider whether the OPO website should display bonus terms more prominently before clients claim bonuses

## Related topics

- [[Bonus Conversion and Volume Requirements]]
- [[Bonus Eligibility and Restrictions]]
- [[Bonus Removal and Withdrawal Interactions]]
- [[Negative Balance Protection]]
- [[Market Abuse Policy]]
- [[Withdrawal Procedure]]
- [[Dormant Account Policy]]
- [[Leverage Adjustment Policy]]
- [[Leverage]]
- [[High Leverage Account]]
- [[Client Categorization]]
- [[Complaints Procedure]]
- [[Account Types Overview]]
- [[Margin]]
- [[Free Margin]]
- [[Equity]]
- [[Balance]]