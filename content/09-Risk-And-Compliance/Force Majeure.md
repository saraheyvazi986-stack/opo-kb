---
title: Force Majeure
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

# Force Majeure

## Simple explanation

Force Majeure (French for "superior force") is a legal concept that suspends normal contractual obligations during catastrophic, unforeseeable events outside either party's control. In a trading context, it gives OPO broad discretionary powers to suspend, modify, or unwind transactions when markets are functioning abnormally — events the broker did not cause and cannot reasonably control.

When OPO declares a Force Majeure event, many normal rules of the Client Agreement are suspended. The broker's protections expand significantly. The trader's options narrow correspondingly.

OPO defines and operates the Force Majeure provisions in the Client Agreement clause 26.

## What qualifies as a Force Majeure event

The Client Agreement clause 26.1 lists examples — non-exhaustive — of what OPO may classify as a Force Majeure event:

> A Force Majeure Event includes without limitation:
> (a) any act, event or occurrence including, without limitation, any national emergency, strike, riot or civil commotion, government actions, acts of terrorism, outbreak or threat of war or hostilities, act of God, earthquake, epidemic, accident, fire, flood, storm, breakdown,
> (b) interruption or malfunction of power supply, electronic, communication equipment or supplier failure, civil unrest, statutory provisions, lock-outs, or any other international calamity, economic or political crisis, or natural disaster
> (c) the suspension, liquidation or closure of any market or the abandonment or failure of any event to which OPO GROUP LLC. relates its Quotes
> (d) abnormal Market Conditions
> (e) Any event, act or circumstances not reasonably within OPO GROUP LLC.'s control

Two categories worth unpacking:

**Real-world catastrophic events:** wars, terrorism, natural disasters, pandemics, government emergencies. These are unambiguous.

**Market-functioning events:** abnormal market conditions, exchange closures, liquidity provider failures, technical outages, "any event not reasonably within OPO's control." This second category is much broader — and it's where most Force Majeure declarations in practice would actually occur.

## What "Abnormal Market Conditions" means

OPO defines [[Abnormal Market Conditions]] in the Client Agreement Appendix A as:

> Conditions contrary to Normal Markets Conditions e.g. when there is low liquidity in the market or rapid price movements in the market or Price Gaps.

So three sub-types qualify as abnormal:

1. **Low liquidity** — too few buyers and sellers to maintain orderly pricing
2. **Rapid price movements** — typically defined as movements much larger than recent average volatility
3. **Price Gaps** — quotes jumping from one level to another without trading at intermediate prices

These conditions occur regularly around major news releases, market opens after closures, and during low-liquidity sessions. The Client Agreement allows OPO to invoke Force Majeure-adjacent protections during these events even if a formal Force Majeure declaration isn't made.

## What OPO can do during Force Majeure

The Client Agreement clause 26.2 grants OPO broad discretionary powers — applied **without prior Written Notice** and at any time:

> (a) increase margin requirements;
> (b) close out any or all Open Positions at such prices as OPO GROUP LLC. considers in good faith to be appropriate;
> (c) suspend or freeze or modify the application of any or all terms of the Operative Agreements to the extent that the Force Majeure Event makes it impossible or impractical for OPO GROUP LLC. to comply with them;
> (d) take or omit to take all such other actions as OPO GROUP LLC. deems to be reasonably appropriate in the circumstances with regard to the position of OPO GROUP LLC., the Client and other Clients;
> (e) increase Spreads;
> (f) decrease Leverage.

In plain terms, during a Force Majeure event, OPO can:

- **Forcibly close your open positions** at prices it considers appropriate (not necessarily your Stop Loss level or current displayed price)
- **Increase your margin requirements** retroactively on positions you already hold, reducing your [[Free Margin]] without you doing anything
- **Widen spreads dramatically** — the typical 1.8-pip spread on EUR/USD could become 20 pips, 50 pips, or more
- **Cut your leverage** mid-position
- **Suspend execution of new trades entirely**
- **Take any other action it deems reasonable** — this is the broadest possible discretion

## What OPO is not liable for during Force Majeure

The Client Agreement clause 26.3 protects OPO from liability during Force Majeure:

> Except as expressly provided in this Client Agreement, OPO GROUP LLC. will not be liable or have any responsibility for any type of loss or damage arising out of any failure, interruption, or delay in performing its obligations under this Client Agreement where such failure, interruption or delay is due to a Force Majeure event.

So losses caused by:
- Delayed order execution during the event
- Inability to execute orders at all
- Spreads widening beyond what would normally be considered acceptable
- Positions closing at much worse prices than expected
- The trading platform being unavailable

...are all losses the trader bears, not the broker.

## How Force Majeure interacts with Leverage Adjustment Policy

The [[Leverage Adjustment Policy]] (Client Agreement clause 14.11) already gives OPO the right to reduce leverage during predictable high-volatility events — news releases, weekends, financial reports. The Force Majeure provisions go further: they give OPO the right to reduce leverage during *unpredictable* events without any prior policy or notice.

