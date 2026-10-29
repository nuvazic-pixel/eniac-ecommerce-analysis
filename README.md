# Eniac — Pricing Exploration & Transaction Data Quality
**Python · pandas · NumPy · Matplotlib · Jupyter**  
Data Analytics coursework portfolio · findings and source-data rerun in progress.

## Business question
How do discounts vary across products, categories and time, and can the transaction data support reliable sales reporting?

## Review the workflow
| Notebook | Implemented work |
| --- | --- |
| [01 — Exploration](01_data_exploration.ipynb) | Dataset structure, missingness, duplicates and unmatched order/SKU checks |
| [02 — Cleaning](02_data_cleaning.ipynb) | Type conversion, duplicate removal and positive-price/quantity filters |
| [03 — Feature engineering](03_feature_engineering.ipynb) | Brand enrichment, rule-based categories, joins and revenue/discount variables |
| [04 — Discount analysis](04_discount_analysis.ipynb) | Discount prevalence/depth, category comparisons and brand revenue charts |
| [05 — Seasonality](05_seasonality_analysis.ipynb) | Monthly sales-value trends and quarterly comparisons |

## What this project practises
- Inspecting table structure before calculating KPIs.
- Checking missing values, duplicates and referential integrity.
- Joining order lines with catalogue and order records.
- Constructing variables and visualising descriptive comparisons.
- Distinguishing a descriptive relationship from a causal or profitability claim.

## Metric definitions
- **Line sales value:** `unit_price * product_quantity`. Aggregates require an explicit order-status policy; existing charts do not all filter to completed orders.
- **Discount percentage:** `(catalogue_price - unit_price) / catalogue_price * 100`. Catalogue price is a reference, not necessarily the price valid on the transaction date.
- **SKU discounted at least once:** distinct sold SKUs with at least one discounted line / all distinct sold SKUs.
- **Discounted line share:** fraction of transaction lines discounted. This is not a unique-SKU or quantity-weighted share.
- **Profit:** not measured; cost and margin data are absent from the published work.

## Results and validation status
The notebooks contain analysis code but no saved execution outputs, and several interpretation cells remain unfinished. The source CSV files are not included. This repository therefore demonstrates the workflow and questions; it does **not** establish that discounts caused higher volume or lower profitability.

The earlier README made stronger claims than the published evidence supported. Those claims have been removed pending a reproducible source-data run.

## Reproduction requirements
The current notebooks expect these coursework CSVs:
- `orders_cl.csv`
- `products_cl(1).csv`
- `orderlines_qu.csv`
- `brands(1).csv`

They use absolute `/mnt/data/` paths. Adapt those paths to your authorised local copies and install pandas, NumPy, Matplotlib and Jupyter. Notebooks 02 and 03 also require `from pathlib import Path` before their export cells.

## Remaining work before a complete analytical case study
1. Parameterise input/output paths and complete missing imports.
2. Preserve and report rejected rows instead of silently dropping records after numeric coercion.
3. Check join cardinality and define a consistent completed-order population.
4. Make discounted/non-discounted SKU groups mutually exclusive; a SKU can currently appear in both bars.
5. Compare reconstructed order totals with `total_paid`, with an explicit tolerance and interpretation of shipping/tax.
6. Execute all notebooks, save outputs and write conclusions tied to the observed values.

No source-data run was performed in this portfolio documentation revision.

[Portfolio](https://github.com/nuvazic-pixel)
