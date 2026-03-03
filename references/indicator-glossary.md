# Technical Indicator Glossary

A comprehensive reference for technical indicators, chart patterns, and analysis tools used in the technical analysis skill.

---

## Moving Averages

Moving averages smooth price data to identify trend direction and dynamic support/resistance levels.

### Simple Moving Average (SMA)

The arithmetic mean of a security's price over a specified number of periods.

- **SMA(20)**: Short-term trend. Used for intraday and swing trading.
- **SMA(50)**: Medium-term trend. Key institutional reference.
- **SMA(100)**: Intermediate trend filter.
- **SMA(200)**: Long-term trend. The most widely watched moving average.

**Formula**: SMA = (P1 + P2 + ... + Pn) / n

### Exponential Moving Average (EMA)

Gives more weight to recent prices, making it more responsive to new information.

- **EMA(12)**: Fast EMA, used in MACD calculation.
- **EMA(26)**: Slow EMA, used in MACD calculation.
- **EMA(9)**: MACD signal line.

**Formula**: EMA = Price(today) * k + EMA(yesterday) * (1 - k), where k = 2 / (n + 1)

### Key Moving Average Signals

| Signal | Condition | Interpretation |
|--------|-----------|----------------|
| Golden Cross | 50-day MA crosses above 200-day MA | Bullish long-term signal |
| Death Cross | 50-day MA crosses below 200-day MA | Bearish long-term signal |
| Price above MA | Close > MA | Bullish bias for that timeframe |
| Price below MA | Close < MA | Bearish bias for that timeframe |
| MA Slope Up | MA value increasing | Uptrend confirmation |
| MA Slope Down | MA value decreasing | Downtrend confirmation |
| MA Convergence | Multiple MAs narrowing | Impending breakout |

---

## Momentum Indicators

### RSI (Relative Strength Index)

Measures the speed and magnitude of recent price changes to evaluate overbought or oversold conditions.

- **Period**: 14 (standard)
- **Range**: 0 to 100
- **Overbought**: Above 70
- **Oversold**: Below 30
- **Centerline**: 50 (bullish above, bearish below)

**Formula**: RSI = 100 - (100 / (1 + RS)), where RS = Average Gain / Average Loss over n periods

| RSI Range | Interpretation |
|-----------|----------------|
| 80 - 100 | Extremely overbought, reversal likely |
| 70 - 80 | Overbought, watch for bearish divergence |
| 50 - 70 | Bullish momentum |
| 30 - 50 | Bearish momentum |
| 20 - 30 | Oversold, watch for bullish divergence |
| 0 - 20 | Extremely oversold, reversal likely |

**Note**: In strong trends, RSI can remain overbought (>70) or oversold (<30) for extended periods. Do not treat these levels as automatic reversal signals.

### MACD (Moving Average Convergence Divergence)

Shows the relationship between two exponential moving averages of a security's price.

- **MACD Line**: EMA(12) - EMA(26)
- **Signal Line**: EMA(9) of the MACD Line
- **Histogram**: MACD Line - Signal Line

| Signal | Condition | Interpretation |
|--------|-----------|----------------|
| Bullish Crossover | MACD crosses above Signal | Buy signal |
| Bearish Crossover | MACD crosses below Signal | Sell signal |
| Zero Line Cross Up | MACD crosses above 0 | Bullish momentum shift |
| Zero Line Cross Down | MACD crosses below 0 | Bearish momentum shift |
| Histogram Expanding | Bars getting taller | Momentum strengthening |
| Histogram Contracting | Bars getting shorter | Momentum weakening |

### Stochastic Oscillator

Compares a security's closing price to its price range over a given period.

- **%K (Fast)**: ((Close - Lowest Low) / (Highest High - Lowest Low)) * 100
- **%D (Slow)**: 3-period SMA of %K
- **Standard Settings**: (14, 3, 3)
- **Overbought**: Above 80
- **Oversold**: Below 20

