---
title: Bonus Eligibility and Restrictions
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

# Bonus Eligibility and Restrictions

## Simple explanation

Not every OPO client is eligible for every bonus. Bonus eligibility depends on the trader's **account type**, **chosen leverage tier**, **country of residence**, **client categorization**, and several other factors. Understanding eligibility before pursuing a bonus prevents the disappointment of accepting an offer and then discovering disqualification.

This note covers the eligibility framework. The mechanics of converting bonus credit to cash are in [[Bonus Conversion and Volume Requirements]]. The conditions under which a bonus can be removed are in [[Bonus Removal and Withdrawal Interactions]].

The eligibility rules are documented across the **OPO Bonus Programs document** and the website's individual bonus terms pages.

## Account type restrictions

Bonus eligibility varies significantly by account type. This is one of the most important upfront filters.

### Bonus-eligible account types (typical)

| Account type | Typically bonus-eligible? |
|---|---|
| [[Standard Account]] | Yes |
| [[ECN Account]] | Yes |
| [[ECN Pro Account]] | Generally yes — depending on bonus |
| [[Social Trade Account]] | Yes |
| [[Social Pro Account]] | Generally yes |
| [[Black Account]] | Variable — depending on tier |
| [[cTrader ECN Account]] | Variable |
| [[cTrader ECN Plus Account]] | Variable |
| [[cTrader Copy Account]] | Variable |

### Bonus-ineligible account types (explicit exclusions)

The Bonus Programs document clause 2.3 specifically excludes high-leverage accounts:

> The bonus is not available on the High Leverage account types: High Leverage Standard, High Leverage ECN, High Leverage ECN-PRO.

This means **any account configured with the dynamic high-leverage model is excluded from all standard bonuses**. A trader on a high-leverage account who wants to claim a bonus must either:

1. Open a separate standard-leverage account specifically for bonus-eligible trading
2. Request a downgrade from high-leverage to standard-leverage on their existing account (which has its own implications)

The trader cannot simply "switch off" the high-leverage configuration to temporarily claim a bonus.

## Leverage restrictions on bonus-eligible accounts

Even on bonus-eligible account types, the leverage tier affects eligibility. The Bonus Programs document clause 2.11 sets a hard cap:

> The maximum leverage available under any active bonus is 1:500.

This means:

- A trader with standard-leverage 1:500 or lower can have a bonus
- A trader with standard-leverage above 1:500 (e.g. 1:1000 or 1:2000) can qualify for a bonus if they request a reduction to 1:500 (per the Bonus Programs document)

The 1:500 cap is industry-typical and reflects the broker's risk management — bonuses combined with very high leverage create high-volatility exposure on the broker's book.

If a trader has an active bonus and somehow ends up with leverage above 1:500 (through a re-categorization, account upgrade, etc.), the consequences depend on the specific bonus terms. Typically:

- The bonus is removed automatically
- Any associated trading profits may be at risk
- The trader is notified through the dashboard

## Country and jurisdiction restrictions

Bonus availability varies by country in two ways:

### Restricted countries

Citizens or residents of countries on the [[Restricted Countries]] list cannot open accounts at OPO at all — therefore they cannot claim any bonus.

### Country-specific bonus availability

Even within accepted countries, specific bonuses may be unavailable in certain jurisdictions due to:

- Local regulations limiting promotional financial offers (common in EU, UK, Australia)
- Tax reporting complexities for the broker
- Anti-money-laundering risk concentrations
- OPO's commercial decisions about market focus

The OPO Bonus Programs document and individual bonus terms specify which countries each bonus is available in. The bonus claim page in the dashboard typically blocks ineligible countries automatically.

This is why a bonus advertised on the website might be unavailable when the trader actually tries to claim it — the geographic restriction filters in at the account level.

## Client categorization restrictions

[[Client Categorization]] also affects bonus eligibility:

| Categorization | Bonus eligibility |
|---|---|
| Retail Client | Generally eligible (default) |
| Professional Client | Generally eligible — may have different terms |
| Eligible Counterparty | Typically not eligible — institutional accounts |

Professional Clients sometimes see modified bonus terms compared to Retail Clients — different volume requirements, different multipliers, or different convertibility rules. The Bonus Programs document is less specific about Professional treatment, but the website's individual bonus terms typically clarify.

Eligible Counterparties (institutional accounts) are generally outside the bonus framework entirely.

## One bonus per client / per account

