# Google Analytics - Predicting Customer Revenue to Maximize ROI
---
## Overview

This project focuses on analyzing customer data from the Google Merchandise Store (GStore) to optimize marketing strategies and maximize the return on investment (ROI). The two-stage approach is designed to:

1. Identify potential buyers to narrow down the target audience for marketing campaigns.
2. Predict revenue for these buyers, enabling precise budget allocation based on predicted revenue contributions.

By leveraging machine learning, this project provides actionable insights to target the right customers and improve marketing ROI.

---

## Project Overview

The 80/20 rule is often observed in customer behavior, where only a small percentage of customers generate most of the revenue. This project uses Google Analytics data to analyze these patterns and build predictive models that help identify both potential spenders and their likely contribution to revenue.

---

## Two-Stage Modeling Approach

To effectively model both purchasing behaviour and, revenue prediction, there is a two-stage approach:
1. Stage 1: Classification Model:
   - Objective: Predict whether a user will make a purchase (binary classification).
   - Benefit: By isolating the subset of users likely to make a purchase, I can focus the second model on predicting revenue amounts, reducing noise from non-purchasing users.
3. Stage 2: Regression Model:
   - Objective: For users likely to make a purchase, predict the amount of revenue generated.
   - Benefit: This approach allows me to model spending behaviour more accurately, focusing only on users identified as potential spenders.

---

## Data Description

The dataset consists of customer visit data for the Google Merchandise Store. Each row in the dataset represents a visit to the store, containing information about:

- Visitor Information (`fullVisitorId`): A unique identifier for each user.
- Visit Details (`visitId`, `visitStartTime`): Details about individual sessions.
- Traffic Source (`trafficSource`, `channelGrouping`): Information about how the user arrived at the store.
- Device and Location (`device`, `geoNetwork`): Specifications about the user’s device and location.
- Session Aggregates (`totals`): Aggregated data per session, including metrics like page views and transaction revenue.

The target variable for prediction is the **total revenue per user** (summed across all sessions), transformed as `ln(y_user + 1)` to account for skewed revenue distribution. This transformation allows the model to learn effectively across a range of user spending patterns.
