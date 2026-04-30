# data-science-portfolio
Portfolio of data science projects including data analysis, modeling, and insights.

# Predictive Bank Marketing Analysis

## Overview
This project analyzes customer behavior from a real-world bank marketing campaign to predict term deposit subscriptions and identify key drivers of conversion.

---

## Dataset
- Source: UCI Bank Marketing Dataset
- 11,162 observations, 17 features
- Includes demographic, financial, and campaign interaction data

---

## Key Findings
- Previous campaign success strongly increases subscription likelihood
- Higher account balance is associated with higher conversion
- Excessive outreach reduces effectiveness
- Timing (month) significantly impacts customer behavior

---

## Model
- Logistic Regression (baseline, interpretable model)
- Accuracy: ~81%

---

## Feature Insights
- Strong positive drivers: duration*, previous success, certain months
- Negative drivers: high contact frequency, loan/housing indicators

\*Note: duration is not usable in real-world prediction (data leakage)

---

## Business Value
- Enables targeted outreach to high-probability customers
- Reduces wasted marketing spend
- Improves campaign efficiency

---

## Tools
- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn

---

## How to Run

1. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn