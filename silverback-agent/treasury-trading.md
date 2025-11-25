# Treasury & Trading

How Silverback manages capital and generates returns.

---

## Treasury Overview

Silverback maintains an on-chain treasury that:

- Provides capital for trading operations
- Funds liquidity provision
- Generates returns for $BACK holders
- Operates transparently on Base

---

## Trading Strategies

Silverback employs multiple strategies to generate returns while managing risk.

### Strategy Categories

| Strategy | Description | Risk Level |
|----------|-------------|------------|
| Cross-Chain Arbitrage | Exploit price differences between networks | Low |
| Liquidity Provision | Earn fees from DEX pools | Low-Medium |
| Perpetuals Trading | Systematic futures strategies | Medium |
| Liquidity Sweeps | Capture inefficiencies in order books | Medium |

### Strategy Selection

The agent selects strategies based on:

- Current market conditions
- Available opportunities
- Risk budget remaining
- Portfolio balance

Not all strategies are active at all times. Silverback adapts to market conditions.

---

## Risk Management

### Core Principle

**Capital preservation comes first.**

Silverback would rather miss opportunities than take losses that damage the treasury.

### Position Sizing

| Rule | Implementation |
|------|----------------|
| Max per trade | 2% of treasury |
| Max correlated exposure | Limited |
| Diversification | Across strategies and assets |

### Stop Losses

Every position has defined exit criteria:

- Price-based stops
- Time-based stops
- Volatility-adjusted stops
- Portfolio-level circuit breakers

### Drawdown Management

If treasury drawdown exceeds thresholds:

1. Reduce position sizes
2. Pause higher-risk strategies
3. Focus on capital preservation
4. Resume normal operation when recovered

---

## Cross-Chain Arbitrage

### How It Works

Operating on both Base and Keeta creates arbitrage opportunities:

```
Price on Base: 1 TOKEN = $100
Price on Keeta: 1 TOKEN = $102

→ Buy on Base, sell on Keeta
→ Capture $2 spread minus fees
```

### Advantages

- **Low risk** — Price discrepancies are factual
- **Fast execution** — Keeta's 400ms settlement
- **Atomic when possible** — Reduce execution risk
- **Consistent returns** — Small but frequent profits

---

## Liquidity Provision

### DEX Liquidity

Silverback provides liquidity to its own DEX:

- Earns swap fees on trades
- Maintains healthy pool depth
- Attracts more traders
- Creates positive flywheel

### Strategic Positioning

- Focus on high-volume pairs
- Optimize fee tiers (V3)
- Rebalance based on market conditions
- Monitor impermanent loss

---

## Perpetuals Trading

### Platform

Silverback uses **Avantis** for perpetuals:

- Zero fees on profitable trades
- Strong backing and liquidity
- Base network native
- Suitable for systematic strategies

### Approach

- Systematic, not discretionary
- Defined entry/exit criteria
- Strict position limits
- No overleveraging

### Risk Controls

| Control | Implementation |
|---------|----------------|
| Max leverage | Conservative limits |
| Position size | Fraction of treasury |
| Stop loss | Always defined |
| Correlation | Monitor exposure overlap |

---

## Performance Reporting

### What's Shared

- **Treasury balance** — Current value
- **Period returns** — Weekly/monthly performance
- **Win rate** — Percentage of profitable trades
- **Drawdown** — Maximum decline from peak
- **Revenue generated** — Contributing to buybacks

### What's Not Shared

- Specific positions in real-time
- Exact entry/exit prices
- Proprietary signal logic
- Upcoming trades

### Why This Balance?

Full transparency on positions would:

- Allow front-running
- Eliminate strategy edge
- Reduce returns for holders

Sharing results without methods provides accountability while maintaining profitability.

---

## Treasury Allocation

General allocation framework:

| Category | Purpose |
|----------|---------|
| Trading Capital | Active strategy deployment |
| Liquidity Reserves | DEX pool provision |
| Stable Buffer | Risk management cushion |
| Buyback Reserve | Accumulated for distributions |

Exact allocations vary based on market conditions and opportunities.

---

## Profit Distribution

When trading generates profits:

1. **Profits accumulate** in treasury
2. **Buybacks execute** — Purchase $BACK from market
3. **Staking pool fills** — Tokens added to rewards
4. **Stakers earn** — Distributed proportionally

See [Revenue Sharing](../back-token/revenue-sharing.md) for full details.

---

## Track Record

Performance metrics will be published regularly once trading operations are fully active.

Key metrics to watch:

- Cumulative returns
- Sharpe ratio (risk-adjusted returns)
- Maximum drawdown
- Win rate by strategy
- Revenue generated for buybacks

---

## FAQ

**Is the treasury audited?**
Treasury is on-chain and publicly viewable. Third-party audits may be conducted for smart contracts.

**What if there are losses?**
Losses reduce treasury and buyback capacity but don't create obligations. Risk management limits downside.

**Can I see all trades?**
Completed trades are visible on-chain. Real-time positions are not disclosed to protect strategy edge.

**How conservative is the trading?**
Very. 2% max per trade, diversified strategies, strict stops. Preservation over aggression.
