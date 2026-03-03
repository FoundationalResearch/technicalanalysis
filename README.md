# @foundationalresearch/technicalanalysis

[![npm version](https://img.shields.io/npm/v/@foundationalresearch/technicalanalysis)](https://www.npmjs.com/package/@foundationalresearch/technicalanalysis)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)
[![AI Skill](https://img.shields.io/badge/type-ai--skill-purple)](https://github.com/FoundationalResearch/technicalanalysis)

A standalone AI skill for structured technical analysis of financial securities. Provides a complete 6-step methodology that LLM-powered agents use to analyze chart patterns, evaluate indicators, identify divergences, and produce actionable trade setups with defined risk parameters.

## What Is This?

This package contains a **SKILL.md** file and a **reference glossary** that give AI agents (Claude Code, Cursor, Codex, and others) deep expertise in technical analysis. When installed, the agent gains a systematic framework for analyzing any stock, ETF, cryptocurrency, or futures contract using classical technical analysis methods.

This is not a code library. It is a knowledge package -- structured instructions and reference material that an LLM agent reads to perform expert-level technical analysis.

## 6-Step Methodology

The skill guides the agent through a complete technical analysis workflow:

### Step 1: Identify the Trend

Classify the prevailing trend across long-term (weekly/monthly), medium-term (daily), and short-term (intraday) timeframes. Evaluate moving average alignment, higher-highs/higher-lows structure, and golden/death cross signals.

### Step 2: Support and Resistance Levels

Map key price levels using pivot points, moving averages, round numbers, volume profile nodes, and gap levels. Classify each level by strength (strong, moderate, weak) and list confluence factors.

### Step 3: Chart Pattern Recognition

Scan for classical reversal patterns (head and shoulders, double top/bottom, triple top/bottom, rounding top/bottom) and continuation patterns (flags, pennants, wedges, rectangles, cup and handle). Calculate measured move targets for each pattern.

### Step 4: Technical Indicators

Evaluate a full suite of indicators across four categories:

- **Trend**: Moving Averages (SMA/EMA), MACD (12, 26, 9), ADX (14)
- **Momentum**: RSI (14), Stochastic Oscillator (14, 3, 3), Rate of Change
- **Volume**: OBV, Volume Moving Average, Accumulation/Distribution
- **Volatility**: Bollinger Bands (20, 2), ATR (14)

### Step 5: Divergence Analysis

Identify bullish, bearish, hidden bullish, and hidden bearish divergences between price and indicators (RSI, MACD, OBV). Rate divergence strength based on multi-indicator confirmation and timeframe.

### Step 6: Risk Assessment

Synthesize all findings into a concrete trade setup with exact entry point, stop loss (ATR-based), three price targets (T1 conservative, T2 moderate, T3 aggressive), risk-reward ratio (minimum 2:1), and position sizing guidance (1-2% portfolio risk).

## Reference Material

The package includes a comprehensive **indicator glossary** (`references/indicator-glossary.md`) covering:

- **Moving Averages** -- SMA and EMA formulas, standard periods (20, 50, 100, 200), golden cross and death cross definitions
- **Momentum Indicators** -- RSI ranges and interpretation, MACD signals, Stochastic Oscillator setups, ADX trend strength levels
- **Volume Indicators** -- OBV divergence signals, volume moving average thresholds
- **Volatility Indicators** -- Bollinger Band squeeze and expansion signals, ATR-based stop loss and position sizing methods
- **Fibonacci Levels** -- Complete retracement table (23.6% through 78.6%) and extension table (100% through 261.8%) with application rules
- **Candlestick Patterns** -- 15 patterns (Doji, Hammer, Shooting Star, Engulfing, Morning/Evening Star, Three White Soldiers, Three Black Crows, and more) with type, signal direction, and reliability rating

## Package Contents

```
technicalanalysis/
  SKILL.md                          The core skill definition (6-step methodology)
  references/
    indicator-glossary.md           Comprehensive indicator and pattern reference
  README.md                         This file
  LICENSE                           MIT License
  package.json                      Package metadata
```

## Usage

### Claude Code

Add the skill to your project configuration so that Claude Code loads it automatically:

```bash
npm install @foundationalresearch/technicalanalysis
```

Reference the skill in your `.claude/settings.json` or project instructions:

```json
{
  "skills": ["@foundationalresearch/technicalanalysis"]
}
```

Then ask the agent to perform technical analysis:

```
Perform a technical analysis of AAPL using the 6-step methodology.
```

### Cursor

Install the package and reference the SKILL.md file in your Cursor rules or project context:

```bash
npm install @foundationalresearch/technicalanalysis
```

Add to `.cursor/rules`:

```
Use the technical analysis methodology in node_modules/@foundationalresearch/technicalanalysis/SKILL.md
for any chart or price analysis tasks. Reference the indicator glossary in the references/ directory.
```

### Codex

Install the package and include the skill in your Codex agent configuration:

```bash
npm install @foundationalresearch/technicalanalysis
```

Reference the SKILL.md in your agent's system instructions or knowledge base to enable structured technical analysis capabilities.

### Direct Use

You can also copy the SKILL.md and references/ directory directly into any LLM-based project or agent framework that supports markdown-based skill definitions.

## Example Output

When the agent follows this skill, it produces structured output like:

```
## Trend Analysis
AAPL is in a long-term uptrend with price above the 200-day SMA ($178.50).
Medium-term shows bullish MA alignment: Price ($195.20) > 20 EMA > 50 SMA > 200 SMA.
Short-term momentum is consolidating after the recent push to $198.

## Key Levels
| Level   | Type       | Strength | Confluence                        |
|---------|------------|----------|-----------------------------------|
| $200.00 | Resistance | Strong   | Round number, prior rejection     |
| $192.50 | Support    | Strong   | 20 EMA, volume node, prior low    |
| $185.00 | Support    | Moderate | 50 SMA, gap fill level            |

## Indicator Summary
| Indicator    | Value  | Signal  | Notes                            |
|-------------|--------|---------|----------------------------------|
| RSI (14)    | 62.3   | Bullish | Above 50, not yet overbought     |
| MACD        | +1.85  | Bullish | Above signal line, histogram +   |
| ADX (14)    | 28.5   | Trend   | Moderate trending condition       |

## Trade Setup
- Entry: $196.00 on close above the 5-day range high
- Stop Loss: $191.50 (2x ATR below entry)
- T1: $200.00 | T2: $208.50 | T3: $215.00
- R:R Ratio: 1:2.8 (to T2)
- Position Size: Risk 1.5% of portfolio
```

## Related Skills

- **@foundationalresearch/fundamentalanalysis** -- Financial statement analysis, valuation models, and earnings review
- **@foundationalresearch/macroanalysis** -- Macroeconomic analysis, sector rotation, and market regime identification

## Contributing

Contributions are welcome. Please open an issue or pull request on the [GitHub repository](https://github.com/FoundationalResearch/technicalanalysis).

## License

[MIT](./LICENSE) -- Copyright (c) 2026 FoundationalResearch
