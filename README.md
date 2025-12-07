# Trader Behavior Insights

**Objective:** Explore relationship between trader performance (Hyperliquid historical trades) and Bitcoin Fear & Greed index. Deliverables include cleaned notebook, EDA, statistical tests, predictive modelling (XGBoost), feature importance and SHAP explainability.

## Files
- `notebook.ipynb` — full Colab notebook (cleaned & runnable)
- `outputs/` — CSVs and figures:
  - `daily_sent_pnl.csv`
  - `top_accounts.csv`
  - `feature_importance.csv`
  - `shap_beeswarm.png`, `shap_bar.png`, `boxplot_pnl_by_sentiment.png`, `ts_pnl_sent.png`
- `executive_summary.md` — 1-page findings & actionables
- `requirements.txt` — pip packages used

## How to run
1. Open `notebook.ipynb` in Google Colab.
2. Upload the two data files (`historical_trades.csv` and `fear_greed_index.csv`) into Colab `/content/`.
3. Run cells top to bottom. Outputs will be saved to `/content/outputs/`.

## Key findings (summary)
- Weekly sentiment momentum (lag7) is predictive of profitable trades.
- XGBoost achieved ROC-AUC ≈ 0.94 for profitable trade prediction.
- Actionables: sentiment-aware trade filters, reduce exposure during negative sentiment momentum, monitor hour-of-day risk windows.


