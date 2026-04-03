# Deep Sales Analysis of Olist Marketplace
[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python)](https://github.com/Sanchal-Benny/Olist-Sales-Analysis)
[![Jupyter Notebook](https://img.shields.io/badge/-Notebook-F37626?logo=jupyter&logoColor=white)](https://github.com/Sanchal-Benny/Olist-Sales-Analysis/blob/main/Olist_Analysis.ipynb)
[![Open In Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

Comprehensive analysis of Brazilian e-commerce data from the Olist marketplace, uncovering key insights and actionable business recommendations.

---

## Contents

- [ Tech Stack \& Methods](#tech-stack-methods)
- [ Project Overview](#project-overview)
- [ Data Source](#data-source)
- [ Main Conclusions](#main-conclusions)
- [ Key Recommendations](#key-recommendations)
- [ How to Run This Project](#how-to-run-this-project)

---

<a id="tech-stack-methods"></a>

## Tech Stack & Methods

**Stack:**

- **Data Analysis:** `Python` `Pandas` `NumPy`
- **Visualization:** `Matplotlib` `Seaborn` `Plotly`
- **Segmentation:** `RFM Analysis` `NPS Calculation`

**Methods:**

- **Exploratory Data Analysis (EDA):**
  - Statistical summaries, missing value analysis, and feature engineering
- **Data Preprocessing:**
  - Merging 9 datasets, datetime parsing, string normalization
- **Sales Analysis:**
  - Monthly revenue trends, Black Friday deep dive, category performance
- **Customer Analysis:**
  - Retention analysis, RFM segmentation, payment behavior
- **Delivery Analysis:**
  - Stage-by-stage delivery breakdown, delay impact on ratings
- **NPS Analysis:**
  - Promoter/Detractor classification and NPS score calculation

[⬆ back to top](#contents)

---

<a id="project-overview"></a>

## Project Overview

Olist is a Brazilian e-commerce platform that connects sellers and buyers, offering a wide range of products and convenient conditions for online sales. Olist also acts as an intermediary, allowing sellers to connect to multiple marketplaces simultaneously, thereby increasing their reach.

This analysis aims to:

- **Evaluate sales performance**
  - Identify seasonal patterns and revenue trends
  - Analyze Black Friday impact and category performance

- **Understand customer behavior**
  - Examine purchasing frequency and retention drivers
  - Segment buyers using RFM analysis

- **Assess delivery performance**
  - Map delivery stage breakdowns and bottlenecks
  - Correlate delivery speed with customer ratings

- **Analyze payment systems**
  - Compare payment method usage and order values
  - Identify risk factors for cancellations

- **Generate actionable insights**
  - Develop data-backed recommendations for business growth
  - Propose customer experience improvements

[⬆ back to top](#contents)

---

<a id="data-source"></a>

## Data Source

The analysis uses the **Olist Brazilian E-Commerce Dataset** ([Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce))

9 CSV files used:
- `olist_orders_dataset.csv`
- `olist_customers_dataset.csv`
- `olist_order_items_dataset.csv`
- `olist_products_dataset.csv`
- `olist_sellers_dataset.csv`
- `olist_order_payments_dataset.csv`
- `olist_order_reviews_dataset.csv`
- `olist_geolocation_dataset.csv`
- `product_category_name_translation.csv`

[⬆ back to top](#contents)

---

<a id="main-conclusions"></a>

## Main Conclusions

### Sales Trends:
  - **Growth & Stabilization**: Sales grew until 2018, then stabilized at 6 - 7K orders and 1-1.2M R$ per month.
  - **Black Friday (11/24/2017)**: 1,147 orders in a single day — 4.7x the daily average of 243.
  - **Geography**: São Paulo dominates (42% of sales), with steady growth in 2018, unlike other regions.

### Customer Behavior:
  - **Low Retention**: 97% of buyers made only one purchase; repeat buyers are rare.
  - **High-Value Buyers**: Customers using 6+ installments spend 2.1x more (R$303 vs R$143).
  - **NPS Score**: 38.1 (Good ) , That is 59.2% Promoters, 21.1% Detractors.

### Delivery Insights:
  - Delayed orders correlate with lower ratings (avg. 19.1 days for 1-star vs. 10.2 days for 5-star).
  - **74% of total delivery time** is spent with carriers - the biggest operational bottleneck.
  - Heavy and expensive orders take longer to deliver and are more likely to be delayed.

### Payment & Risk:
  - **Credit cards dominate**: 76% of transactions.
  - **Installments boost value**: Orders with 6+ installments have 2.1x higher AOV.
  - **Voucher Payments**: Higher cancellation risk than other payment methods.

### Product & Logistics:
  - **Top Categories**: bed_bath_table (R$1.72M), health_beauty (R$1.63M), computers_accessories (R$1.56M).
  - Heavy orders face longer delivery times and lower ratings.
  - **Delivery Bottleneck**: 74% of total delivery time is with carriers.

### Customer Segments (RFM):
  - **Champions**: 23,491 customers (25.2%) - avg spend R$228.
  - **Potential Loyalists**: 17,437 customers (18.7%).
  - **At Risk**: 11,511 customers - last purchase 451 days ago.
  - **Lost**: 5,900 customers (6.3%) - need win-back campaigns.

[⬆ back to top](#contents)

---

<a id="key-recommendations"></a>

## Key Recommendations

### Boost Customer Retention & Repeat Purchases:
  - Launch a loyalty program targeting one-time buyers (97% of customers), offering discounts on second purchases or bonus points.
  - Personalized win-back campaigns for At Risk and Lost RFM segments.
  - Reduce time between purchases via time-bound promotions.

### Fix Delivery Bottleneck:
  - Carrier delivery consumes 74% of total delivery time (9.2 out of 12.4 days).
  - Prioritize carrier performance in critical cities: Salvador, Porto Alegre, Rio de Janeiro.
  - Expedite heavy and expensive orders — they face 2x more 1-star ratings due to delays.

### Leverage Installment Payments:
  - Promote installment plans : customers with 6+ installments spend 2.1x more.
  - Offer 0% interest installment campaigns to boost adoption.

### Optimize Black Friday Logistics:
  - Scale warehouse capacity before November.
  - Pre-stock top categories: Bed Bath Table and Furniture.
  - Add temporary carrier capacity to avoid repeat of 2017's delivery surge.

### Reduce Voucher Cancellations:
  - Voucher users have higher cancellation rates than other payment types.
  - Convert voucher users to credit card payments through incentives.

### Regional Growth:
  - Hyper-local campaigns in São Paulo (42% of sales): fastest delivery and highest volume.
  - Fix underperformers: Maranhão and Ceará have longest delivery times among top states.

[⬆ back to top](#contents)

---

<a id="how-to-run-this-project"></a>

## How to Run This Project

### Prerequisites

- Python 3.8+ installed
- Jupyter Notebook

### Download the Dataset

Download the dataset from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) and place all CSV files in a `data/` folder.

### Install Requirements

```bash
pip install pandas numpy matplotlib seaborn plotly
```

### Run the Notebook

```bash
jupyter notebook Olist_Analysis.ipynb
```

[⬆ back to top](#contents)

---
