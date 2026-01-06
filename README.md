# Customer-Lifetime-Value-CLV-Prediction
End‑to‑end pipeline for calculating Customer Lifetime Value (CLV) and predicting it using Random Forest regression and Gradient Boosting Model

## Business Problem
The company needs to identify high-value customers to improve marketing ROI and customer retention. CLV prediction enables data-driven decision making for long-term revenue growth.

## Dataset
Online retail transaction data containing invoices, products, prices, quantities, customer IDs and countries.

## Methodology (CRISP-DM)

### 1. Business Understanding
Predict future customer revenue to guide marketing and retention strategies.

### 2. Data Understanding
- 541,909 records
- Highly skewed revenue
- Significant customer heterogeneity

### 3. Data Preparation
- Removed missing CustomerID
- Removed cancellations and invalid records
- Created TotalAmount feature
- Engineered RFM & behavioral features
- Outlier treatment (1st–99th percentile)
- Log transformation for skew correction

### 4. Modeling
Models tested:
- Random Forest (baseline)
- Gradient Boosting Regressor (final)

Features used:
Recency, Frequency, Monetary, Tenure, AvgOrderValue, FrequencyPerMonth, RevenuePerMonth

### 5. Evaluation
Final model performance:
MAE: 0.249  
R²: 0.693

### 6. Business Insights
Customers segmented into Bronze, Silver, Gold, Platinum based on predicted CLV.

### Quantitative Performance

The final CLV model achieved strong predictive performance:
Metric	Value
MAE	0.249
R²	0.693
<img width="310" height="73" alt="image" src="https://github.com/user-attachments/assets/953a72e4-934f-46e2-a427-ba3debf9c7ff" />


This indicates that the model explains approximately 69% of the variance in future customer revenue, which is considered strong performance for Customer Lifetime Value modeling.

### Segment-wise CLV Validation

To further validate the model, customers were segmented into four groups based on their predicted CLV:

Bronze – Lowest value customers

Silver – Medium value customers

Gold – High value customers

Platinum – Highest value customers

The following chart shows the average predicted CLV for each segment:

<img width="653" height="595" alt="image" src="https://github.com/user-attachments/assets/ee943734-cfe0-4b0f-adfd-f180b936dee5" />

## Business Impact
- Enables precision marketing
- Improves retention strategy
- Enhances revenue forecasting
- Supports executive decision making
