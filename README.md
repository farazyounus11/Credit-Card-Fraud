This project explores multiple approaches for detecting fraudulent transactions using the Kaggle Credit Card Fraud Dataset. It covers exploratory analysis, feature scaling, distance-based anomaly detection, and ensemble modeling.
Key Highlights:

Data Preprocessing:
Stratified train-test split to maintain class distribution.
Addressed severe class imbalance using undersampling (fraud:non-fraud ≈ 1:5).
Feature scaling with StandardScaler and RobustScaler to handle outliers and improve model performance.

Exploratory Analysis:
Group-wise standardization and visualization of mean feature values for fraud vs non-fraud cases.
Identified features with the largest standardized mean differences.

Distance-Based Anomaly Detection:
Implemented Mahalanobis, Euclidean, and Manhattan distance classifiers using class-specific means and covariance matrices.
Evaluated using confusion matrices and ROC AUC:
Mahalanobis ROC AUC: ~0.92
Euclidean ROC AUC: ~0.89
Manhattan ROC AUC: ~0.90

Ensemble Modeling:
Built a soft voting ensemble combining:
Logistic Regression (L1 regularization)
Random Forest
XGBoost
Achieved strong results:
ROC AUC: ~0.977
Recall (Fraud class): ~0.83
Precision (Fraud class): ~0.40
Feature Importance:
Extracted feature importances from RandomForest and XGBoost to interpret key contributing features.

Results:
The ensemble classifier outperformed simple distance-based methods, providing a high recall on fraud detection while maintaining overall accuracy.
