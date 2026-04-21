# 📝 Note: Multi-Dimensional Retail Analytics on Istanbul Shopping Data

## Methodology

### 1. Data Loading & Quality Assessment
- Loaded `customer_shopping_data.csv` containing **99,457 transactions** across 10 columns
- **No missing values** detected in any column
- **No duplicate rows** found
- 10 shopping malls covered across Istanbul

### 2. Data Preprocessing
- **invoice_date**: Converted from string (`dd/mm/yyyy`) to `datetime64` format
- Extracted **year** (2021, 2022, 2023) and **month** features for temporal analysis
- Created `year_month` period for month-over-month growth calculations

### 3. Multi-Dimensional Spending Analysis
Aggregated total revenue, order counts, and average purchase amounts by:
- **Category** — 8 product categories (Clothing, Shoes, Technology, Cosmetics, Food & Beverage, Toys, Books, Souvenir)
- **Shopping Mall** — 10 Istanbul malls
- **Payment Method** — Cash, Credit Card, Debit Card
- **Gender** — Male vs Female

### 4. Pivot Table Analysis
- Built cross-tabulation of **shopping_mall × category → total revenue**
- Identified which mall-category combinations drive the most revenue
- Added row totals for overall mall performance comparison

### 5. Yearly Trend Analysis
- Compared 2021–2023 revenue by category
- Calculated year-over-year growth rates for each category
- 2023 data is partial (Jan–Mar), so comparisons account for this

### 6. Demographic Analysis
- Compared male vs female spending patterns across all categories
- Calculated gender revenue share percentages per category
- Identified categories with the highest gender imbalance

### 7. Visualizations Created

| # | Chart Type | Description | File |
|---|-----------|-------------|------|
| 1 | Heatmap | Revenue by Mall × Category (Pivot Table) | `chart1_heatmap_mall_category.png` |
| 2 | Line Chart | Yearly Revenue Trend per Category (2021–2023) | `chart2_yearly_trend_category.png` |
| 3 | Grouped Bar | Gender vs Spending by Category | `chart3_gender_category_spending.png` |
| 4 | Horizontal Bar | Total Revenue by Shopping Mall | `chart4_revenue_by_mall.png` |
| 5 | Pie Chart | Payment Method Distribution | `chart5_payment_distribution.png` |
| 6 | Line Chart ⭐ | MoM Revenue Growth (Rolling Avg) — Top 5 Malls | `chart6_mom_growth_top5.png` |
| 7 | Heatmap ⭐ | Payment Method Usage by Category | `chart7_payment_per_category.png` |

### 8. Bonus Features
- **Month-over-Month Growth Rate**: Calculated for each mall with 3-month rolling average visualization
- **Dominant Payment Method per Category**: Identified which payment method leads in each product category

---

## Key Findings

### 🛍️ Category Performance
- **Clothing** is the undisputed leader with ~34% of all transactions and highest total revenue
- **Technology** has the highest average purchase (~$1,741), making it the most valuable per-transaction category
- **Food & Beverage** has the lowest average purchase (~$57) but high transaction volume
- Category revenue spread is extremely wide — Technology at ~$1,741 vs Food & Beverage at ~$57 per order

### 🏬 Shopping Mall Performance
- **Mall of Istanbul** and **Kanyon** consistently rank as top revenue generators
- **Kanyon** has the highest average purchase amount among all malls
- All 10 malls show similar category distribution patterns, with Clothing dominating everywhere

### 💳 Payment Preferences
- **Cash** is the most used payment method at 44.8% of transactions
- **Credit Card** follows at 35.1%
- **Debit Card** at 20.1%
- Cash dominates across all categories, but Technology shows higher card usage

### 👥 Demographics
- **Female** customers drive 59.8% of all transactions
- **Male** customers account for 40.2%
- Gender spending patterns are consistent across categories — females lead in all product lines
- No single category shows a male-dominant spending pattern

### 📅 Temporal Trends
- **2022** was the peak revenue year across all categories
- **2023** data is partial (Jan–Mar), making direct comparison incomplete
- Year-over-year growth from 2021→2022 is consistently positive across all categories

---

## 💡 5 Business Insights

### 1. Clothing Dominates Revenue — Leverage for Cross-Selling
Clothing accounts for ~34% of transactions and leads revenue in all malls. Management should strategically place complementary categories (Shoes, Cosmetics) near clothing sections and create themed shopping bundles to drive cross-category purchases.

### 2. Technology Drives Highest Per-Transaction Value
Despite fewer orders, Technology commands ~$1,741 per transaction. Malls should allocate premium retail spaces to tech brands, offer financing/installment options, and host showcase events to attract high-value shoppers.

### 3. Female Customers Are the Core Revenue Driver
With ~59.8% of transactions, female shoppers are the backbone of mall revenue. Marketing campaigns should be tailored toward female demographics, with expanded women-focused product lines and experiences (lounges, loyalty programs, themed events).

### 4. Cash Still Dominates — Accelerate Digital Adoption
At 44.8%, cash remains the top payment method. Malls should incentivize digital payments through cashback offers and exclusive card-user discounts while maintaining cash infrastructure. This could reduce operational costs and increase average transaction values.

### 5. 2022 Was the Peak — Replicate Success Drivers
2022 saw the highest revenue across all categories. Management should analyze what drove this success (seasonal campaigns, economic conditions, new brands) and replicate those strategies with proactive 2023 planning: flash sales, loyalty extensions, and new store openings.

---

## Technical Stack
- **Python 3.13**: pandas, matplotlib, seaborn
- **Environment**: Jupyter Notebook
- **Dataset**: `customer_shopping_data.csv` (99,457 rows × 10 columns)
- **Source**: [Kaggle — Customer Shopping Dataset](https://www.kaggle.com/datasets/mehmettahiraslan/customer-shopping-dataset)

---

*Analysis completed on April 2026*
