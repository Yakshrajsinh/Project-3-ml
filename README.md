
# 🏦 Digital Banking Customer Risk Classification

## 📌 Project Overview

This project focuses on developing a Machine Learning-based classification system to identify high-risk customers in a digital banking platform.

The system predicts whether a customer belongs to the **Low Risk (0)** or **High Risk (1)** category based on demographic information, transaction activities, credit behavior, and other financial indicators.

The primary objective is to develop an effective early-warning system that helps banks identify customers who may default on payments or exhibit potentially fraudulent behavior.

A major challenge in this project is the highly imbalanced dataset, where high-risk customers represent a minority class. Different sampling techniques and classification algorithms are implemented to improve minority-class detection.

---

## 🎯 Project Objectives

- Build a machine learning classification pipeline.
- Predict high-risk and low-risk customers.
- Handle imbalanced datasets using sampling techniques.
- Implement and compare multiple classification algorithms.
- Evaluate models using advanced classification metrics.
- Optimize model performance using hyperparameter tuning.
- Identify the best-performing model while minimizing false negatives.

---

## 📂 Dataset Description

The dataset contains customer demographic, financial, behavioral, and transaction-related information.

### Dataset Features

| Feature | Description |
|---|---|
| customer_id | Unique customer identifier |
| age | Customer's age |
| gender | Customer's gender |
| region | Customer's geographical region |
| employment_type | Employment category |
| annual_income_inr | Annual income in INR |
| credit_score | Customer's credit score |
| credit_utilization_ratio | Credit utilization ratio |
| missed_payments_12m | Missed payments in the last 12 months |
| avg_late_payment_days | Average payment delay |
| monthly_transaction_count | Number of monthly transactions |
| monthly_spend_inr | Monthly spending in INR |
| cash_advance_count_6m | Cash advances in the last 6 months |
| complaints_last_6m | Customer complaints in the last 6 months |
| failed_login_attempts_3m | Failed login attempts in the last 3 months |
| account_tenure_months | Account age in months |
| last_transaction_date | Date of last transaction |
| debt_balance_inr | Outstanding debt balance |
| risk_status | Target variable |

### Target Variable

- **0 – Low Risk**
- **1 – High Risk**

---

## 🛠️ Technologies & Libraries Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn

---

## ⚙️ Project Workflow

### 1. Data Understanding & Preprocessing

- Load and inspect the dataset.
- Identify input features and target variable.
- Analyze missing values.
- Apply KNN Imputer for numerical missing values.
- Apply categorical imputation.
- Perform feature encoding and scaling.
- Split the dataset into training and testing sets using stratified sampling.

### 2. Baseline Classification Model

Implemented Logistic Regression as the baseline classification algorithm.

Evaluation metrics:
- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1-Score

### 3. Handling Imbalanced Data

The following sampling techniques were implemented:

| Technique | Description |
|---|---|
| Under-Sampling | Reduces majority-class samples |
| Over-Sampling | Increases minority-class samples |
| SMOTE | Generates synthetic minority-class samples |
| ADASYN | Generates synthetic samples based on learning difficulty |

The impact of each technique is compared using Recall, F1-Score, and AUC-ROC.

### 4. Tree-Based Classification Models

The following algorithms were implemented:

- Decision Tree Classifier
- Random Forest Classifier

Training and testing performance are compared to analyze overfitting and model generalization.

### 5. Hyperparameter Tuning

Model optimization is performed using:

- Randomized Search CV
- Grid Search CV

Important hyperparameters are optimized to improve classification performance.

### 6. Model Evaluation & ROC Analysis

All models are evaluated and compared using:

- Accuracy
- Precision
- Recall
- F1-Score
- True Positive Rate (TPR)
- False Positive Rate (FPR)
- AUC-ROC

ROC curves are plotted to compare model performance.

### 7. Final Model Selection

The final model is selected based on business requirements, with particular emphasis on minimizing false negatives.

---

## 📊 Evaluation Metrics

| Metric | Purpose |
|---|---|
| Accuracy | Overall prediction correctness |
| Precision | Correctness of high-risk predictions |
| Recall | Ability to identify actual high-risk customers |
| F1-Score | Balance between precision and recall |
| TPR | Proportion of high-risk customers correctly identified |
| FPR | Proportion of low-risk customers incorrectly flagged |
| AUC-ROC | Overall ability to distinguish between classes |

### Important Business Consideration

**False Negative (Type-II Error):** A high-risk customer is incorrectly classified as low-risk. This may result in financial losses for the bank.

**False Positive (Type-I Error):** A low-risk customer is incorrectly classified as high-risk. This may result in unnecessary customer verification and investigation costs.

Therefore, high-risk customer Recall is an important metric when selecting the final model.

---

## 📁 Project Structure

```text
Digital-Banking-Risk-Classification/
│
├── README.md
│
├── digital_banking_risk_classification.ipynb
│
├── dataset/
│   └── customer_risk.csv
│
├── plots/
│   ├── confusion_matrix.png
│   ├── roc_curve.png
│   └── model_comparison.png
│
└── requirements.txt
```

---

## 🚀 Installation & Execution

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/Digital-Banking-Risk-Classification.git
```

### Step 2: Navigate to the Project Folder

```bash
cd Digital-Banking-Risk-Classification
```

### Step 3: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

### Step 5: Run the Project

Open:

`digital_banking_risk_classification.ipynb`

Place the dataset in the appropriate folder and execute all notebook cells.

---

## 📈 Expected Project Outcomes

- Identification of high-risk banking customers.
- Comparison of multiple classification algorithms.
- Understanding of class imbalance and its impact.
- Performance improvement through sampling techniques.
- Optimized classification models through hyperparameter tuning.
- Selection of a suitable model for early risk detection.

*Actual model performance and the best-performing algorithm will be reported after evaluating the supplied dataset.*

---

## 💡 Future Enhancements

- Implement XGBoost and LightGBM classifiers.
- Perform feature importance analysis.
- Implement cost-sensitive learning.
- Optimize classification thresholds based on business costs.
- Develop an interactive customer risk prediction dashboard.
- Deploy the final model using Flask or Streamlit.

---

## 👨‍💻 Author

**Yashraj**

Machine Learning | Data Science | Python

---

## ⭐ Conclusion

This project demonstrates an end-to-end machine learning approach to customer risk classification in digital banking.

By combining data preprocessing, imbalance-handling techniques, multiple classification algorithms, and hyperparameter optimization, the project aims to develop a reliable early-warning classification system.

The primary focus is to improve the identification of high-risk customers while balancing false positives and false negatives to support better banking risk management.
