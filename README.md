


# Matrix Indicator

## Overview


The Matrix Indicator is a comprehensive TradingView Pine Script v5 tool designed to help traders identify:
- Trend direction
- Buy/sell signals
- Trendline breakouts
- Order blocks (bullish & bearish)
- Fair Value Gaps (FVG)
- Automatic Fibonacci extension levels

It is suitable for both discretionary and algorithmic trading strategies.




### Main Features

- **Buy/Sell Signals**: ATR-based trailing stop and optional Heikin Ashi candles generate buy and sell signals, visually marked on the chart and available for TradingView alerts.
- **Trendline Detection and Breakouts**: Dynamic trendlines based on swing highs/lows, with slope options (ATR, standard deviation, linear regression). Breakout points are highlighted when price crosses trendlines.
- **Order Blocks (Bullish & Bearish)**: Highlights bullish (green) and bearish (red) order blocks, helping to identify potential support and resistance zones.
- **Fair Value Gaps (FVG)**: Detects and highlights all fair value gaps (gaps between candles). Gaps are visually removed/filled when price returns to the gap area.
- **Auto Fibonacci Extension**: Automatically draws Fibonacci extension levels based on recent pivots, with customizable levels and visual options.


### Technical Concepts Used

- **ATR (Average True Range)**: Trailing stop and trendline slope calculation
- **Heikin Ashi Candles**: Optional smoothing for buy/sell signals
- **EMA (Exponential Moving Average)**: Crossover logic for buy/sell signals
- **Swing Highs/Lows**: Pivot detection for trendlines and FIB
- **Standard Deviation & Linear Regression**: Alternative trendline slope methods
- **Order Block Detection**: Last up/down candle before reversal
- **Fair Value Gap (FVG) Detection**: Gaps between candles, with fill/removal logic
- **Fibonacci Extension**: Automatic multi-level FIB drawing
- **TradingView Alerts**: Buy/sell and trendline breakout alerts


## Platform Requirements

- TradingView account (free or paid)
- Access to the TradingView Pine Script editor (web-based)
- Pine Script version 5 (`//@version=5`)

No additional software or dependencies are required. All logic runs within TradingView's platform.


## Getting Started

1. Open TradingView and log in.
2. Go to the Pine Script editor.
3. Copy the contents of `Indicator.pine` into the editor.
4. Add the script to your chart to visualize all features (signals, trendlines, order blocks, FVG, FIB).


## File Structure

- `Indicator.pine` — Main Pine Script indicator file


## Usage

- Customize the script as needed for your trading strategy.
- Save and add the indicator to your preferred chart.

No external libraries or packages are needed.


## License
See the [LICENSE](LICENSE) file for license information.
