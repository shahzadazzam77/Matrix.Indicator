

# Matrix.Indicator

## Overview

The Matrix Indicator is a multi-purpose TradingView Pine Script tool designed to help traders identify trend direction, buy/sell signals, and trendline breakouts on price charts. It is suitable for both discretionary and algorithmic trading strategies.



### Main Features

- **Buy/Sell Signals**: Uses an ATR-based trailing stop and optionally Heikin Ashi candles to generate buy and sell signals. These are visually marked on the chart and can trigger TradingView alerts.
- **Trendline Detection and Breakouts**: Automatically draws dynamic trendlines based on swing highs and lows, with slope calculated using ATR, standard deviation, or linear regression. Highlights breakout points when price crosses these trendlines.
- **Order Blocks (Bullish & Bearish)**: Highlights bullish and bearish order blocks on the chart. Bullish order blocks are shown in green, bearish in red, helping to identify potential support and resistance zones.
- **Fair Value Gaps (FVG)**: Detects and highlights all fair value gaps (gaps between candles) on the chart. Gaps are removed/filled visually when price returns to the gap area, aiding in gap trading strategies.

### Technical Concepts Used

- **ATR (Average True Range)**: Used for trailing stop calculation and as a slope option for trendlines.
- **Heikin Ashi Candles**: Optional input for smoothing price action in signal generation.
- **EMA (Exponential Moving Average)**: Used for crossover logic in buy/sell signal detection.
- **Swing Highs/Lows**: Identifies pivots for trendline anchoring.
- **Standard Deviation & Linear Regression**: Alternative methods for trendline slope calculation.
- **TradingView Alerts**: Alert conditions are set for both buy/sell signals and trendline breakouts.

## Platform Requirements

- TradingView account (free or paid)
- Access to the TradingView Pine Script editor (web-based)
- Pine Script version 5 (as specified by `//@version=5`)

No additional software or dependencies are required. All logic runs within TradingView's platform.

## Getting Started

1. Open TradingView and log in.
2. Go to the Pine Script editor.
3. Copy the contents of `Indicator.pine` into the editor.
4. Add the script to your chart to visualize its signals.

## File Structure

- `Indicator.pine` — Main Pine Script indicator file

## Usage

- Customize the script as needed for your trading strategy.
- Save and add the indicator to your preferred chart.

No external libraries or packages are needed.

## License
See the [LICENSE](LICENSE) file for license information.
