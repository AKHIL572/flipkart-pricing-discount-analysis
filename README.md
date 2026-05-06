# Flipkart Product Pricing & Discount Analysis

> Analyzing how Flipkart can optimize pricing, discounts, and product positioning to increase sales and customer satisfaction.

---

## Project Structure

```
flipkart/
│
├── dashboard/
│    ├── flipkart_dashboard.pbix      # Power BI dashboard source file
│    └── flipkart_dashboard.pdf       # Exported dashboard (PDF)
│
├── data/
│    ├── flipkart_dataset.csv         # Raw dataset (~20,000 records)
│    └── cleaned_flipkart_dataset.csv # Cleaned and processed dataset
│
├── notebook/
│    └── analysis.ipynb               # End-to-end analysis notebook
│
└── README.md
```

---

## Business Problem

Flipkart (2015–2016) carried thousands of products across hundreds of categories with varying pricing and discount strategies. This project investigates:

- Which categories and brands dominate the catalogue?
- How are discounts distributed — and do higher-priced products get discounted less?
- Where are the data quality gaps (missing brands, missing ratings) that limit deeper analysis?

---

## Dataset

| Property | Details |
|---|---|
| Source file | `flipkart_dataset.csv` |
| Time period | 2015 – 2016 |
| Raw records | ~20,000 rows |
| Original columns | 15 (uniq_id, crawl_timestamp, product_url, product_name, product_category_tree, pid, retail_price, discounted_price, image, is_FK_advantage_product, description, product_rating, overall_rating, brand, product_specifications) |
| Columns used | brand, product_name, product_category_tree, product_rating, retail_price, discounted_price |

### Why only 6 columns?

| Excluded column(s) | Reason |
|---|---|
| uniq_id, product_url, pid, image, is_FK_advantage_product, description, product_specifications | No analytical value for the pricing/discount business problem |
| overall_rating | 91% missing values (18,083 nulls) — too sparse to use |
| crawl_timestamp | Not needed — no time-series analysis in scope |

---

## Data Cleaning Steps

1. **Type conversion** — `product_rating`, `retail_price`, and `discounted_price` converted from object to numeric; non-numeric strings coerced to `NaN`.
2. **Dropped price nulls** — 78 rows with missing `retail_price` or `discounted_price` removed (small enough to drop safely).
3. **Filled brand nulls** — 5,864 missing brand values replaced with `"Unknown"` to preserve rows for category-level analysis.
4. **Deduplication** — rows duplicate on `(brand, product_name, retail_price, discounted_price)` removed. Note: same product name at a different price is kept as a distinct listing.
5. **Feature engineering** — `main_category` extracted from `product_category_tree` by parsing the first level of the category path; `discount_percentage` derived as `((retail_price − discounted_price) / retail_price) × 100`.
6. **Saved** to `cleaned_flipkart_dataset.csv` (15,827 rows, 10 columns).

---

## Cleaned Dataset Overview

| Metric | Value |
|---|---|
| Total records | 15,827 |
| Unique product names | 12,626 |
| Unique brands | 3,486 |
| Unique main categories | 251 |
| Average retail price | ₹3,324 |
| Average discount | 39.4% |
| Products with rating data | 10.2% (1,620 rows) |
| Unknown brand rows | 28.9% (4,574 rows) |

---

## Analysis & Key Findings

### Category Analysis
- **Clothing** leads with the most listings (~4,427 rows), followed by **Jewellery** (2,925) and **Automotive** (989).
- **Furniture** has the highest average retail price (~₹22,594), distantly followed by Automation & Robotics (~₹20,000).
- Most products are priced **under ₹500** — 47% of the catalogue falls in the lowest price bucket.

### Discount Analysis
- Overall average discount is **39.4%**, with most products offering discounts in the **40–60% range**.
- **Lower-priced products get deeper discounts**: the `<₹500` bucket averages 46% off, while the `₹5K+` bucket averages only 22%.
- The scatter plot of retail price vs. discount percentage confirms that discount depth drops as price increases.

### Brand Analysis
- **28.9%** of products have no brand information (tagged "Unknown"), limiting brand-level conclusions.
- Among named brands, **Allure Auto** leads in product count (468), followed by Voylla (266) and Karatcraft (211).
- **Clothing** has the highest number of unique competing brands.
- **Rajcraft** offers the highest average discount percentage among named brands.

### Rating Analysis
- Only **10.2%** of products have a numeric rating — results are statistically unreliable and should be treated with caution.
- No meaningful correlation between product rating and retail price could be established due to the data sparsity.

---

## Dashboard

The Power BI dashboard (`dashboard/flipkart_dashboard.pbix`) provides interactive views across:

- Top product categories by listing volume
- Average retail price across categories
- Product distribution across price segments (< ₹500, ₹500–1K, ₹1K–2K, ₹2K–5K, ₹5K+)
- Discount depth distribution by category and brand
- Leading brands by product count
- Data quality indicators (unknown brands, rating coverage)

A static export is available at `dashboard/flipkart_dashboard.pdf`.

---

## How to Run

### Prerequisites
```
Python 3.8+
pandas
matplotlib
seaborn
jupyter
```

### Install dependencies
```bash
pip install pandas matplotlib seaborn jupyter
```

### Run the notebook
```bash
cd flipkart/
jupyter notebook notebook/analysis.ipynb
```

The notebook expects the raw data at `../data/flipkart_dataset.csv` relative to the notebook directory. The cleaned dataset is saved automatically to `../data/cleaned_flipkart_dataset.csv` after running the cleaning cells.

---

## Limitations

- **Rating data is unreliable** — 91% of product ratings are missing; any rating-based conclusions should be treated as indicative only.
- **No time-series analysis** — the crawl timestamp was excluded; trends over 2015–2016 are not explored.
- **Brand coverage** — nearly 29% of products have no brand attribution, which constrains brand-level segmentation.
- **Snapshot data** — this is a scraped catalogue snapshot, not transactional sales data; "product count" is a proxy for catalogue presence, not actual sales volume.

---

## Tools Used

| Tool | Purpose |
|---|---|
| Python (pandas) | Data loading, cleaning, feature engineering |
| Matplotlib / Seaborn | Exploratory visualizations in the notebook |
| Power BI | Interactive dashboard |
| Jupyter Notebook | Analysis and documentation |

---

*Data source: Flipkart product catalogue snapshot (2015–2016)*
