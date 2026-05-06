# Connors RSI-2 - Case Study

## Strategy Overview
- **Type:** Public Strategy
- **Timeframe:** Daily
- **Asset Tested:** NQ1!
- **Backtest Period:** Jun 30 1999 – May 6 2026

## Strategy Origin
Connors RSI-2 is a published strategy developed by Larry Connors, documented in "Short Term Trading Strategies That Work" 
(Connors & Alvarez, 2008). This is an independent recreation and backtest on NQ1! daily timeframe to evaluate real-world performance.
Originally meant for SPX, however this is used on NQ futures.

## Strategy Logic
You long when the market has sold off too aggressively (2 period RSI below 5),
because statistically it’s likely to bounce back toward its average, especially if the broader trend is still upward(candles trading above the 200 SMA).
The opposite logic is true for short positions.

## Entry Rules
- **Long:** Close > SMA(200) and RSI(2) < 5
- **Short:** Close < SMA(200) and RSI(2) > 95

## Exit Rules
- **Long Exit:** Close > SMA(5)
- **Short Exit:** Close < SMA(5)
_no fixed SL_

## Simulation Parameters
- **Initial Capital:** $1,000,000
- **Position Size:** 2 contracts (fixed)
- **Commission:** $2.50 per contract
- **Slippage:** 2 ticks

## Parameter Rationale
- **RSI Length (2):** Very short RSI period as it is more sensitive
- **SMA (200):** Long-term trend filter to trade in the corresponding trade direction
- **RSI Overbought (95) / Oversold (5):** Extreme thresholds to ensure higher probability win rate
- **Exit SMA (5):** Short-term average to exit quickly once mean reversion completes

## Backtest Results
| Win Rate | Profit Factor | Sharpe Ratio | Max Drawdown | No. Trades | Backtest Period |
|----------|---------------|--------------|--------------|------------|-----------------|
| 75.50%   |     3.11     |    −0.148    |    5.54%    |    151    | Jun 30 1999 – May 6 2026 |


## Buy & Hold Comparison
| Strategy Return | Buy & Hold Return |
|-----------------|-------------------|
|      32.82%     |     309.55%       |

# EVALUATION

## What Worked
Very high win rate, very good profit factor, low max drawdown in comparison to returns.

## Weaknesses
The strategy did not provide returns higher than the Buy & Hold return, negative Sharpe ratio.

## Backtest Limitations
- The backtest takes into consideration the periods on NQ when trading volume was low.
- A 27 year backtest period would involve market conditions very different from current market conditions(2008 market crash, Covid-19)
- Connors RSI-2 is known to degrade in live trading despite strong historical backtests



---

## Backtest Results - Image
<img width="3360" height="814" alt="image" src="https://github.com/user-attachments/assets/a557defd-9c97-4eea-9d37-4e6cd6b241e0" />

_Green line indicates strategy return. Blue line indicated Buy & Hold return_
