# AI Agents for Crypto Trading

**Intensive course: 10 sessions**

A course for those who want to build an autonomous trading system powered by AI agents. From installing the tools to a fully autonomous trading system that runs 24/7 on your own server.

Learn more about what it takes for [Artificial Intelligence to trade crypto](https://github.com/Distributed-Validators-Synctems/AI-School/blob/master/AI-crypto-trading.md)

[Payment and other frequently asked questions](https://github.com/Distributed-Validators-Synctems/AI-School/blob/master/FAQ.md)

## How to enroll in the AI School course

Enrollment is now open for a study group with live mentors. To take part:
1. **Fill out the application form:** [Application form](https://forms.gle/H6JGuZuCvZk1wZV2A)
2. **Join the Telegram group:** [AI School RU](https://t.me/+-J39zeyt-s41MWUy)
3. **Write in the chat:** after filling out the form, introduce yourself in the group and mention that the form has been submitted.
---

## Tool stack

- **Environment:** IDE + LLM API
- **Blockchain:** Ethereum / Base L2, Public RPC
- **DEX:** Uniswap V3
- **Execution:** Hummingbot (open-source trading bot)
- **Database:** PostgreSQL
- **Monitoring:** Telegram Bot
- **Infrastructure:** VPS, PM2

---

## Curriculum

### Session 01: GitHub, IDE and LLM API
- Creating a GitHub repository for the trading project
- Installing an IDE and connecting the LLM API
- First crypto script via AI: checking the ETH price
- Security: `.env` and `.gitignore` — why secrets never end up in code
- Result: a working GitHub + IDE + LLM API pipeline

### Session 02: The intelligence of AI agents
- Tokens and context: why an agent "forgets" the rules after working for a long time
- AGENTS.md — the instructions an agent always sees
- Agent Skills — ready-made specializations (code-reviewer, python-expert, senior-architect)
- Designing AGENTS.md for 5 trading agents
- Result: agents have clear roles and don't forget the rules

### Session 03: System architecture and the agent team
- Designing ARCHITECTURE.md: data sources, agents, execution, monitoring
- SPECIFICATION.md: what each component does, its inputs and outputs
- PLAN.md: 6 build phases
- Creating a team of 5 agents: On-Chain, Market, Orchestrator, Risk
- Agents exchange signals through a database
- Testing the chain: signal → orchestrator → risk manager → decision
- Result: a complete architecture and a working team of agents

### Session 04: Blockchain and Uniswap V3
- Ethereum and Base L2: gas, blocks, transactions — what a developer needs to know
- A wallet for the bot: why it should be separate, how to store the private key
- RPC node (free): reading balances, pools, events
- Uniswap V3 under the hood: liquidity pools, swap quotes
- A test swap on Base Sepolia
- Real-time pool monitoring for the On-Chain Agent
- Result: the bot reads the blockchain and can execute a swap

### Session 05: Database
- Creating a PostgreSQL project
- Designing the schema: signals, proposed trades, approved trades, metrics
- Connecting agents to the database: the On-Chain Agent writes signals, the Orchestrator reads them
- Row-Level Security: protecting data from external access
- Result: all signals and trades are stored in a structured way

### Session 06: Hummingbot and the MCP server
- Installing Hummingbot via Docker
- Configuring it for Base + Uniswap V3
- Paper trading with a virtual balance
- Building an MCP server: a bridge between AI agents and Hummingbot
- Test: the agent issues a command → MCP → Hummingbot → swap
- Result: agents control a real trading bot

### Session 07: Backtesting, paper trading and security
- Backtesting the strategy on historical data (30 days)
- Metrics: PnL, Sharpe ratio, win rate, max drawdown, profit factor
- Full system run on paper trading (24+ hours)
- Analyzing the results: which signals are profitable, which are false
- Kill switch: auto-stop when the loss exceeds 5%
- Security audit: private keys, RPC URL, database keys
- Result: the strategy is verified, the system is ready for real money

### Session 08: Telegram bot for monitoring
- Creating the bot
- Commands: `/status`, `/pnl`, `/stop`, `/start`, `/alerts`
- Critical alerts: agent crashed, balance below threshold, abnormal volatility
- Daily automated report every morning at 9:00
- Kill switch via a command from Telegram
- Result: full control of the system from your phone

### Session 09: Deploying to a server
- Buying a VPS (~$4/month)
- Server setup: Ubuntu, Docker, firewall
- Migrating the project: cloning, `.env`, dependencies
- PM2: auto-restart of all agents on failure
- Verification: the system keeps running after disconnecting from SSH
- Server monitoring: CPU, RAM, disk, uptime
- Result: the system runs 24/7

### Session 10: Final project — an autonomous system
- LLM Wiki: agents keep a trade journal in an Obsidian-compatible format
- Auto-compiler: weekly analysis + recommendations for improving strategies
- Auto-improvement: safe changes are applied automatically
- Moving to real money: checklist, minimum deposit ($50-100)
- Presenting the project for your portfolio
- Result: a fully autonomous trading system

---

## What you will build

```
RPC Node → On-Chain Agent → Orchestrator Agent → Risk Agent → Hummingbot → Uniswap
              Market Agent ↗      ↑
            Sentiment Agent ↗    strategies + backtests
```

- **5 AI agents** with specialized roles
- **Hummingbot** — order execution on Uniswap V3 (Base L2)
- **MCP server** — connecting agents to the trading bot
- **Database** — storage for signals, trades, metrics
- **Telegram bot** — 24/7 monitoring
- **Auto-compiler** — weekly analysis and strategy improvements

---

## Differences from the main AI School course

- Crypto context in all examples
- Focus on skills and MCP for crypto trading
- Security: private keys, kill switch, risk limits
