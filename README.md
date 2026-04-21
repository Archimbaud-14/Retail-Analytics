# 🏬 Multi-Dimensional Retail Analytics on Istanbul Shopping Data

> Advanced analytical deep-dive into Istanbul shopping mall data — examining customer demographics, spending patterns and yearly trends across multiple dimensions.

![Python](https://img.shields.io/badge/Python-3.13-3776AB?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.3-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.10-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-4C72B0)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Level](https://img.shields.io/badge/Level-Advanced-red)

---

## 📋 Table of Contents

- [About the Project](#-about-the-project)
- [Dataset Overview](#-dataset-overview)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Analysis Workflow](#-analysis-workflow)
- [Key Findings](#-key-findings)
- [Visualizations](#-visualizations)
- [Business Insights](#-business-insights)
- [Bonus Features](#-bonus-features)
- [Technologies Used](#-technologies-used)

---

## 📖 About the Project

This project performs a **multi-dimensional retail analysis** on a dataset of **99,457 shopping transactions** from **10 major Istanbul shopping malls** spanning 2021–2023. The analysis covers spending patterns by category, mall, payment method, and gender with pivot tables, yearly trend analysis, and demographic comparisons.

### Objectives
- Load data and validate quality (missing values, dtypes, duplicates)
- Convert `invoice_date` to datetime; extract year and month features
- Analyze spending by category, shopping mall, payment method and gender
- Build cross-tabulation pivot tables (mall × category → total revenue)
- Track yearly revenue trends (2021–2023) by category
- Compare male vs female spending across categories
- Generate 5 actionable business insights for AVM management

---

## 📊 Dataset Overview

| Property | Detail |
|----------|--------|
| **Source** | [Kaggle — Customer Shopping Dataset](https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset) |
| **File** | `customer_shopping_data.csv` |
| **Records** | 99,457 transactions |
| **Columns** | 10 features |
| **Date Range** | January 2021 – March 2023 |
| **Malls** | 10 Istanbul shopping centers |
| **Categories** | 8 product categories |
| **Missing Values** | None |

### Column Descriptions

| Column | Type | Description |
|--------|------|-------------|
| `invoice_no` | String | Unique transaction ID |
| `customer_id` | String | Unique customer ID |
| `gender` | Categorical | Male / Female |
| `age` | Integer | Customer age (18–69) |
| `category` | Categorical | Product category (8 types) |
| `quantity` | Integer | Items purchased (1–5) |
| `price` | Float | Total purchase amount ($) |
| `payment_method` | Categorical | Cash / Credit Card / Debit Card |
| `invoice_date` | Date | Transaction date |
| `shopping_mall` | Categorical | Mall name (10 malls) |

### Shopping Malls Covered
Kanyon · Mall of Istanbul · Metrocity · Metropol AVM · Istinye Park · Forum Istanbul · Viaport Outlet · Cevahir AVM · Emaar Square Mall · Zorlu Center

### Product Categories
Clothing · Shoes · Technology · Cosmetics · Food & Beverage · Toys · Books · Souvenir

---

## 📁 Project Structure

```
Retail Analytics on Istanbul Shopping Data/
│
├── 📓 Istanbul_Retail_Analytics.ipynb       # Main Jupyter notebook
├── 📝 note.md                               # Methodology & insights
├── 📄 README.md                             # Project documentation
├── 📊 customer_shopping_data.csv            # Raw dataset
│
├── 🖼️ chart1_heatmap_mall_category.png      # Heatmap: Mall × Category
├── 🖼️ chart2_yearly_trend_category.png      # Line: Yearly trend per category
├── 🖼️ chart3_gender_category_spending.png   # Grouped bar: Gender vs spending
├── 🖼️ chart4_revenue_by_mall.png            # Bar: Revenue by mall
├── 🖼️ chart5_payment_distribution.png       # Pie: Payment methods
├── 🖼️ chart6_mom_growth_top5.png            # ⭐ Line: MoM growth (bonus)
└── 🖼️ chart7_payment_per_category.png       # ⭐ Heatmap: Payment per category
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- Jupyter Notebook

### Installation

```bash
cd "Retail Analytics on Istanbul Shopping Data"

pip install pandas matplotlib seaborn jupyter

jupyter notebook Istanbul_Retail_Analytics.ipynb
```

---

## 🔄 Analysis Workflow

```
┌──────────────────┐    ┌──────────────────┐    ┌──────────────────┐
│  1. Data Load     │───▶│  2. Quality       │───▶│  3. Preprocess    │
│  & Inspection     │    │  Check            │    │  Dates & Features │
└──────────────────┘    └──────────────────┘    └──────────────────┘
                                                         │
        ┌────────────────────────────────────────────────┘
        ▼
┌──────────────────┐    ┌──────────────────┐    ┌──────────────────┐
│  4. Spending      │───▶│  5. Pivot Table   │───▶│  6. Yearly Trend  │
│  by Dimensions    │    │  Mall × Category  │    │  Analysis (YoY)   │
└──────────────────┘    └──────────────────┘    └──────────────────┘
                                                         │
        ┌────────────────────────────────────────────────┘
        ▼
┌──────────────────┐    ┌──────────────────┐    ┌──────────────────┐
│  7. Demographics  │───▶│  8. Visualize     │───▶│  9. Business      │
│  M vs F Spending  │    │  (7 Charts)       │    │  Insights (5)     │
└──────────────────┘    └──────────────────┘    └──────────────────┘
```

---

## 🔍 Key Findings

| Metric | Value |
|--------|-------|
| 💰 **Total Revenue** | ~$68.2M |
| 📦 **Total Transactions** | 99,457 |
| 🏆 **Top Category** | Clothing (~34% of orders) |
| 💎 **Highest Avg Purchase** | Technology (~$1,741) |
| 🏪 **Top Mall (Revenue)** | Mall of Istanbul / Kanyon |
| 💳 **Dominant Payment** | Cash (44.8%) |
| 👩 **Female Share** | 59.8% of all transactions |
| 📅 **Peak Year** | 2022 |

---

## 📈 Visualizations

### Chart 1 — Heatmap: Revenue by Mall × Category
> Cross-tabulation showing total revenue for each shopping mall and product category combination. Reveals which mall-category pairs are the strongest.

### Chart 2 — Yearly Revenue Trend per Category (2021–2023)
> Multi-line chart tracking revenue trajectory for all 8 categories over 3 years. Clothing consistently leads, Technology shows high value.

### Chart 3 — Gender vs Spending by Category
> Grouped horizontal bar chart comparing male vs female total spending in each category. Females lead across all categories.

### Chart 4 — Total Revenue by Shopping Mall
> Horizontal bar ranking all 10 malls by total revenue generated.

### Chart 5 — Payment Method Distribution
> Pie chart showing Cash (44.8%), Credit Card (35.1%), and Debit Card (20.1%) shares.

### Chart 6 — ⭐ MoM Revenue Growth (Top 5 Malls)
> Rolling 3-month average of month-over-month growth for the top 5 revenue-generating malls.

### Chart 7 — ⭐ Payment Method per Category Heatmap
> Shows transaction count for each payment-category combination, revealing category-specific payment preferences.

---

## 💡 5 Business Insights

### 1. 👗 Clothing Dominates — Cross-Sell Opportunity
Clothing leads with ~34% of all transactions. Place complementary categories (Shoes, Cosmetics) near clothing sections and create themed shopping bundles to drive cross-category purchases.

### 2. 💻 Technology = High-Value Transactions
Technology averages ~$1,741 per order. Allocate premium spaces to tech brands, offer installment plans, and host showcase events to attract high-value shoppers.

### 3. 👩 Female Customers Drive 60% of Revenue
With 59.8% transaction share, women are the core audience. Tailor marketing campaigns, expand women-focused lines, and create female-friendly experiences.

### 4. 💵 Cash is King — But Go Digital
Cash at 44.8% still leads. Incentivize card usage with cashback, loyalty points, and exclusive digital discounts to reduce cash-handling costs.

### 5. 📈 2022 Was the Peak — Learn & Replicate
2022 showed highest revenue across all categories. Analyze its success drivers and carry forward effective strategies into future planning.

---

## ⭐ Bonus Features

| Feature | Description |
|---------|-------------|
| **MoM Growth Rate** | Month-over-month revenue growth calculation per AVM with rolling average visualization |
| **Payment Dominance** | Identifies which payment method leads in each product category |

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| **Python 3.13** | Core language |
| **pandas** | Data manipulation, pivot tables, groupby |
| **matplotlib** | Chart creation |
| **seaborn** | Heatmaps & styling |
| **Jupyter Notebook** | Interactive analysis |

---

## ✅ Deliverables Checklist

- [x] Jupyter notebook with full multi-dimensional analysis and comments
- [x] `note.md` with methodology and 5 business insights
- [x] Pivot table heatmap (Mall × Category)
- [x] Yearly trend line chart per category
- [x] Grouped bar chart of gender vs spending by category
- [x] 5 actionable business insights
- [x] ⭐ Month-over-month revenue growth rate per AVM
- [x] ⭐ Dominant payment method per category

---

## 📜 License

This project is for educational purposes as part of an advanced data analysis learning track.

---

<p align="center">
  <i>Built with 🐍 Python | 📊 pandas | 🎨 matplotlib + seaborn</i>
</p>
