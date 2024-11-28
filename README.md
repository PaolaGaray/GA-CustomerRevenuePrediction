# Google Analytics - Predicting Customer Revenue to Maximize ROI
---
## Project Overview
The 80/20 rule is often observed in customer behavior, where only a small percentage of customers generate most of the revenue. 

This project focuses on analyzing customer data from the Google Merchandise Store (GStore) to optimize marketing strategies and maximize the return on investment (ROI). The two-stage approach is designed to:

1. Stage 1 (Classification): Identify potential buyers to narrow down the target audience for marketing campaigns.
2. Stage 2 (Regression): Predict revenue for these buyers, enabling precise budget allocation based on predicted revenue contributions.

---

## Key Features
- Classification Features:
  - Customer behavior: `hits_per_visit`, `bounced`, `time_on_site`.
  - Temporal data: `month`, `day_of_week`, `is_weekend`, `is_holiday_season`.
  - Acquisition channels: `channelGrouping`, `device_category`, `country`.
- Regression Target:
  - `log_transactionRevenue`, transformed as $$\text{ln(revenue+1)}$$

---

## Methodology
1. Data Preparation:
     - Addressed class imbalance using oversampling and class weighting.

2. Stage 1: Buyer Prediction
     - Model: Random Forest Classifier.
     - Techniques: SMOTE, class weighting, and threshold tuning to balance recall (buyers) and precision.
     - Performance:
         - ROC-AUC = 0.9792
         - Precision (Buyers) = 0.31
         - Recall (Buyers) = 0.69
    Result: Identifies potential buyers, effectively narrowing the audience for targeted marketing.

3. Stage 2: Revenue Prediction
    - Dataset: Filtered predicted buyers from Stage 1 and included `log_transactionRevenue` as the target.
    - Target Transformation: Applied $$\text{ln(revenue+1)}$$ to address skewness, stabilize variance, and handle zero values.
    - Model: Random Forest Regressor.
    - Performance:
         - RMSE = 10.7835
         - R² = 0.3419
    Result: Estimates revenue for buyers, enabling prioritization of high-value customers.

--- 

## Impact

1. Optimized Marketing Spend: Focuses budgets on high-value customers.
2. Improved ROI: Guides investment toward customers with higher revenue potential.
3. Scalable Framework: Provides a reliable structure for customer segmentation and revenue prediction.

---

