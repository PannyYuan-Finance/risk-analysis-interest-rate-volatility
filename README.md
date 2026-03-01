# Risk Analytics Framework: Regime-Based Volatility & Tail Risk Monitoring

📄 One-Page Risk Summary: [Download PDF](./reports/Interest_Rate_Equity_Volatility_Risk_Summary.pdf)

---

## Project Overview

This project develops a portfolio analytics framework designed to evaluate how equity performance and volatility respond to different interest rate regimes.

The objective is to simulate how an asset management team would:

- Analyze performance trends under varying macro conditions
- Identify regime-driven shifts in portfolio behavior
- Assess risk-adjusted return metrics
- Evaluate interest rate sensitivity across different time horizons
- Translate quantitative findings into asset allocation and product positioning insights

The framework reflects analytical tools commonly used in asset management to support portfolio strategy and client-facing investment narratives.

---

## Data Sources

- 10-Year Treasury Yield (DGS10) — FRED
- S&P 500 Index (SP500) — FRED
- Frequency: Daily
- Sample Period: 2016–2026

---

## Risk Analytics Framework

### 1️⃣ Volatility Monitoring

- Daily return calculation
- 30-day rolling annualized volatility
- Rolling 60-day correlation tracking

Purpose:
To simulate daily volatility monitoring used in risk dashboards.

---

### 2️⃣ Regime Detection Model

- 63-day yield trend classification
- Tightening vs Easing identification
- Statistical regime comparison (Welch t-test)

Purpose:
To assess regime-dependent volatility behavior.

---

### 3️⃣ Tail Risk Quantification

- Historical VaR (95%, 99%)
- Conditional VaR (Expected Shortfall)
- Maximum drawdown tracking

Purpose:
To evaluate downside exposure under stress scenarios.

---

### 4️⃣ Multi-Horizon Sensitivity Analysis

- Rate change windows: 1d–126d
- Correlation decay and sensitivity evaluation

Purpose:
To detect medium-term macro risk transmission effects.

### Key Results

- Sharpe Ratio: ~0.78
- Maximum Drawdown: -33.9%
- 1-Day VaR (95%): -1.68%
- Regime t-test p-value: < 0.01

---

## Risk Findings

- Volatility exhibits statistically significant regime dependency (p < 0.01).
- Medium-term rate movements (1–3 months) show stronger volatility sensitivity than short-term shocks.
- Tail risk remains elevated during easing cycles.
- Maximum drawdown reached -33.9%, highlighting material downside exposure.
- Risk-adjusted performance remains moderate (Sharpe ~0.78).

The framework demonstrates how macro regime shifts impact portfolio-level risk metrics.

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
This repository is organized to separate research code from executive reporting.

```
risk-analysis-interest-rate-volatility/
│
├── Interest_rate_volatility_analysis.ipynb
│   └── Full analysis notebook (data download, modeling, regime testing, risk metrics)
│
├── README.md
│   └── Project documentation and methodology overview
│
└── reports/
    └── Interest_Rate_Equity_Volatility_Risk_Summary.pdf
        └── Executive one-page summary
```

---

## Author

Panny Yuan  
Economics | Risk Analytics | Quantitative Research  
Contact: zy3112@nyu.edu
