# 🛒 E-Commerce Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

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
