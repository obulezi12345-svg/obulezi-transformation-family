# Obulezi Normalizing Transformation Benchmark

This repository contains the complete Python implementation and diagnostic benchmarking suite for the **Obulezi Normalizing Transformation Family**. It evaluates the proposed analytical operator against 12 classical transformation families and non-parametric rank mapping across Monte Carlo simulation studies and real-world financial return data (S&P 500 Index, 2020–2023).

---

## 📌 Features & Key Capabilities

- **Analytical Profile Likelihood Optimization:** Automated bounded numerical search for the optimal transformation parameter $\lambda$.
- **14 Comparative Transformation Operators:** Includes implementation for Box-Cox, Bickel-Doksum, Manly, Modulus (John-Draper), Yeo-Johnson, Dual Power, Logit, Arcsine Square-Root, Fisher $z$, Bayesian Power, Modified Non-Negative, and Central Normalizing Quantile mapping.
- **Data Acquisition Pipeline:** Automated retrieval and log-return preprocessing for financial asset returns via `yfinance`.
- **Diagnostic Plot Suite:** Script to automatically compute and export high-resolution ($300\text{ DPI}$) vector (`.pdf`) and raster (`.png`) plots across 4 diagnostic grid configurations:
  - Normal Quantile-Quantile (Q-Q) Plots
  - Kernel Density Estimates (KDE)
  - Empirical Cumulative Distribution Functions (ECDF)
  - Comparative Outlier Dispersion Boxplots

---

## 📁 Repository Structure

```text
.
├── simulation_benchmark.py       # Monte Carlo simulation suite across candidate distributions
├── real_data_benchmark.py        # S&P 500 empirical return pipeline and diagnostics
├── requirements.txt              # Core dependencies
├── outputs/                      # Saved figures (.pdf/.png) and summary tables
│   ├── all_transformations_qqplots.pdf
│   ├── all_transformations_kde.pdf
│   ├── all_transformations_ecdf.pdf
│   └── all_transformations_boxplot.pdf
└── README.md                     # Project documentation
