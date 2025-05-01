# Moving Average ADX DMI Indicator

![Indicator Example](screenshot.png) <!-- Add a screenshot if available -->

A multi-colored moving average indicator for TradingView that combines the ADX (Average Directional Index) and DMI (Directional Movement Index) to detect strong trends and visualize bullish/bearish conditions.

## Overview
This indicator integrates a **moving average**, **ADX**, and **DMI** to identify strong market trends. The moving average changes color based on trend strength and direction:
- **Green**: Strong bullish trend (go long)
- **Red**: Strong bearish trend (go short)
- **Yellow**: Weak or no trend (exit positions)

Built with Pine Script, it is designed for traders who want to quickly assess trend conditions using visual cues.

## Features
- **Multi-Indicator Integration**: Combines Moving Average, ADX, and DMI.
- **Color-Coded Trend Detection**: 
  - Green = Bullish
  - Red = Bearish
  - Yellow = No trend
- **Adjustable Parameters**: Customize periods and sensitivity.
- **Trend-Focused**: Optimized for trending markets.

## Installation
1. Open **TradingView** and navigate to the **Pine Editor**.
2. Copy the [indicator code](moving_average_adx_dmi.pine) into a new script.
3. Save and add the indicator to your chart.

## Usage
- **Bullish Signal (Green MA)**: Enter long positions when the moving average turns green.
- **Bearish Signal (Red MA)**: Enter short positions when the moving average turns red.
- **No Trend (Yellow MA)**: Close positions or avoid trades.

**Example Strategy**:
- Buy when the MA turns **green** (ADX > 20, D+ > D−, MA rising).
- Sell when the MA turns **red** (ADX > 20, D+ < D−, MA falling).
- Exit trades when the MA turns **yellow** (ADX < 20).

## Parameters
| Parameter           | Description                          | Default Value |
|---------------------|--------------------------------------|---------------|
| `MA Period`         | Period for the moving average.       | 20            |
| `DMI Period`        | Period for the DMI calculation.      | 20            |
| `ADX Smoothing`     | Smoothing period for the ADX.        | 14            |
| `ADX Trend Level`   | Threshold for trend strength (ADX).  | 20            |

## How It Works
1. **Moving Average**: Identifies the primary trend direction (rising/falling).
2. **ADX**: Measures trend strength. Values above `ADX Trend Level` indicate strong trends.
3. **DMI**: Determines trend direction using `D+` (bullish) and `D−` (bearish) lines.
   - **Bullish**: `D+ > D−` + MA rising.
   - **Bearish**: `D+ < D−` + MA falling.

## Notes
- Best used in **trending markets** (avoid ranging markets).
- Adjust parameters to suit your trading style (e.g., shorter periods for day trading).

