# E-commerce Discount Strategy Impact Analysis (Eniac Case Study)

## 🎯 Project Overview

This project investigates whether aggressive discounting strategies in an e-commerce environment genuinely drive sustainable growth or artificially inflate sales volume.

By reconstructing order-level revenue and comparing it with reported financial metrics, the analysis reveals inconsistencies in pricing logic and highlights how discount-driven growth may negatively impact profitability.

---

## 📊 Dataset & Sources

* Source: Internal e-commerce dataset (orders, orderlines, products, brands)
* Size:

  * Orders: ~100k+
  * Orderlines: ~200k+
  * Products: ~10k+

### Key Fields:

* `order_id`, `created_date`, `total_paid`
* `sku`, `unit_price`, `product_quantity`
* `product_name`, `price`

### Data Issues Identified:

* Inconsistent price formatting (e.g. multiple decimal separators)
* Mismatch between `total_paid` and reconstructed revenue
* Missing values and duplicated records

---

## 🚀 Key Findings

* Discounts significantly increase order volume but degrade revenue quality and margin potential
* A large proportion of products are sold below their listed price → systemic discounting pattern
* Revenue inconsistencies indicate potential data pipeline or reporting issues
* Discount strategies vary across product categories with no clear optimization logic

---

## 📈 Business Recommendations

* Implement category-specific discount strategies instead of uniform discounting
* Reduce discount depth for high-demand products (e.g. smartphones)
* Use accessories and peripherals as controlled promotional drivers
* Improve data pipeline validation to ensure consistency between transactional and reported revenue

---

## 🛠️ Technologies Used

**Programming:**

* Python

**Libraries:**

* pandas
* numpy
* matplotlib

**Environment:**

* Jupyter Notebook / Google Colab

---

## 📁 Project Structure

* 01_data_exploration.ipynb – Data understanding and validation
* 02_data_cleaning.ipynb – Handling missing values and inconsistencies
* 03_feature_engineering.ipynb – Revenue, discount metrics, categories
* 04_discount_analysis.ipynb – Pricing behavior and discount impact
* 05_seasonality_analysis.ipynb – Revenue trends and seasonal patterns

---

## 📌 Conclusion

The analysis demonstrates that while discounting increases short-term sales volume, it may negatively impact long-term profitability. A more targeted and data-driven pricing strategy is required to balance growth and margin sustainability.
