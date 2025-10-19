# Backtest Notebook – Quick Start

**Files**
- `Backtest_AI_Passive_Crypto.ipynb` – open this in Jupyter / VS Code / PyCharm to run the backtest.
- `requirements.txt` – minimal dependencies.

**How to run**
1. Create a virtual environment (recommended).
2. `pip install -r requirements.txt`
3. Open and run `Backtest_AI_Passive_Crypto.ipynb` (it downloads daily prices from Yahoo via `yfinance`).

**Assumptions**
- Period: 2024-10-01 to 2025-10-01 (12 monthly contributions, final valuation on 2025-10-01).
- Strategy 1 (DCA only): Invest $20,000 spread evenly over 12 months **plus** $2,500 monthly (total $4,166.67 per month).
- Strategy 2 (Lump + DCA): $20,000 lump on start date **plus** $2,500 monthly.
- Strategy 3 (Limit DCA 10%): Same monthly total as Strategy 1. For each asset in each month, if any day's close is ≤ 90% of the month's opening close, buy on the **first** such day; otherwise buy on the month's last trading day.

**Tweaks**
- Edit the `WEIGHTS`, `START_DATE`, `END_DATE`, and contribution amounts at the top of the notebook.
- To change GOOGL to GOOG, just edit the `WEIGHTS` tickers.
- CSVs export into `exports/` when you run the notebook.

*Built on 2025-10-19.*
