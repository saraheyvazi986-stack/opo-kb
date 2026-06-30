---
title: Lot
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
# Lot

## Simple explanation

A lot is the standard unit of trade size in forex and CFD trading. It defines how much of an instrument you're buying or selling in a single position. Instead of saying "I want to buy 100,000 euros against US dollars," a trader simply says "I want to buy 1 lot of EUR/USD."

OPO defines lot in the Client Agreement Appendix A as:

> A unit of Securities Base Currency or troy oz. of Precious Metal in the Trading Platform.

And [[Lot Size 1]] as:

> The number of shares, underlying assets or units of Base Currency, or troy oz. of Precious Metal in one Lot defined in the Contract Specifications.

In plain terms: 1 lot represents a specific quantity of the underlying instrument, and that quantity depends on what you're trading.

## Lot sizes at OPO

The exact units in one lot vary by instrument class. From standard industry practice and OPO's Contract Specifications:

| Instrument type | 1 standard lot |
|---|---|
| Forex (most pairs) | 100,000 units of the [[Base Currency]] |
| Gold (XAU/USD) | 100 troy ounces |
| Silver (XAG/USD) | 5,000 troy ounces |
| Indices (e.g. S&P 500) | Varies — typically 1 contract per lot |
| Commodities (oil, gas) | Varies by instrument |
| Cryptocurrencies | Varies — typically 1 unit of the base crypto per lot |
| Stocks (CFDs) | Varies — typically 1 share per lot |

Exact lot definitions per instrument are published in the **Contract Specifications**, accessible inside the trading platform or on the OPO website.

## Fractional lots — mini and micro

A "standard lot" is the full unit, but most traders rarely trade in full lots. OPO allows fractional lot sizes down to **0.01 lots** (Client Agreement specifies minimum trade size in Contract Specifications; account pages confirm 0.01 minimum across all account types).

| Lot size term | Decimal | Forex units (most pairs) | Use case |
|---|---|---|---|
| Standard lot | 1.00 | 100,000 | High-volume traders, large accounts |
| Mini lot | 0.10 | 10,000 | Mid-sized accounts, typical retail |
| Micro lot | 0.01 | 1,000 | Small accounts, beginners, testing strategies |

OPO also allows custom fractional sizes — 0.27 lots, 0.83 lots, etc. — in increments of 0.01.

## How lot size connects to risk and cost

Lot size is the lever that controls how much money is at stake on every trade. Three things scale directly with lot size:

### 1. Pip value

The dollar value of each [[Pip]] movement scales with lot size. On a USD-quoted pair:

| Lot size | Pip value (USD-quoted pair) |
|---|---|
| 1.0 lot | \$10/pip |
| 0.5 lot | \$5/pip |
| 0.1 lot | \$1/pip |
| 0.01 lot | \$0.10/pip |

So a 50-pip adverse move on a 1-lot trade costs \$500; the same move on a 0.01-lot trade costs \$5.

### 2. Margin required

[[Margin]] required to open the position scales with lot size. At 1:100 leverage on EUR/USD:

- 1.0 lot requires ~\$1,100 margin
- 0.1 lot requires ~\$110
- 0.01 lot requires ~\$11

This is why over-sized lot trades reach [[Margin Call]] faster — more margin locked up means less Free Margin to absorb adverse moves.

### 3. Commission

On accounts that charge [[Commission]], the per-lot rate scales linearly:

- 1.0 lot on ECN (\$6/lot): \$6 commission
- 0.1 lot on ECN: \$0.60 commission
- 0.01 lot on ECN: \$0.06 commission

## Lot size limits at OPO

OPO allows a wide range of lot sizes:

- **Minimum trade size:** 0.01 lots (per account pages, all account types)
- **Maximum total trade size:** Unlimited (per account pages, all account types)
- **Trade size increment:** 0.01 lots
- **Maximum simultaneous open orders:** Unlimited

This is more permissive than many brokers. However, the Client Agreement clauses 12.4 and 12.5 give OPO the right to reject orders that are too large for the current market:

