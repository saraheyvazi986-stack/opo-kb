---
title: Margin Call
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
# Margin Call

## Simple explanation

A margin call is the warning state your trading account enters when your [[Margin Level]] falls to a level where the broker becomes concerned that your remaining [[Equity]] is not enough to safely support your open positions. At OPO, the margin call threshold is 80% Margin Level.

**Critical point most traders misunderstand:** OPO is not contractually obliged to actually contact you or issue a warning when your account reaches the margin call level. The "call" in margin call is historic terminology — it does not guarantee a phone call, an email, or any other notification.

## The margin call threshold at OPO

The Client Agreement clause 14.6 states that OPO "is entitled to close the Client's Open Positions without the consent of the Client or any prior Written Notice if the Equity is less than certain rate depending on the account type." The published Margin Call level across all OPO account types is **80%**.

This means: when your Margin Level drops to 80%, your account is in margin call status. Your positions remain open, but you are very close to [[Stop Out]] (the 20% level where positions are forcibly closed).

## Why the warning may not arrive

The Client Agreement clause 14.8 is explicit:

> OPO GROUP LLC. is not obliged to make margin calls for the Client. OPO GROUP LLC. is not liable to the Client for any failure by OPO GROUP LLC. to contact or attempt to contact the Client.

This is a contractually binding statement. Traders cannot rely on receiving a notification at the 80% threshold. In fast-moving markets, an account can move from healthy to Stop Out in seconds, with no margin call warning at any point. This is why **monitoring [[Margin Level]] continuously during active positions is the trader's responsibility**, not the broker's.

## What happens when Margin Level reaches 80%

| Margin Level         | Account state           | What happens                                             |
| -------------------- | ----------------------- | -------------------------------------------------------- |
| Above 100%           | Healthy                 | All positions safe; can open new positions               |
| Between 80% and 100% | Approaching margin call | Free Margin is shrinking; warning territory              |
| At 80%               | Margin Call             | OPO has the right (but no obligation) to issue a warning |
| Between 20% and 80%  | Margin call zone        | Positions can still be managed by the trader             |
| At 20%               | Stop Out                | OPO closes positions automatically                       |

## What the trader should do at margin call

When Margin Level approaches or reaches 80%, the trader has four practical options:

1. **Reduce open position size** — close part of one or more positions to reduce used Margin
2. **Close losing positions entirely** — locks in the loss but stops Margin Level decline
3. **Add funds to the account** — increases Equity directly, raising Margin Level
4. **Avoid opening new positions** — each new position lowers Margin Level further

The wrong move is to "wait for the market to come back" while at 80% Margin Level — if it moves further against the trader, Stop Out triggers and the choice is taken away.

## Why margin call exists

Margin call is not a punishment from the broker — it's a structural feature of leveraged trading. When a trader uses leverage, they control positions much larger than their deposit. If those positions move significantly against the trader, the loss can exceed the deposit. The broker uses Margin Level to detect when an account is heading toward that point and acts to protect both the trader (from owing more than deposited) and the broker (from being unable to recover what the trader owes).

The Client Agreement clause 14.11 (Leverage Adjustment Policy) lists scenarios where OPO pre-emptively reduces leverage to prevent traders reaching margin call during predictable high-volatility events — gold market breaks, weekends and public holidays, major economic news releases, and corporate financial report releases. Even with these protections, traders holding positions through such events can find Margin Level dropping faster than expected because new positions during these windows are subject to tighter leverage caps.

## Risk warning

Margin call is the moment when the broker's automatic risk protections begin to activate. Once Margin Level falls below 80%, the trader is operating in a zone where [[Stop Out]] can trigger without warning. Traders who do not actively monitor Margin Level — especially during volatile periods like economic news releases, market opens, or low-liquidity sessions — can find their accounts closed out with significant losses before they have a chance to react. The Client Agreement explicitly removes any obligation on OPO to provide a margin call warning, so the responsibility to watch the account belongs entirely to the trader.

## Source

- OPO Client Agreement v10, clause 14.6 (right to close positions without consent or notice)
- OPO Client Agreement v10, clause 14.8 (broker not obliged to make margin calls)
- OPO Client Agreement v10, clause 14.11 (Leverage Adjustment Policy)
- OPO website account type pages (80% margin call level)
- Last verified: 2026-05-12

## Internal review notes

- Confirm SVG-jurisdiction terms apply globally, or split when ASIC, FSCA, and Seychelles agreements are obtained
- The 80% threshold is documented on the website but not explicitly in the Client Agreement — the agreement only says "certain rate depending on the account type". Recommend adding the 80% / 20% thresholds explicitly to the Contract Specifications referenced by the agreement, so traders can verify in one authoritative source

## Related topics

- [[Margin]]
- [[Margin Level]]
- [[Equity]]
- [[Free Margin]]
- [[Stop Out]]
- [[Leverage]]
- [[Leverage Adjustment Policy]]
- [[Negative Balance Protection]]
- [[Contract Specifications]]
