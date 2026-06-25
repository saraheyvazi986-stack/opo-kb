---
title: Title Transfer Collateral Arrangement
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

# Title Transfer Collateral Arrangement

## Simple explanation

A Title Transfer Collateral Arrangement (TTCA) is a legal mechanism where a client transfers **ownership** of their funds to the broker, rather than simply depositing those funds for the broker to hold on their behalf. Under TTCA, the funds become the broker's property, and the client holds a contractual claim against the broker for the equivalent value — but no longer owns the actual cash.

This is a meaningful legal distinction. In a normal client-money arrangement, your funds remain your property held by the broker in segregated accounts. In TTCA, the funds are the broker's assets, and you are an unsecured creditor.

**TTCA is excluded by default for Retail Clients** under OPO's Client Agreement. It can apply to Professional Clients and Eligible Counterparties.

The arrangement is documented in Client Agreement clause 6.15.

## What "ownership" means in this context

To understand TTCA, it helps to contrast two ways a broker can hold client funds:

### Segregated client money (standard for Retail Clients)

Under normal client money rules:

- The client deposits funds with the broker
- The broker holds those funds in **segregated accounts** — separate from the broker's own operating accounts
- The funds legally remain the client's property
- If the broker goes bankrupt, the client funds are not part of the broker's assets and are returned to the clients (subject to regulatory protections that vary by jurisdiction)

This is the standard treatment for Retail Clients and is required by virtually all major financial regulators.

### Title Transfer Collateral Arrangement (TTCA)

Under TTCA:

- The client deposits funds with the broker
- **Ownership of the funds transfers to the broker** — they're no longer the client's property
- The broker holds the funds as their own assets, mixed with broker capital
- The client receives a contractual claim against the broker for the equivalent value
- If the broker goes bankrupt, the client is an **unsecured creditor** alongside other creditors, and may recover little or nothing depending on the broker's remaining assets

This is a much weaker protection for the client. It exists because some sophisticated client relationships (institutional, large-balance professionals) benefit operationally from broader collateral usage.

## What OPO's Client Agreement says

Clause 6.15 establishes the framework:

> Any funds, assets or other property held by OPO GROUP LLC. in the Client's name shall not be subject to a Title Transfer Collateral Arrangement (TTCA), unless the Client has been categorized as a Professional Client or Eligible Counterparty.

Two important provisions in this clause:

1. **Retail Clients are excluded by default.** Funds belonging to Retail Clients are not subject to TTCA, period. This is one of the protections that comes with [[Client Categorization|Retail Client status]]
2. **Professional and Eligible Counterparty clients may be subject to TTCA.** TTCA applies if the client is categorized as a Professional Client or Eligible Counterparty per clause 6.15 — it does not require a separate written agreement beyond the client categorization itself

## Why TTCA exists in financial services

TTCA arrangements exist because they offer operational advantages for both parties in certain circumstances:

**For the broker:**
- Funds can be used as part of the broker's operating capital
- More efficient hedging and risk management across pooled assets
- Reduced regulatory capital requirements in some jurisdictions
- Simpler reconciliation processes

**For sophisticated clients:**
- Often associated with reduced fees or improved pricing terms
- Faster settlement on certain transactions
- More flexible margin and collateral usage
- Access to certain prime brokerage services

For institutional and very-high-net-worth clients, the trade-off can be worthwhile. For retail traders, the loss of fund ownership protection vastly outweighs any operational benefit.

## What happens if the broker goes bankrupt

This is the scenario that makes TTCA matter most.

### Without TTCA (Retail Client standard)

If OPO went bankrupt, Retail Client funds in segregated accounts would generally be:
- Identified as client funds, not broker funds
- Returned to clients ahead of broker creditors
- Protected to some degree by SVG regulatory framework
- Subject to certain administrative deductions for bankruptcy proceedings

The exact protection depends on SVG insolvency law and what additional protections (compensation schemes, etc.) exist in the trader's jurisdiction. For SVG specifically, retail protection is more limited than in major regulated markets, but the principle of segregation still applies.

### Under TTCA (Professional/EC by explicit agreement)

If OPO went bankrupt with TTCA funds:
- The TTCA funds are the broker's assets
- The client has only a contractual claim against the broker
- The client is an unsecured creditor in the bankruptcy proceedings
- Recovery depends entirely on what assets the broker has after secured creditors (banks, taxes, etc.) are paid
- Historical broker bankruptcies have produced recoveries from 0% to 80% for unsecured creditors, with most clustering at the low end

This is the meaningful protection that Retail Client status preserves and TTCA gives up.

## How traders end up in TTCA

The only way a trader becomes subject to TTCA at OPO, per clause 6.15, is:

1. The trader is categorized as Professional Client or Eligible Counterparty (see [[Client Categorization]])
2. The trader **explicitly agrees in writing** to TTCA treatment

This means TTCA cannot be applied to a Retail Client by surprise. The combination of categorization upgrade and explicit TTCA agreement is required.

In practice:

- A Retail Client cannot be put under TTCA without first upgrading to Professional
- Professional upgrade requires meeting specific criteria (see [[Client Categorization]])
- Even after upgrade, TTCA requires a separate written agreement

