---
title: Swap Free
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
# Swap Free

## Simple explanation

A Swap-Free account (sometimes called an "Islamic account") is an account configuration where positions held overnight do **not** incur the daily [[Swap]] charge. It exists primarily to accommodate traders whose religious beliefs (most notably Islamic law, which prohibits earning or paying interest — "riba") prevent them from participating in interest-based transactions.

OPO offers Swap-Free options on certain account types, with specific conditions and limitations described in the Client Agreement clause 34.

## Who Swap-Free is for

Swap-Free accounts exist for three main groups:

1. **Muslim traders** observing Islamic finance rules that prohibit riba (interest)
2. **Traders holding positions for extended periods** who want to avoid cumulative swap costs regardless of religious considerations
3. **Position traders** who would otherwise face significant swap drag on their strategies

Important: Swap-Free is **not free trading**. The broker still earns through [[Spread]] and [[Commission]] — only the overnight interest mechanism is removed. Traders sometimes assume Swap-Free means "no overnight cost at all" — this is incorrect.

## How Swap-Free works at OPO

The Client Agreement clause 34.1 sets out the operating model. Two key points:

### Eligibility

Swap-Free is typically activated by request on existing accounts after a minimum balance threshold is met (the website specifies $30,000+ for ECN Pro accounts, but this varies by account type — confirm with OPO support). The exact eligibility criteria are not consistently documented across OPO's materials.

### Swap-Free is not unconditional

The Client Agreement clause 34.1(b) introduces an important caveat:

> the Swap Free charge for all positions open as these may be defined and/or issued by OPO GROUP LLC. from time to time (inclusive of the day of the position is opened and/or closed) and as such charges and duration is provided within the Contract Specifications for Swap Free Accounts section on the Website.

This means: OPO may apply a **flat administrative charge** as a substitute for swap, particularly on positions held beyond a certain duration. This isn't called "swap" formally, but functionally it's a similar fee. The agreement gives OPO discretion over the amount, the affected instruments, and the duration before charges kick in.

In practice, many Swap-Free accounts at most brokers operate this way: truly free for the first few days, then a flat administrative fee applies if positions are held longer. Check the Contract Specifications for OPO's specific Swap-Free fee schedule.

## What OPO prohibits on Swap-Free accounts

The Client Agreement clause 34.1(a) is explicit about behaviour that triggers consequences:

> If OPO GROUP LLC. suspects any fraud, manipulation, swap-arbitrage or other forms of deceitful or fraudulent activity in a Client's account(s) or otherwise related or connected to any and/or all Transactions, then OPO GROUP LLC. reserves the right, at its sole discretion, to close all open positions in the Client's Trading Account and deduct or add a penalty (equivalent to the swap and/or any profit amount) for all Transactions made in the account(s) and decline from accepting any further requests from the Client to be exempted from any swaps;

In plain terms: OPO is watching for traders who open Swap-Free accounts specifically to exploit the swap structure (e.g. holding negative-swap pairs that would normally cost them, getting them for free). If detected, the broker can:

- Close all positions
- Deduct a penalty equivalent to the swap that would have been charged
- Add a penalty equivalent to any profit gained from this practice
- Remove the trader's Swap-Free status permanently
- Deny future Swap-Free applications

This is called "swap arbitrage" in the industry, and it's considered abuse by virtually every broker offering Swap-Free accounts.

## Swap-Free vs standard accounts — what changes

| Feature | Standard Account | Swap-Free Account |
|---|---|---|
| Overnight cost on most positions | [[Swap]] charged/credited | None or flat fee |
| Wednesday triple charge | Yes | No (replaced by flat fee structure) |
| Maximum hold duration | Unlimited | Limited or fee-bearing |
| Risk of swap-arbitrage allegations | None | Yes — strict broker monitoring |
| Religious compliance | No | Yes (designed for Islamic finance) |
| Bonus eligibility | Yes | Same as standard (unless high-leverage tier) |
| Spread/Commission | Same as standard tier | Same as standard tier |

