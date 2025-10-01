🔍 Project Overview

This project aims to detect fraudulent credit card transactions by applying anomaly detection and machine learning techniques. Given the severe class imbalance (very few fraud cases), the workflow focuses on preprocessing, model tuning, combining multiple methods, and visualizing insights.
________________________________________
🛠 Workflow & Steps
1. Import & Setup
Loaded necessary Python libraries.

2. Dataset Structuring & Exploration
Organized dataset; explored basic structure (rows, features, types).

3. Class Imbalance Detection & Visualization
Discovered heavy class imbalance (fraudulent cases are rare).
Visualized distributions, trends, and feature relationships across fraud vs non-fraud.

4. Scaling & Train/Test Split
Applied feature scaling using StandardScaler and split data into training and testing sets.

5. Isolation Forest Modeling
Trained an IsolationForest model; tuned the threshold automatically to detect anomalies.

6. PCA + DBSCAN Optimization
Applied PCA for dimensionality reduction, then used DBSCAN to cluster and isolate potential anomalies.

7. Result Combination & Evaluation
   Merged outputs / decisions from different models.
   Since results were not initially satisfactory, performed hyperparameter tuning.
   Evaluated performance using classification metrics (precision, recall, F1), and visualized with a confusion matrix.

8. Performance Summary
Final confusion matrix:
     [[55586  1065]
     [   25    70]]
Classification report:
Class	Precision	Recall	F1-Score	Support
0	    1.00	      0.98	  0.99	  56,651
1	    0.06	      0.74	  0.11	  95
o	Accuracy: 0.98
o	Macro Avg: Precision 0.53 | Recall 0.86 | F1 0.55
o	Weighted Avg: Precision ~1.00 | Recall ~0.98 | F1 ~0.99
The model is strong in identifying normal (non-fraud) transactions but still struggles with fraud class due to its rarity.

9. SQL Aggregations
   Performed varied SQL queries to aggregate insights on fraudulent transactions (e.g. by time, amount, user behavior).

10. Visualization & Dashboard
Presented all key findings and metrics using Power BI dashboards and visual reports.
________________________________________
📌 Key Takeaways & Challenges
•	Handling extreme class imbalance remains a major challenge: catching fraud (minority class) while keeping false positives low.
•	Combining multiple techniques (IsolationForest, PCA, DBSCAN) and hyperparameter tuning helps improve detection.
•	The model shows very high accuracy for the majority class; detecting fraud is still difficult given data scarcity.
•	Visual dashboards help stakeholders quickly grasp fraud patterns and model insights.

