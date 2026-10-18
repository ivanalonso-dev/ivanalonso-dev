# Ivan Alonso

**Founder & Software Architect | On-Chain Intelligence | Blockchain & Fintech**

Barcelona, Spain · [ivanalonso.dev@gmail.com](mailto:ivanalonso.dev@gmail.com) · [bcsentinel.ai](https://www.bcsentinel.ai) · [x.com/IvanAlonsoBCSen](https://x.com/IvanAlonsoBCSen) · [github.com/ivanalonso-dev](https://github.com/ivanalonso-dev)

Serial entrepreneur with 25 years of taking companies and projects from zero to full operation, first in construction and real estate, now in blockchain technology. I am the founder and software architect of **BCSentinel AI**, an on-chain intelligence platform that anticipates the public launch of crypto protocols by 137 days on average, and of **Crucible Quant**, a statistically validated crypto alert service running in production with automated subscription billing, plus a series of public quantitative research projects on volatility, market regimes and portfolio construction.

I work the way I have always worked: documented decisions, evidence before conclusions, and the persistence to carry long, complex builds through to completion.

| Metric | Context |
|---|---|
| **137 days** | Average lead time of BCSentinel alerts before public announcement (220+ validated cases) |
| **~25,000 lines · 403 tests** | Python codebase and automated test suite of the BCSentinel core |
| **88.8% vs 75.8%** | Crucible double-alert hit rate vs. usual rate (±8% move in 7 days, 2025–26) |
| **25 years** | Founding, building and running companies across four countries |

---

## Technology Ventures

### EMERGE · BCSentinel AI
**Founder & Software Architect** · 2025 – Present · [bcsentinel.ai](https://www.bcsentinel.ai) · [Public overview](https://github.com/ivanalonso-dev/BCSentinelAIpublic)

Future Formation Intelligence: detects how DAOs, protocols and token economies form on-chain before they become public, for institutional investors.

*Stack:* Python, pytest, SQL (Dune Analytics), Blockscout and Etherscan APIs · Ethereum, Arbitrum, Optimism, Base

- Validated on 220+ historical formation cases: alerts preceded the public announcement by 137 days on average. Four live pre-public formations are under real-time, timestamped monitoring for prospective validation.
- Designed the platform through a formal architecture-governance process: 16 Architecture Decision Records, 21 System Architecture Specifications and 13 Conceptual Design Specifications.
- Built the analytical core in Python: ~25,000 lines across 90+ modules, a multichain wallet-investigation pipeline and 32 specialised engines (formation scoring, confidence, fraud risk, temporal decay, relationship verification, outcome probability), backed by 403 automated tests.
- Built proprietary knowledge libraries from raw chain data: 654 calibrated function selectors and 3,542 contract bytecode hashes, plus a failure-inference engine with six empirically catalogued failure archetypes.
- Defined the go-to-market for quantitative crypto funds and institutional allocators (90+ qualified prospects in five regions); institutional sales begin once the first live case is confirmed.

### EMERGE · Trenchwatch
**Founder & Software Architect** · Oct 2026 – Present · [Public overview](https://github.com/ivanalonso-dev/trenchwatchpublic) · [Open standard](https://github.com/ivanalonso-dev/solana-launch-alerts)

Real-time detection of serial token operators and their bot clusters on Solana launchpads, delivered as alerts to launchpads, wallets, trading terminals and security teams.

*Stack:* Python, SQLite, Solana RPC and WebSockets, REST API, HMAC-signed webhooks, TypeScript · pump.fun, Meteora DBC, Raydium LaunchLab, Bags, Bonk.fun

- Built a live pipeline that decodes token launches across five Solana launchpads and attributes each one to known operators: 33,000+ launches and 280,000+ early purchases recorded, with a median launch-to-alert latency under 4 seconds and zero lost transactions.
- Built an operator registry of 520 serial creators and their linked wallets; 42% of all recorded launches came from creators already in the registry.
- Deployed the platform to a dedicated cloud server in a German data centre (Hetzner Cloud, Ubuntu 24.04): the three real-time collection engines run 24/7 as self-healing systemd services under a non-privileged user, hardened with key-only SSH, a firewall, fail2ban and automatic security updates; API keys and other secrets are kept out of the code repository.
- Structured the data libraries (operator registry, launch and early-purchase database, alert history) as managed assets hosted on external data-centre infrastructure, with hourly sync and daily snapshots to a private repository and a retention policy on raw purchase data, ready to be served and licensed from there.
- Designed an out-of-sample validation framework with frozen snapshots, criteria fixed in writing before measurement and matched comparison against tokens of the same activity level; in an out-of-sample test over 2.6 hours of live data, 68 operator alerts fired a median 3.2 seconds after launch, ahead of 1,202 outside wallets that bought 561 SOL; in flagged launches the creator came out ahead 96% of the time versus 69% for equally active unflagged launches (preliminary).
- Shipped the client layer: Telegram and email alerts, HMAC-signed webhooks with replay protection and retries, a REST API with sandbox and OpenAPI documentation, plus licence, SLA and data-protection templates.
- Published Solana Launch Alerts, an open MIT-licensed standard for launch-risk alerts with TypeScript and Python SDKs verified by 52 automated tests.

### Crucible Quant
**Founder & Developer** · Sep 2026 – Present · [Repository](https://github.com/ivanalonso-dev/crucible-quant) · [Telegram bot](https://t.me/CrucibleQuantBot)

Statistically validated crypto volatility alerts, sold as a subscription Telegram service.

*Stack:* Python, pandas, NumPy, SQLite, Telegram Bot API, Linux

- Researched on six years of data for 30 large-cap assets; 10+ directional strategies tested and rejected, all documented publicly.
- Bootstrap confidence intervals, per-coin base rates and multiple-testing correction: double alerts preceded a ±8% move 88.8% of the time vs. 75.8% (2025–26).
- Shipped end to end in weeks: signal engine, auto-renewing Telegram Stars subscriptions, affiliate programme and a public, self-verifying track record.

---

## Quantitative Research

Every project follows the same protocol: rules and acceptance criteria fixed before testing, in-sample / out-of-sample splits, realistic costs, append-only live logs as forward tests, and failed hypotheses published alongside the results.

### Implied Odds · Polymarket vs Deribit Volatility Study
**Oct 2026** · [Repository](https://github.com/ivanalonso-dev/implied-odds)

Does the prediction-market crowd price Bitcoin volatility like the options market?

*Stack:* Python, pandas, NumPy, SciPy, Matplotlib · Polymarket, Deribit and Binance APIs

- Modelled each daily BTC price-bracket market as a strip of digital options: removed the overround and fitted a driftless lognormal centred on Binance spot (SciPy optimisation) to extract the crowd's implied volatility 24, 12, 6, 3 and 1 hours before settlement.
- Built a 75-day dataset from minute-level Polymarket prices, hourly Deribit DVOL and Binance 1-minute candles; the settlement reconstruction matched Polymarket's official outcome on 100% of days.
- Scored against raw DVOL, time-of-day-adjusted DVOL and adjusted realized volatility with Brier score, log-loss and paired t-tests: Polymarket was significantly more accurate 24 h and 12 h ahead (t up to 3.1); a minute-level lag test found no delay versus spot.
- Published code, figures, a public correction log and bilingual PDF reports (English and Spanish).

### Crypto Regime Series · BTC Regime Detector, Bull and Bear Systems
**Oct 2026** · [btc-regime-detector](https://github.com/ivanalonso-dev/btc-regime-detector) · [crypto-bull-regime-system](https://github.com/ivanalonso-dev/crypto-bull-regime-system) · [crypto-bear-regime-system](https://github.com/ivanalonso-dev/crypto-bear-regime-system)

Detect the Bitcoin market regime, then run a separately validated rule set in each regime.

*Stack:* Python, pandas, NumPy, Plotly · Coin Metrics API (on-chain data, 2010–2026), Binance

- **Regime detector:** compared price filters (200-day MA, MA slope, golden cross, majority vote) with an on-chain filter (MVRV versus its 200-day average) by economic value, in-sample 2012–19 and out-of-sample 2020–26. The MVRV filter returned 48% CAGR with a −33% max drawdown versus 45% / −77% for buy-and-hold, held across all six window lengths tested and flagged the last three cycle tops 2–4× faster than moving averages. Three-state model (strong bull, weak bull, not bull) using the Kaufman efficiency ratio, with an interactive Plotly dashboard.
- **Bull-regime system:** daily Donchian-breakout trend following across 19 coins with ATR initial stops, chandelier trailing exits and 0.5% risk-per-trade sizing. The edge held on 10 coins never used in development (+0.41R per trade, profit factor 2.2); a mean-reversion module and pyramiding were rejected after failing out of sample.
- **Bear-regime system:** trend-following shorts, modelled with funding costs, were rejected (−58% drawdown); on-chain accumulation below MVRV 1 passed the pre-registered criteria but is reported as weak evidence (7 episodes). Default rule: cash.

### Crypto Regime Portfolio
**Oct 2026** · [Repository](https://github.com/ivanalonso-dev/crypto-regime-portfolio)

*Stack:* Python, pandas, NumPy, Matplotlib

- Combined the three systems into a 60/40 core–satellite allocation (regime-gated BTC core plus trend-following satellite) with monthly rebalancing, trading costs and yield on idle cash: out-of-sample Calmar 2.01 versus 1.05 for the detector alone and 1.04 for buy-and-hold BTC. Its −43% full-period drawdown breached the pre-registered −35% limit, and it is reported as not adopted under that rule.
- Stress-tested with retail broker costs (1% per side, as charged by eToro): out-of-sample Calmar fell to 1.34 but stayed above buy-and-hold BTC (1.03) and the detector alone (0.77); the trend satellite absorbed most of the cost.
- Built the operating layer: a cash-ledger CLI, a daily action plan sized to real capital (entries, exits, stop-loss updates) and an HTML dashboard, regenerated by a scheduled daily run.

### Markov Chain Trading Framework
**Developer** ·· [Repository](https://github.com/ivanalonso-dev/markov-quant-dashboard)

Modular Python framework for crypto markets: Markov-chain regime detection, technical indicators, multi-factor scoring, risk management and backtesting.

---

## Business & Leadership

### Construction · Founder & Managing Director, Site Manager, Production Manager
**25 years**

Led complex construction projects as Site Manager and Production Manager, then founded and grew my own construction company from zero to full operation: winning and delivering projects, planning and production control, budgets and cash flow, hiring and leading teams and subcontractors, technical documentation, quality, safety and client relationships.

### Founder · Real-Estate Investment & Development
**Ongoing**

Created and run several companies in property investment and development, building a portfolio in Spain, Andorra and Georgia; currently executing an acquisition in the United States (Cleveland, Ohio). Cross-border structuring, financing, due diligence and asset management.

---

## Skills

- **Engineering:** Python (pandas, NumPy, SciPy, pytest, Plotly, Matplotlib), SQL (Dune Analytics, Google BigQuery), REST APIs, Git, Linux, scheduled automation (Task Scheduler, systemd), software architecture (ADRs, system specifications)
- **Blockchain:** on-chain analytics (Ethereum, Arbitrum, Optimism, Base), contract selectors and bytecode, Safe multisig and governance patterns, MVRV and cycle metrics, Blockscout, Etherscan, Coin Metrics, Solidity fundamentals
- **Quant & data:** pre-registered out-of-sample validation, bootstrap inference, paired t-tests, Brier score and log-loss, implied-volatility extraction, regime detection, trend-following system design (Donchian, ATR), position sizing, Calmar / Sharpe evaluation, portfolio allocation, derivatives and prediction-market data (Deribit, Polymarket, Binance)
- **Business:** company founding and operation, P&L and budgeting, project and team leadership, investment analysis, cross-border operations, go-to-market

---

## Education

- **Master in Blockchain Engineering** · Conquer Academy · In progress
- **Master in Data Science & Artificial Intelligence** · ENEB, Barcelona · In progress
- **Global MBA** · ENEB, Barcelona · In progress
- **Master in Full Stack Development** · Atrium, Barcelona · 2023
- Additional training: Machine Learning · Big Data Algorithms · Trading Systems & Financial Markets · Solidity · [IBM Python Certificate](https://www.credly.com/badges/a60b90a4-4e4c-4c55-ac0b-213e347bde0c/public_url)

---

## Music

Professional orchestra conductor. Guest conductor of the Lithuanian State Symphony Orchestra, the Cyprus Symphony Orchestra, Tokyo Sinfonia and the Dubrovnik Symphony Orchestra.

- **Bachelor's and postgraduate degrees in Piano and Chamber Music** · Conservatori Superior de Música del Liceu (Barcelona) and École Normale de Musique de Paris Alfred Cortot
- **Master in Orchestral Conducting**
- **Extension Course in Orchestral Conducting** · The Juilliard School (New York)

---

**Languages:** Spanish (native) · English (fluent)
