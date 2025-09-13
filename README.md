# Pairs Trading Strategy – Statistical Arbitrage

This project explores a **mean-reversion pairs trading strategy** applied to major US banking equities.

## Overview
- **Goal:** Identify a stationary (cointegrated) pair of stocks and exploit deviations from their long-term equilibrium.
- **Universe:** International banking stocks (2000–2020)

## Methodology
1. **Correlation Screening:** Calculated Pearson correlation to shortlist highly correlated pairs (ρ >= 0.8).
2. **Cointegration Testing:**  
   - Used the **Engle-Granger two-step method**.  
   - Modelled the spread (residuals) via linear regression (`sklearn.LinearRegression`).  
   - Applied **Augmented Dickey-Fuller (ADF)** test to verify stationarity at the 5% significance level.
3. **Backtesting:**  
   - Period: 2021–Present  
   - Entry: Deviate 1 std from mean  
   - Exit: revert 0.1 std from mean  
   - Capital: $10,000, with 2.5% allocated per trade  

## Results
- **Identified Pair:** :contentReference[oaicite:1]{index=1} (BAC) & :contentReference[oaicite:2]{index=2} (AXP)  
- **Performance:**  
  - Sharpe ratio: 0.86  
  - Cumulative return: **+242.5%** (gross, no transaction costs)

## Key Skills
- Python (:contentReference[oaicite:3]{index=3}, :contentReference[oaicite:4]{index=4}, :contentReference[oaicite:5]{index=5}, :contentReference[oaicite:6]{index=6})
- Statistical modelling & time series analysis
- Quantitative finance and risk-adjusted performance evaluation

---

📌 *This project was built as a first step into quantitative trading and statistical arbitrage strategies.
