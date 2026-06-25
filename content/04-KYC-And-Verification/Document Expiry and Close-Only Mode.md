---
title: Document Expiry and Close-Only Mode
status: draft
audience: client
category: KYC-And-Verification
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
# Document Expiry / Close-Only Mode

## Simple explanation

When KYC documents on your OPO account expire and aren't renewed within 15 days, your account is automatically moved into **Close-Only Mode**. In this state, you can close existing positions but cannot open new ones, cannot deposit funds, and cannot withdraw funds. The account is functional only for winding down what's already there.

Close-Only Mode is not a punishment — it's the broker's compliance-mandated response when it can no longer verify your identity or address. Recovery requires submitting fresh KYC documents and waiting for re-verification.

The mechanics are documented in Client Agreement clauses 20.6 through 20.9.

## How a trader ends up in Close-Only Mode

The most common path is document expiry without renewal:

1. **You opened the account** and submitted KYC documents (Proof of Identity, Proof of Address)
2. **Time passes.** Your ID approaches its expiry date. Your POA has been on file for years
3. **OPO notices** that one or more of your documents is about to expire (typically 30 days before)
4. **OPO requests renewed documentation** through the dashboard, email, or both
5. **15 days pass without your response** (Client Agreement clause 20.8)
6. **The account moves into Close-Only Mode** automatically

Other paths into Close-Only Mode include:

- **Address change without notification.** A trader who moves but doesn't update their POA may be flagged during routine compliance review
- **Discrepancy detection.** A compliance review identifies inconsistencies between submitted documents and account activity (e.g. unusual login locations, payment method changes)
- **Periodic re-verification cycles.** OPO may request fresh documentation periodically; failure to respond triggers Close-Only Mode
- **Sanctions screening updates.** If a new sanctions list match is detected for an existing client, the account can be moved to Close-Only pending review
- **Specific compliance investigations.** Where suspicious activity is being reviewed (potential market abuse, source-of-funds concerns)

## What "Close-Only Mode" actually means

The Client Agreement clause 20.7 specifies the restrictions:

> Where the Client fails to provide updated identification or supporting documents within fifteen (15) calendar days of OPO GROUP LLC.'s request, the Client's Trading Account shall be placed in Close-Only mode, during which the Client may only close existing Open Positions and shall not be permitted to open new positions, place new Pending Orders, deposit funds, or withdraw funds.

In plain terms, in Close-Only Mode:

| Action | Allowed in Close-Only Mode? |
|---|---|
| Close existing open positions (manual close) | Yes |
| Modify Stop Loss or Take Profit on open positions | Yes |
| Receive automatic position closure (Take Profit, Stop Loss, Stop Out triggering) | Yes |
| Login to platform | Yes |
| View market quotes | Yes |
| Open new positions | **No** |
| Place new pending orders | **No** |
| Deposit funds | **No** |
| Withdraw funds | **No** |
| Modify existing pending orders | Generally no (closure only) |
| Add to existing positions | **No** |

The account becomes a holding pen — you can manage what's there, but you cannot grow it, fund it, or exit funds from it.

## The 15-day grace period

The 15-day window in clause 20.8 is firm. From document expiry plus 15 days, the account moves to Close-Only.

**Day counting:**
- Day 0: OPO sends the request for renewed documentation (or the expiry date passes, whichever is later)
- Day 15: deadline for trader response
- Day 16: account moves to Close-Only Mode

**What counts as a response:**
- Submitting renewed documents through the dashboard
- Explicit communication with support acknowledging the request and committing to a timeline (though this doesn't necessarily stop the clock — depends on OPO's discretion)

**What does NOT count as a response:**
- Logging in to the platform without uploading documents
- Continuing to trade actively (this is irrelevant to the document status)
- Email correspondence with support that doesn't include document submission

## Getting out of Close-Only Mode

To exit Close-Only Mode and restore full account access:

1. **Submit the renewed documentation** through the OPO dashboard or as instructed by support
2. **Wait for OPO review** — typically 1–7 business days, similar to initial KYC
3. **Account is restored to full status** once verification completes

The Client Agreement clause 20.9 specifies:

> Upon receipt and successful verification of all updated identification documents, OPO GROUP LLC. shall restore full Trading Account functionality.

Things that can extend the recovery timeline:

- Submitting incomplete or unclear documentation (each round of clarification adds days)
- Submitting documents from a higher-risk jurisdiction
- Document discrepancies requiring additional review
- High volume periods at OPO compliance (e.g. end of fiscal periods)

## Why this catches traders by surprise

Three common patterns produce surprise Close-Only Mode situations:

### Pattern 1: The forgotten expiry

A trader opens an account in their late 20s using a passport that expires when they turn 30. Five years later, the passport has been expired for over a year, the trader hasn't received OPO emails (or they went to spam), and one Monday morning the trader can't open a position. The trader hasn't done anything wrong — they just forgot.

Protection: when you submit any document, note the expiry date in a calendar and set a reminder 60 days before.

### Pattern 2: The moved trader

A trader moves to a different city or country. They update their address in the OPO dashboard but don't submit a new POA. Months later, compliance reviews their account and notices the POA on file shows an address inconsistent with login locations. The account is moved to Close-Only pending updated POA.

Protection: when you move, submit fresh POA documents within 30 days of the move, even if you haven't been asked.

### Pattern 3: The infrequent trader

