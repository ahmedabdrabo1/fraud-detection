# Financial Transaction Fraud Detection

A machine learning project focused on identifying fraudulent financial transactions through exploratory data analysis, data quality assessment, feature engineering, and classification models.

## Objectives

* Analyze financial transaction data and identify patterns associated with fraudulent activity.
* Perform exploratory data analysis (EDA).
* Investigate class imbalance and fraud distribution across transaction types.
* Examine transaction amounts, account balances, and temporal patterns.
* Assess data quality and identify potential data leakage.
* Prepare suitable features for machine learning.
* Train and evaluate classification models using metrics appropriate for imbalanced datasets.

## Technologies

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Dataset Overview

The dataset contains **6,362,620 financial transactions** and **11 columns**.

| Property             | Description                              |
| -------------------- | ---------------------------------------- |
| Total records        | 6,362,620                                |
| Total columns        | 11                                       |
| Missing values       | 0 detected during the initial inspection |
| Target variable      | `isFraud`                                |
| Additional indicator | `isFlaggedFraud`                         |

### Main Features

| Feature          | Description                                                           |
| ---------------- | --------------------------------------------------------------------- |
| `step`           | Time step associated with the transaction                             |
| `type`           | Transaction type                                                      |
| `amount`         | Transaction amount                                                    |
| `nameOrig`       | Identifier of the originating account                                 |
| `oldbalanceOrg`  | Originating account balance before the transaction                    |
| `newbalanceOrig` | Originating account balance after the transaction                     |
| `nameDest`       | Identifier of the destination account                                 |
| `oldbalanceDest` | Destination account balance before the transaction                    |
| `newbalanceDest` | Destination account balance after the transaction                     |
| `isFraud`        | Target variable indicating fraudulent transactions                    |
| `isFlaggedFraud` | Indicator showing whether the original system flagged the transaction |

## Work Completed

### Milestone 1: Initial Dataset Exploration

* Loaded the dataset using Pandas.
* Inspected dataset dimensions, column names, data types, and memory usage.
* Checked for missing values.
* Examined the distribution of `isFlaggedFraud`.
* Calculated the overall fraud rate.
* Visualized transaction counts by type.

### Milestone 2: Exploratory Data Analysis (EDA)

* Analyzed transaction amount distributions using a logarithmic transformation.
* Examined transaction amounts in relation to the fraud target.
* Investigated changes in originating and destination account balances.
* Visualized fraudulent transactions over time using the `step` feature.
* Examined frequent sender and receiver account identifiers.
* Compared fraud counts and rates across transaction types.
* Investigated the relationship between numerical features using a correlation matrix.
* Examined transactions where the originating account balance became zero.
* Checked for duplicate rows.
* Analyzed the target class distribution and the degree of class imbalance.

## Key Findings

* The dataset contains **6,362,620 transactions** and **11 columns**.
* No missing values were detected during the initial data quality check.
* There are **8,213 fraudulent transactions**, representing approximately **0.1291%** of the dataset.
* Legitimate transactions account for approximately **99.8709%** of the records.
* The target variable is highly imbalanced, so accuracy alone is insufficient for evaluating model performance.
* `TRANSFER` has a fraud rate of approximately **0.769%**, while `CASH_OUT` has a fraud rate of approximately **0.184%**.
* In this dataset, fraudulent transactions were observed only in the `TRANSFER` and `CASH_OUT` categories.
* The dataset's features require further assessment before model training, particularly regarding potential data leakage and feature suitability.

## Current Project Status

**In Progress — Exploratory Data Analysis (EDA)**

Initial dataset inspection and the main exploratory analyses have been completed. The next stage is to review feature suitability, perform data preprocessing and feature engineering, and establish a baseline classification model.

## Planned Next Steps

1. Finalize data quality checks and document the EDA findings.
2. Assess feature relevance and investigate potential data leakage.
3. Define the feature matrix (`X`) and target variable (`y`).
4. Encode categorical variables and prepare suitable numerical features.
5. Split the dataset into training and testing sets using a strategy appropriate for the data.
6. Establish a baseline classification model.
7. Evaluate performance using Precision, Recall, F1-score, and Precision-Recall AUC.
8. Compare additional models and address class imbalance where appropriate.

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

* The raw dataset is excluded from version control.
* The repository contains project code, documentation, notebooks, and analysis rather than the raw dataset.
* Model performance and conclusions will be documented after the training and evaluation stages.
