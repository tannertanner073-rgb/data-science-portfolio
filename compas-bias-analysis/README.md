Algorithmic Bias Analysis: COMPAS Recidivism Risk Scores

# ⚖️ Algorithmic Bias Analysis: COMPAS Recidivism Risk Scores

## 📌 Overview

This project analyzes whether COMPAS risk scores demonstrate bias across demographic groups.
Using real-world criminal justice data, the goal is to evaluate whether prediction errors are distributed fairly.

The analysis follows a structured pipeline:

* Data cleaning (based on ProPublica methodology)
* Exploratory analysis of risk scores
* Comparison of predicted vs actual outcomes
* Evaluation of fairness through error rates

---

## 🎯 Problem

COMPAS is a risk assessment tool used to predict the likelihood of reoffending.
Because these predictions influence high-stakes decisions (e.g., sentencing, parole), it is critical to evaluate whether the model treats individuals fairly.

The key question:

> Do COMPAS risk scores and prediction errors differ across demographic groups?

---

## 📊 Dataset

* Source: ProPublica COMPAS dataset
* Size: ~7,000 individuals
* Features include:

  * Demographics (age, race, sex)
  * Criminal history (priors count)
  * COMPAS risk score (decile_score)
  * Outcome variable (two_year_recid)

---

## 🧹 Data Cleaning

The dataset contains inconsistencies and must be filtered carefully.

Steps:

* Selected relevant features for analysis
* Removed records with invalid screening dates
* Dropped missing values

**Result:**
A clean dataset of valid observations suitable for fairness analysis.

---

## 🔍 Exploratory Analysis

* Examined distribution of COMPAS risk scores
* Compared risk score distributions across racial groups
* Analyzed actual recidivism rates by race

**Key observation:**
Risk scores differ across groups, raising initial concerns about fairness.

---

## ⚖️ Error Analysis (Core Section)

Defined:

* **False Positive:** Predicted high risk but did not reoffend
* **False Negative:** Predicted low risk but did reoffend

Findings:

* Error rates differ across racial groups
* Some groups experience higher false positive rates
* Other groups show higher false negative rates

---

## 🚨 Key Insight

Even when overall model performance appears acceptable, the **distribution of errors is unequal**.

This means:

* Certain groups may be disproportionately labeled as high risk
* Others may be underestimated in risk

These disparities can lead to **systematically unfair real-world outcomes**.

---

## 🧾 Conclusion

This analysis highlights an important limitation of algorithmic decision systems:

> Fairness cannot be evaluated using accuracy alone —
> it must consider how errors are distributed across groups.

The COMPAS case demonstrates how predictive models can produce unequal impacts, emphasizing the need for transparency and fairness evaluation in high-stakes domains.

---

## 🛠️ Tools Used

* Python (Pandas, NumPy)
* Data Visualization (Matplotlib, Seaborn)
* Jupyter Notebook

---

## 📂 Project Structure

compas-bias-analysis/
│
├── data/
├── notebook/
├── visuals/
├── README.md

---

## 🚀 Future Improvements

* Add predictive modeling (logistic regression)
* Evaluate precision/recall across groups
* Apply formal fairness metrics (e.g., equalized odds)
* Extend analysis to additional datasets


---


### Key Takeaways

- Algorithmic systems can produce unequal outcomes even when overall accuracy is acceptable
- Evaluating fairness requires analyzing error distributions, not just predictions
- Data quality and filtering play a critical role in reliable bias analysis
- Transparency in model behavior is essential in high-stakes decision-making contexts