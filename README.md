# Hi, I'm hiddenotebook 👋

I build practical systems with **Python, Linux, Raspberry Pi, APIs and AI**, with a focus on real-time data, automation, observability, investment intelligence and reliable infrastructure.

## 🚀 Featured project: AleyNode

I'm building **AleyNode**, a self-hosted investment-intelligence platform that currently focuses on cryptocurrency spot portfolios and short-horizon futures analysis, with a roadmap toward a broader multi-asset platform.

### Current validated baseline

AleyNode now includes:

- A separated **Market API, Admin API and secondary collector** architecture
- Live/normalized evidence from **Binance, Bybit, OKX, Coinbase and additional secondary adapters**
- Multi-timeframe technical and market-structure analysis
- Long-horizon **Portfolio Guardian** monitoring for spot investments
- Futures microstructure: order book, taker flow, open interest, funding, positioning, liquidations and options context where available
- Per-component freshness, stale-data detection and explicit analysis usability
- A **Python / FastAPI** backend running on Raspberry Pi with Linux and systemd
- Protected remote APIs through **Cloudflare Tunnel / Access**
- An isolated Admin service with a controlled recovery/restart path that remains available while the market service restarts
- A lightweight event-driven market alert watcher that re-checks a fresh full snapshot before notification
- **436 deterministic offline regression tests** protecting the current production behavior
- Git/GitHub-backed development, documentation, validation and rollback practices

The current production deployment remains the working baseline while the next architecture is introduced incrementally behind tests, parity checks and measurable acceptance criteria.

## 🧠 Where AleyNode is going

The active **AleyNode Platform v3** roadmap evolves the project into a shared core with two specialized market arms:

```text
                         AleyNode Core
                              |
              +---------------+---------------+
              |                               |
       AleyNode Crypto                 AleyNode Markets
              |                              IBKR
              +---------------+---------------+
                              |
                    Unified Portfolio Brain
                              |
                         GPT Analyst
                              |
                    Alerts / Risk / Decision
                              |
                    Execution Engine (later)
```

The project runs today in a **human-authorized decision-support mode**, but that is a current operating choice rather than a permanent limitation. The architecture deliberately leaves room for optional assisted, bounded or autonomous execution later, with explicit opt-in, scoped permissions, hard risk limits, auditability, reconciliation and a kill switch.

The design principle is:

> **Data → Analysis → Risk → Decision → Controlled Execution**

## 🔔 Alerting direction

AleyNode already has a lightweight notification-only market watcher. The planned Analyst Alert Orchestrator goes further:

```text
local market trigger
    -> fresh AleyNode re-query
    -> analyst decision agent
    -> second freshness/risk validation
    -> notification
```

The goal is to notify only when fresh, verifiable evidence materially changes risk/reward — not every time a mechanical threshold fires.

## 🧱 What I care about

I prefer systems that are:

- **Reliable** — failures should be visible and bounded
- **Observable** — freshness, health and degraded components should be explicit
- **Recoverable** — operational access should survive service restarts and development mistakes
- **Maintainable** — clear process boundaries, modular integrations and versioned changes
- **Testable** — important behavior should be protected by deterministic regression tests
- **Safe by design** — secrets stay out of repositories and privileged operations stay narrowly scoped

## 🛠 Tech & tools

**Languages**  
Python · C++

**Backend & data**  
FastAPI · REST APIs · WebSockets · real-time market data · local state/persistence

**Systems & hardware**  
Linux · Raspberry Pi · systemd · Arduino

**Infrastructure**  
Cloudflare Tunnel · Cloudflare Access · Git · GitHub

**Areas of interest**  
Automation · AI · Real-time Systems · Data Analysis · Embedded Systems · Market Infrastructure · Portfolio Risk

## 🔧 Current development focus

- Raspberry Pi 5 migration and persistent live-state architecture
- Modular multi-exchange crypto data collection
- Analyst Alert Orchestrator and higher-quality event promotion
- Unified portfolio intelligence across crypto and future listed investments
- IBKR-backed AleyNode Markets architecture
- Data-quality, observability and recovery guarantees
- Progressive path from human-authorized decisions toward optional controlled execution

## 🌱 Philosophy

I use GitHub to build, test, document what I learn and continuously improve the systems I work on.

> **Build. Test. Measure. Improve.**
