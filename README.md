# AI Chip Stocks Analysis

A data-driven deep-dive into **NVDA** (NVIDIA), **AMD**, and **TSM** (TSMC) using two years of daily market data.

---

## 📂 Project Structure

```
ai-chip-stocks-analysis/
├── analysis.ipynb          ← Main Jupyter Notebook (8 sections)
├── analysis.html           ← Exported static HTML report
├── README.md               ← This file
└── charts/                 ← Auto-generated chart PNGs
    ├── 01_price_history.png
    ├── 02_normalised_price.png
    ├── 03_cumulative_returns.png
    ├── 04_return_distributions.png
    ├── 05_volatility.png
    ├── 06_moving_averages.png
    ├── 07_correlation_heatmap.png
    ├── 08_returns_pairplot.png
    ├── 09_volume_analysis.png
    ├── 10_price_vs_volume.png
    └── 11_summary_metrics.png
```

---

## 📊 Notebook Sections

| # | Section | Description |
|---|---------|-------------|
| 1 | **Data Collection** | Download 2 years of OHLCV data via `yfinance` |
| 2 | **Price History** | Per-stock closing price charts + normalised comparison |
| 3 | **Returns Analysis** | Cumulative returns, daily return distributions |
| 4 | **Volatility Analysis** | 30-day rolling annualised volatility & comparison bar chart |
| 5 | **Moving Averages** | 50-day & 200-day SMA with golden/death cross zones |
| 6 | **Correlation Heatmap** | Price-level and returns correlation + pair-scatter matrix |
| 7 | **Volume Analysis** | Daily volume bars (green = up day, red = down day) + Price vs Volume scatter |
| 8 | **Summary Statistics** | Annualised return, volatility, Sharpe ratio, max drawdown |

---

## 🔧 Requirements

```
yfinance
pandas
numpy
matplotlib
seaborn
nbconvert
jupyter
```

Install all dependencies:

```bash
pip install yfinance pandas numpy matplotlib seaborn nbconvert jupyter
```

---

## 🚀 Quick Start

```bash
# 1. Run the full notebook and save outputs
jupyter nbconvert --to notebook --execute analysis.ipynb --output analysis.ipynb

# 2. Export to HTML
jupyter nbconvert --to html analysis.ipynb --output analysis.html

# 3. Or launch the interactive notebook
jupyter notebook analysis.ipynb
```

---

## 📈 Key Metrics (example — re-run for latest figures)

| Metric | NVDA | AMD | TSM |
|--------|------|-----|-----|
| Total Return | computed live | computed live | computed live |
| Ann. Volatility | computed live | computed live | computed live |
| Sharpe Ratio | computed live | computed live | computed live |
| Max Drawdown | computed live | computed live | computed live |

> All metrics are recomputed fresh each time the notebook is executed.

---

## 📦 Data Source

Market data is sourced from **Yahoo Finance** via the [`yfinance`](https://github.com/ranaroussi/yfinance) library (adjusted for splits and dividends).

---

## 📝 Notes

- TSMC is represented by its **NYSE ADR** ticker `TSM` (not the Taiwan Stock Exchange listing).
- All prices are in **USD**.
- Charts are saved automatically to the `charts/` directory on each run.
- The HTML export (`analysis.html`) includes all chart outputs inline.

---

*Generated with Python · yfinance · pandas · matplotlib · seaborn*
