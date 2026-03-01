# Risk Analysis: Interest Rate Regimes & Equity Volatility

## Project Overview

This project analyzes the relationship between U.S. interest rate movements and equity market volatility using Python.  

The goal is to evaluate how changes in the 10-year Treasury yield impact S&P 500 volatility across different time horizons and macro regimes.

---

## Data Sources

- FRED (Federal Reserve Economic Data)
  - 10-Year Treasury Yield (DGS10)
  - S&P 500 Index (SP500)
- Sample Period: 2016–2026
- Frequency: Daily

---

## Methodology

### 1️⃣ Return & Volatility Calculation

- Daily returns computed using percentage change
- 30-day rolling volatility calculated as:
  
  Rolling Standard Deviation × √252

---

### 2️⃣ Multi-Horizon Rate Sensitivity

Interest rate changes analyzed across multiple horizons:

- 1-day
- 5-day
- 10-day
- 21-day
- 63-day
- 126-day

Correlation between rate changes and equity volatility measured for each horizon.

Key Finding:
Rate-volatility sensitivity increases over medium-term horizons (21–63 days).

---

### 3️⃣ Regime Analysis (Tightening vs Easing)

Rate regimes defined by 63-day yield trend:

- Tightening: Yield increasing
- Easing: Yield decreasing

Welch t-test conducted to compare volatility under different regimes.

Result:
Volatility differs significantly across regimes (p < 0.01).

---

### 4️⃣ Risk Metrics

Calculated core risk indicators:

- Annualized Return
- Annualized Volatility
- Sharpe Ratio
- Maximum Drawdown
- Historical VaR (95%, 99%)
- CVaR (Expected Shortfall)

Key Metrics (Sample Results):

- Sharpe Ratio: ~0.78
- Maximum Drawdown: -33.9%
- 1-Day VaR (95%): -1.68%
- Regime t-test p-value: < 0.01

---

## Key Insights

- Equity volatility exhibits regime dependency.
- Medium-term rate trends (1–3 months) show stronger volatility linkage than short-term moves.
- Tail risk increases during easing cycles.
- Risk-adjusted performance is moderate, with significant downside exposure during stress periods.

---

## Technical Stack

- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- pandas_datareader

---

## Project Structure
