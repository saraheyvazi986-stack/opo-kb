---
title: Transaction Size
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
# Transaction Size

## Simple explanation

Transaction Size is the total quantity of an instrument involved in a single trade, measured in units of the [[Base Currency]] (for forex) or the relevant unit for other instruments (troy ounces for metals, contracts for indices, shares for stocks, units for crypto). It is the product of [[Lot]] count and [[Lot Size 1]].

OPO defines transaction size in the Client Agreement Appendix A as:

> Lot Size multiplied by the number of Lots.

In plain terms: if you trade 2 lots of EUR/USD and 1 standard lot = 100,000 EUR, your Transaction Size is **200,000 EUR**.

## The formula
Transaction Size = Number of Lots × Lot Size

Examples:

| Trade | Lots | Lot Size | Transaction Size |
|---|---|---|---|
| 1 lot EUR/USD | 1.0 | 100,000 EUR | 100,000 EUR |
| 0.5 lot GBP/USD | 0.5 | 100,000 GBP | 50,000 GBP |
| 0.1 lot XAU/USD | 0.1 | 100 troy oz | 10 troy oz |
| 2 lots EUR/USD | 2.0 | 100,000 EUR | 200,000 EUR |

## Why Transaction Size matters

Three things scale directly with Transaction Size:

1. **[[Margin]] requirements.** Both [[Initial Margin]] and [[Necessary Margin]] are calculated from Transaction Size, divided by leverage.

2. **[[Pip]] value.** The dollar value of each pip movement is proportional to Transaction Size. Doubling the Transaction Size doubles the pip value.

3. **Commission and spread cost.** [[Commission]] is charged per lot; [[Spread]] cost scales with Transaction Size.

## OPO's right to limit Transaction Size

The Client Agreement clauses 12.4 and 12.5 give OPO discretion to limit trades that exceed normal market size:

> OPO GROUP LLC. may, at its absolute discretion, change these terms if the Client wishes to make a Transaction larger than Normal Market Size for the specified Instrument.

And:

> OPO GROUP LLC. reserves the right not to accept any offer or to enter a Transaction with the Client, e.g., if OPO GROUP LLC. believes that it will not be able to hedge the proposed Transaction in the Underlying Market, or the proposed Transaction is of such a size (too small or too large), that OPO GROUP LLC. does not wish to accept that Transaction.

In practice, retail-sized trades rarely trigger these limits. High-volume traders placing very large orders on illiquid instruments may find orders rejected, partially filled, or executed in tranches.

## Transaction Size and the High Leverage account

On a [[High Leverage Account|high-leverage account]], total Transaction Size across an instrument class determines which dynamic leverage tier applies — see [[Leverage]] for the full table. This is why "Transaction Size" is more than just a label; it's a parameter the broker uses to set risk terms on every new trade.

## Source

- OPO Client Agreement v10, Appendix A (Transaction Size, Normal Market Size definitions)
- OPO Client Agreement v10, clauses 12.4 and 12.5 (right to limit by size)
- OPO Dynamic Leverage Specifications (lot-based leverage tiers)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction definitions apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- Confirm what OPO considers "Normal Market Size" per instrument — this is referenced in clause 12.4 but not publicly defined
- Confirm whether Transaction Size limits apply differently to manual orders vs Expert Advisor / cBot-placed orders

## Related topics

- [[Lot]]
- [[Lot Size 1]]
- [[Base Currency]]
- [[Margin]]
- [[Initial Margin]]
- [[Pip]]
- [[Commission]]
- [[Spread]]
- [[Leverage]]
- [[Normal Market Size]]
- [[Contract Specifications]]