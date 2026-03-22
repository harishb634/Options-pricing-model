# Options Pricing Model: Black-Scholes & Monte Carlo Simulation

**Author:** Harish Bodasinghi | Data Scientist  
**Stack:** Python · NumPy · SciPy · Matplotlib · Seaborn  
**Topics:** Quantitative Finance · Stochastic Modelling · Risk Analytics · Derivatives Pricing

---

## Overview

This project implements two classical approaches to pricing European options and visualizes key risk metrics used in quantitative finance.

### What's implemented:
- **Black-Scholes Analytical Model** — closed-form European call/put pricing
- **Monte Carlo Simulation** — 100,000 stock price paths via Geometric Brownian Motion (GBM)
- **Option Greeks** — Delta, Gamma, Theta, Vega sensitivity analysis
- **Volatility Smile/Skew** — implied volatility surface visualization
- **MC Convergence Analysis** — how Monte Carlo price converges to Black-Scholes as simulations increase

---

## Visualizations

| Chart | Description |
|-------|-------------|
| GBM Price Paths | 200 simulated stock price trajectories |
| Terminal Price Distribution | Log-normal distribution of final stock prices |
| Option Price vs Spot | Call/Put price curves with intrinsic value |
| Volatility Surface | Smile and skew patterns across strikes |
| Greeks Analysis | Delta, Gamma, Vega, Theta across spot prices |
| MC Convergence | Price accuracy vs number of simulations |

---

## Quickstart

```bash
# Clone the repo
git clone https://github.com/harishbodasinghi/options-pricing-model.git
cd options-pricing-model

# Install dependencies
pip install numpy scipy matplotlib seaborn pandas

# Run the notebook
jupyter notebook options_pricing_quant.ipynb
```

---

## Key Results

```
==================================================
   BLACK-SCHOLES OPTION PRICING SUMMARY
==================================================
  Stock Price (S)     : $100.00
  Strike Price (K)    : $105.00
  Time to Expiry (T)  : 1.00 years
  Risk-Free Rate (r)  : 5.0%
  Volatility (sigma)  : 20.0%
--------------------------------------------------
  CALL Price          : $8.0215
  PUT  Price          : $5.5734
--------------------------------------------------
  GREEKS (CALL):
    Delta             : 0.4636
    Gamma             : 0.0188
    Theta (per day)   : $-0.0153
    Vega  (per 1% vol): $0.3752
==================================================

MONTE CARLO vs BLACK-SCHOLES (100,000 simulations)
  CALL — Black-Scholes : $8.0215
  CALL — Monte Carlo   : $8.0187  (±0.0261)
  Difference           : $0.0028
```

---

## Theory

### Black-Scholes Formula

$$C = S_0 N(d_1) - K e^{-rT} N(d_2)$$

$$d_1 = \frac{\ln(S_0/K) + (r + \sigma^2/2)T}{\sigma\sqrt{T}}, \quad d_2 = d_1 - \sigma\sqrt{T}$$

### Geometric Brownian Motion (Monte Carlo)

$$S_t = S_0 \cdot \exp\left[(r - \frac{\sigma^2}{2})t + \sigma W_t\right]$$

---

## File Structure

```
options-pricing-model/
│
├── options_pricing_quant.ipynb   # Main notebook (run this)
├── README.md                      # This file
├── options_analysis.png           # Auto-generated chart
├── greeks_analysis.png            # Auto-generated chart
└── mc_convergence.png             # Auto-generated chart
```

---

## Extensions Planned
- [ ] Implied Volatility extraction from real market data (Yahoo Finance)
- [ ] American option pricing via Least Squares Monte Carlo (Longstaff-Schwartz)
- [ ] Heston Stochastic Volatility Model
- [ ] Portfolio VaR and CVaR computation

---

## Connect
**LinkedIn:** [linkedin.com/in/harishbodasinghi](https://linkedin.com/in/harishbodasinghi)  
**GitHub:** [github.com/harishbodasinghi](https://github.com/harishbodasinghi)
