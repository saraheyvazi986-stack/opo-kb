---
title: Meta Trader 4
status: draft
audience: client
category: accounts
region: global
language: en
owner: product
reviewer:
last_reviewed:
effective_from: 2026-05-18
source_type: official
ai_allowed: false
risk_level: low
version: "1"
---

# MetaTrader 4

## Simple explanation

MetaTrader 4 (MT4) is the industry-standard forex trading platform developed by MetaQuotes. It's the most widely used retail trading platform in the world, prized for its reliability, large library of Expert Advisors (EAs) for automated trading, and a deep ecosystem of custom indicators and add-ons. At OPO, MT4 is the classic platform choice for traders focused on forex and CFD trading.

## Why traders choose MT4

- **Mature, well-documented platform.** MT4 has been around since 2005, so traders coming from any other broker already know how it works.
- **Largest EA library.** Most published automated trading systems target MT4. If you use third-party EAs, MT4 is the default platform.
- **Lightweight and stable.** Runs reliably on older computers and in low-bandwidth environments.
- **Customizable.** Thousands of custom indicators, scripts, and EAs available through the MQL5 marketplace.

## Key features

| Feature              | MT4 at OPO                                             |
| -------------------- | ------------------------------------------------------ |
| Execution type       | Market                                                 |
| Technical indicators | 30+ built-in (50+ per the OPO MT4 page — to reconcile) |
| Time frames          | 9 (1 minute to 1 month)                                |
| Algorithmic trading  | Yes — Expert Advisors (EAs) written in MQL4            |
| Strategy backtesting | Yes — built-in Strategy Tester                         |
| Economic calendar    | Yes — 9 events listed                                  |
| Pending order types  | 4 (Buy Limit, Sell Limit, Buy Stop, Sell Stop)         |
| Hedging              | Supported                                              |
| One-click trading    | Supported                                              |
| Custom indicators    | Supported (MQL4)                                       |
| Scripts              | Supported (MQL4)                                       |
| Trade copying        | Via third-party tools                                  |

## Asset classes available

Through MT4 at OPO, traders can access:

- [[Forex]]
- [[Metals]]
- [[Stocks]]
- [[Indices]]
- [[Commodities]]
- [[Cryptocurrencies]]

## Accessibility

MT4 is available on:

- **Windows desktop** — full-featured native application
- **macOS desktop** — native application
- **Web Terminal** — browser-based, no installation required (per OPO product team)
- **iOS mobile app** — via the App Store
- **Android mobile app** — via Google Play

Note: MT4 is not available through OPO's own mobile app — that integration is exclusive to OpoTrade.

## Available account types

MT4 supports the following OPO accounts:

- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Social Trade Account]]
- [[Social Pro Account]]
- [[Black Account]]

cTrader-family accounts are not available on MT4.

## Strengths

- Most reliable platform for EA-based automated trading
- Familiar interface for traders coming from other brokers
- Vast library of third-party tools, indicators, and EAs
- Lightweight — runs well on modest hardware

## Limitations

- Only 9 timeframes (MT5 has 21)
- 30+ indicators built-in (MT5 has 80+)
- Single-asset architecture — less suited for traders mixing forex, stocks, and other asset classes in one account
- No native depth-of-market view
- Cannot trade stocks with full exchange-style functionality (MT5 handles this better)
- MetaQuotes (the platform vendor) has shifted development focus to MT5, so MT4 receives fewer new features

## How to download

MT4 is downloaded from MetaQuotes directly:

- Windows: https://download.mql5.com/cdn/web/metaquotes.ltd/mt5/mt5setup.exe (note: as of May 2026, the OPO compare-platforms page incorrectly links the MT4 desktop download to the MT5 installer — confirm correct MT4 installer URL with web team)
- macOS: same caveat applies
- iOS: https://apps.apple.com/tr/app/metatrader-4/id496212596
- Android: https://play.google.com/store/apps/details?id=net.metaquotes.metatrader4

After downloading, traders need their OPO login credentials and server name to connect to their account.

## Risk warning

Using MT4 (or any trading platform) does not reduce market risk. CFD and leveraged product trading carries a high level of risk regardless of which platform is used. Traders should ensure they understand MT4's order execution behaviour, especially around hedging, requoting, and slippage, before trading real capital. Automated trading via EAs carries additional risks — an EA can execute many trades very quickly and amplify losses if its logic is flawed or market conditions fall outside what it was designed for.

## Source

- Official MT4 page: https://opo.com/meta-trader-4
- Platform comparison page: https://opo.com/compare-platforms
- Last verified: 2026-05-12


## Related topics

- [[Platforms Overview]]
- [[MetaTrader 5]]
- [[cTrader]]
- [[OpoTrade]]
- [[Standard Account]]
- [[ECN Account]]
- [[ECN Pro Account]]
- [[Expert Advisors]]
- [[How to choose the right platform]]