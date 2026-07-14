# VortexTech AI/ML - Week 2: Classification Model Training

## Project Overview
This week, the pipeline shifts from data exploration to predictive modeling. Using the cleaned Titanic dataset, we trained two distinct machine learning models—**Logistic Regression** and a **Decision Tree Classifier**—to predict passenger survival.

## Features Used
To predict the binary target `Survived` ($0$ = No, $1$ = Yes), we utilized the following features:
* **Numerical:** `Age`, `Fare`
* **Categorical (One-Hot Encoded):** `Pclass`, `Sex`, `Embarked`

---

## Model Performance Comparison

Both models achieved the exact same overall accuracy, but they behaved very differently under the hood:

| Metric | Logistic Regression | Decision Tree Classifier |
| :--- | :---: | :---: |
| **Accuracy** | **79.89%** | **79.89%** |
| **Precision** | 76.39% | **82.76%** |
| **Recall** | **74.32%** | 64.86% |
| **F1-Score** | **75.34%** | 72.73% |

### Key Takeaway
* The **Decision Tree** is highly conservative. When it predicts survival, it is usually right (high Precision), but it misses a lot of actual survivors (poor Recall).
* **Logistic Regression** is the more balanced model for this task, showing a much higher **F1-Score (75.34%)** due to its superior recall.

---

## Future Improvements
1. **Feature Scaling:** Apply `StandardScaler` to normalize continuous variables (`Age` and `Fare`).
2. **Feature Engineering:** Combine family relationship columns to create a single `FamilySize` metric.
3. **Hyperparameter Tuning:** Tune tree depth and regularization parameters to prevent overfitting.

## How to Run the Workspace
1. Clone this repository.
2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn jupyter




   