> OPO GROUP LLC. may, at its absolute discretion, change these terms if the Client wishes to make a Transaction larger than Normal Market Size for the specified Instrument.

And:

> OPO GROUP LLC. reserves the right not to accept any offer or to enter a Transaction with the Client, e.g., if OPO GROUP LLC. believes that it will not be able to hedge the proposed Transaction in the Underlying Market, or the proposed Transaction is of such a size (too small or too large), that OPO GROUP LLC. does not wish to accept that Transaction.

In practice, retail traders almost never hit these limits — but high-volume traders placing 50+ lot orders on illiquid instruments may find orders rejected or split.

## How lot size interacts with the High Leverage account

On a [[High Leverage Account|high-leverage account]], lot volume determines which dynamic leverage tier applies. From the Dynamic Leverage Specifications:

| Total open volume | Leverage on FX Major |
|---|---|
| 0–5 lots | 1:2000 |
| 5–20 lots | 1:1000 |
| 20–50 lots | 1:500 |
| 50–100 lots | 1:200 |
| 100+ lots | 1:100 |

So lot size on a high-leverage account is *also* the variable that determines how much leverage you get on each new position. Opening a 4-lot position when you already have 1 lot open puts you into the 5–20 tier for the new position. See [[Leverage]] for the full picture.

## Choosing the right lot size

The right lot size depends on three factors:

**1. Account size.** A common risk-management rule: don't risk more than 1–2% of account equity per trade. For a \$1,000 account, that's \$10–\$20 per trade. If a strategy uses a 30-pip stop loss, the maximum safe lot size is:

**2. Stop Loss distance.** Wider stops require smaller lots to keep dollar risk constant. A trader with a \$20 risk tolerance can place 0.1 lot with a 20-pip stop, but only 0.04 lot with a 50-pip stop.

**3. Volatility of the instrument.** Volatile instruments (crypto, exotic FX, indices during news events) require smaller lot sizes than calm instruments, because price can move further before reaching a Stop Loss.

## Risk warning

Lot size is the single most direct lever for trade risk. Most retail trader losses come not from being wrong about market direction, but from being right in direction with too-large lot sizes — the position size amplifies normal market noise into a loss large enough to trigger emotional decisions or [[Stop Out]]. Beginners are strongly recommended to start with 0.01 lot trades, regardless of account size, until they have a documented track record of consistent risk management. The minimum lot size at OPO is 0.01, which means even a \$100 account can practice realistic trading without risking destructive losses on a single trade. Traders should always calculate the dollar value of their planned lot size *before* placing the trade — not after.

## Source

- OPO Client Agreement v10, Appendix A (Lot, Lot Size, Transaction Size definitions)
- OPO Client Agreement v10, clauses 12.4 and 12.5 (Normal Market Size, right to reject)
- OPO Dynamic Leverage Specifications (lot-based leverage tiers)
- OPO website account type pages (0.01 minimum, unlimited maximum)
- OPO Contract Specifications (per-instrument lot definitions)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction lot conventions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm exact lot units for non-forex instruments at OPO — specifically indices, commodities (oil, gas, agricultural), stocks (CFDs), and the major cryptocurrencies. These should be published in Contract Specifications but are not summarized in a single accessible place for traders
- Confirm whether "Normal Market Size" (clause 12.4) is published anywhere for traders to consult, or whether it's purely an internal threshold
- Confirm whether maximum lot size on dynamic-leverage accounts is capped beyond the 100+ tier or if traders can theoretically open unlimited size at 1:100 leverage
- Consider adding a position-sizing calculator linked from this note — this is one of the highest-value trader tools and OPO does not appear to currently provide one

## Related topics

- [[Lot Size 1]]
- [[Pip]]
- [[Pipette]]
- [[Spread]]
- [[Commission]]
- [[Margin]]
- [[Free Margin]]
- [[Leverage]]
- [[Margin Call]]
- [[Stop Out]]
- [[Stop Loss]]
- [[Base Currency]]
- [[Transaction Size]]
- [[Contract Specifications]]
- [[Normal Market Size]]
