# Promo Efficiency Analysis

This repository provides a comprehensive framework to measure and analyze promotional effectiveness in retail. The solution is designed using Python, pandas, and matplotlib, and includes techniques for uplift calculation, discount analysis, baseline estimation, and promotional side-effects like cannibalization and halo effects.

---

## Project Overview

Retailers often invest heavily in promotions but lack a consistent analytical method to evaluate their true impact. This project addresses that gap through:

- **Baseline Sales Estimation** (Static & Moving Average)
- **Promo Uplift Calculation**
- **Discount Analysis**
- **Profitability and Efficiency Estimation**
- **Cannibalization & Halo Effects**
- **Basket-Level Behavior During Promotions**
- **Promo Detection Using Price Drop**
- **Cross-sell Effect in Promo Baskets**
- **Promo Efficiency Dashboard**

---

## Structure

- `notebooks/`: Jupyter Notebooks for baseline, uplift, and basket analysis
- `scripts/`: Python files modularizing the logic
- `data/`: Sample data files (`merged_data.csv`)
- `promo_efficiency_app/`: Streamlit-based dashboard (optional)
- `README.md`: Documentation

---

## Key Features

- Detects promo periods using price drop detection.
- Computes static and moving average baselines.
- Calculates uplift and promotional ROI.
- Measures promo spillover using cannibalization and halo effects.
- Evaluates basket value changes during promotions.
- Provides region-wise and category-wise insights.

---

## Core Metrics & Formulas

- **Promo Uplift (%)** = \((\text{Promo Sales} - \text{Baseline Sales}) / \text{Baseline Sales} \times 100\)
- **Discount (%)** = \((1 - \text{Promo Price} / \text{Baseline Price}) \times 100\)
- **Promo Efficiency Index** = \(\text{Uplift (%)}/\text{Discount (%) }\)
- **Basket Size** = Total Value of `check_id` items during promo vs regular
- **Halo / Cannibalization Effect** = Change in sales of non-promoted SKUs in the same category

---

## Requirements

- Python 3.8+
- pandas
- matplotlib
- numpy
- streamlit *(optional, for UI)*

You can install dependencies via:

```bash
pip install -r requirements.txt
