# Bitcoin Infrastructure Efficiency & Payback Engine

An enterprise-grade financial simulation platform built to model Bitcoin mining economics through the lens of thermodynamic asset valuation. Instead of evaluating hardware profitability via fixed manufacturer brand labels, this framework treats **ASIC Efficiency ($J/\text{TH}$)** as the definitive dependent variable driving facility survival and procurement strategies.

## 🛠️ The Core Mathematical Logic

This platform mathematically isolates the maximum power tariff overhead a facility can withstand before hardware operating costs entirely consume mining yields.

### 1. Maximum Viable Efficiency Ceiling ($E_{\text{max}}$)
The point at which daily revenue per Terahash exactly matches the electrical cost to generate it ($0.00 breakeven baseline):

$$E_{\text{max}} = \left( \frac{\left( \frac{10^{12} \times 86400 \times BR}{Difficulty \times 2^{32}} \right) \times P_{\text{BTC}} \times (1 - Fee)}{R_{\text{elec}}} \right) \times \left( \frac{1000}{24} \right)$$

### 2. CapEx Payback Horizon Matrix
Calculates the absolute capital depreciation return schedules by checking live operational unit net margins against dynamic wholesale equipment market price layers:

$$\text{Estimated Payback (Days)} = \frac{\text{Wholesale Equipment Unit Price (\$)}}{\text{Daily Unit Revenue (\$/Day)} - \text{Daily Unit OpEx Cost (\$/Day)}}$$

## 📊 Application Visual Architecture

The dashboard implements an interactive **Sidebar Layout** divided into four major analytical zones:

*   **Zone A (Input Console):** Responsive sliders enabling real-time stress testing of variables, including Bitcoin spot price, global network difficulty epochs, local electricity tariffs ($/kWh), and pool fees.
*   **Zone B (Executive Readout Cards):** High-contrast KPI displays presenting the calculated Maximum Viable Efficiency, the Recommended Sourcing Target (incorporating a safe 30% OpEx margin cushion), and an automated structural risk verdict.
*   **Zone C (Continuous Yield Curve Plot):** Generates a continuous thermodynamic efficiency spectrum curve scaled to **Petahashes per second (PH/s)**, explicitly shading the boundaries between profitable territory and the grid obsolescence zone.
*   **Zone D (Wholesale Sourcing Grid):** A tabular procurement lookup matrix that maps live market miner models against the calculated economic threshold, dynamically computing single-unit margins and exact capital return (ROI) windows.

---

## 🚀 Quick Start Guide

### Prerequisites
Ensure your local Python environment or Jupyter Notebook instance has the required visualization dependencies installed:

```bash
pip install dash plotly pandas
