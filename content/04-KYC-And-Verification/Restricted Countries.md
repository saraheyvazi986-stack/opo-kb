---
title: Restricted Countries
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
# Restricted Countries

## Simple explanation

OPO does not provide services to residents of certain countries. The list of restricted countries varies depending on which OPO document you consult — and the documentation is currently inconsistent. Citizens and residents of restricted countries cannot open accounts, cannot trade, and may have existing accounts closed if their residency is later identified as restricted.

This is governed by Client Agreement clauses 5.9 and 5.10. **There is a known inconsistency between these clauses, the website footer, and the actual list applied during account opening — flagged for compliance resolution.**

## Why brokers restrict countries

Brokers restrict service to specific jurisdictions for several reasons:

1. **Regulatory prohibition.** Some countries prohibit residents from trading CFDs or forex through unlicensed foreign brokers. Offering services to those residents would expose the broker to legal liability in that country
2. **Sanctions compliance.** International sanctions lists (UN, US OFAC, EU, UK) prohibit financial services to certain jurisdictions or to persons in those jurisdictions
3. **Licensing gaps.** Some countries require local licensing the broker doesn't hold. OPO operating under SVG license cannot legally offer services where SVG-licensed status isn't recognized
4. **Risk concentration.** Brokers may restrict countries with high fraud rates, high regulatory complaints, or operational difficulties (payment processing, KYC verification, dispute resolution)
5. **Tax reporting obligations.** Countries with strict tax reporting requirements (FATCA, CRS variations) may be operationally difficult to serve

## What the Client Agreement says

The Client Agreement v10 contains two clauses that address restricted countries, and they specify different lists. This is one of the open issues flagged for compliance resolution.

### Clause 5.9

> OPO GROUP LLC. shall not provide the services to the residents of certain countries, such as United States of America (USA), Japan, Australia, and Canada or to the residents of any other country which the Company at its sole discretion considers as restricted from time to time.

This clause lists four countries:
- United States of America (USA)
- Japan
- Australia
- Canada

### Clause 5.10

> The Client warrants and represents that he/she is not a citizen or resident of any country which the Company at its sole discretion considers as restricted from time to time.

This clause acts as the trader's representation — the trader confirms they are not from a restricted country. It does not enumerate a specific list, deferring to OPO's discretion.

### The OPO website footer

The website typically lists restricted countries in its footer or terms section. The list observed includes:
- Turkey
- United States of America (USA)
- Japan
- Canada
- North Korea

This list differs from clause 5.9 by:
- **Adding** Turkey and North Korea
- **Removing** Australia

### The inconsistency

A trader trying to determine whether they can open an account at OPO faces conflicting information depending on which document they read:

| Source | USA | Japan | Australia | Canada | Turkey | North Korea |
|---|---|---|---|---|---|---|
| CA Clause 5.9 | Restricted | Restricted | Restricted | Restricted | Not listed | Not listed |
| CA Clause 5.10 | (defers to discretion) | (defers to discretion) | (defers to discretion) | (defers to discretion) | (defers to discretion) | (defers to discretion) |
| Website footer | Restricted | Restricted | Not listed | Restricted | Restricted | Restricted |

The reality is that OPO applies one operational list during account opening — but which document accurately reflects that operational list is currently unclear.

## What "restricted" actually means in practice

For residents of a restricted country, the practical consequences:

**At account opening:**
- Account application may be rejected automatically based on declared country
- Some applications proceed through registration but block at KYC verification
- Documents from restricted-country issuers are flagged during compliance review

**After account opening (if restricted residency is detected):**
- Account moved to Close-Only Mode pending review
- Open positions may be closed
- Withdrawals may be processed back to original deposit methods (with anti-money-laundering verification)
- Account may be terminated under Client Agreement clause 27

**The Client Agreement clause 5.10 places the burden on the trader:**

> The Client warrants and represents that he/she is not a citizen or resident of any country which the Company at its sole discretion considers as restricted from time to time.

This means: if you open an account from a restricted country (or move to one later), and OPO later discovers this, you've breached your representation. The consequences include all of the above, plus potential confiscation of profits as misrepresentation under clause 27.2.

## Dual citizenship and residency complications

Many traders have complex citizenship or residency situations that don't map cleanly to "is this country restricted":

**Dual citizens of restricted and unrestricted countries:**
- Generally, the country of *residence* is what matters, not citizenship
- A US citizen who genuinely lives in (e.g.) Germany may be able to open an account based on German residency
- However, US citizens specifically face additional complications due to FATCA reporting obligations
- Each broker handles this differently; OPO's specific policy needs verification

**Residents of unrestricted countries with citizenship in restricted countries:**
- Documentation typically focuses on POA showing current residence
- Trader should be prepared to explain the discrepancy if questioned during compliance review

**Recent movers:**
- A trader who recently moved from a restricted to an unrestricted country must update their account information promptly
- The POA showing the new address is essential

**Long-term travelers and digital nomads:**
- Tax residency may differ from physical location at any moment
- OPO will typically use tax residency for restriction purposes

## Why the United States in particular is restricted

US residents are restricted at OPO (and most similar offshore brokers) for specific reasons that go beyond general restriction lists:

1. **The Dodd-Frank Act** requires brokers serving US clients to register with the CFTC and meet US-specific regulatory standards. OPO is not so registered
2. **FATCA reporting** requires extensive ongoing reporting on US clients' accounts to the IRS. The compliance overhead is substantial
3. **US dispute resolution and class action exposure** is significantly more litigation-heavy than other jurisdictions. Many offshore brokers explicitly avoid US clients to avoid this exposure
4. **The CFTC's enforcement reach** extends extraterritorially in ways that create real risk for non-US-licensed brokers offering services to US persons

