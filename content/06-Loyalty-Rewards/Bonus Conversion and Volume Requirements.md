---
title: Bonus Conversion and Volume Requirements
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
# Bonus Conversion and Volume Requirements

## Simple explanation

When you receive a bonus from OPO, the credit is added to your trading account immediately — but it's not immediately withdrawable. To convert bonus credit into real, withdrawable cash, you have to trade a specific volume of lots over a specific period. This is the **volume requirement** (also called "turnover requirement" or "trading volume condition"), and it's the single most important mechanic to understand before accepting any bonus.

The volume requirement is the broker's way of ensuring the bonus is earned through genuine trading activity, not just claimed as a deposit-and-withdraw arbitrage. The requirement is also where many traders find they cannot realistically convert the bonus, even if they intended to trade through it.

The mechanics are governed by the **OPO Bonus Programs document**, with specific volume formulas varying by bonus type.

## How the volume requirement works

The volume requirement specifies how many lots you must trade to "earn" the bonus and convert it to withdrawable cash. Per the OPO Bonus Programs document (clause 2.7), the formula is:

> **(Total Bonus Amount x 4) = Number of Standard Lots required**

**Example from the PDF (clause 2.7):** A client deposits $1,000 and receives a 30% bonus = $300 bonus credit. The volume requirement is 75 standard lots.

| Bonus amount | Required standard lots |
|---|---|
| $100 bonus | 25 lots |
| $300 bonus | 75 lots |
| $500 bonus | 125 lots |
| $1,000 bonus | 250 lots |

> **Internal review note — PDF inconsistency:** The formula text in clause 2.7 says "Total Bonus Amount **x 4**" (multiply by 4), but the worked example in the same clause shows $300 bonus = 75 standard lots, which is $300 **÷ 4** = 75 (i.e., 0.25 lots per dollar of bonus). These are contradictory: multiplying $300 by 4 would yield 1,200 lots, not 75. The example (the concrete reference) yields Bonus ÷ 4 = lots. This inconsistency exists in the source PDF and should be raised with the document owner for clarification. Until resolved, the example figure (75 lots for a $300 bonus) is used as the authoritative reference throughout this article.

The specific multiplier for any given bonus may vary by promotion — traders should check the current promotion terms before accepting.

## What counts toward volume

The Bonus Programs document specifies which trades count toward the volume requirement. Generally:

| Trade characteristic | Counts toward volume? |
|---|---|
| Standard market orders (Commodities, Energies, Forex, Indices, USD Index, Metals) | Yes |
| Pending orders that execute and become positions | Yes |
| Positions held for at least 120 seconds (2 minutes) | Yes |
| Positions with at least 3 pips difference between open and close price | Yes |
| Positions closed at a profit | Yes |
| Positions closed at a loss | Yes |
| Stop Loss / Take Profit triggered closures | Yes |
| Stop Out forced closures | Sometimes — varies by bonus terms |
| Scalping trades (held under 120 seconds) | NO |
| Trades with less than 3 pips difference between open and close price | NO |
| Hedged positions (matched long + short) | NO — excluded from volume requirement |
| Trades on instruments excluded from the bonus (e.g. Cryptocurrencies, Stocks) | NO |
| Bonus credit-only trades (using bonus before deposited funds) | Varies |

**The minimum holding duration of 120 seconds (2 minutes)** (clause 2.8) matters because it prevents traders from rapidly opening and closing positions to inflate volume artificially. A scalper who normally holds positions for under 2 minutes may find none of their trades count.

**The 3-pip minimum** (clause 2.8) requires at least 3 pips difference between the open and close price of a trade for it to count toward the volume requirement. Trades that close within 3 pips of the opening price are excluded, even if they meet the duration requirement.

**Hedged positions** are explicitly excluded from the volume requirement (clause 2.8). Hedged positions have offsetting risk and could be used to accumulate volume with no net market exposure. OPO excludes all hedged volume — there is no partial counting or reduction.

## A worked example

Suppose a trader deposits $1,000 and receives a 30% Deposit Bonus = $300 bonus credit with a 90-day expiry.

**Required volume:** 75 standard lots (per clause 2.7: $300 bonus = 75 lots)

**Calculating realistic feasibility:**

| Trading frequency | Lots needed per period | Realistic for typical retail trader? |
|---|---|---|
| All 50 lots in 1 week | 7 lots/day for 7 days | Aggressive but possible |
| All 50 lots in 30 days | ~1.7 lots/day | Reasonable for active traders |
| All 50 lots in 90 days | ~0.6 lots/day | Easy for most active traders |

