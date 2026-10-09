# 📉 AI-Powered Customer Churn & Retention Command Center

End-to-end customer churn analytics project: analyze customer behavior, predict churn probability with machine learning, identify churn drivers, and monitor retention risk through an interactive Power BI dashboard.

![Dashboard Overview](screenshots/___dashboard_overview.png)

**Key results**
- Overall churn rate: **26.54%** across **7,043 customers**
- Best overall model: **Logistic Regression**, with **80.7% accuracy**, **0.609 F1-score** and **0.842 ROC-AUC** on the test set
- **488 customers (6.9%)** were classified as **High Risk**, with an average churn probability of **75.1%**

---

## 📌 Project Overview

Customer churn directly affects revenue, and keeping an existing customer is usually cheaper than acquiring a new one. This project helps a telecom company find customers who are likely to leave so the retention team can act early.

Using Python, machine learning and Power BI, the project:

- Cleans and prepares customer data
- Explores factors linked to churn
- Trains and compares three classification models
- Identifies the main churn drivers
- Predicts a churn probability for every customer
- Groups customers into Low, Medium and High risk
- Suggests a retention action for each risk level
- Presents everything in an interactive Power BI dashboard

---

## 🎯 Business Questions

- What percentage of customers have churned?
- Which contract types, services and payment methods show higher churn?
- Which customer groups are most at risk?
- Which model predicts churn best?
- Which customers should the retention team contact first?

---

## 📊 Dataset

- **Name:** Telco Customer Churn dataset
- **Source:** ___ (for example, Kaggle)
- **Size:** 7,043 customers
- **Churn rate:** 26.54%

| Category | Columns |
|----------|---------|
| Demographics | Gender, senior citizen, partner, dependents |
| Account | Tenure, contract type, payment method, paperless billing |
| Services | Phone service, internet service, online security, tech support, streaming |
| Charges | Monthly charges, total charges |
| Target | Churn (Yes / No) |

---

## 🔄 Project Workflow

```
Raw Customer Data
       ↓
Data Cleaning
       ↓
Exploratory Data Analysis
       ↓
Feature Preparation (encoding categorical variables, scaling)
       ↓
Train / Test Split (80% / 20%)
       ↓
Model Training (Logistic Regression, Decision Tree, Random Forest)
       ↓
Model Evaluation & Comparison
       ↓
Churn Driver Analysis
       ↓
Churn Probability & Risk Classification
       ↓
Retention Actions
       ↓
Power BI Command Center
```

---

## 🧹 Data Cleaning & Preparation

- Checked data types, missing values and duplicates
- Converted `TotalCharges` to a numeric column and handled blank values
- Encoded categorical variables into 30 model features
- Scaled features for Logistic Regression
- Split the data into **5,634 training** and **1,409 test** customers (80% / 20%)

---

## 🔍 Exploratory Data Analysis: Key Findings

**Churn by contract type**

| Contract | Churn Rate |
|----------|-----------|
| Month-to-month | 42.7% |
| One year | 11.3% |
| Two year | 2.8% |

**Churn by payment method**

| Payment Method | Churn Rate |
|----------------|-----------|
| Electronic check | 45.3% |
| Mailed check | 19.1% |
| Bank transfer (automatic) | 16.7% |
| Credit card (automatic) | 15.2% |

**Churn by internet service**

| Internet Service | Churn Rate |
|------------------|-----------|
| Fiber optic | 41.9% |
| DSL | 19.0% |
| No internet | 7.4% |

**Churn by tenure**

| Tenure | Churn Rate |
|--------|-----------|
| 0 - 12 months | 47.4% |
| 13 - 24 months | 28.7% |
| 25 - 48 months | 20.4% |
| 49+ months | 9.5% |

---

## 🤖 Model Results

Three classification models were trained and compared on a held-out test set of 1,409 customers.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.807 | 0.658 | 0.567 | 0.609 | 0.842 |
| Decision Tree | 0.794 | 0.631 | 0.540 | 0.582 | 0.827 |
| Random Forest | 0.803 | 0.673 | 0.500 | 0.574 | 0.845 |