## OPO's discretion

The Client Agreement clause 34.1(c) gives OPO broad authority to change Swap-Free terms:

- Amend the Swap-Free charge amount at any time
- Amend which instruments are eligible
- Discontinue the swap-free account without warning to the Client

So Swap-Free is not a permanent contractual right — it's a discretionary feature OPO can modify or remove. Traders relying on Swap-Free for strategy planning should be aware that this can change.

## Clearly erroneous orders on Swap-Free accounts

Clause 34.2 adds an additional protection (for OPO) specific to Swap-Free accounts:

> In the event that OPO GROUP LLC. determines, in its sole discretion, that an Order(s) submitted by the Client is clearly erroneous, OPO GROUP LLC. reserves the right to disable the relevant account of the Client to Close Only Mode.

A "clearly erroneous order" is defined as an order placed at a price substantially different from the prevailing market. If detected, the account is moved to Close-Only mode — meaning no new positions, only closing existing ones. This is meant to prevent exploitation but means Swap-Free traders face additional scrutiny on order placement.

## How to apply for Swap-Free at OPO

The exact application process is not fully documented in the Client Agreement or on the public account pages. Based on standard industry practice and clauses 34.1(b)–(c), the process typically involves:

1. Submitting a request through the OPO dashboard or to customer support
2. Providing documentation supporting eligibility (for religious-grounds requests, this may include a written declaration)
3. Acknowledging the Swap-Free terms including the flat-fee structure
4. Awaiting OPO's approval at their discretion

Traders should contact OPO support directly for the current application process and eligibility criteria.

## Risk warning

Swap-Free is not a license to hold positions indefinitely without cost. The flat-fee structure can accumulate over long holds, and aggressive use of the feature to capture positive-swap-equivalent positions is monitored as potential swap-arbitrage. OPO retains broad discretion to apply penalties, close positions, and remove Swap-Free status if abuse is suspected — and the Client Agreement places the determination of abuse at OPO's "sole discretion." Traders should treat Swap-Free as a religious accommodation feature with strict usage expectations, not as a swap-replacement strategy. Position traders who simply want to avoid swap costs (without religious considerations) should carefully weigh the Swap-Free flat fee against actual swap charges over their typical hold periods — Swap-Free is not always cheaper for non-religious users.

## Source

- OPO Client Agreement v10, clause 34.1 (Swap-Free Account terms)
- OPO Client Agreement v10, clause 34.1(a) (anti-arbitrage provisions)
- OPO Client Agreement v10, clause 34.1(b) (Swap-Free charges)
- OPO Client Agreement v10, clause 34.1(c) (right to modify or discontinue)
- OPO Client Agreement v10, clauses 34.2–34.5 (clearly erroneous orders on Swap-Free)
- OPO website account type pages (Swap-Free availability mentioned for ECN Pro at $30,000+)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction Swap-Free terms apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- **Document the Swap-Free application process explicitly.** This is not currently visible to traders before they open an account, which is a friction point — religious-grounds traders especially benefit from upfront clarity
- Confirm the actual Swap-Free fee schedule referenced in clause 34.1(b) — what's the typical "free duration" and what's the flat fee after that
- Confirm which account types offer Swap-Free at OPO and the eligibility threshold for each
- Confirm whether Swap-Free accounts can hold bonus credits (Bonus Programs documents are silent on this interaction)
- Consider publishing an "Islamic Account FAQ" as a separate note in 04-KYC-And-Verification or a new dedicated folder, since the documentation around this is currently scattered

## Related topics

- [[Swap]]
- [[Long Position]]
- [[Short Position]]
- [[Open Position]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Social Trade Account]]
- [[Spread]]
- [[Commission]]
- [[Contract Specifications]]
- [[Carry Trade]]
- [[Margin Call]]