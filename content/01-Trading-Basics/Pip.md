---
title: Pip
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
# Pip

## Simple explanation

A pip is the standard unit of measurement for price movement in forex and most CFD trading. It stands for "Percentage in Point" or "Price Interest Point." For most currency pairs, one pip equals **0.0001** of the quote currency — the fourth decimal place.

The pip exists because forex prices move in tiny increments. Saying "EUR/USD moved from 1.1000 to 1.1015" is harder to parse than "EUR/USD moved up 15 pips." Pips give traders a universal language for talking about price movement, regardless of the instrument's actual price level.

## How pips work for different instrument types

### Most forex pairs (4-decimal quoting)

For pairs like EUR/USD, GBP/USD, AUD/USD: **1 pip = 0.0001**

| Price change | Pips moved |
|---|---|
| 1.1000 → 1.1001 | 1 pip |
| 1.1000 → 1.1010 | 10 pips |
| 1.1000 → 1.1100 | 100 pips |

### Japanese Yen pairs (2-decimal quoting)

For pairs like USD/JPY, EUR/JPY, GBP/JPY: **1 pip = 0.01**

The yen has a much smaller per-unit value than other major currencies, so the quoting convention shifts the decimal. A USD/JPY move from 150.00 to 150.10 is a 10-pip move, not a 1000-pip move.

### Indices, commodities, and crypto

The "pip" concept is sometimes used loosely for non-forex instruments, but the unit varies:

- **Gold (XAU/USD)**: 1 pip is typically $0.01 or $0.10 depending on the broker — OPO's quoting convention should be confirmed
- **Indices** (S&P 500, NASDAQ): usually quoted in points rather than pips
- **Crypto** (BTC/USD): usually quoted in whole-dollar increments or with fractional decimals; "pip" is not a meaningful unit for instruments priced in thousands

For non-forex instruments, traders should check the Contract Specifications on OPO for the exact tick size and value.

## Pipettes — the fifth decimal place

Modern brokers, including OPO, often quote forex pairs to **five decimal places** instead of four. The fifth decimal is called a **pipette** — one-tenth of a pip.

Example for EUR/USD: `1.10005 / 1.10018`
- The fourth decimal place is the pip (the "0" in 1.1000**0** and the "1" in 1.1001**8**)
- The fifth decimal place is the pipette
- The spread here is 13 pipettes = 1.3 pips

This finer granularity allows tighter spreads. A broker quoting to 4 decimals can offer a minimum spread of 1 pip; a broker quoting to 5 decimals can offer 0.8 pips, 0.3 pips, or even 0.0 pips on certain accounts. OPO uses 5-decimal quoting on most forex pairs, which is why account pages can advertise sub-1-pip spreads on ECN, ECN Pro, and similar accounts.

## The dollar value of one pip

The cash value of a pip depends on three things: the **lot size** of the trade, the **instrument**, and the **account currency**.

### Standard formula

For a USD-quoted pair (EUR/USD, GBP/USD, AUD/USD) on a USD account:


| Trade size | Lot units | Pip value (USD-quoted pair) |
|---|---|---|
| 1.0 standard lot | 100,000 | $10 |
| 0.1 mini lot | 10,000 | $1 |
| 0.01 micro lot | 1,000 | $0.10 |

So a 1-lot EUR/USD position making a 50-pip profit earns: 50 × $10 = $500.

### Cross-currency pairs

For pairs where USD is *not* the quote currency (EUR/GBP, AUD/JPY, etc.), the pip value depends on the current exchange rate between the quote currency and the account currency. Trading platforms calculate this automatically — traders don't need to compute it manually, but should be aware that pip values fluctuate as exchange rates change.

### Yen pairs

For yen pairs on a USD account, the pip value of 1 standard lot is approximately:

At a USD/JPY rate of 150, one pip on a standard-lot USD/JPY position is approximately $6.67. This is lower than the $10/pip on most other major pairs.

## Why pips matter for traders

Pips are the unit you'll think in every day as a trader:

- **Spread is measured in pips.** "0.8 pip spread" on the ECN account, "1.8 pip" on Standard.
- **Stop Loss and Take Profit are usually set in pips.** "Stop Loss 30 pips below entry."
- **Strategy results are measured in pips.** "This strategy averaged +12 pips per trade last month."
- **Risk-reward ratios use pips.** "Risk 20 pips to make 60 pips" is a 1:3 ratio.

A trader who can read pip movements quickly has a fundamental advantage over one who has to compute every move in decimal terms.

## Risk warning

Pips can feel abstract — they sound like small movements ("5 pips") but the dollar impact scales rapidly with lot size and leverage. A 100-pip adverse move on a 1-lot EUR/USD position is $1,000 in loss. The same 100-pip move on a 10-lot position is $10,000. Traders should always know the dollar value of a pip on their specific trade size *before* placing the trade, not after. Setting a Stop Loss in pips without confirming the dollar equivalent is one of the most common reasons retail traders lose more than they intended on a single trade.

## Source

- OPO Client Agreement v10 — note: "pip" is not defined in Appendix A's glossary, despite being referenced operationally throughout the document. This note draws from industry-standard definitions widely used across the forex industry
- OPO Contract Specifications (referenced in clauses 9.1, 11.4, 14.2 of the Client Agreement)
- OPO website account type pages (spreads expressed in pips)
- Last verified: 2026-05-12

## Internal review notes

- **Pip is not defined in the OPO Client Agreement.** This is the first trading-basics note built without a direct OPO citable definition. Compliance review should verify that the industry-standard definition used here matches OPO's operational practice on MT4, MT5, cTrader, and OpoTrade
- Recommend OPO add "Pip" and "Pipette" to the Appendix A glossary in the next Client Agreement revision — these are fundamental terms used throughout trader-facing documentation but not formally defined in the agreement
- Confirm pip value conventions for non-forex instruments at OPO: specifically gold (XAU/USD), silver (XAG/USD), indices, commodities, and crypto. These vary across brokers and should be documented in the Contract Specifications
- Confirm 5-decimal pricing applies across all platforms (MT4, MT5, cTrader, OpoTrade) and all account types
- Consider adding a pip value calculator linked from this note — traders frequently miscalculate pip values, especially on cross-currency pairs and yen pairs
- Confirm SVG-jurisdiction conventions apply globally — pip definitions are industry-standard and should not vary by jurisdiction, but worth verifying

## Related topics

- [[Spread]]
- [[Bid]]
- [[Ask]]
- [[Lot]]
- [[Lot Size 1]]
- [[Pipette]]
- [[Stop Loss]]
- [[Take Profit]]
- [[Contract Specifications]]
- [[Commission]]