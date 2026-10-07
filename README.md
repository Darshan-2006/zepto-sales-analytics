# Zepto Sales Analytics

**Business Intelligence Report on Zepto Quick-Commerce Sales**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Period](https://img.shields.io/badge/Period-Jan%20–%20Mar%202025-blue)]()
[![Orders](https://img.shields.io/badge/Orders-1%2C500-success)]()
[![Revenue](https://img.shields.io/badge/Revenue-₹5.64L-orange)]()

---

## Overview

This repository presents a complete analysis of Zepto sales transactions. The goal is to identify **top revenue drivers**, understand **category and customer performance**, evaluate **delivery operations**, and surface **actionable business insights**.

| Metric                    | Value          |
|---------------------------|----------------|
| Total Sales               | ₹5,63,992      |
| Total Orders              | 1,500          |
| Unique Customers          | 300            |
| Unique Products / SKUs    | 200            |
| Units Sold                | 4,207          |
| Average Order Value       | ₹376           |
| Average Delivery Time     | 24.7 min       |
| Successful Delivery Rate  | 83.7%          |

**Data Period:** 1 January 2025 – 1 March 2025  
**Source File:** [`data/zepto_sales_raw.xlsx`](data/zepto_sales_raw.xlsx)

---

## Repository Structure

```
zepto-sales-analytics/
├── data/
│   └── zepto_sales_raw.xlsx   # Raw transactional dataset
├── README.md                  # This report
├── LICENSE
└── .gitignore
```

---

## Key Findings

### 1. Top Revenue Drivers

**Top 10 SKUs by Sales**

| Rank | SKU     | Product      | Category    | Sales (₹) | Orders |
|------|---------|--------------|-------------|-----------|--------|
| 1    | SKU30   | Product_30   | Veg         | 5,188     | 8      |
| 2    | SKU139  | Product_139  | Fruits      | 5,112     | 7      |
| 3    | SKU12   | Product_12   | Frozen      | 4,754     | 8      |
| 4    | SKU160  | Product_160  | Essentials  | 4,727     | 7      |
| 5    | SKU84   | Product_84   | Other       | 4,399     | 8      |
| 6    | SKU102  | Product_102  | Veg         | 4,361     | 7      |
| 7    | SKU13   | Product_13   | Baby        | 4,339     | 8      |
| 8    | SKU198  | Product_198  | Frozen      | 4,338     | 7      |
| 9    | SKU85   | Product_85   | Beverages   | 4,296     | 8      |
| 10   | SKU18   | Product_18   | Essentials  | 4,194     | 8      |

> The top 10 SKUs contribute ~8% of total revenue while representing only 5% of the catalogue — a clear concentration of value in a small set of hero products.

### 2. Category Performance

| Category   | Sales (₹) | Share  | AOV (₹) |
|------------|-----------|--------|---------|
| Beverages  | 82,603    | 14.7%  | 391     |
| Frozen     | 76,044    | 13.5%  | 371     |
| Veg        | 73,582    | 13.1%  | 402     |
| Snacks     | 72,713    | 12.9%  | **416** |
| Fruits     | 61,713    | 10.9%  | 339     |
| Dairy      | 61,073    | 10.8%  | 359     |
| Essentials | 36,991    | 6.6%   | 349     |
| Other      | 35,419    | 6.3%   | 354     |
| Baby       | 34,274    | 6.1%   | 365     |
| Bakery     | 29,579    | 5.2%   | 400     |

- **Beverages** is the highest-revenue category.
- **Snacks** delivers the highest Average Order Value.
- Beverages + Frozen + Veg + Snacks together account for **~54%** of total sales.

### 3. Customer Insights

| Dimension          | Insight                                      |
|--------------------|----------------------------------------------|
| Customer Type      | **Bulk** customers generate **83%** of sales |
| Top Segment        | **Office** leads in revenue                  |
| Weakest Segment    | **Household** has lowest delivery success (79%) |
| Top City           | **Bangalore** (35.8% of sales)               |
| Preferred Payment  | **UPI** (~33% of orders & sales)             |

Every customer in the dataset placed exactly **5 orders**, indicating uniform engagement across the base.

### 4. Delivery Performance

| Status     | Orders | Share  |
|------------|--------|--------|
| Delivered  | 1,256  | 83.7%  |
| Cancelled  | 114    | 7.6%   |
| Failed     | 82     | 5.5%   |
| Returned   | 48     | 3.2%   |

- **16.3%** of orders were not successfully delivered → **₹94,392** in potential lost revenue.
- Average delivery time: **24.7 minutes** (median: 25 min).
- Only **34%** of delivered orders arrived within 20 minutes; **73%** within 30 minutes.
- Delivery performance is consistent across Bangalore, Delhi, and Mumbai (~24.5–25.1 min).

### 5. Temporal Patterns

| Pattern        | Observation                                      |
|----------------|--------------------------------------------------|
| Monthly        | Jan ₹2.83L → Feb ₹2.71L (stable, –4%)            |
| Strongest days | Thursday, Wednesday, Sunday                      |
| Weakest day    | Monday                                           |
| Peak windows   | Early-month and late-month (salary-cycle effect) |

---

## Business Recommendations

1. **Protect hero SKUs** — Maintain deep inventory and high visibility for SKU30, SKU139, SKU12, SKU160, and SKU84.
2. **Grow high-value categories** — Prioritise Beverages (highest sales) and Snacks (highest AOV) with targeted promotions and bundles.
3. **Reduce non-delivery rate** — Cut the 16.3% failure/cancellation/return rate, starting with the Household segment.
4. **Tighten delivery SLAs** — Move more orders into the sub-20-minute window to strengthen the quick-commerce promise.
5. **Double down on digital payments** — UPI already leads; further reduce COD friction and optimise the checkout flow.
6. **Invest in loyalty** — Returning customers show the highest AOV; design retention programmes around them.
7. **Lean into Office demand** — The strongest segment; explore B2B / bulk ordering features.

---

## How to Use

```bash
git clone https://github.com/<your-username>/zepto-sales-analytics.git
cd zepto-sales-analytics
```

Open `data/zepto_sales_raw.xlsx` in Excel, Google Sheets, Power BI, or Python (`pandas`) to explore the raw data and the pre-built pivot tables.

---

## License

This project is licensed under the [MIT License](LICENSE).
