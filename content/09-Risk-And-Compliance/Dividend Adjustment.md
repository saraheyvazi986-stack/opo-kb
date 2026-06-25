---
title: Dividend Adjustment
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

# Dividend Adjustments

## Simple explanation

When a stock or index pays a dividend, OPO makes a corresponding adjustment to your CFD position to reflect the economic effect of that dividend. If you're holding a [[Long Position]] on the stock or index CFD, OPO **may credit** your account with an amount equivalent to the dividend, at its sole discretion. If you're holding a [[Short Position]], you're **debited** an amount equivalent to the gross dividend.

This adjustment exists because CFDs are derivative contracts on the underlying instrument, not actual ownership. Without a dividend adjustment, the CFD price would drop on the ex-dividend date (mirroring the real stock's price drop), and long-position traders would lose money equal to the dividend they would have received if they'd owned the underlying stock. The dividend adjustment is intended to help offset this effect, though long position credits are applied at OPO's sole discretion.

The policy is documented in the Client Agreement clause 9.14.

## How dividends work in the underlying market

To understand the CFD adjustment, it helps to understand what happens to the underlying stock:

1. **Declaration date:** the company announces a dividend will be paid (e.g. "$0.50 per share dividend, ex-date June 15, payable July 1")
2. **Ex-dividend date (ex-date):** the cutoff. Anyone who owns the stock at market close on the day *before* ex-date is entitled to the dividend; anyone who buys *on* or after ex-date is not
3. **Stock price drops on ex-date:** the stock typically opens approximately the dividend amount lower than the previous close, reflecting that new buyers won't receive the dividend
4. **Payable date:** the actual cash dividend is paid to entitled shareholders (typically 2–4 weeks after ex-date)

For a CFD trader, only the ex-date matters. The adjustment happens then.

## How OPO applies the adjustment

From the Client Agreement clause 9.14:

> Dividends are adjustments applied by the Company on the open positions of the relevant Underlying Asset of the Instrument as a result of corporate actions of the issuer of the Underlying Asset. Such adjustments will be reflected on the Client's Trading Account.

The mechanics:

- **Trigger:** the ex-dividend date of the underlying stock or index component
- **Timing:** the adjustment is typically posted at OPO's daily rollover (around 17:00 New York time / 21:00 UTC) on the ex-date
- **Amount:** approximately equal to the dividend per share, multiplied by the position size (lots × contract size)
- **Direction:**
  - Long CFD position → OPO may credit the equivalent dividend amount to [[Balance]], at its sole discretion based on internal policies, market conditions, and account activity
  - Short CFD position → gross dividend amount debited from [[Balance]]

The adjustment appears as a separate transaction in trade history, typically labelled "Dividend Adjustment" or similar.

## A worked example

Suppose a trader holds 100 contracts (1 lot) of a CFD on a stock that announces a $0.50 per-share dividend, with ex-date next Tuesday.

| Trader's position | Effect on Monday (day before ex-date) | Effect on Tuesday rollover (ex-date) |
|---|---|---|
| Long 100 shares CFD | Position unchanged; stock close: $50.00 | OPO may credit: 100 × $0.50 = **up to +$50.00** to Balance (discretionary) |
| Short 100 shares CFD | Position unchanged; stock close: $50.00 | Gross dividend debit: 100 × $0.50 = **–$50.00** from Balance |

On Tuesday's market open, the underlying stock typically opens around $49.50 (down approximately the dividend amount). The CFD price reflects this drop. So:

- The **long trader** loses ~$50 in unrealized P/L from the price drop, but may receive up to $50 from the dividend credit if OPO applies one — potentially net zero economic impact
- The **short trader** gains ~$50 in unrealized P/L from the price drop, but pays $50 in gross dividend debit — also net zero economic impact

The dividend adjustment exists specifically to produce this neutral outcome. Without it, long traders would systematically lose money on dividend events, and short traders would systematically profit — neither of which reflects genuine market participation.

## Important characteristics of the adjustment

### Tax withholding may apply to long positions

In some jurisdictions, dividends paid to non-resident shareholders are subject to withholding tax. The Client Agreement clause 9.14 reflects this:

> Such adjustments will be reflected on the Client's Trading Account, taking into account any applicable taxation as imposed by the relevant authority.

In practice: the credit applied to a long CFD position may be **less than** the headline dividend amount, with the difference representing withheld tax. The exact treatment varies by:

- The country issuing the underlying stock
- OPO's tax treaty arrangements
- The trader's jurisdiction (in some cases)

Traders holding long CFDs on US stocks, for example, may receive ~70-85% of the headline dividend due to withholding tax. UK and Hong Kong stocks may have different rates. Traders should not assume they'll receive the full headline dividend on long positions.

### Short positions typically pay the **full** dividend

Short CFD traders generally pay the full dividend amount as a debit (no tax credit applies). This is because the trader is effectively obligated to "deliver" the dividend to whoever holds the long side of the CFD contract, in the same way a short seller of actual stock must pay the dividend to the security lender.

This creates a small asymmetry: short positions can pay more than long positions receive (due to withholding tax reducing the long credit). The difference goes to the broker/system, not to either trader.

### Index CFDs receive proportional adjustments

For index CFDs (S&P 500, FTSE 100, etc.), dividend adjustments happen when component stocks of the index pay dividends. Since indices contain many stocks paying dividends at different times, index CFDs may receive dividend adjustments on many days, with the adjustment amount being a fraction of the headline aggregate.

The complexity makes the adjustments smaller per event but more frequent. Index CFD traders should expect a steady stream of small dividend adjustments rather than occasional large ones.

### Minimum holding period may apply

The Client Agreement clause 9.14 includes important conditional language:

> Such adjustments may be subject to specific eligibility requirements imposed by the Company, including but not limited to a minimum holding period before and/or after the ex-dividend date.

This means OPO may require traders to hold positions for some minimum period (e.g. open before market close the day before ex-date, hold until at least the open after) before the trader is eligible for the dividend adjustment. The exact requirements are not publicly documented in the Client Agreement — traders should check the Contract Specifications for the specific stock or index CFD they're trading.

A trader who opens a long position on the morning of the ex-date specifically to capture the dividend credit may find:
- They're not eligible for the credit (failed minimum-hold requirement)
- The position still suffers the ex-date price drop
- They lose money on what they thought was a "free" dividend trade

This is intentional — OPO discourages "dividend capture" trades that don't reflect genuine market participation.

## When traders care about dividend adjustments

Three categories of traders should pay attention to dividend dates:

**1. Long-term stock CFD holders.** A trader holding a long CFD on a high-dividend stock for several months will accumulate dividend credits as a steady income stream. This is a small but real component of total return.

**2. Short stock CFD positions.** A trader who is short a high-dividend stock pays the dividend on each ex-date. Over time, this is a meaningful cost. Holding a short position through multiple ex-dates can produce dividend debits that exceed any actual market profit.

**3. Index CFD traders.** Frequent small adjustments mean the running P/L can look different than expected. A trader checking their account balance and confused about a small unexplained credit or debit is often seeing a component dividend adjustment.

## Risk warning

Dividend adjustments are economically neutral when the system works correctly — the long trader receives approximately what they lose to the ex-date price drop, and vice versa for short traders. But two real risks apply: (1) withholding tax on long positions can result in receiving meaningfully less than the headline dividend, so the trader's economic outcome may be slightly negative for the day; (2) minimum-holding-period requirements can disqualify dividend-capture strategies, meaning a trader who opens a position specifically to receive the dividend may receive nothing while still suffering the price drop. The dividend adjustment system is not a profit opportunity — attempting to game it through short-term positioning typically results in losses. Traders interested in dividend income should consider whether actually owning the underlying stock (rather than trading CFDs) better matches their goal.

## Source

- OPO Client Agreement v10, clause 9.14 (Dividends)
- OPO Contract Specifications (minimum-hold requirements per instrument, when documented)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction dividend treatment applies globally, or split when ASIC, FSCA, and Seychelles agreements are obtained. Withholding tax rules vary substantially by jurisdiction and source-country combinations
- Document the specific withholding tax rates currently applied for stocks in major jurisdictions (US, UK, EU, Japan, Hong Kong, Australia) — this is the kind of practical information traders need but is rarely published clearly
- Document the specific minimum-holding-period requirements per instrument — the Client Agreement is silent on specifics, leaving this to the Contract Specifications. Centralizing this information would reduce trader complaints
- Confirm whether the dividend adjustment is calculated using the actual declared dividend amount or a broker-determined estimate. Some brokers use the latter, which can cause confusion
- Confirm the exact timing of the adjustment posting — is it at OPO's rollover, at the underlying market's ex-date open, or at the underlying market's open following ex-date?
- Document the small but real asymmetry between long credits (reduced by tax) and short debits (typically full amount) — this is fair, but traders deserve to understand it
- Consider creating a separate sub-note "Index CFD Dividend Mechanics" if index trading becomes a major use case — the per-component-stock adjustment pattern is meaningfully different from single-stock CFDs

## Related topics

- [[Long Position]]
- [[Short Position]]
- [[Open Position]]
- [[Balance]]
- [[Swap]]
- [[Spread]]
- [[Commission]]
- [[Floating Profit/Loss]]
- [[Completed Transaction]]
- [[Contract Specifications]]
- [[Stocks]]
- [[Indices]]
- [[Force Majeure]]
- [[Market Abuse Policy]]