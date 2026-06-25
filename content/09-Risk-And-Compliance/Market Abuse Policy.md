---
title: Market Abuse Policy
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
# Market Abuse Policy

## Simple explanation

The Market Abuse Policy is OPO's defence against trading behaviours that exploit the broker's pricing, execution, or systems rather than genuinely engaging with market risk. If OPO determines that a trader is engaging in market abuse, it can close positions, confiscate profits from the abusive activity, suspend or terminate the account, and refuse to pay out withdrawals.

The policy is documented in the Client Agreement clauses 35.1 through 35.5.

This is one of the more consequential policies in the Client Agreement because:
- The definition of "abuse" is broad and discretionary
- The penalties are severe
- OPO is the sole judge of what constitutes abuse, with limited formal appeal
- A finding of abuse can void the [[Negative Balance Protection]] (clause 16.6) and bonus protections

## What OPO classifies as market abuse

The Client Agreement clause 35.1 lists specific behaviours OPO treats as abuse:

> The Company strictly prohibits the following trading techniques and/or activities, which may be considered, at the absolute discretion of the Company, abusive trading, market abuse, or market manipulation:

The agreement then enumerates the prohibited behaviours. Each is described below.

### Arbitrage trading

Trading strategies that exploit price differences between OPO and another broker, exchange, or liquidity source — without taking genuine market risk. The trader is not betting on price direction; they're capturing a guaranteed (or near-guaranteed) profit from a pricing mismatch.

Examples:
- Two-broker arbitrage: simultaneously buying on one broker and selling on another to capture a price difference
- Cross-instrument arbitrage: trading correlated instruments to capture pricing inefficiencies
- Cash-vs-CFD arbitrage: holding a position on a spot exchange and an offsetting CFD position on OPO

### Latency arbitrage

Specifically exploiting **delays in OPO's price feeds** to trade against stale prices. The trader sees a future price (from a faster data source) before OPO does, and places trades that are essentially guaranteed wins.

This is particularly serious because:
- It requires sophisticated technical setup
- It produces consistent, predictable profits that don't reflect market risk
- It directly harms OPO's market-making margins

OPO monitors for latency arbitrage patterns automatically.

### Picking and sniping

Trading techniques aimed at quickly entering and exiting positions to capture small inefficiencies in pricing — typically during periods of low liquidity or during the milliseconds when a quote is briefly inaccurate.

The Client Agreement specifically mentions:

> picking and/or sniping on the OPO GROUP LLC.'s prices

Both are forms of high-frequency trading designed to exploit pricing mechanics rather than make genuine directional bets.

### Strategies designed to exploit specific market events

The Client Agreement clause 35.1 also addresses:

> trading strategies which take advantage of price latency, off-market quotes during volatile periods, [[Error Quote (Spike)|Error Quotes (Spikes)]], or expression of quotes through any other mechanism, including in particular abnormal market conditions

In plain terms: trading aggressively during the exact moments when prices are most likely to be wrong (immediately after news, during low-liquidity rollovers, during platform glitches) is treated as abuse — even if individual trades technically follow the rules.

### Use of Expert Advisors and automated systems for prohibited purposes

The Client Agreement clause 35.1 prohibits:

> the use of any Expert Adviser or any other automated software programme that is not directly approved by the Company

EAs and automated trading are not categorically forbidden — many traders use them for legitimate purposes. But OPO retains the right to flag automated strategies that demonstrate any of the abusive patterns above. An EA that systematically picks off stale quotes will be classified as abuse, regardless of whether the EA was openly disclosed.

### Misuse of bonuses and promotions

Specifically separate from the Bonus Programs document but cross-referenced:

> any other behaviour that the Company, at its sole and absolute discretion, considers as abusive of OPO GROUP LLC.'s bonus offers

Examples:
- Opening multiple accounts to claim the same promotional bonus multiple times
- Coordinating with other traders to manipulate bonus-conversion volume requirements
- Using bonus credits in patterns specifically designed to exploit the bonus mechanics

### Collusion between traders

Multiple traders coordinating positions to manipulate OPO's liquidity, pricing, or risk exposure. This typically involves traders trading against each other on accounts they control or coordinate, creating artificial volume or hedging the broker's risk in patterns the broker hasn't approved.

### The catch-all clause

The most consequential provision is the closing language of clause 35.1:

> any other behaviour that the Company at its sole and absolute discretion considers as abusive

