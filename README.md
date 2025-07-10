# E-Commerce Data Pipeline – Databricks Project

This project showcases a full end-to-end **E-Commerce Data Engineering Pipeline** using **Apache Spark**, **Delta Lake**, and **Databricks**. It demonstrates the ingestion, transformation, and visualization of real-time data using the **Medallion Architecture**: **Bronze**, **Silver**, and **Gold** layers.

---

## YouTube Demo

Watch a complete walkthrough of the project and dashboard here:  
🔗 [Watch on YouTube](https://www.youtube.com/watch?v=rh47vtvR8wE)

---

## Project Structure

| Notebook                     | Description |
|-----------------------------|-------------|
| `reader_factory.ipynb`      | Implements a factory pattern to support multiple data source readers (CSV, JSON, Parquet). |
| `Stream Data Partitioning.ipynb` | Demonstrates partitioning strategies on streaming data using Spark Structured Streaming. |
| `Bronze.ipynb`              | Reads raw streaming data and writes it into the Bronze layer in Delta format. |
| `Silver.ipynb`              | Cleans, filters, and deduplicates data from Bronze, and writes enriched data to the Silver layer. |
| `Gold.ipynb`                | Aggregates business metrics (e.g., total sales, top products) from Silver data for analytics/reporting. |
| `Dashboard Notebook.ipynb`  | Visualizes the processed Gold-layer data using Databricks dashboards (sales KPIs, charts). |

---

## Medallion Architecture

- **Bronze Layer**: Ingests raw data from streaming sources in append-only mode.
- **Silver Layer**: Applies transformations like filtering, joins, and type casting to clean the data.
- **Gold Layer**: Performs aggregations and prepares data for reporting and BI consumption.

---

## ⚙️ Tech Stack

- **Apache Spark (Structured Streaming)**
- **Delta Lake (Bronze / Silver / Gold)**
- **Databricks**
- **PySpark**
- **Databricks Dashboards**

---

## Key Features

- Real-time data ingestion using Spark Structured Streaming
- Layered data transformation (Bronze → Silver → Gold)
- Clean and scalable architecture with Delta Lake
- Live dashboards for business users (sales, performance, etc.)

---

# Dataset Overview

This project uses the **Brazilian E-Commerce Public Dataset by Olist**, available on Kaggle.

- **Source**: [Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data)
- **Provider**: Olist (via Kaggle)
- **License**: Public dataset for educational and research purposes

---

## Dataset Description

The dataset provides a detailed view of the Brazilian e-commerce industry and includes:
- Customer orders from multiple sellers across various product categories
- Information about:
  - Orders and order items
  - Customers and sellers
  - Payments and deliveries
  - Product metadata and reviews

---

## Files Included in Kaggle Dataset

| File Name                      | Description |
|-------------------------------|-------------|
| `olist_orders_dataset.csv`     | Order status, purchase and delivery timestamps |
| `olist_order_items_dataset.csv`| Products included in each order |
| `olist_products_dataset.csv`   | Product categories, dimensions |
| `olist_customers_dataset.csv`  | Customer locations |
| `olist_sellers_dataset.csv`    | Seller locations |
| `olist_order_reviews_dataset.csv`| Review scores and comments |
| `olist_order_payments_dataset.csv`| Payment methods and values |
| `product_category_name_translation.csv`| English translations of product categories |

---

## How to Access

To download the dataset:
1. Create a Kaggle account at [kaggle.com](https://www.kaggle.com/)
2. Visit the dataset page: [https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data)
3. Click on **Download** or use the Kaggle API:
   ```bash
   kaggle datasets download -d olistbr/brazilian-ecommerce

## ⚙️ How to Run This Project

1. **Clone this repo**:
   ```bash
   git clone https://github.com/yourusername/ecommerce-data-pipeline.git
   cd ecommerce-data-pipeline
   ```

2. **Upload Notebooks to Databricks**

3. **Follow this execution order**:
   - `reader_factory.ipynb`
   - `Stream Data Partitioning.ipynb`
   - `Bronze.ipynb`
   - `Silver.ipynb`
   - `Gold.ipynb`
   - `Dashboard Notebook.ipynb`

4. **Place dataset** in your cloud storage (DBFS, S3, ADLS) accessible from Databricks.

5. **Create dashboards** from the Gold table outputs.