A trader uses the account regularly for a year, then stops trading for two years. During the inactive period, both ID and POA expire. When the trader returns to the platform, ready to trade, they discover the account is in Close-Only Mode (sometimes with no open positions to close, meaning the account is effectively frozen pending document renewal).

Protection: even when not actively trading, periodically check document status and renew as needed.

## What happens if you ignore Close-Only Mode indefinitely

If a trader never responds to the documentation request and never submits renewed KYC:

1. **The account remains in Close-Only Mode** — all trading restrictions apply
2. **Open positions can still trigger Stop Loss, Take Profit, or Stop Out** as normal market activity
3. **Funds remain in the account** but inaccessible (no withdrawals possible without verification)
4. **Dormant account fees may begin** if no trading activity for 6 months (see [[Dormant Account Policy]]) — these can drain the account over time
5. **After 60 days, OPO may begin account closure procedures** under Client Agreement clause 20.8, which provides a 60-day timeline after which the account may be terminated

The combination of Close-Only Mode + dormant account fees is particularly dangerous: a frozen account that's slowly being drained, and the trader can't withdraw the remaining balance without first completing fresh KYC.

## How Close-Only Mode interacts with other policies

| Policy | Effect in Close-Only Mode |
|---|---|
| [[Margin Call]] / [[Stop Out]] | Still trigger as normal — positions can be forcibly closed |
| [[Force Majeure]] | All Force Majeure provisions still apply |
| [[Swap]] charges | Continue to accrue on open positions |
| [[Dormant Account Policy]] | Fee accrual begins if 6 months of no activity |
| [[Bonus Programs]] | Bonus credits typically removed or frozen |
| [[Withdrawal Procedure]] | Withdrawals are blocked entirely until exit from Close-Only |

A trader in Close-Only Mode with open losing positions and no way to deposit additional funds can find themselves stopped out of all positions during a volatile event, with no way to take any preventive action like adding capital. This is the worst-case scenario and is preventable through routine document renewal.

## Practical guidance

1. **Track document expiry dates.** When you upload an ID or POA, immediately add the expiry date to your calendar with a 60-day-prior reminder
2. **Renew proactively.** Submit renewed documents 30 days before expiry, not after
3. **Update address proactively.** When you move, submit fresh POA within 30 days
4. **Don't ignore compliance emails.** OPO compliance messages may go to spam — check periodically
5. **Maintain access to the email registered with your account.** A trader who loses access to their registration email can't receive renewal requests
6. **Keep document recovery accessible.** If your ID is being renewed and there will be a gap, contact OPO support before the existing document expires to coordinate
7. **If you stop trading temporarily, withdraw funds.** A small remaining balance in a Close-Only account that goes dormant can be drained by fees

## Risk warning

Close-Only Mode is a particularly disruptive state because it removes the trader's ability to manage their account exposure in either direction. A trader with open positions in Close-Only Mode cannot add to winning trades, cannot deposit to cover margin pressure, and cannot withdraw profits. If market conditions move against open positions, the only available response is closing them — at whatever price the market offers. The 15-day grace period from document expiry to Close-Only is firm and not extended for travel, illness, or other circumstances. Traders should treat document maintenance as a continuous account hygiene task, not a one-time onboarding event. The combination of Close-Only Mode and accumulated dormant account fees (after 6 months of inactivity) can quietly drain a forgotten account to zero, with no way for the trader to take corrective action without first completing fresh KYC verification.

## Source

- OPO Client Agreement v10, clauses 20.6–20.9 (Document Status and Close-Only Mode)
- OPO Client Agreement v10, clause 20.7 (Close-Only Mode definition and restrictions)
- OPO Client Agreement v10, clause 20.8 (15-day grace period)
- OPO Client Agreement v10, clause 20.9 (account restoration after verification)
- OPO Client Agreement v10, clause 27 (account termination)
- OPO Client Agreement v10, clause 9.11 (dormant account fee)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction Close-Only provisions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. Some jurisdictions have stricter rules about advance notice required before restricting account access
- Confirm whether OPO sends advance notification (and how many days before document expiry) — the Client Agreement is silent on advance notice, only specifying the 15-day grace period from request. Best practice would be 60-day advance notice via multiple channels
- Document specific situations where the 15-day grace period might be extended (e.g. trader in hospital, trader in country with passport renewal delays, etc.) — currently no exception process is documented
- Confirm whether traders can request voluntary Close-Only mode (for example, to prevent additional trading during a planned absence). Some brokers allow this; OPO documentation is silent
- Document the specific compliance review timeline after document submission — currently described generically as "review process" but traders need to know whether to expect days or weeks
- Confirm whether dormant account fees accrue during Close-Only Mode or are paused. The Client Agreement is silent on this interaction
- Confirm whether bonus credits are removed immediately upon entry to Close-Only Mode, or only after a specified period
- Consider whether the OPO dashboard should display upcoming document expiry dates prominently — many traders would benefit from this

## Related topics

- [[KYC and Account Activation]]
- [[Client Categorization]]
- [[Restricted Countries]]
- [[Dormant Account Policy]]
- [[Withdrawal Procedure]]
- [[Margin Call]]
- [[Stop Out]]
- [[Force Majeure]]
- [[Bonus Programs]]
- [[Complaints Procedure]]
- [[Open Position]]
- [[Pending Order]]