For a trader placing 5 trades of 0.1 lots per day, that's 0.5 lots/day, totaling 45 lots over 90 days — just under the requirement. They would need to slightly increase activity to meet the volume.

For a trader placing 1 trade of 0.5 lots per day, that's 0.5 lots/day, hitting 45 lots — same situation.

For a position trader holding 1 trade per week of 1.0 lots, that's about 13 lots in 90 days — far short of the requirement. This trader cannot realistically convert the bonus.

The lesson: **the trader's actual trading style determines whether the volume requirement is achievable**. Based on the PDF formula (Bonus Amount × 4 = lots), a $300 bonus requires 75 lots in 90 days — realistic for active traders but unconvertible for position traders. Position traders should generally decline bonuses.

## Time limits on volume requirements

Most OPO bonuses include a **time limit** — a specific period within which the volume must be completed. Common ranges:

- 30 days for short promotional bonuses
- 60-90 days for standard Welcome Bonus
- 180-365 days for larger Deposit Bonuses

If the volume requirement isn't met by the expiry date:

- The bonus credit is **removed** from the account
- Profits earned **using the bonus credit** may also be removed (depends on bonus terms)
- Profits earned using **deposited funds** are not affected
- The trader retains the deposited principal

This is why time limits matter — a trader who plans to "trade through" the bonus over many months may find it expires before they meet the requirement.

## The instrument restriction

Not all instruments count equally toward volume. Many OPO bonuses restrict counting to specific instrument categories:

| Instrument category | Typical volume contribution |
|---|---|
| Major forex pairs (EUR/USD, GBP/USD, etc.) | Full count |
| Minor and exotic forex pairs | Full count, sometimes |
| Gold (XAU/USD) | Full count |
| Silver | Variable |
| Indices | Sometimes restricted |
| Cryptocurrencies | Often excluded or heavily restricted |
| Stocks (CFDs) | Often excluded |
| Commodities (oil, gas) | Variable |

A trader planning to trade primarily crypto or stock CFDs may find their volume doesn't count toward the bonus requirement, even if they're meeting the lot count.

This is one of the most common bonus surprises. The trader's preferred instruments may not contribute to the volume requirement.

## Partial conversion

Some OPO bonuses support partial conversion — meeting a fraction of the volume requirement converts a proportional fraction of the bonus to withdrawable status. Others are all-or-nothing.

The Bonus Programs document is currently inconsistent on this:

- Some bonus types appear to support partial conversion
- Others require full volume completion before any conversion
- The specific behaviour depends on the individual bonus terms

A trader should verify the conversion structure (partial or all-or-nothing) before accepting any bonus, particularly if they're uncertain whether they can meet the full requirement.

## How conversion appears on your account

When bonus credit converts to withdrawable status, the platform behavior varies:

- The bonus balance may be reclassified as part of regular [[Balance]]
- A specific "Converted Bonus" line may appear in account statements
- The bonus credit may simply disappear from one balance category and increase another

After conversion, the converted funds are subject to the standard [[Withdrawal Procedure]] — including the deposit-method matching rule, the no-activity withdrawal penalty (typically not applicable since trading has occurred to meet volume), and standard processing times.

## What to verify before accepting a bonus

Before accepting any specific bonus, traders should confirm:

1. **The volume formula** — the standard formula per clause 2.7 is (Total Bonus Amount × 4) = lots required, but different promotions may vary
2. **The expiry timeframe** — 30 days? 90 days? Longer?
3. **Which instruments count** — per clause 2.8: Commodities, Energies, Forex, Indices, USD Index, and Metals are eligible; Cryptocurrencies and Stocks are not listed
4. **The minimum holding duration** — 120 seconds per clause 2.8
5. **Whether partial conversion is allowed** — or is it all-or-nothing?
6. **What happens to profits if volume isn't met** — bonus removed, but are profits kept?
7. **What happens if you also withdraw deposited funds during the bonus period** — see [[Bonus Removal and Withdrawal Interactions]]

If any of these questions cannot be clearly answered from the bonus terms, decline the bonus or get clarification from OPO support before accepting.

## Why volume requirements are so consequential

Volume requirements are the mechanism that makes most bonuses net-zero or net-negative for the trader. The math:

