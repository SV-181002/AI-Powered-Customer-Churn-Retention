# 📉 AI-Powered Customer Churn & Retention Command Center

End-to-end customer churn analytics project: analyze customer behavior, predict churn probability with machine learning, identify churn drivers, and monitor retention risk through an interactive Power BI dashboard.

![Dashboard Overview](screenshots/___dashboard_overview.png)

**Key result:** Overall churn rate of **26.54%** across **7,043 customers**. The best model (**___**) reached **___% accuracy** and **___% recall**.

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
Feature Preparation (encoding categorical variables)
       ↓
Train / Test Split
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
- Fixed the `TotalCharges` column (___ blank values handled by ___)
- Encoded categorical variables for machine learning
- Split the data into training and test sets (___% / ___%)

---

## 🔍 Exploratory Data Analysis (Key Findings)

- Overall churn rate is **26.54%**
- Customers on **___** contracts churn the most (___%)
- Customers with **shorter tenure** are more likely to churn (___)
- **___** payment method shows the highest churn (___%)
- **___** (add one more finding from your analysis)

---

## 🤖 Model Results

Three classification models were trained and compared on a held-out test set.

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Logistic Regression | ___ | ___ | ___ | ___ |
| Decision Tree | ___ | ___ | ___ | ___ |
| Random Forest | ___ | ___ | ___ | ___ |

**Selected model:** ___, because ___ (for example, it had the best recall, so it catches more customers who will actually churn).

---

## 🔑 Key Churn Drivers

The factors most associated with churn were:

1. ___
2. ___
3. ___
4. ___

---

## 🚦 Customer Risk Levels & Retention Actions

Each customer receives a churn probability and a risk level.

| Risk Level | Customers | Suggested Retention Action |
|------------|-----------|----------------------------|
| Low | ___ | ___ |
| Medium | ___ | ___ |
| High | ___ | ___ |

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

1. ___ (for example, encourage month-to-month customers to move to longer contracts with a discount)
2. ___ (for example, give early-tenure customers onboarding support)
3. ___ (for example, contact all High-risk customers with a targeted offer)

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
- Add hyperparameter tuning and cross-validation
- Handle class imbalance (for example, SMOTE or class weights)
- Deploy the model as a simple web app

---

## 👨‍💻 Author

**Durgampudi S V Krishna Reddy**
MCA — Data Analyst

📧 reddydsvkrishna@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/sv181002) | [GitHub](https://github.com/SV-181002)
