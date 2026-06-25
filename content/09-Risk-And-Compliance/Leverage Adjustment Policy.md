---
title: Leverage Adjustment Policy
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
# Leverage Adjustment Policy

## Simple explanation

OPO reserves the right to **automatically reduce the leverage available** on your account during specific high-volatility events. This is done to protect both the trader and the broker from outsized losses during predictable periods when markets become unpredictable. The Leverage Adjustment Policy describes when these adjustments happen, what they affect, and how broad OPO's discretion is.

The policy is documented in two places that now agree:
- **Client Agreement v10, clause 14.11** (the contractual basis)
- **Dynamic Leverage Specifications document** (the operational details)

A previous contradiction between these two documents has been resolved as of the current Dynamic Leverage Specifications revision.

## Two categories of adjustment

The Leverage Adjustment Policy describes two distinct mechanisms:

1. **Scheduled adjustments** — applied at known, recurring times around predictable high-volatility events (weekends, news releases, market breaks)
2. **Discretionary adjustments** — applied at OPO's judgment to specific clients categorized as high-risk, or during exceptional market conditions

Both can apply simultaneously. A trader can find their leverage reduced both because a news event is approaching *and* because OPO's risk team has flagged their trading pattern.

## Scheduled adjustments

### Gold market breaks

Gold (XAUUSD) trades on a different schedule than forex pairs, with daily market breaks. OPO reduces leverage on gold **30 minutes before** the daily market break.

This protects against:
- Liquidity drying up before the close
- Sharp price moves at the open after the break
- Stop Loss orders failing to execute at the requested level during the gap

### Weekends and public holidays

Leverage on most instruments is reduced **3 hours before** the market's scheduled closing time on Fridays and the eve of recognized public holidays. The reduced caps applied to **newly opened positions**:

- **Forex instruments:** up to 1:100
- **Metals / Indices / Energies:** up to 1:50

So a trader on a high-leverage account at 1:2000 cannot open a 1:2000 leveraged position on EUR/USD during the 3 hours before Friday close — only 1:100. The trader can still close existing positions, modify them, or open them at 1:100.

This is anticipating:
- Reduced liquidity going into weekend closure
- Weekend gap risk if news breaks while markets are closed
- Monday morning gap moves that can be 50–200 pips on major pairs after significant weekend events

### Significant economic news

Leverage is adjusted **15 minutes before and 10 minutes after** scheduled major economic announcements. The reduced caps:

- **Forex instruments:** up to 1:100
- **Metals / Indices / Energies:** up to 1:50
- **Cryptocurrencies:** up to 1:10

This protects against the 5–30 second windows immediately after news releases when spreads widen dramatically, liquidity vanishes briefly, and prices can gap 20+ pips in a single tick. Traders who open positions during this window at very high leverage frequently see immediate Margin Call or Stop Out.

The exact list of instruments classified as triggering "significant economic news" is not published explicitly. Generally accepted candidates include:
- Non-Farm Payrolls (NFP) — first Friday of each month
- Federal Reserve, ECB, Bank of Japan, Bank of England rate decisions
- Consumer Price Index (CPI) releases for major economies
- GDP releases
- Major central bank press conferences

### Release of the Company's Financial Report

When OPO's own underlying assets (specifically stocks where OPO is the underlying issuer, if applicable) release financial reports, leverage is adjusted **30 minutes before the stock market closes** and **20 minutes before it reopens**.

This is a narrower trigger that affects far fewer trades — relevant primarily for stock CFD traders during corporate disclosure events.

## Dynamic leverage tier (High Leverage account)

The Leverage Adjustment Policy interacts with the [[High Leverage Account]] dynamic tier system. On a high-leverage account, leverage is *already* tier-based depending on total open lot volume. The temporary caps from the Leverage Adjustment Policy come on top of these tiers — whichever is more restrictive wins.

