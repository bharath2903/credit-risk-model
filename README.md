# 🧠 Credit Risk Prediction Model

A machine learning project to predict whether a customer is likely to default on a loan, using demographic, financial, and credit bureau data. This project demonstrates a complete end-to-end ML workflow — from raw data integration to model deployment using Streamlit.

---

## 🚀 Project Overview

**Goal**: Develop a classification model to predict loan default risk based on customer and credit history.  
**Solution**: Trained and deployed a logistic regression model with 93% accuracy and strong business interpretability.

---

## 📦 Data Sources
> ⚠️ *The dataset used in this project is provided as part of a [CodeBasics](https://codebasics.io) course and is not included in this repository due to licensing restrictions.*
The datasets include 50,000 rows and 3 tables:
- **Customer data** (demographics, income, residence, employment etc)
- **Loan application data** (loan amount, fees, purpose etc)
- **Credit bureau data** (accounts, defaults, utilization, DPD etc)

> Final dataset created by merging `customers.csv`, `loans.csv`, and `bureau_data.csv` using `cust_id`.

---

## 🛠 Tech Stack

- **Python**, **pandas**, **NumPy**
- **scikit-learn**, **XGBoost**
- **Streamlit** for deployment,**Optuna** for hyperparameter tuning
- **Matplotlib**, **Seaborn** for visualizations

---

## 📊 Project Workflow

### 1. Data Integration & Cleaning
- Merged data from 3 sources
- Handled missing values, removed duplicates
- Cleaned categorical and numerical columns
- Addressed class imbalance early in the pipeline

### 2. Exploratory Data Analysis (EDA)
- Univariate and bivariate analysis of key features
- Outlier detection with boxplots
- Created new features: `credit_utilization_ratio`, `delinquency_ratio`, etc.

### 3. Feature Engineering
- **VIF** used for numerical feature selection
- **Information Value (IV)** used for categorical feature ranking

### 4. Modeling & Evaluation
- Trained Logistic Regression, Random Forest, and XGBoost classifiers
- Chose **Logistic Regression** for interpretability with:
  - Accuracy: **0.93**
  - Recall: **0.94**
  - ROC AUC: **0.98**
  - KS Statistic: **85%**
  - Gini Coefficient: **0.96**
- Hyperparameter tuning done using **Optuna**

### 5. Deployment
- Deployed using **Streamlit**
- Modular structure:
  - `main.py` – Frontend app
  - `prediction_helper.py` – Model and preprocessing logic

---

## 🌐 Live Demo

👉 [Streamlit App](https://bharath2903-credit-risk-model.streamlit.app/)

---

## 🗂️ Repository Structure

credit-risk-model/
├── artifacts/
│   └── model_data.joblib        # Trained model saved using joblib
├── main.py                      # Streamlit UI for user interaction
├── prediction_helper.py         # ML prediction logic and preprocessing
├── requirements.txt             # Project dependencies
├── .gitignore                   # Files/folders to ignore in Git
└── README.md                    # Project documentation

--

## ✅ Key Learnings

- How to engineer and evaluate features for **credit risk** modeling
- Practical experience in dealing with **imbalanced classes**
- Full pipeline from raw data to **production-ready ML app**
- Importance of **model interpretability** in financial applications

---

## 🖥️ How to Run Locally

# 1. Clone the repository
```bash
git clone https://github.com/bharath2903/credit-risk-model.git
cd credit-risk-model
```
# 2. (Optional) Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate
```
# 3. Install dependencies
```bash
pip install -r requirements.txt
```
# 4. Run the Streamlit app
```bash
streamlit run main.py
```
## 📸 Screenshots 
<img width="1443" height="659" alt="image" src="https://github.com/user-attachments/assets/1130d49f-f7a0-4940-b8ed-a6b4257c34f2" />
<img width="693" height="466" alt="image" src="https://github.com/user-attachments/assets/5c031e90-960d-48af-b0e6-41d151f0ee0e" />
<img width="1048" height="409" alt="image" src="https://github.com/user-attachments/assets/854df32c-2593-4a41-9461-d5e11e2debc1" />

## 🙋‍♂️ Author

- **Bharath Srinivas**
- [LinkedIn](https://www.linkedin.com/in/bharath-srinivas-286460344/) 

> Project built as part of the CodeBasics ML course.