So protecting Retail Client status is the primary protection against TTCA. A trader who never upgrades from Retail will never be subject to TTCA at OPO.

## Why this matters even if you're staying Retail

Three reasons every trader should understand TTCA, even those who plan to remain Retail:

### 1. Understanding what you're protecting

Knowing that Retail Client status protects against TTCA helps you understand why staying Retail matters. The protections aren't just abstract regulatory language — they have concrete meaning for what happens to your money in stressful scenarios.

### 2. Recognizing professional upgrade pitches

When a broker offers Professional Client status (or "VIP," "Premium," etc.), one of the things you're being asked to give up — sometimes implicitly — is the TTCA exclusion. If the upgrade documentation mentions TTCA, collateral arrangements, or "title transfer," that's a flag to read carefully and probably decline.

### 3. Understanding broker risk

Even for Retail Clients, the broker holding your funds matters. If OPO had a financial crisis, the segregation of Retail Client funds is the primary protection. Understanding the legal framework helps you assess broker risk more accurately.

## What Retail Clients should not do

The protection works only if you maintain the conditions for it. Practical guidance:

1. **Don't upgrade to Professional unless you genuinely need it.** The marginal benefits (slightly higher leverage, marginal product access) rarely outweigh the lost protections
2. **If you're offered an upgrade, ask specifically about TTCA and segregation.** A broker that doesn't clearly explain these is one to be cautious of
3. **Read the categorization documentation carefully.** Some brokers bundle TTCA agreement into the categorization upgrade documents, so a trader signing the upgrade form is also agreeing to TTCA without realizing
4. **If you're Professional or Eligible Counterparty, TTCA may apply to you under clause 6.15.** Verify your TTCA status with OPO support if uncertain

## How TTCA interacts with other policies

| Policy | Retail (no TTCA) | Professional + TTCA |
|---|---|---|
| [[Negative Balance Protection]] | Applies (CA 15.8) | Not automatic |
| Fund segregation | Yes | No — broker owns funds |
| Broker insolvency outcome | Client funds returned | Unsecured creditor claim |
| Daily account management | No practical difference | No practical difference |
| Margin calculation | Standard | Standard |
| Withdrawal rules | [[Withdrawal Procedure]] standard | [[Withdrawal Procedure]] standard |

For day-to-day trading, TTCA looks identical to non-TTCA. The difference only manifests in bankruptcy or other extreme scenarios. This is what makes TTCA so easy to agree to without understanding — there's no visible day-to-day cost.

## Risk warning

Title Transfer Collateral Arrangement is one of the most consequential things a trader can agree to, and one of the easiest to agree to without realizing. Under TTCA, you no longer own your trading funds — they become the broker's assets, and you become an unsecured creditor. If the broker faces financial difficulty or insolvency, TTCA funds are part of the broker's assets to be distributed to creditors, and your recovery can range from nothing to most of the balance depending on the broker's situation. Retail Client status excludes you from TTCA by default at OPO — protecting that status is the primary protection. Be skeptical of any documentation upgrading you out of Retail status, and read carefully for any mention of "title transfer," "collateral arrangement," or similar language. If you don't understand exactly what fund-holding arrangement you're agreeing to, do not sign — ask OPO support to clarify in plain language first.

## Source

- OPO Client Agreement v10, clause 6.15 (Title Transfer Collateral Arrangement)
- OPO Client Agreement v10, clause 4 (Client Categorization framework)
- OPO Client Agreement v10, clause 4.5 (Retail default)
- OPO Client Agreement v10, clause 15.8 (Negative Balance Protection — also Retail-only)
- OPO Client Agreement v10, clauses 6.1–6.14 (general fund-holding provisions)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction TTCA provisions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. TTCA treatment varies significantly across jurisdictions — EU MiFID II in particular has strict rules limiting when TTCA can apply
- Confirm OPO's actual operational practice — is TTCA actually offered to any clients, or is it purely a contractual provision that hasn't been activated?
- If TTCA is operationally available, document the specific written agreement process — what document does a Professional Client sign to enter TTCA, and what specific disclosures are required
- Document the fund segregation practices OPO applies for Retail Clients — which banks are funds held with, what insurance or compensation arrangements apply, what the operational segregation looks like
- Document any historical OPO insolvency proceedings or near-misses, if any, that demonstrated how funds were actually handled. Most brokers haven't experienced this, but the documentation should be ready
- Clarify the interaction between TTCA and [[Negative Balance Protection]] for Professional Clients — both protections may apply or be lost together; the relationship should be explicit
- Document the specific disclosures provided when a client upgrades from Retail to Professional Client — does the upgrade documentation explicitly mention TTCA risk, or is this an additional separate agreement
- Consider whether the OPO website should make the Retail/Professional distinction (and the TTCA exclusion) more prominent in onboarding and during any upgrade flows

## Related topics

- [[Client Categorization]]
- [[Negative Balance Protection]]
- [[Withdrawal Procedure]]
- [[Force Majeure]]
- [[Complaints Procedure]]
- [[Account Types Overview]]
- [[KYC and Account Activation]]
- [[Bonus Programs]]