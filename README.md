# Google Analytics - Predicting Customer Revenue to Maximize ROI
---
## Project Overview
The 80/20 rule is often observed in customer behavior, where only a small percentage of customers generate most of the revenue. 

This project focuses on analyzing customer data from the Google Merchandise Store (GStore) to optimize marketing strategies and maximize the return on investment (ROI). The two-stage approach is designed to:

1. Stage 1 (Classification): Identify potential buyers to narrow down the target audience for marketing campaigns.
2. Stage 2 (Regression): Predict revenue for these buyers, enabling precise budget allocation based on predicted revenue contributions.

By leveraging machine learning, this project provides actionable insights to target the right customers and improve marketing ROI.

---

## Key Features
- Classification Features:
  - Customer behavior: `hits_per_visit`, `bounced`, `time_on_site`.
  - Temporal data: `month`, `day_of_week`, `is_weekend`, `is_holiday_season`.
  - Acquisition channels: `channelGrouping`, `device_category`, `country`.
- Regression Target:
  - `log_transactionRevenue`, transformed as ln(revenue+1).

---
