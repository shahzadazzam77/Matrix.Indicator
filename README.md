


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
# RSI + MACD Combo Indicator

## Overview

This repository now contains a combined TradingView Pine Script v6 study that packages an advanced RSI module (with optional divergence detection, multiple smoothing methods, Bollinger Bands, gradients) together with a classic MACD module rendered in its own separate pane.

The goal: a compact, configurable momentum suite you can drop on a chart and immediately monitor relative strength extremes, divergence signals, and MACD momentum shifts.

> NOTE: Previous README content (trendlines, order blocks, FVG, auto Fibonacci) described an earlier version of this project. The current `Indicator.pine` file only includes the RSI + MACD logic described below.

## Main Features

### RSI Panel
* Core RSI (length configurable) with upper (70), middle (50), and lower (30) bands.
* Gradient fills for overbought (50→100) and oversold (0→50) zones for quick visual intensity.
* Optional smoothing overlay (select from: None, SMA, SMA + Bollinger Bands, EMA, SMMA/RMA, WMA, VWMA).
* Optional Bollinger Bands around the selected RSI SMA (when "SMA + Bollinger Bands" is chosen) with configurable standard deviation multiplier.
* Regular Bullish & Bearish Divergence Detection (toggle via input) with:
	- Automatic pivot identification (configurable lookback constants in code)
	- Labeled arrows (Bull / Bear) and colored segment highlighting
	- Alert conditions for both divergence types

### MACD Panel (separate pane)
* Standard MACD calculation (fast, slow, signal lengths configurable; SMA or EMA option for both oscillator and signal line MAs).
* Histogram coloring distinguishes momentum acceleration vs deceleration in both positive and negative territories.
* Zero line reference.
* Alert conditions for histogram state transitions (rising→falling, falling→rising).

## Inputs Summary

| Group | Input | Purpose |
|-------|-------|---------|
| RSI Settings | RSI Length | Period for RSI calculation |
| RSI Settings | Source | Price source for RSI |
| RSI Settings | Calculate Divergence | Enables divergence detection & alerts |
| Smoothing | Type | Select smoothing MA (or none) |
| Smoothing | Length | Length for smoothing MA / BB basis |
| Smoothing | BB StdDev | Standard deviation multiplier for Bollinger Bands |
| MACD | Fast Length | Fast EMA/SMA length |
| MACD | Slow Length | Slow EMA/SMA length |
| MACD | Source | Price source for MACD |
| MACD | Signal Smoothing | Signal line length |
| MACD | Oscillator MA Type | SMA or EMA for MACD base lines |
| MACD | Signal Line MA Type | SMA or EMA for signal line |

## Alerts Provided
* Regular Bullish Divergence (RSI vs Price)
* Regular Bearish Divergence (RSI vs Price)
* MACD Histogram state change: rising → falling
* MACD Histogram state change: falling → rising

Enable only the alerts you need to avoid unnecessary notifications.

## Platform Requirements
* TradingView account (free or paid)
* Pine Script Editor access (web)
* Pine Script version 6 (`//@version=6`) — already declared at top of `Indicator.pine`.

No external dependencies; everything executes within TradingView.

## Getting Started
1. Open TradingView.
2. Open the Pine Script editor.
3. Paste the contents of `Indicator.pine`.
4. Click Add to Chart.
5. (Optional) Enable divergence detection if you want pivot-based signals (disabled by default for performance).

## Usage Tips
* Divergence logic uses fixed lookback constants (currently 5/5); adjust in code if you need more/less sensitivity.
* If you only want MACD, you can hide the RSI plots via the style settings (eye icons) and vice versa.
* Bollinger Bands only show when the smoothing Type = "SMA + Bollinger Bands".
* For cleaner charts, disable divergence when not actively scanning for reversal signals.

## Limitations
* The combined script shows two panes: the main RSI pane and the MACD pane created with `indicator.new`. TradingView does not support more than one top-level `indicator()` call, so the secondary pane relies on `indicator.new` (Pine v6 feature). Both are still part of one script for easier maintenance.
* Only regular (classic) bullish/bearish divergences are included. Hidden divergences are not implemented.
* Alerts for divergence require divergence calculation to be enabled.

## File Structure
* `Indicator.pine` – RSI + MACD combo script (current version)

## Changelog (Recent)
* Added combined RSI + MACD script (v6)
* Added divergence alert conditions
* Added Bollinger Band option to RSI smoothing
* Deprecated prior multi-feature Matrix version (trendlines, order blocks, FVG, auto FIB) in this repository snapshot

## Roadmap (Ideas)
* Hidden divergence detection
* User-adjustable divergence lookback via inputs
* Multi-timeframe RSI or MACD overlay option
* Optional smoothing of histogram

## License
See the [LICENSE](LICENSE) file for license information.
