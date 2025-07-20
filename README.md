# ⚔️ UT Bot Strategy (v4) for TradingView

The **UT Bot Strategy** combines trailing stop logic with signal generation via Heikin Ashi candles (optional) and ATR-based volatility calculations. Configurable for both fixed and adaptive TP/SL, it empowers traders to align strategy sensitivity with asset volatility, while layering on EMA, RSI, and ATR filters for sharper entries.

---

## 📈 Strategy Highlights

- 🎯 **Core Logic**:
  - Uses trailing stop band based on ATR sensitivity
  - Switches bias on crossover confirmation
  - Optional Heikin Ashi-based signal mode

- 🔒 **Risk Controls**:
  - Fixed or ATR-based stop loss & take profit levels
  - Manual SL/TP configuration with % toggles
  - Visual plotting of SL/TP bands per trade

- 🧠 **Filter Suite**:
  - EMA trend confirmation
  - RSI strength analysis
  - Volatility screen using ATR-to-price % ratio

- 📊 **Visuals & Alerts**:
  - Buy/Sell signals with shape labels
  - Color-coded bar overlays
  - TP/SL plotted dynamically as circular markers
  - Configurable alert conditions for automation

---

## ⚙️ Input Parameters

| Input                 | Functionality                                |
|----------------------|-----------------------------------------------|
| `Key Value` (a)       | Sensitivity multiplier for trailing bands     |
| `ATR Period` (c)      | Determines trailing stop length               |
| `Heikin Ashi Mode`    | Toggle to use HA candles for signal logic     |
| `Fixed TP/SL`         | Enable classic percentage-based exits         |
| `ATR TP/SL`           | Dynamic exit points based on volatility       |
| `EMA Filter`          | Optional trend filter using EMA 233           |
| `RSI Filter`          | Optional entry condition using RSI            |
| `Volatility Filter`   | Filters low-ATR conditions                    |

---

## 📦 Strategy Logic Overview

- **Buy Logic**:
  - Price > trailing stop
  - EMA crossover confirms entry
  - Filters (if enabled) must pass: RSI < Overbought, Volatility ≥ Threshold

- **Sell Logic**:
  - Price < trailing stop
  - EMA cross-under confirms entry
  - Filters must pass: RSI > Oversold, Volatility ≥ Threshold

---

## 🚀 Getting Started

1. Paste the code into Pine Editor on TradingView
2. Set your SL/TP preferences and filters
3. Add to chart, backtest with Strategy Tester
4. Monitor Buy/Sell labels and live TP/SL updates
5. Customize alerts for webhooks or automation platforms

---

## 📊 Visual Outputs

- Buy/Sell labels at entry
- Bar color overlays (green for Buy, red for Sell)
- EMA filter line (if enabled)
- TP/SL markers as green/red circular plots

---

## 👤 Author

Crafted by [Rao Aksee Nasir] — strategy architect and automation enthusiast blending Pine precision with global trade logic.

---

## 📝 License

MIT License. Open for modification, usage, and sharing with attribution.

---

## 📬 Feedback

Found an edge? Suggest an upgrade or optimization via GitHub issues or pull requests.
