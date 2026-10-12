# Financial Transaction Fraud Detection

A machine learning project for detecting fraudulent financial transactions using exploratory data analysis, data preprocessing, and classification models.

## Dataset

* **Source:** [Fraud Detection Dataset — Kaggle](https://www.kaggle.com/datasets/amanalisiddiqui/fraud-detection-dataset?resource=download)
* **Records:** 6,362,620
* **Columns:** 11
* **Target variable:** `isFraud`
* **Fraudulent transactions:** 8,213 (approximately 0.1291%)

## Technologies

* Python
* Pandas and NumPy
* Matplotlib and Seaborn
* Scikit-learn
* Jupyter Notebook

## Work Completed

* Performed exploratory data analysis (EDA) and initial data quality checks.
* Analyzed fraud distribution across transaction types.
* Investigated transaction amounts, account balances, and temporal patterns.
* Examined class imbalance and potential data leakage.
* Selected relevant transaction and account balance features.
* Encoded categorical features using `OneHotEncoder`.
* Scaled numerical features using `StandardScaler`.
* Established a baseline using `DummyClassifier`.
* Trained a class-weighted `LogisticRegression` model.
* Tuned the classification threshold using validation data.
* Evaluated the selected threshold on the test set.

## Baseline Model

**Algorithm:** Logistic Regression

**Classification threshold:** `0.99`

### Test Results

| Metric            | Fraud Class |
| ----------------- | ----------: |
| Precision         |        0.49 |
| Recall            |        0.55 |
| F1-score          |        0.52 |
| Average Precision |      0.5606 |

### Confusion Matrix

| Actual / Predicted | Legitimate | Fraud |
| ------------------ | ---------: | ----: |
| Legitimate         |  1,269,965 |   916 |
| Fraud              |        746 |   897 |

The model detected 897 fraudulent transactions and missed 746. It also incorrectly classified 916 legitimate transactions as fraudulent.

Because the dataset is highly imbalanced, accuracy alone is insufficient for evaluating fraud detection performance. Precision, Recall, F1-score, and Average Precision provide more informative evaluation metrics.

## Project Status

In Progress — Baseline Modeling and Evaluation

The Logistic Regression model serves as the initial benchmark. Further experiments are required to improve fraud detection performance.

## Next Steps

* Train and evaluate a Decision Tree classifier.
* Compare additional classification algorithms.
* Investigate feature engineering and class imbalance strategies.
* Analyze feature importance and model errors.
* Select a suitable model and classification threshold using validation results.

## Project Structure

```text
fraud-detection/
├── data/
├── notebooks/
├── src/
├── models/
├── reports/
├── .gitignore
├── requirements.txt
└── README.md
```

## Notes

* The raw dataset is excluded from version control.
* Dataset usage is subject to the source's terms and license.
* The current model is intended for experimentation and is not validated for production use.
