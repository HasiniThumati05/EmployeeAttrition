# ============================================================
# EMPLOYEE ATTRITION PREDICTION — COMPLETE PROJECT SETUP
# ============================================================

# ------------------------------------------------------------
# STEP 1: CREATE PROJECT FOLDER
# ------------------------------------------------------------
mkdir employee-attrition-prediction
cd employee-attrition-prediction

# ------------------------------------------------------------
# STEP 2: CREATE VIRTUAL ENVIRONMENT
# ------------------------------------------------------------
python -m venv venv

# Activate:
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# ------------------------------------------------------------
# STEP 3: INSTALL DEPENDENCIES
# ------------------------------------------------------------
pip install flask pandas numpy scikit-learn matplotlib seaborn joblib

# ------------------------------------------------------------
# STEP 4: CREATE FOLDER STRUCTURE
# ------------------------------------------------------------
mkdir data notebooks templates static images

# ============================================================
# FILE 1: requirements.txt
# ============================================================
cat > requirements.txt << 'EOF'
flask
pandas
numpy
scikit-learn
matplotlib
seaborn
joblib
EOF

# ============================================================
# FILE 2: README.md
# ============================================================
cat > README.md << 'EOF'
# Employee Attrition Prediction

A machine learning web application that predicts whether an employee is likely to leave the organization, based on HR data. Built with Python, Scikit-learn, and Flask.

---

## 📌 Table of Contents
- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Dataset](#-dataset)
- [Project Workflow](#-project-workflow)
- [Model Performance](#-model-performance)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Results & Insights](#-results--insights)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 📖 Overview

Employee attrition is a major challenge for organizations, leading to increased hiring costs, lost productivity, and knowledge drain. This project uses **machine learning** to identify employees who are at risk of leaving, enabling HR teams to take proactive retention measures.

The project includes:
- End-to-end data preprocessing and exploratory data analysis (EDA)
- Feature engineering and model training
- Model evaluation and selection
- A **Flask web application** for real-time attrition prediction

---

## ❓ Problem Statement

Given a dataset of employee records (demographics, job role, satisfaction, income, tenure, etc.), build a predictive model that classifies whether an employee will **attrite (Yes/No)**. The goal is to provide HR with an early-warning system to reduce turnover.

---

## ✨ Features

- 📊 Exploratory Data Analysis with visualizations
- 🧹 Data cleaning and missing value handling
- ⚙️ Feature engineering (encoding, scaling, selection)
- 🤖 Multiple ML models trained and compared
- 📈 Model evaluation using Accuracy, Precision, Recall, F1-Score, ROC-AUC
- 🌐 Flask web app for real-time predictions
- 📝 Clean, documented, and reproducible code

---

## 🛠 Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.x |
| Libraries | Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn |
| Web Framework | Flask |
| Frontend | HTML, CSS, Bootstrap |
| Notebook | Jupyter Notebook / Google Colab |
| Version Control | Git, GitHub |

---

## 📂 Dataset

- **Source:** IBM HR Analytics Employee Attrition Dataset (Kaggle)
- **Size:** ~1,470 records, 35 features
- **Target Variable:** `Attrition` (Yes / No)

Key Features: Age, Gender, MaritalStatus, Department, JobRole, JobLevel, MonthlyIncome, YearsAtCompany, JobSatisfaction, OverTime, BusinessTravel, StockOptionLevel.

---

## 🔄 Project Workflow

1. Data Collection — Load HR dataset (CSV).
2. Data Cleaning — Handle missing values, drop irrelevant columns.
3. EDA — Visualize attrition patterns.
4. Feature Engineering — Encode categorical, scale numerical.
5. Model Training — Logistic Regression, Decision Tree, Random Forest, Gradient Boosting.
6. Model Evaluation — Accuracy, Precision, Recall, F1, ROC-AUC.
7. Model Selection — Pick best model.
8. Deployment — Save with joblib and serve via Flask.

---

## 📊 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 0.85 | 0.72 | 0.60 | 0.65 | 0.82 |
| Decision Tree | 0.80 | 0.65 | 0.55 | 0.60 | 0.75 |
| Random Forest | 0.88 | 0.78 | 0.68 | 0.73 | 0.87 |
| Gradient Boosting | **0.90** | **0.82** | **0.72** | **0.77** | **0.90** |

✅ Best Model: Gradient Boosting

---

## ⚙️ Installation

```bash
git clone https://github.com/HasiniThumati/employee-attrition-prediction.git
cd employee-attrition-prediction
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
/

▶️ Usage
python app.py
/

🗂 Project Structure
employee-attrition-prediction/
├── app.py
├── model.pkl
├── scaler.pkl
├── requirements.txt
├── README.md
├── data/
│   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── notebooks/
│   └── Employee_Attrition_Prediction.ipynb
├── templates/
│   ├── index.html
│   └── result.html
├── static/
│   └── style.css
└── images/
/
📈 Results & Insights
🔴 Overtime employees are ~3x more likely to attrite.

💰 Lower monthly income correlates with higher attrition.

⏳ Employees with < 3 years tenure show highest attrition.

🧑‍💼 Sales and HR departments show higher turnover.

😊 Low JobSatisfaction and WorkLifeBalance predict attrition.

🚀 Future Improvements
SHAP / LIME for explainability

Deploy on Render / AWS

User authentication

HRMS integration

Auto-retraining pipeline

Power BI dashboard

👤 Author
Hasini Thumati

🎓 B.Tech CSE (AI & ML), Sir C.R. Reddy College of Engineering

📧 hasinithumati07@gmail.com
