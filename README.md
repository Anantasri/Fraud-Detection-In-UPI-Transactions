# Fraud Detection in UPI Transactions Using Random Forest Classifier

This project presents a machine learning-based approach to detect fraudulent transactions in Unified Payments Interface (UPI) systems using a Random Forest Classifier. The model is designed to identify anomalies and fraud patterns in transaction data by analyzing features such as transaction amount, frequency, and time-based attributes.

## Project Overview

With the rise of digital payments, fraud detection has become a crucial component of financial security. This project addresses the challenge by:

- Building a classification model using Random Forest
- Using SMOTE to handle class imbalance
- Performing feature selection with SelectKBest
- Scaling data using StandardScaler
- Evaluating model performance with metrics like precision, recall, F1-score, and ROC-AUC

## Tech Stack

- **Language:** Python
- **Libraries:** `pandas`, `numpy`, `scikit-learn`, `imblearn`, `matplotlib`, `seaborn`
- **Model Used:** Random Forest Classifier

## Dataset Description

The dataset contains 1,000 UPI transactions with the following features:

- Transaction ID, Timestamp
- Sender & Receiver details
- Amount, Status

## Preprocessing Steps

1. **Data Cleaning:** Removed duplicates and handled missing values.
2. **Feature Engineering:**
   - Extracted time-based features (Day, Hour, Weekday, Month)
   - Created `Transaction_Velocity` to measure transaction frequency
3. **Label Encoding:** Converted categorical variables.
4. **Scaling:** Normalized numerical values using `StandardScaler`.
5. **Class Balancing:** Applied `SMOTE` to oversample minority (fraud) class.
6. **Feature Selection:** Used `SelectKBest` with `f_classif` to keep top 10 features.

## Model Training

- Model: `RandomForestClassifier(n_estimators=100, max_depth=10)`
- Train/Test Split: 80% / 20%
- Target: `is_fraud`

### Performance Metrics:
- **Accuracy:** ~91%
- **Precision:** 86%
- **Recall:** 98%
- **F1-Score:** 92%
- **ROC-AUC:** 0.97

## Visualizations

- Confusion Matrix Heatmap
- ROC Curve

These visuals help in evaluating true positives, false positives, and model efficiency in distinguishing between fraudulent and legitimate transactions.

## Key Takeaways

- Random Forest provides robust performance with interpretability.
- Handling class imbalance using SMOTE significantly improved fraud detection accuracy.
- Time-based and behavioral features (like transaction velocity) are crucial in identifying fraud.

## Future Improvements

- Use real-world fraud labels instead of synthetic ones for better model generalization.
- Incorporate advanced behavioral analytics (e.g., transaction networks, user profiles).
- Experiment with other models (e.g., XGBoost, RNNs) for sequential fraud patterns.

## Authors

- **M. H. Ananta Sri** 
- **S. Akshalya**
- **P. Preethi Angel Arokia Mary**

Department of B.C.A, Ethiraj College for Women (Autonomous), Chennai.
> This project was submitted as part of the BCA degree requirement for the academic year 2024–2025.
