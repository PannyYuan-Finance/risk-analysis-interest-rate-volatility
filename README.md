# Risk Analysis: Interest Rate Regimes & Equity Volatility

📄 One-Page Risk Summary: [Download PDF](./reports/Interest_Rate_Equity_Volatility_Risk_Summary.pdf)

---

## Project Overview

This project investigates how U.S. interest rate regimes impact equity market volatility and downside risk.

Using daily data from FRED (2016–2026), the analysis evaluates:

- Multi-horizon interest rate changes
- Equity volatility sensitivity
- Regime-dependent risk behavior
- Tail risk exposure (VaR & CVaR)

The objective is to replicate a simplified macro risk monitoring framework commonly used in risk management and asset management settings.

---

## Data Sources

- 10-Year Treasury Yield (DGS10) — FRED
- S&P 500 Index (SP500) — FRED
- Frequency: Daily
- Sample Period: 2016–2026

---

## Methodology

### 1️⃣ Return & Volatility Modeling

- Daily returns computed using percentage change
- 30-day rolling volatility annualized via:

Volatility = Rolling Std × √252

---

### 2️⃣ Multi-Horizon Rate Sensitivity Analysis

Interest rate changes evaluated across:

- 1-day
- 5-day
- 10-day
- 21-day
- 63-day
- 126-day

Finding:
Medium-term horizons (21–63 days) show stronger correlation with equity volatility than short-term rate shocks.

---

### 3️⃣ Regime Classification (Tightening vs Easing)

Regimes defined using 63-day yield trend:

- Tightening: 63-day yield change > 0
- Easing: 63-day yield change < 0

A Welch t-test was conducted to test volatility differences across regimes.

Result:
Volatility differs significantly across regimes (p < 0.01).

---

### 4️⃣ Core Risk Metrics

Calculated institutional-style risk indicators:

- Annualized Return
- Annualized Volatility
- Sharpe Ratio
- Maximum Drawdown
- Historical VaR (95%, 99%)
- Conditional VaR (CVaR)

### Key Results

- Sharpe Ratio: ~0.78
- Maximum Drawdown: -33.9%
- 1-Day VaR (95%): -1.68%
- Regime t-test p-value: < 0.01

---

## Risk Insights

- Equity volatility exhibits clear macro regime dependency.
- Medium-term yield trends have stronger predictive linkage to volatility.
- Tail risk remains elevated during easing cycles.
- Downside exposure during stress periods is substantial (MDD ~ -34%).

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


---

## Author

Panny Yuan  
Economics | Risk Analytics | Quantitative Research  
Contact: zy3112@nyu.edu