**Selected model:** Logistic Regression. It had the highest accuracy, recall and F1-score, so it identifies more of the customers who actually churn, and its coefficients are easy to explain to a business team. Random Forest had the highest ROC-AUC (0.845) and precision, but missed more churners (recall 0.500).

---

## 🔑 Key Churn Drivers

**Factors that increase churn risk** (Logistic Regression coefficients)

1. Fiber optic internet service
2. Higher total charges
3. Streaming movies and streaming TV
4. Multiple phone lines

**Factors that reduce churn risk**

1. Longer tenure
2. Two-year and one-year contracts
3. Online security

**Most important features** (Random Forest): tenure, total charges, monthly charges, fiber optic internet, two-year contract and electronic check payment.

> Note: monthly charges and total charges are strongly related to tenure, so their individual coefficients should be interpreted with caution.

---

## 🚦 Customer Risk Levels & Retention Actions

Each customer receives a churn probability and is placed in a risk level.

| Risk Level | Customers | Share | Suggested Retention Action |
|------------|-----------|-------|----------------------------|
| Low Risk | 4,947 | 70.2% | ___ |
| Medium Risk | 1,608 | 22.8% | ___ |
| High Risk | 488 | 6.9% | ___ |

**High-risk customer profile:** average churn probability 75.1%, average tenure 6.3 months, average monthly charges 85.39.

---

## 📈 Power BI Command Center

The dashboard lets the retention team monitor churn and act on high-risk customers.

It includes:

- Churn rate and customer KPIs
- Churn by contract type, services and payment method
- Customer profile analysis
- Churn probability and risk-level distribution
- Churn drivers and retention insights
- Filters to explore specific customer groups

![Dashboard Page 2](screenshots/___page_2.png)

![Dashboard Page 3](screenshots/___page_3.png)

---

## 💡 Business Recommendations

1. **Move month-to-month customers to longer contracts.** Month-to-month customers churn at 42.7%, compared with 2.8% for two-year customers.
2. **Support new customers in their first year.** Customers in their first 12 months churn at 47.4%.
3. **Review the electronic check experience.** Customers paying by electronic check churn at 45.3%, so offering automatic payment discounts may help.
4. **Check fiber optic service quality and pricing.** Fiber optic customers churn at 41.9% compared with 19.0% for DSL.
5. **Contact High Risk customers first.** The 488 high-risk customers have an average churn probability of 75.1%.

---

## 🛠️ Tools & Technologies

| Area | Tools |
|------|-------|
| Programming | Python, Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Power BI |
| Machine Learning | Scikit-learn (Logistic Regression, Decision Tree, Random Forest) |
| Environment | Jupyter Notebook, Anaconda, VS Code |
| Version Control | Git, GitHub |

---

## 📁 Project Structure

```
AI-Powered-Customer-Churn-Retention
│
├── data
│   └── ___.csv
│
├── python
│   └── ___.ipynb
│
├── powerbi
│   └── ___.pbix
│
├── screenshots
│
├── .gitignore
└── README.md
```

---

## ▶️ How to Run

1. Clone the repository
   ```
   git clone https://github.com/SV-181002/AI-Powered-Customer-Churn-Retention.git
   ```
2. Install the required libraries
   ```
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```
3. Open the notebook in the `python` folder and run all cells
4. Open the `.pbix` file in Power BI Desktop to explore the dashboard

---

## ⚠️ Limitations & Future Improvements

- The dataset is a single snapshot, so trends over time cannot be analyzed
- Recall is around 0.5-0.57, so some customers who will churn are still missed; threshold tuning could improve this
- Add hyperparameter tuning and cross-validation
- Handle class imbalance (for example, SMOTE or class weights)
- Deploy the model as a simple web app

---

## 👨‍💻 Author

**Durgampudi S V Krishna Reddy**
MCA — Data Analyst

📧 reddydsvkrishna@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/sv181002) | [GitHub](https://github.com/SV-181002)