| Instrument class | Normal leverage at 0–5 lots | During news/weekends |
|---|---|---|
| FX Major | 1:2000 | 1:100 |
| FX Minor | 1:1000 | 1:100 |
| FX Exotic | 1:500 | 1:100 |
| XAUUSD (gold) | 1:500 | 1:50 |
| Commodities | 1:300 | 1:50 |
| Indices | 1:300 | 1:50 |
| Cryptocurrencies | 1:50 | 1:10 |

A trader holding 0–5 lots of FX Major at 1:2000 leverage approaching a major news event finds their available leverage on **new** positions drop to 1:100 — a 20× reduction. The positions already open keep their original margin requirements (unless Force Majeure is invoked).

## What "applies only to newly opened positions" actually means

This is the subtle but critical clause. From the Dynamic Leverage Specifications and Client Agreement clause 14.12:

> Unless otherwise explicitly stated by the Company, Leverage adjustments under this policy shall apply only to newly opened positions and shall not retroactively alter the margin requirements of existing open positions.

In plain terms:

- **Position already open at 1:2000:** keeps its 1:2000 margin requirement throughout the news event
- **New position opened during the news window:** opens at the temporary 1:100 cap (or the dynamic tier, whichever is lower)
- **Existing position closed during the news window and reopened:** the reopened position is "new" and gets the temporary cap

This is generally favourable to the trader — existing positions are not retroactively margined harder during volatile events. But it has a counterintuitive effect: traders cannot rebuild a position at the same leverage they had before. Closing and reopening during a leverage adjustment effectively forces a downsize.

**Exception:** the Client Agreement clause 14.12 and Dynamic Leverage Specifications General Provisions section both reserve OPO's right to **apply changes to existing positions** during exceptional conditions:

> In exceptional market conditions, including but not limited to Force Majeure Events, abnormal volatility, low liquidity conditions, market disruptions, trading halts, pricing anomalies, or geopolitical events, the Company reserves the right to: reduce Leverage, increase margin requirements, restrict opening of new positions, limit trading on specific Instruments, or take any other measures deemed necessary by the Company for risk management purposes.

So during a true Force Majeure or extraordinary event, even existing positions can be re-margined upward, which can produce sudden [[Margin Call]] or [[Stop Out]] on positions that were comfortable at their original leverage.

## Dynamic leverage adjustments for high-risk clients

The Client Agreement clause 14.11 and Dynamic Leverage Specifications grant OPO broad discretion to apply enhanced restrictions to specific clients classified as "high-risk":

> The Company reserves the right to apply a dynamic Leverage model, enhanced margin requirements, or other trading restrictions to Clients categorized by the Company as high-risk Clients based on internal risk management assessments.

The factors OPO may consider:

- **Trading behaviour** — patterns suggesting reckless or systematic exploitation of market mechanics
- **Exposure concentration** — large positions concentrated in a single instrument or correlated instruments
- **Abusive trading practices** — picking, sniping, arbitrage strategies prohibited under [[Market Abuse Policy]]
- **Latency arbitrage activity** — exploiting price feed delays for guaranteed profits
- **Toxic flow indicators** — internal classifications of trading patterns that consistently disadvantage the broker's market-making
- **Excessive volatility exposure** — frequent trading during news/volatile periods at maximum leverage
- **Liquidity-related risks** — positions of a size that materially affect the broker's hedging
- **Any other risk management considerations determined by the Company**

The final catch-all phrase makes this discretion essentially unlimited. A trader classified as high-risk may find their leverage reduced, margin requirements increased, instruments restricted, or trading suspended entirely — with no prior notice.

Critically: this is **not a publicly defined threshold**. A trader does not know in advance whether they are high-risk. The classification is opaque, applied at OPO's discretion, and not subject to formal appeal beyond the standard [[Complaints Procedure]].

## What this means for traders in practice

Three practical takeaways:

**1. Plan around scheduled events.** If you trade major economic news, you cannot rely on high leverage during the news window. Either accept the lower temporary leverage or pre-position before the adjustment window opens.

