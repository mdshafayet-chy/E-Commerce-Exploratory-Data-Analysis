# 🛒 E-Commerce Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)


> Uncovering customer behaviour, data quality issues, and revenue drivers across a multi-table e-commerce dataset.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset Characteristics](#-dataset-characteristics)
- [Prerequisites & Installation](#-prerequisites--installation)
- [How to Run](#-how-to-run)
- [Data Cleaning & Integration](#-data-cleaning--integration)
- [Key Findings](#-key-findings)
- [Repository Files](#-repository-files)
- [License](#-license)

---

## 🧭 Project Overview

This repository presents a full **Exploratory Data Analysis (EDA)** of an e-commerce platform spanning three interconnected datasets — Customers, Sessions, and Orders.

The primary objectives are:

- 🔍 Detect and resolve data quality issues across all tables
- 👥 Understand customer acquisition, engagement, and conversion behaviour
- 💰 Identify the core drivers of revenue and uncover high-value customer segments

---

## 📦 Dataset Characteristics

| Dataset | Records | Description |
|---|---|---|
| 👤 **Customers** | 5,050 | Acquisition channels, device types, age groups, premium membership status |
| 🌐 **Sessions** | 30,150 | Session duration, pages viewed, funnel stages, UTM sources |
| 🧾 **Orders** | 12,100 | Product categories, unit prices, discount percentages, total revenue, order status |

> ✅ **Final merged dataset:** `11,878` complete records, ready for analysis.

---

## ⚙️ Prerequisites & Installation

Ensure you have **Python 3.8+** installed, then install the required libraries:

```bash
pip install pandas matplotlib seaborn jupyter
```

| Library | Purpose |
|---|---|
| `pandas` | Data manipulation, aggregation, and merging |
| `matplotlib` | Base plots and custom visualisations |
| `seaborn` | Statistical visualisation and theming |
| `jupyter` | Interactive notebook environment |

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/your-username/ecommerce-eda.git
cd ecommerce-eda

# 2. (Optional) Create and activate a virtual environment
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install pandas matplotlib seaborn jupyter

# 4. Launch the notebook
jupyter notebook eda.ipynb
```

---

## 🧹 Data Cleaning & Integration

Three-stage cleaning pipeline applied before merging:

- **Duplicates removed** across all three tables (Customer IDs, Session IDs, Order IDs)
- **Invalid entries dropped** — negative numerical values, invalid dates, and out-of-range fields
- **Missing values handled** — categorical nulls filled with `"unknown"`, numerical nulls imputed with **median values**
- **Tables merged** via a left join on `customer_id`, producing a clean, unified analytical dataset

```
Customers ──┐
             ├──► Left Join on customer_id ──► 11,878 records
Sessions  ──┘    (aggregated to customer level)
             +
Orders    ──►  Final Merged Dataset
```

---

## 💡 Key Findings

### 📊 Revenue Distribution
- Revenue is **severely right-skewed** — mean (£388) is more than double the median (£180)
- The **top 1% of customers** generate ≥ £2,941, representing a concentrated high-value segment
- Gini coefficient of **0.643** confirms a strong Pareto revenue distribution

### 🔗 Revenue Drivers

| Feature Pair | Correlation (r) | Interpretation |
|---|---|---|
| Unit Price → Revenue | **0.74** | Strong — price is the primary driver |
| Quantity → Revenue | 0.42 | Moderate — volume contributes but less |
| Session Duration → Revenue | 0.007 | Negligible — browsing time ≠ spending |
| Discount % → Revenue | −0.07 | Negligible — discounts don't drive value |

### 📅 Conversion Behaviour
- Conversion rates are **flat across all days of the week** (72.6% – 74.2% range)
- No weekend uplift observed — promotions should target **product category and customer history**, not timing
- Only **4.7% of all visitors** convert to a completed purchase

### 📱 Device & Channel Insights
- **Mobile leads** completed order volume (55%) but carries a higher return rate (17.8% vs 11.4% desktop)
- **Referral** is the dominant acquisition channel (49%) — paid ads account for only 7.5%

---

## 📂 Repository Files

```
ecommerce-eda/
│
├── 📁 data/                       ← Dataset files used in the analysis
│   ├── customers.csv                  (5,050 records)
│   ├── sessions.csv                   (30,150 records)
│   ├── orders.csv                     (12,100 records)
│
├── 📓 eda.ipynb                   ← Full Python EDA: cleaning, feature engineering,
│                                     visualisations, and hypothesis testing
│
├── 📄 E-Commerce-EDA-Report.pdf  ← Visual summary of methodology, distributions,
│                                     and final business verdicts
│
└── 📘 README.md                   ← Project documentation (you are here)
```


---

<p align="center">
  Made with 🐍 Python &nbsp;|&nbsp; 🐼 Pandas &nbsp;|&nbsp; 📊 Seaborn &nbsp;|&nbsp; 📓 Jupyter
</p>
