---
title: Quote Currency
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
# Quote Currency

## Simple explanation

The Quote Currency is the **second** currency in a currency pair. It's the currency you're effectively paying with when you buy the [[Base Currency]], and receiving when you sell it.

OPO defines quote currency in the Client Agreement Appendix A as:

> The second currency in the Currency Pair which can be bought or sold by the Client for the Base Currency.

## How to identify the Quote Currency

Every forex pair is written as `BASE/QUOTE`. The Quote is on the right:

| Pair | [[Base Currency]] | Quote Currency |
|---|---|---|
| EUR/USD | EUR (Euro) | USD (US Dollar) |
| GBP/USD | GBP (British Pound) | USD (US Dollar) |
| USD/JPY | USD (US Dollar) | JPY (Japanese Yen) |
| AUD/CAD | AUD (Australian Dollar) | CAD (Canadian Dollar) |

## What the price actually means

In the quote EUR/USD = 1.1000:

- USD is the Quote Currency
- The price 1.1000 tells you: "**1 unit of the Base Currency costs 1.1000 units of the Quote Currency**"
- So 1 EUR costs 1.10 USD
- Equivalently: 1.10 USD will buy 1 EUR

When you see EUR/USD rise from 1.1000 to 1.1100, that means the Quote Currency (USD) has become *weaker* relative to the Base Currency (EUR) — it now takes more USD to buy 1 EUR. Conversely, EUR has become stronger.

## Quote Currency and pip value

For most major forex pairs, the dollar value of a [[Pip]] depends on whether your account currency matches the Quote Currency:

- **EUR/USD on a USD account** — pip value is consistent at $10 per lot, because the Quote Currency matches the account currency
- **EUR/GBP on a USD account** — pip value fluctuates with the GBP/USD exchange rate, because the pip is measured in GBP and must be converted to USD
- **USD/JPY on a USD account** — pip value depends on the current USD/JPY rate; a pip is worth 0.01 JPY, which converts to a fluctuating USD amount

This is why traders new to non-USD-quoted pairs sometimes find their dollar P/L doesn't match what they expected from pip count — they were calculating in the wrong currency.

## Quote Currency and account currency

The currency of your trading account (USD, EUR, GBP, etc.) determines how all P/L is ultimately reported. When you trade a pair where neither currency matches your account currency, OPO converts the P/L into your account currency at prevailing rates. The Client Agreement clause 10.1 covers this:

> OPO GROUP LLC. is entitled, without prior notice to the Client, to make any currency conversions which OPO GROUP LLC. considers necessary or desirable for the purposes of complying with its obligations or exercising its rights under the Operative Agreements or any Transaction.

So traders trading exotic crosses on a USD account effectively bear two layers of currency risk: the trade itself, and the conversion back to USD.

## Source

- OPO Client Agreement v10, Appendix A (Quote Currency, Currency Pair definitions)
- OPO Client Agreement v10, clause 10.1 (currency conversions)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm conversion rates used when P/L is converted between account currency and Quote Currency — clause 10.1 gives OPO discretion, which could be a source of trader complaints if rates differ significantly from interbank

## Related topics

- [[Base Currency]]
- [[Quote]]
- [[Bid]]
- [[Ask]]
- [[Long Position]]
- [[Short Position]]
- [[Pip]]
- [[Swap]]
- [[Currency of the Trading Account]]