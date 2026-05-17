# Climate Transition Risk Stress Test

## Overview

This project explores how climate transition risk can propagate into traditional bank credit risk metrics under rising carbon price scenarios.

Using a Python-based stress testing framework, I simulate how higher carbon prices affect the financial health of industrial borrowers across high-emission sectors such as:

- Steel
- Cement
- Chemicals
- Utilities

The framework is inspired by climate transition scenarios from the Network for Greening the Financial System (NGFS) and broader ECB expectations around climate-related stress testing and risk management.

---

## Core Idea

The transmission mechanism is simple:

Higher carbon prices → higher operating costs → lower profitability → weaker debt repayment capacity.

To measure this deterioration, the model tracks the Interest Coverage Ratio (ICR), which measures how easily a company can pay interest on its debt using operating profits.

---

## Model Features

To make the simulation more realistic, the model includes:

- Sector-specific emissions profiles
- Different debt levels across firms
- Pricing power / cost pass-through
- Partial carbon exposure
- Non-linear stress amplification
- Heterogeneous company distributions

---

## Carbon Price Scenarios

The portfolio is stressed under multiple carbon price scenarios:

- €0 / ton
- €50 / ton
- €100 / ton
- €150 / ton
- €200 / ton
- €250 / ton

---

## Visualization

The ridge plot below shows how the portfolio’s debt repayment capacity shifts as carbon prices rise.

A visible leftward migration emerges at higher carbon prices, with weaker firms increasingly clustering near distressed credit thresholds.

<img width="828" height="644" alt="image" src="https://github.com/user-attachments/assets/f06eae29-26d3-4e5e-a21d-2e3f86a0a3a9" />


---

## Key Assumptions

### EBITDA
Represents operating profitability available to service debt.

Each company’s EBITDA is randomly generated using sector-based distributions.

---

### Scope 1 Emissions
Represents direct operational CO₂ emissions.

Emissions are modeled using log-normal distributions to create realistic concentration and tail-risk effects.

---

### Pricing Power (Pass-Through)
Not all firms absorb carbon costs equally.

Some companies can pass part of the carbon cost to customers depending on sector dynamics and market structure.

---

### Carbon Exposure
Not all emissions are immediately priced due to:
- free allowances
- transition frictions
- regulatory phase-ins

---

## Important Limitations

This is a stylized educational framework, not a production bank model.

The simulation:
- assumes static balance sheets
- excludes mitigation investment
- excludes macroeconomic feedback loops
- excludes PD/LGD calibration
- focuses only on Scope 1 emissions

The purpose is to illustrate how climate transition risk can propagate into traditional credit risk metrics.

---

## Files

| File | Description |
|---|---|
| `climate_transition_model.ipynb` | Interactive notebook |
| `climate_transition_model.py` | Python script |
| `portfolio_results.csv` | Simulated portfolio outputs |
| `final_joyplot.png` | Visualization used in LinkedIn post |

---

## Author

Built as part of an independent exploration into climate risk, stress testing, and transition risk analytics.