| Signal | Condition | Interpretation |
|--------|-----------|----------------|
| Bullish Crossover | %K crosses above %D below 20 | Buy signal |
| Bearish Crossover | %K crosses below %D above 80 | Sell signal |
| Bullish Divergence | Price lower low, Stochastic higher low | Potential reversal up |
| Bearish Divergence | Price higher high, Stochastic lower high | Potential reversal down |

### ADX (Average Directional Index)

Measures trend strength regardless of direction.

- **Period**: 14 (standard)
- **Range**: 0 to 100
- **Components**: ADX, +DI (positive directional indicator), -DI (negative directional indicator)

| ADX Value | Trend Strength |
|-----------|----------------|
| 0 - 20 | Weak or no trend (range-bound) |
| 20 - 25 | Emerging trend |
| 25 - 50 | Strong trend |
| 50 - 75 | Very strong trend |
| 75 - 100 | Extremely strong trend (rare) |

| Signal | Condition | Interpretation |
|--------|-----------|----------------|
| Bullish Trend | +DI above -DI, ADX rising | Strong uptrend |
| Bearish Trend | -DI above +DI, ADX rising | Strong downtrend |
| Trend Weakening | ADX declining from high levels | Momentum fading |
| No Trend | ADX below 20, DI lines intertwined | Range-bound market |

---

## Volume Indicators

### OBV (On-Balance Volume)

A cumulative volume indicator that adds volume on up days and subtracts volume on down days.

- **Calculation**: If close > previous close, OBV = Previous OBV + Volume. If close < previous close, OBV = Previous OBV - Volume.

| Signal | Condition | Interpretation |
|--------|-----------|----------------|
| Confirmation | OBV rising with price | Uptrend supported by volume |
| Confirmation | OBV falling with price | Downtrend supported by volume |
| Bullish Divergence | Price lower low, OBV higher low | Accumulation, potential reversal up |
| Bearish Divergence | Price higher high, OBV lower high | Distribution, potential reversal down |
| Breakout Validation | OBV breaks to new high/low | Confirms price breakout |

### Volume Moving Average

Compares current volume to its historical average to gauge participation.

- **Standard Period**: 20-day SMA of volume

| Condition | Interpretation |
|-----------|----------------|
| Volume > 150% of average | High conviction move, validates breakouts |
| Volume > 100% of average | Above-average interest |
| Volume < 50% of average | Low conviction, breakouts are suspect |
| Volume spike on reversal candle | Potential climax / exhaustion |
| Declining volume in trend | Trend losing participation |

---

## Volatility Indicators

### Bollinger Bands

A volatility envelope set above and below a moving average using standard deviations.

- **Middle Band**: SMA(20)
- **Upper Band**: SMA(20) + 2 * standard deviation
- **Lower Band**: SMA(20) - 2 * standard deviation

| Signal | Condition | Interpretation |
|--------|-----------|----------------|
| Squeeze | Bands narrowing significantly | Low volatility, big move imminent |
| Expansion | Bands widening | Increased volatility, trend underway |
| Upper Band Walk | Price rides upper band in uptrend | Strong bullish momentum |
| Lower Band Walk | Price rides lower band in downtrend | Strong bearish momentum |
| W-Bottom | Price bounces off lower band twice | Bullish reversal pattern |
| M-Top | Price rejected at upper band twice | Bearish reversal pattern |

### ATR (Average True Range)

Measures market volatility by decomposing the entire range of an asset price for a given period.

- **Period**: 14 (standard)
- **True Range**: Max of (High - Low), |High - Previous Close|, |Low - Previous Close|

**Uses**:

| Application | Method |
|-------------|--------|
| Stop Loss | Entry - (2 * ATR) for longs; Entry + (2 * ATR) for shorts |
| Position Sizing | Risk Amount / ATR = Number of shares |
| Volatility Filter | High ATR = volatile, reduce size; Low ATR = calm, increase size |
| Breakout Validation | Breakout move > 1.5 * ATR is significant |
| Trailing Stop | Trail by 2-3 * ATR behind the price |

