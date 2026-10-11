# Financial Transaction Fraud Detection

A machine learning project focused on identifying fraudulent financial transactions through exploratory data analysis, data preprocessing, and classification models.

## Objectives

* Understand and explore financial transaction data.
* Perform exploratory data analysis (EDA).
* Investigate fraudulent and legitimate transaction patterns.
* Prepare data for machine learning.
* Train and evaluate classification models.
* Assess model performance using appropriate evaluation metrics for imbalanced datasets.

## Technologies

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Dataset Overview

The dataset contains financial transaction records with the following characteristics:

* **Total records:** 6,362,620
* **Total columns:** 11
* **Missing values:** 0, based on the initial check
* **Target variable:** `isFraud`
* **Additional indicator:** `isFlaggedFraud`

### Main Features

| Feature          | Description                                                                  |
| ---------------- | ---------------------------------------------------------------------------- |
| `step`           | Time step associated with the transaction                                    |
| `type`           | Transaction type                                                             |
| `amount`         | Transaction amount                                                           |
| `nameOrig`       | Identifier of the originating account                                        |
| `oldbalanceOrg`  | Originating account balance before the transaction                           |
| `newbalanceOrig` | Originating account balance after the transaction                            |
| `nameDest`       | Identifier of the destination account                                        |
| `oldbalanceDest` | Destination account balance before the transaction                           |
| `newbalanceDest` | Destination account balance after the transaction                            |
| `isFraud`        | Target variable indicating fraudulent transactions                           |
| `isFlaggedFraud` | Indicator showing whether the transaction was flagged by the original system |

## Work Completed

### Milestone 1: Initial Dataset Exploration

* Loaded the dataset using Pandas.
* Inspected the dataset dimensions and column names.
* Reviewed data types and memory usage.
* Checked for missing values.
* Examined the distribution of the `isFlaggedFraud` indicator.
* Calculated the percentage of fraudulent transactions using `isFraud`.
* Visualized the distribution of transaction types.
* Compared fraud rates across transaction types.

### Initial Findings

* The dataset contains **6,362,620 transactions** and **11 features**.
* No missing values were detected during the initial check.
* Fraudulent transactions represent approximately **0.13%** of all records.
* The dataset is highly imbalanced, making appropriate evaluation metrics essential.
* Initial visualizations were created to explore transaction types and fraud rates by type.

## Current Project Status

**In Progress — Exploratory Data Analysis (EDA)**

The initial dataset inspection and visualizations have been completed. Further analysis is required before selecting features, preparing the data, and training machine learning models.

## Planned Next Steps

1. Investigate the distribution of the target variable, `isFraud`.
2. Analyze transaction amounts and account balance changes.
3. Check for duplicate records and potential data quality issues.
4. Investigate potential data leakage and feature suitability.
5. Prepare the data for model training.
6. Establish a baseline classification model.
7. Evaluate models using Precision, Recall, F1-score, and Precision-Recall AUC.

## Repository Structure

```text
fraud-detection/
├── data/
├── notebooks/
│   └── 01_exploratory_data_analysis.ipynb
├── src/
├── models/
├── reports/
├── .gitignore
├── requirements.txt
└── README.md
```

## Notes

The dataset is excluded from version control. The repository stores the project code, documentation, and analysis rather than the raw dataset.
