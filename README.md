# ML_Assignment_2
## Name: Soumyajit De
## BITS ID: 2026CT05037

# Problem statement
Predict whether a telecom customer will churn (leave the company) based on their account, service and
billing information. This is a binary classification problem. Five classifiers (Logistic Regression,
Decision Tree, kNN, Gaussian Naive Bayes, Random Forest) are trained on the same dataset and
compared using Accuracy, AUC, Precision, Recall, F1 and MCC.

#  Dataset description
1. Source: IBM Telco Customer Churn dataset
2. Link: https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv
3. Instances: 7,043 (7,021 after removing 22 duplicate rows)
4. Features: 20 raw (19 after dropping the customerID identifier)
5. Target variable: Churn (Yes = 1, No = 0)
6. Feature types:
    - Numeric: tenure, MonthlyCharges, TotalCharges, SeniorCitizen (0/1)
    - Categorical (15): gender, Partner, Dependents, PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, StreamingTV, StreamingMovies, Contract, PaperlessBilling, PaymentMethod
7. Missing values: TotalCharges has 11 blank entries (new customers with tenure 0), converted to NaN and imputed.

# GITHub Repository Link
### [https://github.com/2026ct05037-SoumyajitDe/ML_Assignment_2.git](https://github.com/2026ct05037-SoumyajitDe/ML_Assignment_2)

# Model details
## Model configurations
| Model | Key hyper-parameters |
| --- | --- |
| Logistic Regression | `max_iter=1000` |
| Decision Tree | `max_depth=5`, `min_samples_leaf=20` |
| kNN | `n_neighbors=15` |
| Naive Bayes | `GaussianNB()` (defaults) |
| Random Forest | `n_estimators=300`, `max_depth=10`, `min_samples_leaf=5` |

## Models used – comparison table
| ML Model Name | Accuracy | AUC | Precision | Recall | F1 | MCC |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Logistic Regression | 0.8021 | 0.8403 | 0.6588 | 0.5242 | 0.5838 | 0.4614 |
| Decision Tree | 0.7950 | 0.8294 | 0.6228 | 0.5726 | 0.5966 | 0.4603 |
| kNN | 0.7900 | 0.8166 | 0.6199 | 0.5349 | 0.5743 | 0.4381 |
| Naive Bayes | 0.6811 | 0.8110 | 0.4457 | 0.8387 | 0.5821 | 0.4087 |
| Random Forest (Ensemble) | 0.7986 | 0.8400 | 0.6561 | 0.5027 | 0.5693 | 0.4475 |
