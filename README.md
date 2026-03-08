# Ecommerce Sales Analysis

Analyze ecommerce sales data to identify revenue trends, top-performing regions, product categories, and high-value customers.

## Purpose

This project aims to transform raw, multi-channel ecommerce data into actionable business intelligence. By analyzing B2B/B2C sales, inventory levels, and cross-platform pricing data, we uncover insights that drive profitability and operational efficiency. The analysis answers critical real-world questions such as:

- How do sales and revenue compare across the top 10 states?
- What are the distinct purchasing behaviors between B2B and B2C channels?
- How does our product pricing strategy compare across major platforms (Amazon, Flipkart, Myntra, etc.)?
- Which product categories face potential stockouts or overstocking based on current inventory?

These insights directly support inventory optimization, pricing strategy, and targeted expansion efforts.

## Table of Contents

- [Ecommerce Sales Analysis](#ecommerce-sales-analysis)
  - [Purpose](#purpose)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Tech Stack](#tech-stack)
  - [Project Structure](#project-structure)
  - [Dataset](#dataset)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)

## Features

- **Top 10 States Sales Analysis**: Visualizes top-performing states by sales revenue using bar charts to identify key regional markets.
- **B2B vs B2C Segmentation**: Comparative analysis of wholesale versus retail performance on Amazon.
- **Cross-Platform Pricing**: Evaluation of MSRP strategies across major Indian e-commerce marketplaces.
- **Inventory Management Insights**: Stock level analysis paired with category performance to flag supply chain risks.

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
├── data/                  # excluded from version control (.gitignore)
│   ├── raw/               # place downloaded dataset here
│   └── processed/         # auto-generated after running the notebook
├── images/                # charts and visualizations exported from the notebook
├── notebooks/             # Jupyter notebooks for analysis and exploration
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
4. Download the dataset via Kaggle API:
```bash
   pip install kaggle
   kaggle datasets download thedevastator/unlock-profits-with-e-commerce-sales-data -p data/raw --unzip
```
5. Rename data files to Python-friendly `snake_case`:
```bash
   cd data/raw
   mv "Amazon Sale Report.csv" "amazon_sale_report.csv"
   mv "Cloud Warehouse Compersion Chart.csv" "cloud_warehouse_compersion_chart.csv"
   mv "Expense IIGF.csv" "expense_iigf.csv"
   mv "International sale Report.csv" "international_sale_report.csv"
   mv "May-2022.csv" "may_2022.csv"
   mv "P  L March 2021.csv" "p_l_march_2021.csv"
   mv "Sale Report.csv" "sale_report.csv"
   cd ../..
```
6. Launch the Jupyter notebook:
```bash
   jupyter notebook notebooks/01_top10_states_sales.ipynb
```