For these reasons, "US residents cannot open accounts" is essentially universal among offshore brokers, regardless of the specific listed reason.

## Why Japan is restricted

Japan has specific financial services regulations (Financial Instruments and Exchange Act) that require local licensing for FX/CFD brokers. Foreign brokers without Japanese licenses cannot legally solicit Japanese residents. This is a hard restriction — Japan actively pursues unlicensed operators.

## Why Turkey appears on some lists

Turkey has implemented specific regulatory measures restricting Turkish residents from trading with unlicensed foreign brokers. The Capital Markets Board of Turkey (SPK) has taken enforcement actions against unlicensed FX/CFD providers serving Turkish clients.

This is why the website footer adds Turkey to the restricted list — likely reflecting recent operational reality. The Client Agreement clause 5.9 may simply be outdated and not yet updated to reflect this change.

## What this means for traders

Three categories of trader concerns:

### "Am I allowed to open an account at OPO?"

Check the most current operational list, which is best determined by:
1. The country selection dropdown during account registration (most authoritative)
2. The OPO website footer or restricted countries page (operational current state)
3. OPO customer support direct confirmation
4. The Client Agreement clauses 5.9 and 5.10 (legal foundation)

If any of these sources lists your country as restricted, the practical answer is no.

### "I moved to a restricted country. What now?"

Notify OPO promptly:
1. Update your address in the dashboard
2. Submit POA showing the new address
3. Contact support to ask about the implications
4. Understand that the account may move to Close-Only Mode pending review
5. Be prepared to close positions and withdraw funds

Attempting to hide the move is misrepresentation under clause 5.10 and can result in worse outcomes than addressing it openly.

### "I'm a citizen of a restricted country but genuinely live elsewhere. Can I open an account?"

Likely yes, depending on the specific countries involved. The KYC process will focus on POA showing current residence, but you should:
1. Be prepared to provide additional documentation
2. Be honest about your citizenship — discrepancies discovered later are treated as misrepresentation
3. Be aware that US citizenship specifically can create additional FATCA reporting obligations regardless of residence
4. Confirm with OPO support before depositing significant funds

## Documentation gap and current state

The inconsistency between Client Agreement clauses 5.9 and 5.10 and the website footer is a known issue. Until reconciled:

- **For trader-facing AI:** the safest answer to "is my country restricted?" is to direct the trader to OPO's current operational list, not to a specific KB-stored list that may be outdated
- **For compliance:** the documentation should be reconciled so all sources show the same list
- **For legal:** clause 5.9 specifically should be updated to include Turkey (if Turkey is operationally restricted) and to remove Australia (if Australia is no longer operationally restricted)

The Client Agreement clauses 5.10 and 5.9 do provide a fallback — both allow OPO to add countries to the restricted list at its discretion. So operationally, the current list applied during account opening is authoritative, regardless of what specific countries are enumerated in any single source document.

## Risk warning

Traders applying for accounts from restricted countries face certain rejection. Traders who hide their residency to open accounts face misrepresentation findings under Client Agreement clause 27.2 — which can result in immediate account termination, confiscation of profits, refusal of withdrawals, and potential reporting to financial crime authorities. The documentation inconsistency between clause 5.9 and the website footer creates real uncertainty for traders from countries in the "depends which source you read" gap. Such traders should clarify their status with OPO support before depositing funds, not after — there is no good outcome from discovering restriction after a deposit and trading activity. Country restrictions can also change over time; a trader from a currently-unrestricted country who moves or whose country's regulatory status changes may find their account access affected later.

## Source

- OPO Client Agreement v10, clause 5.9 (enumerated restricted countries: USA, Japan, Australia, Canada)
- OPO Client Agreement v10, clause 5.10 (trader representation of non-restricted residency)
- OPO Client Agreement v10, clause 27.2 (termination for misrepresentation)
- OPO website footer (operational restricted countries list)
- Last verified: 2026-05-12

## Internal review notes

- **CRITICAL: Documentation inconsistency.** Client Agreement clause 5.9 lists USA/Japan/Australia/Canada. Website footer lists USA/Japan/Canada/Turkey/North Korea. These sources should be reconciled. Recommend: update clause 5.9 in the next Client Agreement revision to reflect the operational list, including Turkey (if operationally restricted) and removing Australia (if no longer restricted). Add North Korea explicitly if not already there
- Confirm SVG-jurisdiction restricted country list applies globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. Different licensed entities may have different restricted country lists
- Document whether the OPO website displays the restricted countries list prominently and accessibly, or only in footers. A dedicated FAQ entry would help reduce trader confusion
- Document the exact procedure for a trader who discovers their country has been added to the restricted list while they have an active account
- Document specific handling for dual citizens and recent movers — this is a common edge case currently lacking clear documentation
- Confirm the FATCA position for US citizens with non-US residency — whether OPO accepts such clients with appropriate documentation or rejects categorically
- Clarify whether visiting a restricted country temporarily (vacation, business trip) affects account access — most brokers don't restrict during travel, but the policy should be explicit
- Document the appeals process for traders who believe their country has been incorrectly classified as restricted

## Related topics

- [[KYC and Account Activation]]
- [[Document Expiry / Close-Only Mode]]
- [[Client Categorization]]
- [[Withdrawal Procedure]]
- [[Market Abuse Policy]]
- [[Aggressive Behavior Policy]]
- [[Complaints Procedure]]
- [[Account Types Overview]]