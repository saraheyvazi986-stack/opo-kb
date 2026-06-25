---
title: Leverage
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
# Leverage

## Simple explanation

Leverage is a borrowing arrangement that lets you control a position much larger than the money you've actually deposited. OPO defines it in the Client Agreement Appendix A as:

> Leverage is offered by brokers to maximize traders' buying power by giving them the ability to deposit a small amount of funds and trade larger volumes. Leverage is expressed as a ratio form, so if it is 1:30 for example, a trader's buying power is magnified 30 times.

In plain terms: with 1:100 leverage and $1,000 in your account, you can open positions worth up to $100,000 in market exposure. The broker is effectively letting you "borrow" the difference.

## How leverage works mathematically

When you open a leveraged position, you're not actually borrowing cash — you're entering a contract whose value moves as if you owned the full position size. The broker requires you to put up a fraction of the position size as [[Margin]] (collateral).

Margin required = Position size ÷ Leverage ratio

Example: opening a 1-lot EUR/USD position worth €100,000 at 1:100 leverage:
Margin = 100,000 ÷ 100 = $1,000


So $1,000 of your account is locked as Initial Margin. But your profit and loss is calculated on the **full €100,000** of exposure — not on the $1,000 of margin.

## Why this amplifies both profit and loss

A 1% favourable move in the market produces:

| Without leverage | With 1:100 leverage |
|---|---|
| $1,000 invested → $1,010 (1% gain) | $1,000 margin → $2,000 (100% gain) |
| $1,000 invested → $990 (1% loss) | $1,000 margin → $0 (100% loss — margin wiped out) |

Leverage doesn't change market risk — it changes the **scale of impact** market moves have on your account. The market moved the same 1%. The trader's outcome was wildly different.

This is why the Client Agreement Appendix A definition ends with the explicit warning: *"Leverage provides opportunities for multiplied profits but at the same time one may have multiplied losses as well."*

## OPO offers two leverage models

OPO offers two distinct leverage products, selected at account opening:

### Standard leverage account

A fixed leverage ratio between 1:100 and 1:500, chosen by the trader at account opening. The leverage stays the same regardless of trade size — opening 1 lot or 100 lots uses the same leverage. Available across all account types (Standard, ECN, ECN Pro, Social Trade, Social Pro, Black, cTrader-family).

### High leverage account (Dynamic Leverage)

A **tiered leverage model** where the maximum leverage **decreases automatically as total open lot volume grows**. The trader does not choose a single leverage ratio — the system applies the appropriate tier based on how many lots are currently open across the account, by instrument class.

The "up to 1:2000" advertised maximum is only available at the lowest volume tier (0–5 lots) and only on FX Major instruments. As volume grows or as the trader trades less-liquid instruments, the effective leverage steps down automatically.

## The Dynamic Leverage table

The full dynamic leverage schedule by instrument class and volume tier:

| Instrument class | 0–5 lots | 5–20 lots | 20–50 lots | 50–100 lots | 100+ lots |
|---|---|---|---|---|---|
| FX Major | 1:2000 | 1:1000 | 1:500 | 1:200 | 1:100 |
| FX Minor | 1:1000 | 1:500 | 1:300 | 1:150 | 1:100 |
| FX Exotic | 1:500 | 1:200 | 1:150 | 1:100 | 1:100 |
| XAUUSD (gold) | 1:500 | 1:300 | 1:200 | 1:100 | 1:100 |
| Commodities | 1:300 | 1:200 | 1:150 | 1:100 | 1:100 |
| Indices | 1:300 | 1:200 | 1:150 | 1:100 | 1:100 |
| Cryptocurrencies | 1:50 | 1:30 | 1:20 | 1:10 | 1:10 |

**Important things this table reveals:**

- **Crypto is heavily restricted.** Even at the lowest tier, cryptocurrencies are capped at 1:50 — substantially less than the FX maximum
- **Gold and exotic FX never reach 1:2000.** The "1:2000 maximum" is a Major FX feature only
- **Above 100 lots, leverage is the same as a standard account** across almost all instruments
- **Trading at scale erases most of the leverage advantage.** A trader running 100+ lots of FX Major or gold has 1:100 leverage — the same as a standard-account trader on FX Major