This is intentionally broad. OPO is not committing to a fixed list — any trading pattern the broker classifies as abusive can be sanctioned, even if it doesn't fit one of the explicit examples above.

## What OPO can do when it finds abuse

The Client Agreement clauses 35.2 through 35.5 grant OPO broad enforcement powers:

> Upon a determination by OPO GROUP LLC. that the Client has engaged in market abuse or any of the prohibited activities described above, OPO GROUP LLC. shall be entitled to:

> (a) close, suspend, freeze, or restrict the Client's Trading Account(s);
> (b) cancel or reverse any Transaction or part thereof that the Company determines was generated by the abusive activity;
> (c) confiscate profits, including any profits generated using market abuse or arising from any breach of this Section 35;
> (d) recover any losses or damages incurred by OPO GROUP LLC. as a result of the abusive activity;
> (e) refuse to pay any withdrawal requests for funds derived from abusive activity;
> (f) terminate the Client Agreement with immediate effect;
> (g) cancel the Client's right to receive any benefits including bonuses;
> (h) take any other action OPO GROUP LLC. reasonably considers appropriate.

Of particular concern to traders:

- **(c) Profit confiscation:** profits made from abusive activity can be deducted from the account
- **(d) Loss recovery:** OPO can pursue the trader for losses the broker itself suffered as a result of the abuse
- **(e) Withdrawal refusal:** funds deemed to come from abusive activity may be permanently held
- **(f) Account termination:** the trading relationship can be ended without notice
- **(g) Bonus cancellation:** all promotional credits forfeited

## Interaction with Negative Balance Protection

The [[Negative Balance Protection]] (Client Agreement clause 15.8) normally caps a retail trader's loss at the deposit. But clause 16.6 contains a critical exception:

> In the event of a negative balance in a retail Client account, OPO GROUP LLC. will not file a claim against the Client for that amount, except in cases where the Client has used illicit methods to create it.

A finding under the Market Abuse Policy triggers this exception. So a trader who:
1. Engages in latency arbitrage
2. Generates a negative balance during a volatile event
3. Is found to have committed market abuse

...may find that:
- The Negative Balance Protection does not apply to them
- OPO can pursue the negative balance as a debt
- Any profits from the abusive strategy are confiscated

This is one of the most important consequences of the Market Abuse Policy. The trader-friendly NBP backstop disappears for traders classified as abusing the system.

## What is and isn't abuse — practical guidance

The line between legitimate strategy and abuse is sometimes unclear. Generally:

**Legitimate trading (not abuse):**
- Holding directional positions based on technical or fundamental analysis
- Using Stop Loss, Take Profit, Trailing Stop, and Pending Orders for risk management
- Running well-known strategies (trend-following, mean reversion, breakout, carry trade)
- Hedging existing positions
- Day trading and scalping with reasonable spread/commission costs (where you bear the cost on every trade)
- Using Expert Advisors that genuinely engage with market risk
- Trading actively during normal volatility
- Long-term position holding through events

**Likely to be flagged as abuse:**
- Strategies that profit consistently from millisecond-level pricing inefficiencies
- Strategies that profit specifically from quote glitches or pricing errors
- Trading patterns showing systematic exploitation of broker vs market-wide price differences
- Multiple-account coordination
- Heavy reliance on prices during the first few seconds after news releases
- Automated systems demonstrating any of the above patterns
- Repeated heavy bonus-volume gaming

**The middle ground (depends on execution):**
- Very high-frequency trading without arbitrage purpose
- Strategies that look statistically similar to arbitrage even when not intended as such
- EAs that rapidly capture small profits in many small trades
- Trading patterns that closely resemble those of known abusive traders

In ambiguous cases, OPO's classification stands unless successfully appealed through [[Complaints Procedure]].

## The opacity of the abuse classification

The Market Abuse Policy creates an asymmetry that traders should understand:

|                                                           | OPO             | Trader                             |
| --------------------------------------------------------- | --------------- | ---------------------------------- |
| Defines what constitutes abuse                            | ✓ (clause 35.1) | ✗                                  |
| Determines whether specific activity meets the definition | ✓ (clause 35.2) | ✗                                  |
| Applies enforcement actions                               | ✓ (clause 35.3) | ✗                                  |
| Can appeal classification                                 | n/a             | Via complaints procedure (limited) |
| Publishes specific criteria publicly                      | No              | n/a                                |
| Notifies traders before classification                    | No requirement  | n/a                                |