---

## Fibonacci Levels

Fibonacci ratios derived from the Fibonacci sequence are used to identify potential support, resistance, and price targets.

### Fibonacci Retracement Levels

Used to identify potential support/resistance during pullbacks within a trend.

| Level | Ratio | Interpretation |
|-------|-------|----------------|
| 23.6% | 0.236 | Shallow retracement, strong trend |
| 38.2% | 0.382 | Moderate retracement, common pullback level |
| 50.0% | 0.500 | Halfway point (not a Fibonacci ratio, but widely used) |
| 61.8% | 0.618 | Golden ratio retracement, key level |
| 78.6% | 0.786 | Deep retracement, last defense before full reversal |

### Fibonacci Extension Levels

Used to project potential price targets beyond the prior swing.

| Level | Ratio | Use |
|-------|-------|-----|
| 100% | 1.000 | Measured move target (equal legs) |
| 127.2% | 1.272 | Conservative extension target |
| 161.8% | 1.618 | Golden ratio extension, primary target |
| 200% | 2.000 | Double measured move |
| 261.8% | 2.618 | Extended target for strong trends |

### Fibonacci Application Rules

1. Draw from swing low to swing high (for uptrend retracements) or swing high to swing low (for downtrend retracements).
2. The 38.2% and 61.8% levels are the most significant.
3. Confluence of Fibonacci levels with other support/resistance (MAs, pivot points) increases reliability.
4. Use extensions to project profit targets after a confirmed breakout.

---

## Candlestick Patterns

Single and multi-candle patterns that signal potential reversals or continuations.

| Pattern | Type | Candles | Signal | Reliability |
|---------|------|---------|--------|-------------|
| Doji | Neutral | 1 | Indecision; potential reversal at trend extremes | Moderate |
| Hammer | Bullish | 1 | Long lower shadow at bottom of downtrend; buyers stepping in | Moderate |
| Inverted Hammer | Bullish | 1 | Long upper shadow at bottom of downtrend; buying interest emerging | Weak-Moderate |
| Shooting Star | Bearish | 1 | Long upper shadow at top of uptrend; sellers stepping in | Moderate |
| Hanging Man | Bearish | 1 | Long lower shadow at top of uptrend; selling pressure building | Weak-Moderate |
| Bullish Engulfing | Bullish | 2 | Large green candle engulfs prior red candle at bottom | Strong |
| Bearish Engulfing | Bearish | 2 | Large red candle engulfs prior green candle at top | Strong |
| Morning Star | Bullish | 3 | Red candle, small body, large green candle at bottom | Strong |
| Evening Star | Bearish | 3 | Green candle, small body, large red candle at top | Strong |
| Three White Soldiers | Bullish | 3 | Three consecutive long green candles with higher closes | Strong |
| Three Black Crows | Bearish | 3 | Three consecutive long red candles with lower closes | Strong |
| Piercing Line | Bullish | 2 | Green candle closes above midpoint of prior red candle | Moderate |
| Dark Cloud Cover | Bearish | 2 | Red candle closes below midpoint of prior green candle | Moderate |
| Tweezer Bottom | Bullish | 2 | Two candles with matching lows at bottom of downtrend | Moderate |
| Tweezer Top | Bearish | 2 | Two candles with matching highs at top of uptrend | Moderate |

### Candlestick Confirmation Rules

1. **Context matters**: A hammer at the bottom of a downtrend is bullish. The same candle in the middle of a range is meaningless.
2. **Volume confirms**: Candlestick patterns with above-average volume are more reliable.
3. **Wait for confirmation**: A reversal candle should be followed by a candle that confirms the direction change.
4. **Higher timeframes are more reliable**: A weekly engulfing pattern is far more significant than a 5-minute engulfing pattern.