A trader who trades 50 lots specifically to meet a $500 bonus requirement pays:
- [[Spread]] on every trade (50 lots × typical 1.5 pip spread on EUR/USD = ~$750 in spread costs)
- [[Commission]] if applicable (50 lots × $6/lot on ECN = $300 in commission)
- [[Swap]] charges on any positions held overnight
- Trading risk on every position (some will be losing trades)

So earning a $500 bonus costs the trader approximately $750-1,000+ in trading costs alone, before counting any losses on the trades themselves. The bonus is only valuable if:

- The trader was going to trade that volume anyway
- The trading costs are roughly offset by trading profits (the trader has a positive expectancy)
- The bonus represents genuine additional capital that produces additional opportunity

For traders who would not naturally trade the required volume, the bonus is a cost trap disguised as a gift.

## Strategies for actually capturing bonus value

For traders who want to benefit from bonuses (rather than be hurt by them), the practical approach:

1. **Calculate breakeven first.** What volume would generate enough in spread/commission to cancel out the bonus value? Set this as a minimum threshold for accepting
2. **Match the bonus to your trading style.** Active traders benefit from short-expiry, high-multiplier bonuses. Position traders should accept only very low-multiplier or long-expiry bonuses, or decline entirely
3. **Don't change your trading pattern to chase volume.** Increasing position size or frequency to hit volume requirements typically destroys profitability
4. **Treat the bonus as a small edge, not a primary motivator.** If your trading would be profitable without the bonus, the bonus adds value. If you only trade because of the bonus, you're likely losing
5. **Have a withdrawal plan from the start.** Know what happens to your bonus if you need to withdraw during the period

## Risk warning

Volume requirements are the mechanism through which most retail trader bonuses become net-negative for the trader. The combination of trading costs (spread, commission, swap) plus inevitable losses on a subset of forced trades typically exceeds the bonus value. Traders who plan trading activity specifically to meet bonus volume requirements — rather than trading their normal strategy and incidentally meeting volume — are at high risk of losing more to costs than they gain from the bonus. Time limits on volume requirements compound this risk: a trader who fails to meet the requirement by expiry loses the bonus and the associated trading costs, with no compensation. The safest assumption is that any bonus's volume requirement is harder to meet than it appears, takes longer than expected, and costs more in trading expenses than the bonus's headline value. Accept bonuses only when the volume requirement matches your natural trading activity, not the other way around.

## Source

- OPO Bonus Programs document (volume requirements and conversion rules)
- OPO Bonus Programs document, clause 2.6 (bonus removal conditions)
- OPO Bonus Programs document, clause 2.11 (1:500 leverage cap with bonus)
- OPO Bonus Programs document (instrument restrictions, vary by bonus)
- OPO Client Agreement v10, clause 9.13 (swap charges affect volume calculations)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG/Seychelles jurisdictional bonus rules apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. ASIC and several major regulators have specific restrictions on bonus volume requirements that may apply
- Document the **specific volume multipliers per current bonus type** — currently these are scattered across promotional pages and not centralized. A single accessible reference table would dramatically reduce trader confusion
- Document the **specific minimum holding durations per bonus type** — typically 5-15 minutes, but varies
- Document the **specific instrument inclusions and exclusions per bonus type** — particularly the treatment of crypto, stock CFDs, and exotic forex
- Document whether **partial conversion is supported** for each bonus type, and the specific partial-conversion math when applicable
- Document **what happens to trade profits earned during the bonus period** if the volume requirement isn't met — currently the policy seems to vary by bonus
- Document **whether bonus volume requirements are reduced during Force Majeure or abnormal market conditions** — traders unable to trade due to broker-caused outages shouldn't have their volume clock continue
- Confirm whether **scalping is genuinely excluded** from volume counting, and how OPO defines scalping (under-X-second holds, automated systems, others)
- Consider whether a **bonus volume calculator** tool on the OPO website would help traders evaluate bonuses realistically before accepting

## Related topics

- [[Bonus Programs Overview]]
- [[Bonus Eligibility and Restrictions]]
- [[Bonus Removal and Withdrawal Interactions]]
- [[Spread]]
- [[Commission]]
- [[Swap]]
- [[Lot]]
- [[Withdrawal Procedure]]
- [[Negative Balance Protection]]
- [[Market Abuse Policy]]
- [[Open Position]]
- [[Completed Transaction]]
- [[Stop Loss]]
- [[Stop Out]]
- [[Balance]]
- [[Free Margin]]
- [[Leverage]]