Traders are subject to a policy whose specific application criteria are not public, judged by the broker, with limited formal appeal. This is consistent with industry practice — virtually every regulated broker has similar provisions — but it places real responsibility on traders to behave conservatively when their strategy might look like abuse.

## What traders should do

1. **Avoid arbitrage-pattern trading.** Even if your intent is not arbitrage, strategies that produce consistent profits from millisecond-level inefficiencies will be flagged
2. **Be cautious about trading the first 10–60 seconds after major news.** Even if you're directionally informed, executing in that window resembles latency arbitrage to detection systems
3. **Use Expert Advisors transparently.** Don't run EAs designed to exploit specific OPO pricing characteristics
4. **Don't coordinate with other traders** to manipulate volume or risk in patterns that benefit one or all of you
5. **Don't run multiple accounts** for the purpose of bonus collection or other promotional abuse
6. **Be skeptical of "guaranteed profit" trading strategies.** If they're real, they're probably arbitrage, and they will be classified as abuse
7. **Keep trade records.** If you're ever subject to an abuse classification you believe is wrong, having detailed records of your strategy logic and decision-making protects you in the [[Complaints Procedure]]

## Risk warning

The Market Abuse Policy is the most consequential trader-facing policy in the Client Agreement. A finding under this policy can result in confiscation of trading profits, termination of the trading relationship, refusal of withdrawals, and (in extreme cases) loss of Negative Balance Protection — meaning the broker can pursue a negative balance as a debt. The definition of abuse is broad and applied at OPO's sole discretion, with limited formal appeal. Traders engaged in strategies that consistently profit from market-mechanics inefficiencies (rather than directional market views) are at elevated risk of classification, even if their individual trades are technically legitimate. The safest position is to engage with genuine market risk through clear directional strategies, using transparent execution, and avoiding trading patterns that closely resemble arbitrage or systematic exploitation.

## Source

- OPO Client Agreement v10, clause 35.1 (definition of market abuse)
- OPO Client Agreement v10, clause 35.2 (determination process)
- OPO Client Agreement v10, clause 35.3 (enforcement actions)
- OPO Client Agreement v10, clause 35.4 (notification provisions)
- OPO Client Agreement v10, clause 35.5 (right to retain funds)
- OPO Client Agreement v10, clause 16.6 (illicit methods exception to Negative Balance Protection)
- OPO Client Agreement v10, clause 27.13 (agreement termination)
- OPO Bonus Programs document (bonus abuse provisions)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction Market Abuse Policy applies globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. ASIC and other developed-market regulators have specific market abuse definitions that may differ from OPO's contract-based definitions
- The broad discretion in clause 35.1's catch-all ("any other behaviour the Company at its sole and absolute discretion considers as abusive") creates legal risk for OPO if the determination feels arbitrary in court. Consider whether specific criteria could be published — at minimum, examples of behaviours that would and would not be considered abuse — to reduce trader complaints and litigation risk
- Document any past cases of Market Abuse Policy enforcement, with anonymized details. This kind of historical record both builds trader trust and demonstrates good-faith application of the policy
- Document the appeals process specifically for abuse classifications, beyond the general [[Complaints Procedure]]
- Clarify the relationship between the Market Abuse Policy and the [[Aggressive Behavior Policy]] (clause 37) — both can trigger account suspension and there may be overlap
- Consider whether bonus-related abuse should be documented separately in the Bonus Programs section, since the rules and enforcement may differ
- The interaction between Market Abuse findings and refund of deposited funds (vs. confiscation of profits only) is not entirely clear in clause 35.3. Specifically: if a trader deposited $1,000, made $5,000 in abusive profits, can OPO withhold the $1,000 deposit? Clarification would reduce disputes
- Confirm whether bonus credits and promotional balances are treated identically to deposited funds in the context of abuse findings

## Related topics

- [[Negative Balance Protection]]
- [[Leverage Adjustment Policy]]
- [[Force Majeure]]
- [[Error Quote]]
- [[Error Quote (Spike)]]
- [[Abnormal Market Conditions]]
- [[Aggressive Behavior Policy]]
- [[Complaints Procedure]]
- [[Bonus Programs]]
- [[Expert Advisors]]
- [[Slippage]]
- [[Quote]]
- [[Stop Out]]
- [[Withdrawal Procedure]]
- [[Account Types Overview]]
