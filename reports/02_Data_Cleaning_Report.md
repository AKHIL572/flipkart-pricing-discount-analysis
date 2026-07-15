# Data Cleaning Report

## Project
Flipkart Product Pricing & Discount Analysis

---

# 1. Objective

The objective of the data cleaning process was to improve the quality, consistency, and usability of the Flipkart product catalogue before performing exploratory data analysis and building the Power BI dashboard.

The raw dataset contained duplicate records, missing values, inconsistent data types, and nested category information that required preprocessing before meaningful analysis could be performed.

---

# 2. Raw Dataset Overview

| Metric | Value |
|---------|------:|
| Original Records | 20,000 |
| Original Columns | 6 (selected from original dataset) |
| Dataset Source | Flipkart Product Catalogue (2015–2016) |

Columns retained for analysis:

- Brand
- Product Name
- Product Category Tree
- Product Rating
- Retail Price
- Discounted Price

---

# 3. Initial Data Quality Assessment

## Missing Values

| Column | Missing Values | Percentage | Action Taken |
|---------|---------------:|-----------:|-------------|
| Brand | 5,864 | 29.32% | Filled with "Unknown" |
| Retail Price | 78 | 0.39% | Removed rows |
| Discounted Price | 78 | 0.39% | Removed rows |
| Product Rating | Stored as text | Converted to numeric |

### Observation

The Brand column contained a significant number of missing values. Since removing nearly 30% of the dataset would result in unnecessary data loss, missing brands were replaced with **"Unknown"**.

Retail Price and Discounted Price contained only 78 missing records each (0.39%), making row removal an appropriate strategy.

---

# 4. Data Type Validation

## Before Cleaning

| Column | Original Type |
|---------|--------------|
| Brand | Object |
| Product Name | Object |
| Product Category Tree | Object |
| Product Rating | Object |
| Retail Price | Float |
| Discounted Price | Float |

### Issues Identified

- Product Rating stored as text.
- "No rating available" prevented numerical analysis.
- Category stored as nested JSON-like text.
- Missing Brand values.
- Duplicate product listings.

---

# 5. Duplicate Analysis

Two levels of duplicate detection were performed.

## Exact Duplicate Records

Fully identical rows:

**3,737**

These records contained no additional information and were removed.

---

## Soft Duplicate Detection

Products sharing the same:

- Brand
- Product Name
- Retail Price
- Discounted Price

Rows detected:

**5,719**

After manual inspection, many represented repeated catalogue entries.

Rows with genuine pricing differences were preserved.

---

# 6. Cleaning Decisions

## Product Rating

Original values included:

- 4.3
- 3.9
- No rating available

Conversion:

```python
pd.to_numeric(errors="coerce")
```

Result:

- Numeric ratings retained
- "No rating available" converted to NaN

Final missing ratings:

14,207

This is expected because the original dataset contains very limited rating information.

---

## Retail Price

Rows with missing Retail Price:

78

Action:

Rows removed.

Reason:

Pricing analysis requires valid price information.

---

## Discounted Price

Rows with missing Discounted Price:

78

Action:

Rows removed.

Reason:

Discount calculations cannot be performed without discounted prices.

---

## Brand

Missing values:

5,864

Action:

Filled using

```python
Unknown
```

Reason:

Preserves product records while clearly identifying unavailable brand information.

---

# 7. Feature Engineering

Several analytical fields were created to simplify downstream analysis.

---

## Feature 1 — Discount Percentage

Formula

```
((Retail Price − Discounted Price)
/ Retail Price) × 100
```

Purpose

- Discount analysis
- Dashboard KPIs
- Category comparison
- Scatter plot

---

## Feature 2 — Main Category

Extracted from:

```
product_category_tree
```

Example

```
Clothing
```

Purpose

- Category analysis
- Dashboard filters
- Category KPIs

---

## Feature 3 — Sub Category

Example

```
Women's Clothing
```

Purpose

Provides a deeper level of product categorization for future analysis.

---

## Feature 4 — Price Bucket

Products segmented into

| Price Bucket |
|--------------|
| <₹500 |
| ₹500–1K |
| ₹1K–2K |
| ₹2K–5K |
| ₹5K+ |

Purpose

Supports pricing segmentation and dashboard analysis.

---

# 8. Final Dataset Summary

| Metric | Value |
|---------|------:|
| Final Records | 15,827 |
| Final Columns | 10 |
| Products Removed | 4,173 |
| Remaining Missing Brand Values | 0 |
| Remaining Missing Prices | 0 |
| Remaining Missing Ratings | 14,207 (Expected) |

---

# 9. Data Validation

Validation checks performed after cleaning:

✔ No missing Retail Price

✔ No missing Discounted Price

✔ Brand column standardized

✔ Duplicate records removed

✔ Discount percentage verified

✔ Category hierarchy extracted

✔ Price buckets validated

✔ Numeric fields converted successfully

---

# 10. Risks & Limitations

Although the dataset was cleaned successfully, several limitations remain due to the source data.

### Rating Coverage

Approximately 90% of products do not contain ratings.

Therefore, rating-based conclusions should be interpreted cautiously.

---

### Missing Brand Information

Nearly one-third of products originally lacked brand information.

Although replaced with "Unknown", this reduces the reliability of brand-level analysis.

---

### Catalogue Dataset

The dataset represents product listings rather than transaction data.

Therefore, this project evaluates catalogue characteristics rather than actual customer purchasing behaviour.

---

# 11. Deliverables Produced

The cleaning process generated:

- cleaned_flipkart_dataset.csv
- Discount Percentage
- Main Category
- Sub Category
- Price Bucket

These outputs serve as the primary input for:

- Exploratory Data Analysis
- Power BI Dashboard
- Business Insights
- Executive Summary

---

# 12. Conclusion

The data cleaning process transformed the raw Flipkart catalogue into a structured analytical dataset suitable for business intelligence reporting.

The cleaned dataset contains 15,827 validated product listings enriched with engineered analytical features, enabling reliable pricing, discount, and category-level analysis throughout the project.