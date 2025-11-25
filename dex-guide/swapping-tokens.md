# Swapping Tokens

Complete guide to swapping tokens on Silverback DEX.

---

## Base Network Swaps

### How It Works

When you swap on Base, Silverback automatically:

1. Checks our native liquidity pools
2. Queries OpenOcean aggregator for better rates
3. Routes your trade through the best path
4. Executes with optimal pricing

### Step-by-Step

1. Navigate to the **Swap** page
2. Select **Base** network from the dropdown
3. Choose your **input token** (what you're selling)
4. Choose your **output token** (what you're buying)
5. Enter the amount you want to swap
6. Review the quote:
   - Exchange rate
   - Price impact
   - Slippage tolerance
7. Click **"Swap"**
8. Approve the transaction in your wallet
9. Wait for confirmation (~2 seconds)

### Adjusting Slippage

Click the gear icon ⚙️ to adjust slippage tolerance:

| Setting | Use Case |
|---------|----------|
| 0.1% | Very stable pairs (stablecoins) |
| 0.5% | Default — works for most trades |
| 1-3% | Volatile tokens or larger trades |
| 5%+ | Very volatile or low liquidity tokens |

> **Warning:** Higher slippage means you may receive fewer tokens. Only increase when necessary.

---

## Keeta Network Swaps

Keeta offers two swap methods:

### Option 1: AMM Pool Swaps

Standard automated market maker swaps through Silverback's liquidity pools.

1. Navigate to **Swap** page
2. Select **Keeta** network
3. Select tokens and enter amount
4. The app finds the best pool automatically
5. Click **"Swap"**
6. Confirm in Keythings wallet

**Settlement: ~400ms**

### Option 2: FX Anchor Swaps

Access both official Keeta FX anchors and user-created Silverback pools through one interface.

1. Navigate to **Keeta → Anchor** page
2. Select your token pair
3. Enter swap amount
4. View available quotes:
   - 🔵 **Blue quotes** = Official FX Anchors
   - 🟠 **Orange quotes** = Silverback user pools
5. Best rate is auto-selected (you can choose manually)
6. Click **"Swap"**

**Two-Transaction Process:**

| Step | What Happens |
|------|--------------|
| TX1 | You sign to send tokens to the pool |
| TX2 | Backend automatically sends output tokens to you |

Both transactions are required for the swap to complete.

---

## Understanding Price Impact

Price impact measures how much your trade affects the market price.

### Why It Matters

Large trades relative to pool liquidity will "move" the price against you. The bigger your trade, the worse your effective rate.

### Reading Price Impact

| Impact | Status | Recommendation |
|--------|--------|----------------|
| < 0.1% | 🟢 Excellent | Trade freely |
| 0.1% - 1% | 🟢 Good | Normal range |
| 1% - 3% | 🟡 Moderate | Consider smaller size |
| 3% - 5% | 🟠 High | Split into multiple trades |
| > 5% | 🔴 Very High | Find deeper liquidity |

### Reducing Price Impact

- **Smaller trades** — Split large orders into multiple smaller ones
- **Different pairs** — Route through intermediate tokens (ETH → USDC → TARGET)
- **Wait for liquidity** — Pools may have more liquidity at different times
- **Use Anchors (Keeta)** — Check anchor page for alternative pools

---

## Token Approvals

### What Are Approvals?

ERC-20 tokens require you to "approve" a smart contract before it can spend your tokens. This is a security feature.

### How It Works

1. First time trading a token → Approval transaction required
2. Approve once per token per contract
3. After approval, you can trade that token freely

### Approval Options

- **Exact amount** — Only approve the amount you're trading (most secure)
- **Unlimited** — Approve infinite spending (more convenient, less secure)

> **Security Tip:** For maximum security, approve only the amount you need. For convenience with tokens you trade often, unlimited approval saves gas on future trades.

---

## Swap Settings

Access settings via the gear icon ⚙️:

| Setting | Description | Default |
|---------|-------------|---------|
| Slippage Tolerance | Max price movement accepted | 0.5% |
| Transaction Deadline | Time before trade expires | 20 minutes |
| Expert Mode | Bypass confirmation warnings | Off |

---

## Tips for Better Trades

1. **Check price impact** before confirming
2. **Compare rates** between AMM and Anchor swaps on Keeta
3. **Trade popular pairs** for better liquidity and rates
4. **Avoid trading during high volatility** unless necessary
5. **Split large trades** to minimize price impact
