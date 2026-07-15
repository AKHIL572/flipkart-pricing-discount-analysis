# Data Dictionary

## Project

Flipkart Product Pricing & Discount Analysis

---

# Purpose

This document describes every field used throughout the project.

It provides:

- Column definitions
- Data types
- Business meaning
- Data quality observations
- Transformations performed during preprocessing

The objective is to ensure that anyone working with the dataset can correctly interpret every variable used in the analysis.

---

# Dataset Summary

| Attribute | Value |
|------------|-------|
| Original Records | 20,000 |
| Records After Cleaning | 15,827 |
| Original Columns | 15 |
| Columns Used | 6 |
| Engineered Columns | 4 |

---

# Original Columns Used

---

## 1. Brand

| Property | Description |
|-----------|-------------|
| Column Name | `brand` |
| Data Type | Object (String) |
| Business Meaning | Brand or manufacturer of the product |
| Missing Values | 5,864 (29.3%) |
| Cleaning Applied | Missing values replaced with `"Unknown"` |
| Business Usage | Brand-level analysis and filtering |

### Data Quality Note

A significant portion of products lacked brand information, reducing the reliability of brand-level insights.

---

## 2. Product Name

| Property | Description |
|-----------|-------------|
| Column Name | `product_name` |
| Data Type | Object (String) |
| Missing Values | None |
| Unique Values | 12,626 |
| Business Meaning | Name of the listed product |
| Cleaning Applied | No changes |
| Business Usage | Product counting and duplicate identification |

---

## 3. Product Category Tree

| Property | Description |
|-----------|-------------|
| Column Name | `product_category_tree` |
| Data Type | Object (String) |
| Missing Values | None |
| Business Meaning | Hierarchical category assigned to the product |
| Cleaning Applied | Parsed into Main Category and Sub Category |
| Business Usage | Category analysis and dashboard filtering |

### Example

```
Clothing >> Women's Clothing >> Lingerie
```

---

## 4. Product Rating

| Property | Description |
|-----------|-------------|
| Column Name | `product_rating` |
| Data Type (Original) | Object |
| Data Type (Final) | Float |
| Missing Values After Cleaning | 14,207 |
| Original Values | Numeric ratings and `"No rating available"` |
| Cleaning Applied | Converted to numeric using `errors='coerce'` |
| Business Usage | Limited rating analysis |

### Data Quality Note

Only approximately **10.2%** of products contained valid ratings.

Any rating-based conclusions should therefore be interpreted cautiously.

---

## 5. Retail Price

| Property | Description |
|-----------|-------------|
| Column Name | `retail_price` |
| Data Type | Float |
| Missing Values | 78 |
| Cleaning Applied | Rows with missing values removed |
| Business Usage | Pricing analysis and discount calculation |

---

## 6. Discounted Price

| Property | Description |
|-----------|-------------|
| Column Name | `discounted_price` |
| Data Type | Float |
| Missing Values | 78 |
| Cleaning Applied | Rows with missing values removed |
| Business Usage | Pricing analysis and discount calculation |

---

# Engineered Columns

The following variables were created during preprocessing.

---

## 7. Discount Percentage

| Property | Description |
|-----------|-------------|
| Column Name | `discount_percentage` |
| Data Type | Float |
| Derived From | Retail Price & Discounted Price |

### Formula

```
((Retail Price - Discounted Price) / Retail Price) × 100
```

### Business Usage

Measures the percentage discount offered on each product.

Used extensively throughout pricing and promotional analysis.

---

## 8. Main Category

| Property | Description |
|-----------|-------------|
| Column Name | `main_category` |
| Data Type | String |
| Derived From | Product Category Tree |

### Example

```
Clothing
Furniture
Jewellery
Automotive
```

### Business Usage

Primary grouping variable used in:

- Category analysis
- Dashboard slicers
- KPI reporting

---

## 9. Sub Category

| Property | Description |
|-----------|-------------|
| Column Name | `sub_category` |
| Data Type | String |
| Derived From | Product Category Tree |

### Example

```
Women's Clothing
Living Room Furniture
Mobile Accessories
```

### Business Usage

Provides a more detailed view of product segmentation and enables drill-down analysis.

---

## 10. Price Bucket

| Property | Description |
|-----------|-------------|
| Column Name | `price_bucket` |
| Data Type | Categorical |
| Derived From | Discounted Price |

### Categories

- Below ₹500
- ₹500–₹1K
- ₹1K–₹2K
- ₹2K–₹5K
- Above ₹5K

### Business Usage

Used to analyze pricing distribution and compare discount strategies across different price segments.

---

# Excluded Columns

The following columns were intentionally excluded because they were not relevant to the defined business problem.

| Column | Reason for Exclusion |
|---------|----------------------|
| uniq_id | Technical identifier with no analytical value |
| crawl_timestamp | Not required as this is not a time-series analysis |
| product_url | Navigational field only |
| pid | Internal product identifier |
| image | Not required for pricing analysis |
| is_FK_Advantage_product | Outside the scope of the selected business problem |
| description | Unstructured text not analyzed in this project |
| overall_rating | 91% missing; duplicates the limitations of `product_rating` |
| product_specifications | Unstructured text outside the current scope |

---

# Data Cleaning Summary

The following preprocessing steps were performed:

- Selected only business-relevant columns.
- Converted product ratings from text to numeric.
- Replaced `"No rating available"` with `NaN`.
- Removed records with missing price information.
- Filled missing brands with `"Unknown"`.
- Removed duplicate listings.
- Parsed hierarchical categories.
- Created engineered analytical features.

---

# Data Quality Summary

| Issue | Observation | Action Taken |
|--------|-------------|--------------|
| Missing Brand | 5,864 records | Filled with `"Unknown"` |
| Missing Prices | 78 records | Removed |
| Missing Ratings | 14,207 records | Retained as `NaN` |
| Duplicate Listings | Exact duplicates identified | Removed |
| Category Hierarchy | Nested strings | Split into Main & Sub Category |

---

# Known Limitations

The dataset represents product catalogue listings only.

It does **not** include:

- Customer information
- Orders
- Sales transactions
- Revenue
- Profit
- Inventory
- Seller information
- Time-series pricing

As a result, the analysis is limited to catalogue composition, pricing, and discount behaviour.

---

# Conclusion

This data dictionary serves as the reference guide for all variables used throughout the project. It documents the origin, meaning, quality, and business purpose of each field, ensuring consistency across data preparation, analysis, visualization, and reporting.