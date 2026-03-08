# Ecommerce Sales Analysis

Analyze ecommerce sales data to identify revenue trends, top-performing regions, product categories, and high-value customers.

## Table of Contents

- [Ecommerce Sales Analysis](#ecommerce-sales-analysis)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Tech Stack](#tech-stack)
  - [Project Structure](#project-structure)
  - [Dataset](#dataset)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)

## Features

- **Data Processing**: End-to-end workflow including data loading, inspection, cleaning, and feature engineering.
- **Exploratory Data Analysis**: Deep dive into ecommerce transaction records and sales metrics.
- **Business Insights**: Identification of peak revenue, top-performing geographic regions, and high-value customers.
- **Visualizations**: Production of insightful charts such as monthly revenue trends and customer distributions.

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
├── data/
│   ├── raw/
│   └── processed/
├── images/
├── notebooks/
└── src/
```

## Dataset

Source: [Kaggle - Unlock Profits with E-commerce Sales Data](https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data)

The dataset contains ecommerce transaction records with fields such as:

- `order_id` — unique transaction identifier
- `order_date` — date of purchase
- `customer_id` — unique customer identifier
- `region` — geographic sales region
- `category` — product category
- `product_name` — product sold
- `quantity` — number of units sold
- `unit_price` — price per unit

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
5. Launch the Jupyter notebook:
   ```bash
   jupyter notebook notebooks/analysis.ipynb
   ```