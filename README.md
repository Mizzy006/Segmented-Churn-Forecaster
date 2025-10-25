# Segmented Churn Forecaster 
An integrated Machine Learning pipeline designed to move customer retention efforts from reactive spending to proactive, value-based targeting. The project's core output is a Prioritization Matrix that directs budget to high-value, high-risk customer segments.
## Project Goal
To accurately identify customers most likely to churn and prioritize intervention only for those who also have a high predicted Customer Lifetime Value (CLTV).
## Key Results
### Classification AUC

Model: Random Forest

Result: 0.87

Insight: High accuracy in predicting churn risk.

### Regression R^2

Model: Random Forest Regressor

Result: 0.26

Insight: Sufficient stability for relative value prioritization.

### Target Group

Model: Prioritization Matrix

Result: 153 Customers

Insight:  The total number of High-Risk, High-Value customers requiring immediate action.

## Technical Stack
•	Primary Language: Python

•	Libraries: Pandas, NumPy, Scikit-learn (PCA, K-Means, RF Classifier/Regressor), Matplotlib/Seaborn.

•	Techniques: One-Hot Encoding, SMOTE, Log Transformation, Hyperparameter Tuning.

## Methodology Pipeline
The solution integrates three distinct ML models:
### 1.	Unsupervised Learning (Segmentation):
o	Used PCA and K-Means (K=4) to cluster customers into four distinct behavioral groups (e.g., Urgent Churners, High Value Loyalists).

o	Result: The resulting ClusterID was the single most important feature for churn prediction.
### 2.	Classification (Risk Prediction):
o	Trained a Random Forest Classifier to predict P(Churn).

o	Top Churn Driver: ClusterID and Tenure Months.
### 3.	Regression (Value Quantification):
o	Trained a Random Forest Regressor on the CLTV target.

o	Top Value Driver: Tenure Months and Total Charges.

## Actionable Recommendation
The Prioritization Matrix guides the final strategy:

The most critical group is the 74.5% of High-Value/High-Risk customers who belong to the Urgent Churners segment.

Final Offer Strategy: To address the customer's two core issues (high cost and low commitment), deploy a combined offer:
Offer a 15% discount on the Monthly Charge, contingent upon signing a Two-Year Contract. This strategy uses risk reduction to secure value maximization.