Most OPO bonuses are subject to one-claim-per-client restrictions. The general rules:

- **Welcome Bonus:** typically available once per client, on the first deposit. A trader who already claimed a Welcome Bonus cannot claim it again
- **Deposit Bonus:** sometimes available multiple times, sometimes limited to specific frequencies (one per month, one per quarter)
- **Cashback Bonus:** typically ongoing, accumulating based on trading volume
- **Referral Bonus:** typically unlimited but with per-referral caps

The "per client" framing matters — opening multiple accounts to claim Welcome Bonuses multiple times is one of the most common bonus-abuse patterns and triggers severe consequences under the [[Market Abuse Policy]] (including profit confiscation, account closure, and permanent bonus ban).

OPO uses several mechanisms to detect this:
- KYC data matching (same person, different account)
- IP address analysis
- Payment method matching (same card or bank account)
- Behavioural pattern detection across accounts

## Minimum deposit and KYC requirements

Per clause 2.2 of the Bonus Programs document, the **minimum deposit to qualify for any bonus is USD 100**. Deposits below this threshold are not eligible for bonus credit.

Per clause 2.13, **KYC verification must be completed before receiving a bonus**. Partially approved clients cannot claim or receive bonus credit.

## Deposit method restrictions

Some OPO bonuses include restrictions on the deposit method used to qualify:

- Cryptocurrency deposits often have different bonus terms than card or bank deposits
- Some bonuses exclude certain payment methods entirely (e.g. specific e-wallets)
- Bonus matching may apply per-deposit rather than cumulatively (so 10 × $100 deposits may not equal one $1,000 deposit for bonus purposes)

These restrictions are typically in each bonus's specific terms, not in the general Bonus Programs document.

## Time restrictions

Bonuses can also be time-restricted in two ways:

### Promotional period

Some bonuses are time-limited promotions — available for claim only during a specific window (e.g. a 30-day campaign). After the window closes, the bonus cannot be claimed even by eligible clients.

### Account age restrictions

Some bonuses (particularly Welcome Bonus types) are available only to:

- New clients (first deposit)
- Clients within a certain age range from registration
- Reactivating dormant accounts after a specific period

A trader who registers but doesn't deposit immediately may find the Welcome Bonus offer has expired by the time they actually fund the account.

## Stacking restrictions

Most OPO bonuses are not stackable — meaning if you have one active bonus, you typically cannot claim another simultaneously. The Bonus Programs document is somewhat permissive about this in general terms, but specific bonuses often explicitly state "not combinable with other offers."

In practice:

- Welcome Bonus and Deposit Bonus typically cannot stack
- Cashback and other bonus types may stack with deposit-based bonuses (cashback is typically considered separately)
- Promotional/contest bonuses are typically not stackable with standard offers

A trader who claims one bonus is generally locked out of others until the active bonus is converted, expires, or is removed.

## Trader behaviour restrictions

Beyond formal eligibility, several behavioural patterns make a trader ineligible for bonuses or trigger bonus removal:

### Multiple accounts / family / business linkages

OPO treats certain types of related accounts as a single client for bonus purposes:

- Multiple accounts opened by the same person
- Accounts opened from the same IP, household, or device
- Accounts using the same payment methods
- Accounts of family members who appear coordinated
- Business accounts with overlapping beneficial owners

A trader operating in any of these patterns may find their bonus claims rejected or reversed, even if technically each account is in a different name.

### Previous abuse findings

A trader who has been found to engage in [[Market Abuse Policy|abusive trading]] or bonus arbitrage in the past:

- May be permanently banned from future bonus offers
- May have existing bonus claims rejected
- May find that any new claims trigger immediate compliance review

This ban is typically permanent and not appealable through routine [[Complaints Procedure]].

### Recently closed accounts

A trader who closes an account and reopens later may face restrictions on claiming bonuses they previously had access to. This prevents "account churn" arbitrage where traders cycle through Welcome Bonuses.

## What to check before pursuing a bonus

Before deciding to claim a specific bonus, verify:

1. **Account type eligibility** — does your account type qualify?
2. **Current leverage tier** — is it 1:500 or lower?
3. **Country of residence** — is the bonus available in your country?
4. **First-time vs. repeat** — have you claimed this bonus before?
5. **Deposit method** — does your preferred deposit method qualify?
6. **Time window** — is the bonus still being offered?
7. **Stacking** — do you have other active bonuses?
8. **Trading history flags** — any previous compliance issues?

