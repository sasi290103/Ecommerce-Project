# 📦 Dataset Overview

This project uses the **Brazilian E-Commerce Public Dataset by Olist**, available on Kaggle.

- **Source**: [Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data)
- **Provider**: Olist (via Kaggle)
- **License**: Public dataset for educational and research purposes

---

## 📊 Dataset Description

The dataset provides a detailed view of the Brazilian e-commerce industry and includes:
- Customer orders from multiple sellers across various product categories
- Information about:
  - Orders and order items
  - Customers and sellers
  - Payments and deliveries
  - Product metadata and reviews

---

## 📂 Files Included in Kaggle Dataset

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

## 📥 How to Access

To download the dataset:
1. Create a Kaggle account at [kaggle.com](https://www.kaggle.com/)
2. Visit the dataset page: [https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce/data)
3. Click on **Download** or use the Kaggle API:
   ```bash
   kaggle datasets download -d olistbr/brazilian-ecommerce
