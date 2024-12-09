# Google Analytics - Predicting Customer Revenue to Maximize ROI
---
## Project Overview
In e-commerce, the 80/20 rule—where a small fraction of customers generates the majority of revenue—commonly holds true. However, in this case, the analysis shows an even starker reality: **99% of users do not make purchases**. This highlights the critical importance of optimizing marketing resources to focus on high-value customers.

This project aims to:
1. Identify potential buyers to narrow the target audience for marketing campaigns.
2. Predict revenue contributions from buyers to prioritize and optimize marketing spend.

---

## Key Insights
### Purchasers vs. Non-Purchasers
The stark disparity between purchasers and non-purchasers in e-commerce is visualized below, demonstrating the need for a focused strategy. 

<img src="images/number_users.png" alt="Purchasers vs Non-Purchasers" width="400">

### Behavioral Differences
Purchasers display significantly different behaviours compared to non-purchasers. On average, they: 
- Visit the site more often.
- Interact with more pages.
- Spend substantially more time on the site.

<img src="images/purcharsesVSnon-purcharsers.png" width="600">

---

## Methodology
1. Data Preparation:
     - Addressed class imbalance using SMOTE and class weighting.
     - Engineered features from customer behaviour and temporal data.

2. Stage 1: **Buyer Prediction (Classification)**
     - Model: Random Forest Classifier.
     - Objective: Accurately identify potential buyers.
     - Key Metrics:
         - ROC-AUC = 0.9792
         - Precision (Buyers) = 0.31
         - Recall (Buyers) = 0.69

3. Stage 2: **Revenue Prediction (Regression)**
    - Model: Random Forest Regressor.
    - Objective: Predict revenue for potential buyers to prioritize high-value customers.
    - Target Transformation: Applied $$\text{ln(revenue+1)}$$ to handle skewness and zero values.
    - Key Metrics:
         - RMSE = 10.7835
         - R² = 0.3419
--- 

## Impact

1. Optimized Marketing Spend: Focuses budgets on high-value customers.
2. Improved ROI: Guides investment toward customers with higher revenue potential.
3. Scalable Framework: Provides a reliable structure for customer segmentation and revenue prediction.

---
## Dashboadr
---

