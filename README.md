# SyriaTel Customer Churn Prediction Analysis

## Project Overview
This project analyzes customer churn prediction for SyriaTel, a telecommunications company. The goal is to develop a machine learning model that can accurately identify customers who are likely to churn (cancel their service). By predicting churn, the company can proactively offer incentives and implement retention strategies to reduce revenue loss.

## Dataset
- Source: [Kaggle Telecom Churn Dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)
- Size: 3,333 customers, 21 features
- Target Variable: `churn` (binary: yes/no)

## Key Findings
- The dataset has no missing values.
- The target variable `churn` is imbalanced (14.5% churn rate).
- Key predictors of churn:
    - **Customer service calls:** Customers who churn tend to make more service calls.
    - **International plan:** Customers with international plans are more likely to churn.
    - **Total day minutes:** Higher usage during the day is correlated with churn.

## Models
- **Logistic Regression:** A baseline linear model for interpretability.
- **Decision Tree:** A tuned model using `GridSearchCV` to capture non-linear relationships.

## Performance Metrics
The primary metric for model evaluation is **Recall**, as minimizing false negatives (failing to identify churners) is crucial.

| Metric            | Logistic Regression | Tuned Decision Tree |
|-------------------|----------------------|-----------------------|
| True Negatives (TN) | 468                  | 494                   |
| False Positives (FP)| 102                  | 76                    |

- The tuned Decision Tree model outperformed Logistic Regression, achieving a higher true negative rate and a lower false positive rate.

## Business Recommendations
1. **Improve Customer Service:** Focus on resolving customer issues quickly to reduce the number of service calls.
2. **Review International Plans:** Investigate pricing and service quality for international plans to reduce churn among these users.
3. **Target High-Usage Customers:** Consider proactive outreach to high-usage daytime customers to address potential concerns.

## Code and Libraries
The analysis was performed using Python and the following libraries:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Usage
1.  Clone the repository.
2.  Install the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  **Run the `Customer Churn Prediction.ipynb`**

## Author
Antony Njoroge