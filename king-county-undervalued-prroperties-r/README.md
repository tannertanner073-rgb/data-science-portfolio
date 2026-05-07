# King County Undervalued Property Analysis

##  Overview

This project builds a simple pricing model to identify homes that may be **mispriced relative to their estimated market value**.

Instead of asking:
> “What drives housing prices?”

This project answers:
> **“Where is the market potentially getting pricing wrong?”**

---

##  Approach

- Built a **linear regression model** using key features:
  - Square footage
  - Grade (quality)
  - Bathrooms
  - View / Waterfront

- Used the model as a **pricing benchmark**, not a perfect predictor

- Calculated:
  ```r
  price_difference = predicted_price - actual_price
  ```

- Interpreted:
  - Positive → Potential undervaluation  
  - Negative → Potential overvaluation  

---

##  Key Visualization

[Actual vs Predicted](images/actual_vs_predicted.png)

**How to read this:**
- Red line = perfect pricing  
- Above line → undervalued  
- Below line → overvalued  

---

##  Key Insights

- The model explains a meaningful portion of price variation (**R² ≈ 0.59**)
- Mispricing is **not random** — it clusters in certain property types
- Higher-end homes show **larger prediction errors**, suggesting:
  - Pricing depends on factors not captured in the model  
  - (e.g., condition, timing, negotiation dynamics)

 **Most important insight:**
> The value is not predicting price perfectly —  
> it's identifying **systematic pricing gaps**.

---

##  Business Value

This approach can be used to:

- Screen for **potential investment opportunities**
- Identify **pricing inefficiencies** in the market
- Support **pricing decisions for listings**

---

##  Limitations

This model does **not capture**:
- Interior condition
- Renovation quality
- Market timing
- Buyer/seller negotiation behavior

Results should be interpreted as **signals**, not guaranteed opportunities.

---

##  Takeaway

This project demonstrates how a simple model can be used not just for prediction,  
but for **decision-making and opportunity identification**.
