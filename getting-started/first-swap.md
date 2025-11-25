# Your First Swap

Complete your first token swap on Silverback DEX.

---

## On Base Network

### Step-by-Step

1. **Connect your wallet** (see [Connect Your Wallet](connect-wallet.md))

2. **Navigate to Swap**
   - Click "Swap" in the navigation menu
   - Ensure "Base" is selected in the network dropdown

3. **Select your tokens**
   - **From**: Choose the token you want to sell
   - **To**: Choose the token you want to receive

4. **Enter amount**
   - Type the amount you want to swap
   - The output amount will auto-calculate

5. **Review the details**
   - **Exchange Rate**: How many output tokens per input token
   - **Price Impact**: How much your trade affects the market price
   - **Minimum Received**: Accounting for slippage

6. **Adjust slippage (optional)**
   - Click the gear icon ⚙️
   - Default is 0.5%
   - Increase for volatile tokens or large trades

7. **Approve token (first time only)**
   - If this is your first time trading this token, you'll need to approve it
   - Click "Approve" and confirm in your wallet
   - This is a one-time transaction per token

8. **Execute the swap**
   - Click "Swap"
   - Review the confirmation popup
   - Confirm the transaction in your wallet

9. **Wait for confirmation**
   - Transaction typically confirms in ~2 seconds on Base
   - You'll see a success message when complete

> **Pro Tip:** Silverback automatically routes through our pools and OpenOcean to find you the best rate.

---

## On Keeta Network

### Option 1: AMM Swap

1. **Connect Keythings wallet**
2. **Select Keeta network** from the dropdown
3. **Navigate to Swap page**
4. **Select tokens and amount**
5. **Click "Swap"**
6. **Confirm in Keythings wallet**
7. Done! Settlement is ~400ms

### Option 2: Anchor Swap (Often Better Rates)

1. **Navigate to Keeta → Anchor** page
2. **Select your token pair**
3. **Enter the amount** you want to swap
4. **View available quotes:**
   - 🔵 **Blue** = Official FX Anchors
   - 🟠 **Orange** = Silverback user pools
5. The best rate is **automatically selected**
6. **Click "Swap"**
7. **Sign two transactions:**
   - TX1: Send your tokens to the pool
   - TX2: Backend sends output tokens to you
8. Done!

---

## Understanding the Swap Interface

### Price Impact

Price impact shows how much your trade will move the market price.

| Impact | Meaning |
|--------|---------|
| < 0.1% | Excellent — minimal impact |
| 0.1% - 1% | Good — normal for most trades |
| 1% - 5% | Moderate — consider splitting into smaller trades |
| > 5% | High — you may want to reduce size or find more liquidity |

### Slippage Tolerance

The maximum price movement you'll accept between submitting and execution.

- **0.5%** — Default, good for stable pairs
- **1-3%** — Better for volatile tokens
- **5%+** — Only for very volatile or low-liquidity tokens

If price moves more than your tolerance, the transaction will fail (protecting you from bad fills).

---

## Common Issues

**"Insufficient Balance"**
- Make sure you have enough of the input token
- Remember you need ETH (Base) or KTA (Keeta) for gas fees

**"Price Impact Too High"**
- Your trade is too large relative to pool liquidity
- Try a smaller amount or split into multiple trades

**"Transaction Failed"**
- Increase slippage tolerance
- Make sure you have enough gas
- The price may have moved — try again

See [Troubleshooting](../faq-troubleshooting/troubleshooting.md) for more help.
