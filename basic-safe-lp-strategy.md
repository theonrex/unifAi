---
description: >-
  A low-risk liquidity strategy that focuses on high-quality, active SOL pools.
  Small, diversified allocations with stop-loss, take-profit, and weekly
  compounding help your capital grow steadily and saf
---

# Basic Safe LP Strategy



```markup
Every 4h:
Find DLMM pools with the following criteria:
FDV: >= $20,000,000 and <= $250,000,000
TVL: >= $1,000,000
Liquidity: >= $500,000
24h fees: >= $3,000
Quote Token: SOL
Base Fee: >= 0.8%
Bin step: >=60 and <=180
24h Volume/TVL: >= 5%
Base Token Age: >= 7 days
Base Token 24h Volume: >= $1,000,000
Base Token 7d Volume Growth%: > 0
Base Jupiter Organic Score: >= 70

Only keep one pool per token: keep the one with the higher 24h volume
Only if all the above conditions are met, and the estimated transaction cost (including slippage) is < 1% of the intended position size, proceed to add liquidity. Otherwise, skip.
If token already exists in current positions, do not add again.

If the selected pool satisfies all conditions, and the current number of positions is less than 2, proceed to add liquidity:
Size: 0.008 SOL per pool (diversify more broadly)

Strategy: 50% single-sided SOL bid position (set to sell SOL with a range 5% above the current price), 50% balanced "spot strategy" range (±4% from the current market price)
Real-time stop loss: PnL% -5%
Real-time take profit: PnL% +12%

Out of range: If current pool price moves ±4% outside the position range, remove liquidity and claim fees. Immediately re-run the pool selection analysis to find another qualified pool. If a new pool is found, open a new position. If not, hold the capital in SOL.
Weekly auto-compound: Add earned fees back into the same pool. Direct the capital to the liquidity range that currently has the highest TVL and volume.
Apart from take-profit, stop-loss, out-of-range, or rotation triggers, do not remove liquidity under any other conditions.
```

## **Strategy Explanation**

This strategy is designed for safe but consistent returns while minimizing risks that most LPs face. Let’s break it down:

### 1. Pool Selection (Every 4h Check)

We only enter pools that are healthy and sustainable:

* FDV between $20M–$250M → avoids tiny meme coins and overvalued large caps.
* TVL ≥ $1M & Liquidity ≥ $500K → ensures there’s enough depth, reduces risk of sudden rug pulls or slippage.
* Strong trading activity: 24h Volume/TVL ≥ 5% → means traders are actually using the pool, so fees will flow.
* Token maturity: Age ≥ 7 days + positive 7d volume growth → filters out brand new, untested tokens.
* High quality scoring: Jupiter Organic Score ≥ 70 → extra safeguard against risky pools.\


### Result: You only LP in active, liquid, and trusted pools not ghost pools or scams.

***

### 2. Capital Allocation & Diversification

* Max 3 pools at a time → spreads risk without overextending.
* 0.3 SOL per pool → smaller chunks = less risk if one pool underperforms.
* Balanced strategy: 50% SOL single-sided + 50% range LP → lowers impermanent loss while still farming fees.

This way, you’re not putting “all your SOL in one basket.”

***

### 3. Risk Controls (Active Protection)

* Stop loss: -5% PnL → cuts losers early, prevents heavy drawdowns.
* Take profit: +12% PnL → locks in winners instead of waiting for reversals.
* Out-of-range check: ±4% → if market moves too far, exit and rotate to stronger pools.\


These rules protect LPs from being trapped in dead pools.

***

### 4. Compounding (The Hidden Edge)

* Weekly auto-compound: All earned fees are reinvested into the best performing pool.\

* Over time, this small adjustment boosts effective APR significantly compared to just letting rewards sit idle.\


Many LPs ignore this, but compounding is how you turn steady returns into exponential growth.

***

### 5. Why This Strategy Works

* Safer entry: Only high-liquidity, high-activity pools qualify.\

* Lower risk: Small allocations + strict stop-loss.\

* More consistent returns: Balanced LP + compounding fees.\

* Adaptability: Every 4h scans keep you in the best pools, not lagging ones.

This is a risk-aware LP strategy that any liquidity provider can follow to maximize rewards without gambling their capital.

***

### This strategy is built on three timeless principles of LP survival:

1. **Capital Preservation First**\
   Most LPs lose because they chase APR without considering drawdowns. By narrowing your pool selection to strong TVL + mid-cap FDV tokens, you’re avoiding “pump-and-dump” coins and protecting your liquidity. This keeps your capital safer than chasing meme pools.
2. **Smarter Entry & Exit (Timing Layer)**\
   Instead of just “set and forget,” this strategy tracks volatility and price momentum before deploying liquidity. That means you’re entering pools when they’re stable and exiting when they show signs of bleeding. It’s not just about returns — it’s about avoiding unnecessary loss.
3. **Compounding Returns (Hidden Edge Most Ignore)**\
   The overlooked part: many LPs let rewards sit idle. Here, rewards are compounded back into the strongest pools every 24h. That little edge means while others earn 10–12% APR, you could effectively push 15–18% APR just by recycling rewards.

### Why should LPs choose this?

Because it balances safety + profitability. Instead of “all risk, high return” or “all safety, low return,” this strategy hits the middle ground, keeping your capital alive while still growing steadily. Over weeks, the compounding effect turns “small wins” into big cumulative profits.

\
