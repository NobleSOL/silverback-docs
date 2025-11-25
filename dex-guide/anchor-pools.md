# Anchor Pools (Keeta)

Create your own liquidity pools with custom fees on Keeta Network.

---

## What Are Anchor Pools?

Anchor pools are user-created liquidity pools that compete in Keeta's FX anchor aggregator. Unlike standard AMM pools with fixed 0.3% fees, anchor pools let you:

- **Set custom fees** from 0.01% to 10%
- **Earn fees** when swaps route through your pool
- **Compete** with official FX anchors and other user pools

When users swap on the Anchor page, the system automatically routes to the pool offering the best rate — including yours.

---

## Creating an Anchor Pool

### Requirements

- Keythings wallet connected
- Both tokens you want to pair
- 3-5 KTA for transaction fees
- Enough liquidity to be competitive

### Step-by-Step

1. Navigate to **Keeta → My Anchors** page

2. Click **"Create New Anchor Pool"**

3. Fill in the details:

   | Field | Description |
   |-------|-------------|
   | Token A | First token in the pair |
   | Amount A | How much of Token A to deposit |
   | Token B | Second token in the pair |
   | Amount B | How much of Token B to deposit |
   | Fee (bps) | Your fee in basis points |

4. **Review your pool:**
   - Initial price ratio = Amount B ÷ Amount A
   - LP tokens you'll receive = √(Amount A × Amount B)

5. Click **"Create Pool"**

6. **Complete the four-step process:**

   | Step | Action |
   |------|--------|
   | 1 | Backend creates pool account and LP token |
   | 2 | You confirm sending Token A to pool |
   | 3 | You confirm sending Token B to pool |
   | 4 | Backend mints LP tokens to your wallet |

7. **Success!** Your pool is now live and will appear in the Anchor aggregator.

---

## Understanding Fees (Basis Points)

Fees are set in **basis points (bps)**. 100 bps = 1%.

| Basis Points | Percentage | Strategy |
|--------------|------------|----------|
| 10 bps | 0.1% | Aggressive — attract maximum volume |
| 30 bps | 0.3% | Standard — competitive with most pools |
| 50 bps | 0.5% | Moderate — balance volume and earnings |
| 100 bps | 1.0% | Conservative — higher margin, less volume |

### Fee Strategy Tips

- **Check competitors** — Look at existing pools for the same pair
- **Slightly undercut** — Being 5-10 bps lower often wins the trade
- **Balance volume vs margin** — Lower fees = more trades but less per trade
- **Monitor and adjust** — Change fees based on performance

---

## Managing Your Pools

From the **My Anchors** page, you can manage all your pools:

### Update Fee

1. Click **"Update Fee"** on your pool card
2. Enter new fee (1-1000 bps)
3. Confirm the transaction
4. New fee takes effect immediately

> **Tip:** Monitor your 24h volume. If it drops, try lowering your fee. If volume is high and you want more per trade, try increasing slightly.

### Pause Pool

Temporarily stop accepting swaps:

- Pool remains funded
- No swaps will route to your pool
- Resume anytime

Use this when:
- You need to rebalance
- Market conditions are unfavorable
- You're adjusting strategy

### Resume Pool

Reactivate a paused pool to start earning again.

### Close Pool

Permanently close the pool:

1. Remove all liquidity first
2. Close the pool structure
3. Cannot be undone

---

## Pool Analytics

Each pool card displays:

| Metric | Description |
|--------|-------------|
| 24h Volume | Total value swapped through your pool |
| 24h Swaps | Number of trades |
| Fees Collected | Your earnings |
| Current Reserves | Pool balances (Token A / Token B) |

### Reading Your Analytics

- **High volume, low fees collected?** → Consider raising fee
- **Low volume?** → Try lowering fee or adding liquidity
- **Unbalanced reserves?** → Lots of one-way trading, may need rebalancing

---

## Strategy Guide

### Competitive Positioning

Your pool competes for every swap. The aggregator routes to the best rate, considering:

1. **Your fee** — Lower fee = better rate for users
2. **Your liquidity** — More liquidity = less price impact
3. **Current reserves** — Balanced reserves = better rates

### Winning More Trades

1. **Undercut on fees** — Be 5-10 bps lower than competitors
2. **Deeper liquidity** — Add more capital to reduce price impact
3. **Stay balanced** — Imbalanced pools offer worse rates
4. **Popular pairs** — Focus on high-demand token pairs

### Maximizing Earnings

| Strategy | Approach |
|----------|----------|
| Volume Play | Low fees (10-20 bps), high volume |
| Margin Play | Higher fees (50-100 bps), accept lower volume |
| Balanced | Moderate fees (30 bps), steady earnings |

### Risk Management

- **Don't over-concentrate** — Spread across multiple pools
- **Monitor impermanent loss** — Same risks as regular LP
- **Watch for arbitrage** — Large price moves can drain one side
- **Keep reserves balanced** — Add liquidity to lagging side

---

## FAQ

**Can I have multiple anchor pools?**

Yes! Create one pool per token pair. You cannot have two pools for the same pair from the same wallet.

**Can others add liquidity to my pool?**

Not currently. Each user creates and manages their own pools independently.

**What fee should I start with?**

Start at 30 bps (0.3%) — it's competitive with standard AMM pools. Adjust based on performance.

**How do I know if my pool is getting trades?**

Check the 24h Volume and 24h Swaps metrics on your pool card.

**Why isn't my pool getting volume?**

Common reasons:
- Fee is too high compared to competitors
- Not enough liquidity (high price impact)
- Reserves are imbalanced
- Low demand for this token pair

---

## Troubleshooting

**Pool creation failed**
- Verify you have enough of both tokens
- Ensure 3-5 KTA for fees
- Check you don't already have this pair

**LP tokens not received**
- Wait a moment for the final transaction
- If still missing, contact support

**Pool not appearing in aggregator**
- May take a few moments to index
- Ensure pool is not paused
- Verify pool has liquidity