## How dynamic leverage works in practice

When you open a position on a high-leverage account, the system:

1. Calculates your **total open lot volume per instrument class** (e.g. how many FX Major lots you have open in total)
2. Identifies which **volume tier** that total falls into
3. Applies the leverage for that tier to the **new position**

A worked example: Suppose you already hold 8 lots of EUR/USD (which is FX Major) and you want to open another 15 lots.

- Your current total in FX Major: 8 lots — that's the 5–20 lot tier, where leverage is 1:1000
- After opening 15 more lots: 23 lots total — that's the 20–50 lot tier, where leverage is 1:500
- The new position is margined at the 20–50 tier rate (1:500) because that's the tier the post-trade total falls into

So **opening larger positions costs more margin per lot** on a high-leverage account than the headline 1:2000 suggests.

## When OPO automatically changes your leverage

The Client Agreement clause 14.11 and the Dynamic Leverage Specifications document describe scenarios where OPO temporarily adjusts leverage during high-volatility events. These adjustments apply to **newly opened positions** during the specified periods — existing open positions retain their original margin requirements (except during [[Force Majeure]] or exceptional market conditions).

### Gold market breaks

Leverage on gold trading is adjusted **30 minutes before** the daily gold market break.

### Weekends and public holidays

Leverage is adjusted **3 hours before** the market's scheduled closing time. Temporary caps applied to new positions:

- Forex instruments: up to 1:100
- Metals / Indices / Energies: up to 1:50

### Major economic news

Leverage is adjusted **15 minutes before and 10 minutes after** major economic announcements. Temporary caps:

- Forex instruments: up to 1:100
- Metals / Indices / Energies: up to 1:50
- Cryptocurrencies: up to 1:10

### Company financial reports

When the underlying company's financial report is released, leverage is adjusted **30 minutes before stock market close** and **20 minutes before reopening**.

### Dynamic leverage for high-risk clients

OPO also reserves the right (Client Agreement clause 14.11) to apply enhanced margin requirements or trading restrictions to any client categorized as high-risk based on trading behaviour, exposure concentration, abusive practices, latency arbitrage activity, or other risk factors. These restrictions may be applied without prior notice.

See [[Leverage Adjustment Policy]] for the full operational detail on each of these scenarios.

## What "applies only to newly opened positions" actually means

The Client Agreement clause 14.12 states that leverage adjustments apply only to **newly opened positions** and do not retroactively change the margin requirements of existing open positions. So if you already have positions open when a news event approaches, those existing positions keep their original margin. But new positions opened during the restricted window face the lower leverage caps — and your [[Free Margin]] may not be sufficient even if it would have been under your normal leverage.

**Exception:** during a [[Force Majeure]] event or "exceptional market conditions", clause 14.12 gives OPO the right to apply leverage changes to existing open positions too.

## Choosing between Standard and High Leverage

| Factor | Standard Leverage Account | High Leverage Account |
|---|---|---|
| Leverage model | Fixed (you pick once) | Dynamic (decreases with volume) |
| Headline maximum | 1:500 | 1:2000 |
| Real leverage at 50+ lots | Same as chosen (e.g. 1:500) | Often 1:100–1:200 |
| Predictability | High — you know your leverage | Lower — depends on current volume |
| Bonus eligibility | Yes | **No** — bonus programs are not available on high-leverage accounts |
| Best for | Most traders | Small-volume, high-frequency traders who never accumulate large positions |

**Important caveat from the Bonus Programs document (clause 2.11):** High Leverage account holders (High Leverage Standard, High Leverage ECN, High Leverage ECN-PRO) are explicitly excluded from bonus programs. A trader who wants both high leverage and bonuses cannot have both simultaneously.

## How to choose your leverage tier on a Standard account

For traders on a standard leverage account, the chosen leverage ratio is a one-time decision. Higher is not "better" — it's a different risk profile:

| Question | If yes, lean lower leverage | If yes, lean higher leverage |
|---|---|---|
| Are you new to trading? | ✓ | |
| Do you plan to hold positions for days or weeks? | ✓ | |
| Are you a short-term trader (scalping, day trading)? | | ✓ |
| Will you use Stop Loss orders religiously? | | ✓ |
| Have you experienced a Stop Out before? | ✓ | |
| Is the trading account a small portion of your wealth? | | ✓ |
| Is the trading account a meaningful portion of your wealth? | ✓ | |

