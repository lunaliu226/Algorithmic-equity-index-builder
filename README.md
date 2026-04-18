# Algorithmic Equity Index Builder
A deterministic rules engine for selecting and weighting equity constituents based on quantitative thresholds.

## Product Overview
This project systematizes equity constituent selection into a scalable, automated pipeline. It ingests empirical market data for a basket of AI-sector equities and applies a multi-factor decision matrix to isolate high-performing, risk-adjusted assets, removing qualitative bias from the index creation process.

## Methodology & Governance
The engine utilizes a strict algorithmic filtration protocol to ensure portfolio stability:
* **Structural Outlier Removal:** Assets ranking in the top 20% of annualized volatility are systematically eliminated to prevent mathematical distortions in the final index.
* **Momentum Threshold:** Constituents must demonstrate positive 1-year momentum to qualify for inclusion.
* **Multi-Factor Weighting:** Surviving assets are assigned weights using an inverse volatility optimization model. This ensures lower-risk constituents receive proportionally higher mathematical weight, stabilizing the overall index yield.

## Technical Stack
* **Language:** Python
* **Libraries:** `yfinance` (Data Ingestion), Pandas (DataFrames & Logic), NumPy (Statistical Math)

## Future Roadmap
* Integrate a dynamic SQL decision matrix to abstract the filtration logic into a relational database schema.
* Build a variance attribution diagnostic tool to backtest the yield against standard market benchmarks (e.g., QQQ).