A practical sequence during an extreme event:
1. **Normal conditions** → standard leverage, normal spreads
2. **Approaching scheduled event** → Leverage Adjustment Policy kicks in (e.g., 30 minutes before major news)
3. **During the event** → spreads widen, execution slows
4. **If event becomes genuinely catastrophic** → Force Majeure declared, all of clause 26.2's powers become available

The transition from #2 to #4 can be sudden. Traders should not expect a clear warning of when "normal volatility management" becomes "Force Majeure response."

## Real-world examples of Force Majeure-eligible events

These are events from recent market history that would qualify under clause 26.1:

- **Swiss National Bank EUR/CHF un-peg (January 2015)** — instant 30%+ move in seconds, multiple liquidity providers failed
- **Brexit referendum overnight (June 2016)** — GBP gapped 1000+ pips between sessions
- **COVID-19 market disruption (March 2020)** — multi-day extreme volatility, multiple exchanges halted trading
- **Russia-Ukraine war commencement (February 2022)** — currency exchanges suspended, commodities gapping
- **Hamas-Israel conflict spike (October 2023)** — weekend gap in oil markets opened far from prior close
- **Major flash crashes** — sub-second moves of multiple percent in major instruments

Each of these caused brokers worldwide to invoke Force Majeure or equivalent provisions.

## What traders should do about Force Majeure risk

Force Majeure events are by definition unpredictable, but the categories of events that produce them are not. Practical risk management:

1. **Reduce position sizes around scheduled high-risk events** — central bank decisions, election results, geopolitical announcements. These don't trigger Force Majeure themselves but increase the probability of one being triggered
2. **Avoid holding positions over weekends or extended market closures** when major news could break in the gap
3. **Use position sizing that survives Force Majeure-level adverse moves** — your worst-case loss should be bearable, not catastrophic, even with spreads widening 10x
4. **Recognize that [[Stop Loss]] orders provide reduced protection during Force Majeure** — clause 26.2(b) lets OPO close positions at prices it determines, which can be significantly worse than your Stop Loss level
5. **Don't expect [[Negative Balance Protection]] to make losses small** — NBP caps loss at the deposit, but the deposit itself can be wiped out during Force Majeure

## Risk warning

Force Majeure is the broker's broadest legal protection and operationally the most consequential clause in the Client Agreement. During a Force Majeure event, the standard rules of the trading relationship are largely suspended in OPO's favour. Stop Loss orders may not protect at the level set; spreads may widen by orders of magnitude; positions may be closed at prices the trader has no input over; new trades may be rejected entirely. The Client Agreement clause 26.3 explicitly absolves OPO of liability for losses arising from Force Majeure events. Traders should size positions and design strategies with the assumption that, eventually, they will experience a Force Majeure event during an open position — and the loss in that event must be one they can absorb. [[Negative Balance Protection]] (clause 15.8) caps the maximum loss at the deposit for retail clients, which is the most important backstop, but does not protect against losing the entire deposit.

## Source

- OPO Client Agreement v10, clause 26.1 (Force Majeure Event definition)
- OPO Client Agreement v10, clause 26.2 (OPO's rights during Force Majeure)
- OPO Client Agreement v10, clause 26.3 (OPO liability exclusion during Force Majeure)
- OPO Client Agreement v10, clause 14.11 (Leverage Adjustment Policy — preventive measures)
- OPO Client Agreement v10, clause 15.8 (Negative Balance Protection)
- OPO Client Agreement v10, Appendix A (Abnormal Market Conditions, Normal Market Conditions, Price Gap definitions)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction Force Majeure provisions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. Force Majeure provisions vary substantially across jurisdictions and ASIC in particular may impose stricter requirements on how Force Majeure can be invoked
- Confirm OPO's internal process for declaring a Force Majeure event — does it require executive approval, can it be invoked by operations or compliance, who notifies clients
- Confirm how Force Majeure declarations are communicated to clients (in-platform notice, email, website banner) — clause 26.1 says "OPO GROUP LLC. will, in due course, take reasonable steps to inform the Client" but doesn't specify timing or channel
- Document any prior Force Majeure declarations by OPO, if any have occurred, with dates and circumstances. This kind of operational history builds trust
- The breadth of clause 26.2(d) — "take or omit to take all such other actions as OPO GROUP LLC. deems to be reasonably appropriate" — is very broad and could be a source of trader disputes. Consider whether more specific guidance on what is and isn't covered would reduce post-event complaints
- Clarify the interaction between Force Majeure and the Leverage Adjustment Policy. Traders need to understand which provisions apply when

## Related topics

- [[Leverage Adjustment Policy]]
- [[Abnormal Market Conditions]]
- [[Normal Market Conditions]]
- [[Price Gap]]
- [[Margin]]
- [[Free Margin]]
- [[Necessary Margin]]
- [[Leverage]]
- [[Spread]]
- [[Stop Loss]]
- [[Stop Out]]
- [[Margin Call]]
- [[Negative Balance Protection]]
- [[Open Position]]
- [[Order]]
- [[Quote]]
- [[Slippage]]
- [[Error Quote]]
- [[Error Quote (Spike)]]
- [[Market Abuse Policy]]