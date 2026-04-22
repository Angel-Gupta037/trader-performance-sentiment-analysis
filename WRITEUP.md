# Trader Performance vs Market Sentiment - Analysis Summary

## Methodology

**Data:**
- Fear & Greed Index: Daily Bitcoin sentiment (Fear/Greed/Neutral)
- Hyperliquid Trader Data: Individual trades with PnL, size, side, leverage
- 
**Preparation:**
- Converted timestamps to daily level
- Aggregated per trader per day: total PnL, trade count, win rate, avg position size, long/short ratio
- Merged sentiment data (inner join on date)

**Analysis:**
- Compared performance metrics (PnL, win rate, loss rate) across Fear/Greed days
- Analyzed behavioral changes (frequency, position size, long/short bias)
- Segmented traders by volume, frequency, and profitability

## Key Insights

**1. Performance differs by sentiment**
- Greed days: Higher PnL and win rate
- Fear days: Lower PnL, higher loss rate (52% vs 38%)

**2. Behavior reverses on Greed days**
- Trade frequency drops by 28.5 trades/day
- Long ratio decreases 52% → 47% (shift to short bias)
- Total volume decreases by $185M

**3. Segments behave differently**
- High volume traders outperform low volume by 292% on Fear days (vs 49% on Greed)
- Frequent traders outperform on Fear (+93%) but underperform on Greed (-23%)
- Profitable traders have LOWER win rates (28% vs 37% on Greed) - win rate alone is misleading

## Strategy Recommendations

1. **Segment by sentiment before analysis** - Relationships reverse between Fear and Greed days. Do not use one-size-fits-all models.

2. **Don't trust win rate alone** - Use PnL per trade or risk-reward ratios instead of win rate as a standalone metric.

## Visualizations

All charts available in `/charts` folder.