If any answer is uncertain, contact OPO support before depositing funds specifically to claim a bonus. Discovering ineligibility after deposit is significantly worse than confirming eligibility before.

## When eligibility appears ambiguous

Some traders fall into ambiguous categories where eligibility isn't immediately clear from the documentation:

**Multi-account traders:** A trader with multiple OPO accounts (some bonus-eligible, some not) may want to claim a bonus on the eligible account. The Bonus Programs document is unclear on whether having any high-leverage or otherwise ineligible accounts excludes all the trader's accounts from bonuses. Practical answer: typically the specific eligible account can still claim, but verify with support.

**Recently re-categorized clients:** A trader who recently moved from Retail to Professional (or vice versa) may face questions about which terms apply. The current categorization at the moment of claim is typically what governs.

**Account upgrade in progress:** A trader who has requested a high-leverage upgrade but hasn't been fully processed yet faces uncertainty. Generally, the actual account state at the moment of claim is what matters.

**Recently moved residents:** A trader who recently moved between countries may find the bonus offer changes during the move. Generally, current verified address is what governs.

In all ambiguous cases, the safest course is to contact OPO support, explain the situation, and confirm eligibility in writing before depositing or claiming.

## Risk warning

Bonus eligibility restrictions exist for legitimate reasons — they prevent abuse, ensure fairness, and protect both broker and client from excessive risk concentration. But the rules are complex and not always clearly documented. Traders who pursue bonuses without confirming eligibility risk depositing funds expecting a bonus that won't be granted, missing the opportunity to use those funds differently, or being flagged for attempting to claim ineligible bonuses. The high-leverage exclusion in particular catches many traders by surprise — a trader on a 1:1000 standard-leverage account or any high-leverage account is excluded from bonuses without realizing it until claim time. The 1:500 leverage cap forces traders to choose between maximum leverage and bonus eligibility. The safest approach is to confirm eligibility before depositing, treat ambiguous situations as ineligible until clarified, and never deposit funds specifically counting on a bonus until the bonus is confirmed available.

## Source

- OPO Bonus Programs document, clause 2.3 (high-leverage account exclusion)
- OPO Bonus Programs document, clause 2.11 (1:500 leverage cap)
- OPO Bonus Programs document (general eligibility provisions across all clauses)
- OPO website (individual bonus terms — current promotions)
- OPO Client Agreement v10, clause 5.9 (restricted countries)
- OPO Client Agreement v10, clause 4 (Client Categorization)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG/Seychelles jurisdictional bonus eligibility applies globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. Many regulators have strict bonus restrictions that may make most or all bonus types unavailable in certain jurisdictions
- Document the **specific country-by-country bonus availability list** — currently this is scattered across individual bonus terms pages. A single accessible reference would help traders confirm eligibility before depositing
- Document the **specific eligibility rules per current bonus type** at OPO — Welcome, Deposit, Cashback, Referral, others. The general framework is documented but specifics vary
- Document the **handling of multiple accounts under the same beneficial owner** — when do separate accounts share bonus history vs. when are they treated separately
- Document the **specific account-state restrictions during account changes** — what happens to a bonus if a trader is upgrading from Retail to Professional, changing leverage tier, or changing country of residence
- Confirm whether **bonuses can be "queued" until eligible conditions are met** — for example, can a trader who is currently on 1:1000 leverage claim a bonus that activates once they reduce to 1:500?
- Document the **specific timeline restrictions for re-claiming bonuses after account closure and re-opening** — currently unclear
- Document the **appeals process specifically for bonus eligibility decisions** — currently traders rely on general [[Complaints Procedure]], but bonus-specific procedures may be needed
- Consider implementing an **eligibility-check tool** in the OPO dashboard where traders can verify their bonus eligibility before depositing

## Related topics

- [[Bonus Programs Overview]]
- [[Bonus Conversion and Volume Requirements]]
- [[Bonus Removal and Withdrawal Interactions]]
- [[High Leverage Account]]
- [[Leverage]]
- [[Leverage Adjustment Policy]]
- [[Client Categorization]]
- [[Restricted Countries]]
- [[KYC and Account Activation]]
- [[Market Abuse Policy]]
- [[Account Types Overview]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Black Account]]
- [[Social Trade Account]]
- [[Complaints Procedure]]
- [[Withdrawal Procedure]]