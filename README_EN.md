# Customer Repurchase Propensity

## About the Project

This project aims to analyze customer purchasing behavior and develop machine learning models to predict which customers are more likely to make another purchase.

The analysis uses the **Online Retail II** dataset and considers features such as recency, invoice count, total quantity purchased, and total spending.

## Objectives

- Explore and understand the sales data.
- Prepare the data for analysis.
- Create features that represent customer purchasing behavior.
- Train and evaluate machine learning models.
- Compare model performance and identify opportunities for marketing actions.

## Project Structure

```text
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_exploratory_analysis.ipynb
│   ├── 02_features_and_target.ipynb
│   └── 03_modeling_and_evaluation.ipynb
├── reports/
│   └── model_results.csv
├── README.md
├── README_EN.md
└── requirements.txt
```

## Analysis Steps

### 1. Exploratory Data Analysis

Initial exploration of the dataset, identification of purchasing patterns, and data quality checks.

### 2. Data Preparation

Data cleaning and creation of a customer-level dataset containing information about each customer's purchasing history.

### 3. Feature and Target Engineering

The following features were used:

- `recency_days`: number of days since the last purchase.
- `invoice_count`: number of invoices.
- `total_quantity`: total quantity of products purchased.
- `total_spend`: total amount spent.

The target indicates whether a customer made another purchase within the time window defined for the analysis.

### 4. Modeling

Three approaches were compared:

- Baseline based on invoice count.
- Logistic Regression.
- Random Forest.

### 5. Evaluation

The models were evaluated using ROC-AUC and PR-AUC.

| Model | ROC-AUC | PR-AUC |
|---|---:|---:|
| Baseline - Invoice Count | 0.713 | 0.758 |
| Logistic Regression | 0.729 | 0.793 |
| Random Forest | 0.715 | 0.791 |

Logistic Regression achieved the best results among the evaluated models. However, its ROC-AUC improvement over the baseline was small, so the results should be interpreted with caution.

## How to Run

1. Clone or download this repository.
2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the `notebooks` folder.
4. Run the notebooks in the following order:

   1. `01_exploratory_analysis.ipynb`
   2. `02_features_and_target.ipynb`
   3. `03_modeling_and_evaluation.ipynb`

Check file paths and dependencies before running the project in another environment.

## Limitations

- The analysis uses a single retail dataset.
- Model performance may vary across different time periods.
- Validation on new periods is important to assess generalization.
- The results do not guarantee that a customer will make another purchase.

## Data Source

Online Retail II — UCI Machine Learning Repository.

https://archive.ics.uci.edu/