Most professional traders use far less leverage than their broker offers them — not because they can't access higher leverage, but because they've experienced the downside and prefer to keep [[Margin Level]] comfortably high.

## Leverage and Margin Call / Stop Out

Higher leverage means smaller market moves can trigger [[Margin Call]] and [[Stop Out]]. With 1:2000 leverage, a market move of less than 0.05% against your full-margin position can wipe out your account. With 1:100 leverage, the same wipe-out requires a 1% move — twenty times more market movement.

On a high-leverage account, this means the **earliest trades you place** are the most dangerous — they're at maximum leverage. Once you've built volume and the system has stepped you down to a lower tier, the per-lot risk per trade is reduced — but if a previous trade is still open, it remains at its original margin from when it was opened.

This is why the trading basics chain — [[Margin]] → [[Equity]] → [[Free Margin]] → [[Margin Level]] → [[Margin Call]] → [[Stop Out]] — matters most on high-leverage accounts. The mechanics are identical; the speed at which they trigger is not.

## Risk warning

Leverage is the single most powerful risk amplifier in retail trading. It is the reason a trader can lose their entire deposit on a single bad trade. OPO offers headline leverage up to 1:2000 on FX Major instruments, which is among the highest available in the industry — this is a trader-protection issue, not a feature to be celebrated. Many regulators in major jurisdictions (ASIC, ESMA, FCA) cap retail leverage at 1:30 specifically because high leverage produces extreme retail trader losses. Traders considering high-leverage accounts should understand that the 1:2000 maximum is only available at very small volume on the most liquid instruments — actual leverage on most trades will be lower than the headline number. Traders should be honest about their risk tolerance, their ability to monitor positions in real time, and their willingness to accept that a single fast market move can wipe out the account. OPO's automatic leverage adjustments around news events are protective — they exist because experience shows traders consistently underestimate volatility around those events.

## Source

- OPO Dynamic Leverage Specifications (revised version with reconciled timing/caps)
- OPO Client Agreement v10, Appendix A (Leverage definition)
- OPO Client Agreement v10, clause 14.11 (Leverage Adjustment Policy)
- OPO Client Agreement v10, clause 14.12 (Leverage Adjustment Policy General Provisions)
- OPO Bonus Programs document, clause 2.3 and 2.11 (high-leverage accounts excluded from bonuses; 1:500 maximum under bonuses)
- OPO website account type pages (standard tier 1:100–1:500)
- Last verified: 2026-05-12

## Internal review notes

- The Dynamic Leverage Specifications document (revised version dated 2026) has been reconciled with Client Agreement clause 14.11 — timings and caps now agree. Earlier inconsistencies are resolved
- Confirm SVG-jurisdiction definitions apply globally, or split into region-specific notes when ASIC, FSCA, and Seychelles agreements are obtained — ASIC in particular caps retail leverage at 1:30 by regulation, so the ASIC version of this note will be significantly different
- Confirm the exact list of instruments classified as "FX Major", "FX Minor", and "FX Exotic" for dynamic leverage purposes — these categorizations are not currently documented in the Specifications document
- Confirm the exact instruments triggering the "Significant Economic News" adjustment, and where that list is published
- Confirm whether dynamic leverage adjustments are applied per-instrument-class total or per-account total — the document doesn't make this explicit
- Confirm the auto-adjustment behaviour is identical across MT4, MT5, cTrader, and OpoTrade platforms
- Confirm whether high-leverage account holders receive in-platform notification before each automatic adjustment, or only post-hoc

## Related topics

- [[Margin]]
- [[Initial Margin]]
- [[Free Margin]]
- [[Margin Level]]
- [[Margin Call]]
- [[Stop Out]]
- [[Leverage Adjustment Policy]]
- [[Dynamic Leverage]]
- [[Force Majeure]]
- [[Contract Specifications]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Black Account]]
- [[Negative Balance Protection]]
- [[Bonus Programs]]