**2. Don't be surprised by reduced leverage going into weekends.** Friday afternoon trades on a high-leverage account will not get high-leverage execution — the 3-hour pre-close window is firmly enforced.

**3. Avoid behaviours that flag you as high-risk.** Trading near news events at maximum leverage repeatedly, holding extreme concentration in a single instrument, or exhibiting patterns associated with arbitrage strategies all increase the probability of being classified as high-risk and having permanent restrictions applied. The classification is opaque and not formally appealable.

## How leverage adjustments interact with other policies

The Leverage Adjustment Policy is one of three OPO powers to alter trading conditions on the fly:

| Policy | Trigger                                       | Effect |
|---|---|---|
| Leverage Adjustment Policy | Scheduled events + high-risk classification   | Reduced leverage caps on new positions |
| [[Force Majeure]] (CA 26) | Genuinely catastrophic / unforeseeable events | Can affect existing positions, spreads, all trading conditions |
| Margin requirement changes (CA 14.3–14.5) | OPO discretion + Force Majeure                | Margin requirements can change with 3 days notice (or no notice during FM) |

In a true crisis, all three operate simultaneously. The Leverage Adjustment Policy is the most predictable of the three; Force Majeure is the most powerful.

## Risk warning

The Leverage Adjustment Policy is largely a trader-protective mechanism — it exists because retail trader losses around news events at maximum leverage are catastrophic and predictable. But the policy is broad enough that traders should not assume "I have 1:2000 leverage" means they have 1:2000 leverage at all times. The temporary caps around scheduled events, combined with the dynamic tier system on high-leverage accounts, mean effective leverage on a typical FX Major trade can vary from 1:100 to 1:2000 depending on time, lot count, and risk classification. The "high-risk client" provisions in particular create an opaque category that can affect trading conditions without prior notice or formal appeal. Traders depending on high leverage as a strategic edge should size positions to remain viable at the reduced temporary leverage levels, not at the headline maximum.

## Source

- OPO Client Agreement v10, clause 14.11 (Leverage Adjustment Policy contractual basis)
- OPO Client Agreement v10, clause 14.12 (General Provisions)
- OPO Client Agreement v10, clauses 14.3, 14.4, 14.5 (margin requirement changes)
- OPO Client Agreement v10, clause 26 (Force Majeure)
- OPO Dynamic Leverage Specifications (revised version with reconciled timing/caps)
- OPO Dynamic Leverage Specifications, section 1.1 (Leverage Adjustment Policy)
- OPO Dynamic Leverage Specifications, section 1.2 (General Provisions)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction provisions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. ASIC in particular has stricter rules on leverage adjustments — the ASIC version of this note may differ substantially
- Confirm the exact list of instruments triggering "Significant Economic News" classification, and where this list is published or made available to traders
- Document the high-risk classification criteria more concretely — at least describe boundaries for what trading patterns trigger review, even if the final determination remains discretionary. Currently the criteria are too vague to allow traders to self-correct
- Document the appeal/review process if a trader believes they have been incorrectly classified as high-risk
- Confirm the exact reconciliation status of timing and caps between Client Agreement and Dynamic Leverage Specifications — the new Dynamic Leverage Specifications document appears to align (3 hours / 15-10 min) but cross-reference should be formally documented
- Document any past instances of Leverage Adjustment Policy being invoked for high-risk classification, if any are available to publish

## Related topics

- [[Leverage]]
- [[High Leverage Account]]
- [[Dynamic Leverage]]
- [[Margin]]
- [[Initial Margin]]
- [[Necessary Margin]]
- [[Free Margin]]
- [[Margin Call]]
- [[Stop Out]]
- [[Force Majeure]]
- [[Abnormal Market Conditions]]
- [[Market Abuse Policy]]
- [[Complaints Procedure]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Open Position]]
- [[Bonus Programs]]




