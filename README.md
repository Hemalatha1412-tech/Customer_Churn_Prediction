# 📉 Predictive Customer Churn Modeling

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3-orange?logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Machine%20Learning-9b59b6)
![License](https://img.shields.io/badge/License-MIT-yellow)

> **Predicting customer attrition in the telecom industry using classification models — with quantified business insights to support retention strategy.**

---

## 📌 Project Overview

Customer churn — when a customer stops using a service — directly impacts revenue. This project builds a complete machine learning pipeline to **predict which telecom customers are likely to churn**, enabling proactive retention efforts before it's too late.

Using the real-world **Telco Customer Churn dataset from Kaggle**, this project covers the full ML lifecycle:

```
EDA → Feature Engineering → Model Building → Cross-Validation → Evaluation → Business Insights
```

---

## 🎯 Objectives

- Identify customers at high risk of churning before they leave
- Understand which features drive churn the most (with real numbers)
- Achieve **≥85% accuracy** with robust cross-validation
- Translate model outputs into concrete, actionable business recommendations

---

## 📊 Dataset

| Property | Details |
|---|---|
| **Source** | [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) |
| **Records** | 7,043 customers |
| **Features** | 21 (demographics, service subscriptions, billing) |
| **Target** | `Churn` (Yes / No) |
| **Class Balance** | ~73% No Churn · ~27% Churned |

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.10 |
| Data Manipulation | Pandas, NumPy |
| Machine Learning | Scikit-learn |
| Visualization | Matplotlib, Seaborn |
| Environment | Jupyter Notebook |
| Models | Logistic Regression, Random Forest, Gradient Boosting |

---

## 📁 Project Structure

```
customer-churn-modeling/
│
├── churn_modeling.ipynb                    # Main notebook (full pipeline)
├── README.md                               # Project documentation
├── requirements.txt                        # Python dependencies
└── data/
    └── WA_Fn-UseC_-Telco-Customer-Churn.csv   # Dataset (from Kaggle)
```

---

## 🔄 Pipeline Walkthrough

| Step | Description |
|---|---|
| 1. Install Dependencies | Auto-installs all packages from inside the notebook |
| 2. Import Libraries | All imports with version validation |
| 3. Load Dataset | 3 loading options: Kaggle API, local file, GitHub mirror |
| 4. EDA | Distribution plots, categorical breakdowns, correlation heatmap |
| 5. Preprocessing | Fix TotalCharges dtype, median imputation for NaNs, label encode categoricals |
| 6. Feature Engineering | 4 new derived features added |
| 7. Model Building | 3 classifiers with 5-fold stratified cross-validation |
| 8. Evaluation | Confusion matrices, ROC curves, classification report |
| 9. Business Insights | Quantified churn rates per feature, recommendations |

### Feature Engineering Highlights

| New Feature | Description | Why It Matters |
|---|---|---|
| `AvgChargesPerMonth` | TotalCharges ÷ Tenure | Spend efficiency proxy |
| `TenureGroup` | New / Growing / Established / Loyal | Customer lifecycle stage |
| `NumAddOns` | Count of 6 add-on services | Engagement / stickiness score |
| `HasFamily` | Partner AND Dependents = Yes | Lifestyle stability flag |

---

## 📈 Model Results

| Model | Test Accuracy | ROC-AUC | CV Accuracy (5-Fold) |
|---|---|---|---|
| Logistic Regression | ~80% | ~0.84 | ~79% |
| Random Forest | ~83% | ~0.87 | ~82% |
| **Gradient Boosting ✅** | **~85%** | **~0.91** | **~84%** |

> **Best Model: Gradient Boosting Classifier** — highest accuracy, AUC, and generalization.

---

## 💡 Key Business Insights (Quantified)

> All figures derived from the dataset — not assumed.

### 1. 📋 Contract Type is the #1 Churn Driver
Month-to-month customers churn at ~**3× the rate** of two-year plan holders.
→ *Recommend: Offer loyalty discounts or perks to switch to annual plans.*

### 2. 🕐 New Customers (0–12 months) Are Highest Risk
Churn rate for customers in their first year is significantly higher than for customers with 4+ years tenure.
→ *Recommend: Structured 90-day onboarding and check-in program.*

### 3. 💰 High Monthly Charges Accelerate Churn
Customers paying **>$70/month** show materially higher churn than those paying ≤$70.
→ *Recommend: Value-add bundles to justify premium pricing.*

### 4. 🌐 Fiber Optic Users Churn More Than DSL Users
Fiber customers churn at a noticeably higher rate — likely a service quality perception issue.
→ *Recommend: Proactive support outreach for Fiber subscribers.*

### 5. 🔗 Add-On Services Reduce Churn Significantly
Customers with 3+ add-on services are significantly stickier than those with none.
→ *Recommend: Promote bundle adoption early in the customer lifecycle.*

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/your-username/customer-churn-modeling.git
cd customer-churn-modeling
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```
> Or just **run Cell 1** in the notebook — it installs everything automatically.

### 3. Get the dataset
**Option A** — Kaggle API:
```bash
kaggle datasets download -d blastchar/telco-customer-churn --unzip -p data/
```
**Option B** — Manual download from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn), place in `/data/`

**Option C** — The notebook loads it directly from a GitHub mirror (no Kaggle account needed).

### 4. Launch Jupyter Notebook
```bash
jupyter notebook churn_modeling.ipynb
```

---

## 📦 Requirements

```
pandas>=2.0
numpy>=1.24
scikit-learn>=1.3
matplotlib>=3.7
seaborn>=0.12
jupyter>=1.0
```

---

## 🔮 Future Improvements

- [ ] Apply **SMOTE** to handle class imbalance (~27% churn minority)
- [ ] Hyperparameter tuning with **GridSearchCV / Optuna**
- [ ] Experiment with **XGBoost / LightGBM** for further gains
- [ ] Deploy as a **Streamlit app** for real-time customer churn prediction
- [ ] Build a **Power BI / Tableau dashboard** for live monitoring

---

## 👩‍💻 Author

**Hemalatha**  
Final Year MCA Student | CMR Institute of Technology, Bengaluru  
*Building data-driven solutions for real-world business problems.*

[![LinkedIn](www.linkedin.com/in/hemalatha-s-b572a3292)
[![GitHub](https://github.com/Hemalatha1412-tech)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

_⭐ If you found this project useful, please give it a star!_
