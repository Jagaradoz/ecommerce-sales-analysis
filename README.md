# Ecommerce Sales Analysis

Analyze ecommerce sales data to identify revenue trends, top-performing regions, product categories, and high-value customers.

## Purpose

This project aims to transform raw ecommerce data into actionable business intelligence. By analyzing B2B/B2C sales, inventory levels, and cross-platform pricing data, we uncover insights that drive profitability and operational efficiency. The analysis answers critical real-world questions such as:

- How do sales and revenue compare across the top 10 states?
- What are the distinct purchasing behaviors between B2B and B2C channels?
- How does our product pricing strategy compare across major platforms (Amazon, Flipkart, Myntra, etc.)?
- Which product categories face potential stockouts or overstocking based on current inventory?

These insights directly support inventory optimization, pricing strategy, and targeted expansion efforts.

## Features

- **State Sales Analysis** (`01_state_sales_analysis.ipynb`): Geographic sales performance across Indian states
  - Top 10 states by revenue with multi-currency comparison (INR, USD, THB)
  - Fulfillment method distribution (Amazon vs Merchant fulfillment)
  - Order volume vs revenue performance analysis
  - Average order value by state
  - State-level performance metrics and insights
  
- **Time Series Analysis** (`02_time_series_analysis.ipynb`): Temporal patterns and trends in sales data
  - Daily sales revenue trends with 7-day moving average
  - Daily order volume tracking
  - Revenue distribution analysis
  - Monthly sales performance (revenue and quantity)
  - Day-of-week performance patterns
  - Peak sales identification and trend analysis
  
- **Category Performance** (`03_category_performance.ipynb`): Product category insights and optimization
  - Category-wise revenue analysis and market share
  - Cancellation rate analysis by category
  - Fulfillment method performance comparison (Amazon vs Merchant)
  - B2B vs B2C sales patterns by category
  - Average order value by category
  - Actionable recommendations for inventory and marketing strategy

## Table of Contents

- [Ecommerce Sales Analysis](#ecommerce-sales-analysis)
  - [Purpose](#purpose)
  - [Features](#features)
  - [Table of Contents](#table-of-contents)
  - [Tech Stack](#tech-stack)
  - [Project Structure](#project-structure)
  - [Dataset](#dataset)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)

## Tech Stack

| Technology   | Role                             |
| :----------- | :------------------------------- |
| `Python`     | Core language                    |
| `Pandas`     | Data manipulation and analysis   |
| `NumPy`      | Numerical computing              |
| `Matplotlib` | Basic data visualization         |
| `Seaborn`    | Statistical data visualization   |
| `Jupyter`    | Interactive notebook environment |

## Project Structure
```text
ecommerce-sales-analysis/
├── data/                                       # excluded from version control (.gitignore)
│   ├── amazon_sale_report.csv                  # primary transaction records
│   ├── international_sale_report.csv           # B2B wholesale transactions
│   ├── sale_report.csv                         # inventory catalog
│   ├── may_2022.csv                            # pricing comparison
│   ├── p_l_march_2021.csv                      # pricing comparison
│   ├── expense_iigf.csv                        # operational expenses
│   └── cloud_warehouse_compersion_chart.csv    # shipping expenses
├── images/                                     # charts and visualizations exported from notebooks
│   ├── 01_state_sales_analysis/                # state-level sales visualizations
│   ├── 02_time_series_analysis/                # temporal trend charts
│   └── 03_category_performance/                # category and product insights
├── notebooks/                                  # Jupyter notebooks for analysis
│   ├── 01_state_sales_analysis.ipynb           # state-wise sales performance
│   ├── 02_time_series_analysis.ipynb           # temporal patterns and forecasting
│   └── 03_category_performance.ipynb           # product category analysis
└── README.md
```

## Dataset

Source: [Kaggle - Unlock Profits with E-commerce Sales Data](https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data)

The dataset consists of multiple related exports reflecting diverse business operations:

- `amazon_sale_report.csv` — Primary transaction records for Amazon India (includes fulfillment, location, B2B flags, and sales amounts).
- `international_sale_report.csv` — B2B wholesale transactions with international clients.
- `sale_report.csv` — Master inventory catalog detailing stock levels by SKU, category, and size.
- `may_2022.csv` & `p_l_march_2021.csv` — Cross-platform pricing comparison charts (Amazon, Flipkart, Myntra, Ajio, Limeroad, Paytm).
- `expense_iigf.csv` & `cloud_warehouse_compersion_chart.csv` — Operational and shipping expenses.

## Getting Started

### Prerequisites

- `Python` 3.8+
- [Kaggle API](https://github.com/Kaggle/kaggle-api) setup for downloading the dataset.

### Installation

1. Clone the repository:
```bash
   git clone https://github.com/yourusername/ecommerce-sales-analysis.git
   cd ecommerce-sales-analysis
```
2. Create and activate a virtual environment:
```bash
   python3 -m venv .venv
   source .venv/bin/activate
```
3. Install dependencies:
```bash
   pip install -r requirements.txt
```
4. Download and prepare the dataset:
```bash
   pip install kaggle
   kaggle datasets download thedevastator/unlock-profits-with-e-commerce-sales-data -p data/ --unzip
   
   # Rename files to Python-friendly format
   cd data/
   mv "Amazon Sale Report.csv" "amazon_sale_report.csv"
   mv "Cloud Warehouse Compersion Chart.csv" "cloud_warehouse_compersion_chart.csv"
   mv "Expense IIGF.csv" "expense_iigf.csv"
   mv "International sale Report.csv" "international_sale_report.csv"
   mv "May-2022.csv" "may_2022.csv"
   mv "P  L March 2021.csv" "p_l_march_2021.csv"
   mv "Sale Report.csv" "sale_report.csv"
   cd ..
```
5. Launch Jupyter notebooks:
```bash
   jupyter notebook notebooks/
```