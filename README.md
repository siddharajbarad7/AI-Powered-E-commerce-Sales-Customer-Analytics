
# 🛒 AI-Powered E-Commerce Analytics Dashboard

<div align="center">

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

**An end-to-end data analytics project combining SQL, Python, Machine Learning, and Power BI to simulate real-world business intelligence and decision-making.**

[📊 View Dashboard](#dashboard-preview) · [🤖 AI Model](#ai-churn-model) · [🚀 Quick Start](#quick-start) · [📁 Project Structure](#project-structure)

</div>

---

## 📌 Project Overview

This project analyses **805,549 e-commerce transactions** from a UK-based online retail store (2010–2011). It covers the full data analytics pipeline — from raw data cleaning to AI-powered churn prediction — and delivers insights through an interactive **6-page Power BI dashboard**.

> 💡 This project simulates how a real Data Analyst or Business Intelligence Engineer would approach e-commerce analytics in a professional environment.

---

## 🎯 Business Questions Answered

| # | Business Question | Tool Used |
|---|---|---|
| 1 | Which customers are at risk of churning? | Python · Random Forest |
| 2 | What are the monthly revenue trends? | SQL · Power BI |
| 3 | Which products drive the most revenue? | SQL · Power BI |
| 4 | Who are our highest-value customers? | SQL · Python |
| 5 | Which countries generate the most sales? | SQL · Power BI |
| 6 | Is our average order value growing? | DAX · Power BI |

---

## 📊 Key Findings

| Metric | Value |
|---|---|
| 💰 Total Revenue | £17,743,429 |
| 🛒 Total Orders | 36,969 |
| 👥 Total Customers | 5,878 |
| 📦 Total Products | 4,631 |
| 🌍 Countries | 41 |
| ⚠️ Churn Rate | 50.9% |
| 🚨 High Risk Customers | 2,989 |
| 🤖 Model Accuracy | 87% |
| 📡 ROC-AUC Score | 0.931 |

### 🔑 Top Insights

- **Thursday** is the highest revenue day (£3.84M) — confirms B2B wholesale purchasing behaviour
- **November** is peak month — B2B buyers stocking up for Christmas retail season
- **Netherlands** has the highest AOV at £2,541 — 3× the UK average
- **Top signal for churn** = `days_inactive` (48% of model prediction weight)
- **EIRE** is the top international market at £621,631
- **50.9% of customers** have gone inactive — the most urgent business priority

---

## 🤖 AI Churn Model

A **Random Forest Classifier** was trained to predict customer churn risk.

### Model Performance

| Metric | Score |
|---|---|
| Accuracy | 87% |
| Precision (Churned) | 85% |
| Recall (Churned) | 80% |
| F1 Score | 0.82 |
| ROC-AUC | **0.931** |

### Feature Importance

| Rank | Feature | Importance |
|---|---|---|
| 1 | Days Inactive | 48.2% |
| 2 | Order Count | 21.3% |
| 3 | Tenure Days | 12.0% |
| 4 | Total Spend | 10.1% |
| 5 | Total Items | 5.1% |
| 6 | Avg Order Value | 3.2% |

> **Business insight:** The single most actionable finding — re-engage customers **before** they hit 90 days of inactivity. That one signal drives nearly half of all churn predictions.

### Risk Band Output

| Risk Band | Customers | % |
|---|---|---|
| 🔴 High Risk | 2,989 | 50.9% |
| 🟡 Medium Risk | 837 | 14.2% |
| 🟢 Low Risk | 2,052 | 34.9% |

---

## 📋 Dashboard Pages

The Power BI dashboard (`eCommerce_sales_dashboards.pbix`) contains **6 interactive report pages**:

| Page | Description | Key Visuals |
|---|---|---|
| 1️⃣ Executive Summary | High-level KPIs at a glance | 4 KPI Cards, Revenue Trend, Churn Donut |
| 2️⃣ Revenue Trends | Monthly performance & patterns | Bar Chart, Day-of-Week, MoM Growth |
| 3️⃣ Product Performance | Top products by revenue | Horizontal Bar, Top N Filter |
| 4️⃣ Customer Segments | Purchase frequency & LTV | Customer Table, Risk Bands |
| 5️⃣ Churn Risk AI | AI model results visualised | Risk Donut, Probability Table |
| 6️⃣ Geographic Analysis | Revenue by country | Filled Map, Country Bar Chart |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Data Storage** | SQLite (via SQLAlchemy) |
| **Data Analysis** | Python · Pandas · NumPy |
| **Visualisation (EDA)** | Matplotlib · Seaborn |
| **Machine Learning** | Scikit-learn (Random Forest) |
| **Database Queries** | SQL (SQLite syntax) |
| **Business Dashboard** | Microsoft Power BI Desktop |
| **DAX Measures** | 15 custom DAX measures |

---

## 📁 Project Structure

```
ecommerce-analytics/
│
├── data/
│   ├── raw/
│   │   └── online_retail.xlsx          # Original UCI dataset
│   └── clean/
│       ├── customers.csv
│       ├── products.csv
│       ├── orders.csv
│       ├── order_items.csv
│       ├── cleaned_data.csv            # Full cleaned dataset
│       ├── revenue_by_month.csv
│       ├── product_performance.csv
│       ├── customer_features.csv       # ML input features
│       └── churn_predictions.csv       # AI model output
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb          # Data loading & cleaning
│   ├── 02_sql_analysis.ipynb           # SQL queries via Python
│   ├── 03_eda_visualisation.ipynb      # Exploratory Data Analysis
│   └── 04_churn_model.ipynb            # ML model training & evaluation
│
├── sql/
│   ├── schema.sql                      # Database table definitions
│   ├── revenue_queries.sql             # Revenue analysis queries
│   ├── product_queries.sql             # Product performance queries
│   └── churn_queries.sql               # Churn signal queries
│
├── powerbi/
│   └── eCommerce_sales_dashboards.pbix # Power BI dashboard file
│
├── requirements.txt
└── README.md
```

---

## 🚀 Quick Start

### Prerequisites

- Python 3.10+
- Power BI Desktop (free download)
- Jupyter Notebook or VS Code

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/ecommerce-analytics.git
cd ecommerce-analytics
```

### 2. Install Python dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

Download the **UCI Online Retail dataset** from Kaggle:
- Search: `UCI Online Retail Dataset` on [kaggle.com](https://www.kaggle.com)
- Save as: `data/raw/online_retail.xlsx`

### 4. Run the notebooks in order

```bash
jupyter notebook

# Run in this order:
# 1. notebooks/01_data_cleaning.ipynb
# 2. notebooks/02_sql_analysis.ipynb
# 3. notebooks/03_eda_visualisation.ipynb
# 4. notebooks/04_churn_model.ipynb
```

### 5. Open the Power BI dashboard

```
Open Power BI Desktop
→ File → Open → powerbi/eCommerce_sales_dashboards.pbix
→ Home → Refresh (to reload from your local CSV files)
```

---

## 📦 Requirements

```
pandas>=1.5.0
numpy>=1.23.0
scikit-learn>=1.1.0
matplotlib>=3.6.0
seaborn>=0.12.0
sqlalchemy>=1.4.0
openpyxl>=3.0.0
jupyter>=1.0.0
```

Save as `requirements.txt` or install directly:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn sqlalchemy openpyxl jupyter
```

---

## 📈 SQL Queries Included

| Query | File | Purpose |
|---|---|---|
| Monthly revenue trend | `revenue_queries.sql` | Power BI line chart |
| Revenue by day of week | `revenue_queries.sql` | Peak trading day analysis |
| Top 10 products | `product_queries.sql` | Product performance page |
| Revenue by country | `product_queries.sql` | Geographic analysis |
| Customer purchase frequency | `churn_queries.sql` | Customer segmentation |
| Days inactive per customer | `churn_queries.sql` | Churn signal |
| Full customer feature table | `churn_queries.sql` | ML model input |
| Churn rate summary | `churn_queries.sql` | Executive KPI |

---

## 🧠 Machine Learning Pipeline

```
Raw Data
   ↓
SQL: Extract customer features
   ↓
Python: Feature engineering + log transforms
   ↓
Train/Test Split (80/20, stratified)
   ↓
StandardScaler normalisation
   ↓
Random Forest (100 trees, balanced class weights)
   ↓
Evaluation: Accuracy 87%, ROC-AUC 0.931
   ↓
Score all 5,878 customers with churn probability
   ↓
Export: churn_predictions.csv → Power BI
```

---

## 📸 Dashboard Preview

> *Screenshots of the 6 Power BI dashboard pages*

| Page | Preview |
|---|---|
| Executive Summary | *(Add screenshot)* |
| Revenue Trends | *(Add screenshot)* |
| Product Performance | *(Add screenshot)* |
| Customer Segments | *(Add screenshot)* |
| Churn Risk AI | *(Add screenshot)* |
| Geographic Analysis | *(Add screenshot)* |

> 💡 **Tip:** Take screenshots of each page in Power BI (View → Fit to page → Snipping Tool) and save as `screenshots/page1.png` etc. Then replace *(Add screenshot)* with `![Page 1](screenshots/page1.png)`

---

## 👤 Author

**Your Name**
- LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- GitHub: [github.com/yourusername](https://github.com/yourusername)
- Email: your.email@example.com

---

## 📄 Dataset Source

- **Dataset:** UCI Online Retail Dataset
- **Source:** [Kaggle — UCI Machine Learning Repository](https://www.kaggle.com/datasets/vijayuv/onlineretail)
- **Period:** December 2010 – December 2011
- **Records:** 541,909 raw transactions → 805,549 after processing

---

## 🏷️ Tags

`data-analytics` `power-bi` `python` `machine-learning` `sql` `churn-prediction` `random-forest` `e-commerce` `business-intelligence` `data-science` `pandas` `scikit-learn` `sqlite` `dax`
