# E-commerce Revenue & Discount Strategy Analysis (Eniac Case Study)

## 🎯 Project Overview
This project analyses transactional data from an e-commerce company to evaluate the real impact of discount strategies on revenue and profitability. The goal was to validate whether increased sales volume driven by discounts actually leads to business growth.

Using Python (pandas) and data validation techniques, I compared reported revenue with reconstructed order-level revenue and analysed pricing inconsistencies. The results highlight critical gaps between perceived growth and actual financial performance.

---

## 📊 Dataset & Sources
- Source: Internal e-commerce dataset (orders, orderlines, products)
- Size: 
  - Orders: ~100k+
  - Orderlines: ~200k+
  - Products: ~10k+
- Key Features:
  - `order_id`, `created_date`, `total_paid`
  - `product_id`, `unit_price`, `quantity`
  - `product_name`, `price`
- Notes:
  - Data inconsistencies between product price and transaction price
  - Missing values and duplicated records handled during cleaning

---

## 🚀 Key Findings & Results

- Discounted products generate higher order volume but reduce overall revenue quality
- Significant mismatch found between `total_paid` and reconstructed order value (data integrity issue)
- Some products are consistently sold below listed price → potential margin loss
- High variability in discount application across categories (no clear strategy)
- Business Insight:
  - Revenue growth is partially artificial due to aggressive discounting
  - Current strategy may increase sales volume but harms profitability

---

## 🛠️ Technologies Used

**Programming:**
- Python

**Libraries:**
- pandas
- numpy
- matplotlib

**Environment:**
- Google Colab / Jupyter Notebook

---

## 📁 Project Structure
