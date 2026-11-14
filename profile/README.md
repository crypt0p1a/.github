<div align="center">

# Cryptopia

**Open source tools for crypto trading, written in Rust**

From a complete Kraken Spot client, to a scalping bot running on it, to a team of AI agents that build the next thing.

<br>

[![kraken-rust](https://img.shields.io/badge/kraken--rust-library-5741d9?style=for-the-badge&logo=rust&logoColor=white)](#-kraken-rust)
[![kraken-trading-bot](https://img.shields.io/badge/kraken--trading--bot-bot-0b9a6d?style=for-the-badge&logo=rust&logoColor=white)](#-kraken-trading-bot)
[![hivemind](https://img.shields.io/badge/hivemind-agents-e8a317?style=for-the-badge&logo=rust&logoColor=white)](#-hivemind)

</div>

<br>

## 📚 kraken-rust

> The Kraken Spot REST API in Rust, and in Kotlin and Swift through UniFFI

[![crates.io](https://img.shields.io/crates/v/kraken-spot-api?style=flat-square&logo=rust&label=kraken-spot-api&color=5741d9)](https://crates.io/crates/kraken-spot-api)
![Rust](https://img.shields.io/badge/Rust-000?style=flat-square&logo=rust)
![Kotlin Multiplatform](https://img.shields.io/badge/Kotlin_Multiplatform-7f52ff?style=flat-square&logo=kotlin&logoColor=white)
![Swift](https://img.shields.io/badge/Swift-f05138?style=flat-square&logo=swift&logoColor=white)

- **Every endpoint** of Kraken Spot: market data, account, trading, TWAP, Earn, subaccounts, funding
- **A shared rate limiter**, nonces and signatures handled for you
- **One library, every platform**: Rust, the JVM, Android, iOS, macOS, Linux, Windows

```rust
let limiter = Arc::new(RateLimiter::default());
let public_api = PublicApi::new(RestOptions::default(), limiter.clone())?;
let tickers = public_api.tickers(&["XBTUSD".into()]).await?;
```

**[→ crypt0p1a/kraken-rust](https://github.com/crypt0p1a/kraken-rust)**

<br>

## 📈 kraken-trading-bot

> The only trading bot for scalping you need: Kraken Spot, its terminal dashboard and its notifications on the phone

![Docker](https://img.shields.io/badge/Docker-2496ed?style=flat-square&logo=docker&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003b57?style=flat-square&logo=sqlite&logoColor=white)
![ratatui](https://img.shields.io/badge/ratatui-dashboard-0b9a6d?style=flat-square)
![ntfy](https://img.shields.io/badge/ntfy-notifications-317f6f?style=flat-square)

Each **manager** trades its own budget on one pair with limit orders only: it buys below the market, sells for what it cost plus a margin, fees included, and starts again. Several accounts, virtual managers for the idle money, and a dashboard to follow it all.

<a href="https://github.com/crypt0p1a/kraken-trading-bot"><img src="https://raw.githubusercontent.com/crypt0p1a/kraken-trading-bot/main/assets/screenshots/desk.svg" alt="The dashboard of the bot: key figures, managers, orders, markets" width="100%"></a>

**[→ crypt0p1a/kraken-trading-bot](https://github.com/crypt0p1a/kraken-trading-bot)**

<br>

## 🐝 hivemind

> A company of Claude Code agents — CEO, CTO, developers, marketing — that split the work, ask each other questions and report back to you

![Claude Code](https://img.shields.io/badge/Claude_Code-d97757?style=flat-square&logo=anthropic&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-tools-e8a317?style=flat-square)
![Slack](https://img.shields.io/badge/Slack-4a154b?style=flat-square&logo=slack&logoColor=white)

- **Agents with roles**: each one is a `claude -p` process, on your own Claude subscription
- **They collaborate**: delegate tasks, ask each other, ask you when they need to
- **Follow them** from the CLI, the live dashboard or Slack — `hive demo` runs a simulated company, nothing to configure

<a href="https://github.com/crypt0p1a/hivemind"><img src="https://raw.githubusercontent.com/crypt0p1a/hivemind/main/docs/dashboard.svg" alt="hive dash: a demo company at work" width="100%"></a>

**[→ crypt0p1a/hivemind](https://github.com/crypt0p1a/hivemind)**

<br>

<details>
<summary><b>More repositories</b></summary>

<br>

| Repository | |
|---|---|
| [kotlin-cex-spot-trading](https://github.com/crypt0p1a/kotlin-cex-spot-trading) | the CEX.IO counterpart of kraken-rust |
| [cex-trading-bot](https://github.com/crypt0p1a/cex-trading-bot) | the CEX.IO trading bot that kraken-trading-bot was ported from |
| [cexio-exchange-plus](https://github.com/crypt0p1a/cexio-exchange-plus) | the Node.js client for CEX.IO Exchange Plus API |
| [trade](https://github.com/crypt0p1a/trade) | you wished you knew this repo earlier instead of wasting your money on GPUs |

</details>

<div align="center">
<br>
<sub>Built in the open · contributions and stars welcome ⭐</sub>
</div>
