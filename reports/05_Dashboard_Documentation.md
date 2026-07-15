# Dashboard Documentation

## Project
Flipkart Product Pricing & Discount Analysis

---

# 1. Dashboard Overview

The Power BI dashboard provides an interactive overview of Flipkart's product catalogue, enabling users to explore pricing behaviour, discount strategies, category composition, and brand distribution.

The dashboard was designed for business users rather than technical users, allowing category managers, pricing analysts, and management teams to identify trends without requiring SQL or Python knowledge.

The dashboard emphasizes simplicity, interactivity, and business decision support.

---

# 2. Dashboard Objectives

The dashboard was created to answer the following business questions:

- Which product categories dominate the catalogue?
- Which categories have the highest average prices?
- How are products distributed across different price ranges?
- Which brands have the largest catalogue presence?
- How are discounts distributed across categories?
- Do pricing and discount strategies differ across price segments?
- What data quality issues exist within the catalogue?

---

# 3. Dashboard Layout

The dashboard is organized into four logical sections.

## Section 1 — KPI Summary

The top section provides a quick overview of the catalogue using key performance indicators.

These KPIs allow users to understand the overall size, pricing, discount levels, and data quality without interacting with any visuals.

---

## Section 2 — Filters

Three slicers allow users to dynamically filter all dashboard visuals.

Available filters include:

- Main Category
- Price Bucket
- Brand

These filters enable users to focus on specific market segments.

---

## Section 3 — Analytical Visualizations

The center of the dashboard contains interactive visualizations covering:

- Category distribution
- Pricing analysis
- Discount analysis
- Brand analysis
- Price segmentation

Each visualization is connected through Power BI cross-filtering.

---

## Section 4 — Key Insights

The final section summarizes the most important business findings and provides context for decision-makers.

This allows executives to understand the major conclusions without interpreting every chart individually.

---

# 4. KPI Documentation

## KPI 1 — Total Products

**Purpose**

Displays the total number of product listings available after data cleaning.

**Business Value**

Provides the overall catalogue size used throughout the analysis.

---

## KPI 2 — Average Discount (%)

**Purpose**

Displays the average percentage discount across all products.

**Business Value**

Measures the overall promotional intensity of the marketplace.

---

## KPI 3 — Average Retail Price

**Purpose**

Shows the average retail price of products in the filtered dataset.

**Business Value**

Provides an overview of pricing levels across the selected products.

---

## KPI 4 — Total Brands

**Purpose**

Displays the number of identified brands after excluding "Unknown" and "Generic".

**Business Value**

Represents catalogue diversity and brand participation.

---

## KPI 5 — Unknown Brand Percentage

**Purpose**

Displays the percentage of products without identifiable brand information.

**Business Value**

Acts as a data quality indicator.

High values indicate incomplete catalogue metadata.

---

## KPI 6 — Products with Ratings

**Purpose**

Shows the percentage of products with valid numerical ratings.

**Business Value**

Measures the completeness of customer feedback data.

---

## KPI 7 — Total Categories

**Purpose**

Displays the number of unique product categories.

**Business Value**

Represents catalogue diversity.

---

# 5. Filter Documentation

## Main Category

Allows users to analyze a single product category or compare categories.

---

## Price Bucket

Segments products into predefined pricing groups.

Price Buckets:

- Below ₹500
- ₹500–₹1K
- ₹1K–₹2K
- ₹2K–₹5K
- Above ₹5K

---

## Brand

Allows users to focus on specific brands.

Unknown and Generic brands are intentionally excluded to improve analytical relevance.

---

# 6. Visual Documentation

## Visual 1

### Top Product Categories by Listing Volume

**Business Question**

Which categories contain the largest number of products?

**Insight**

Highlights catalogue concentration and competitive segments.

---

## Visual 2

### Average Retail Price Across Categories

**Business Question**

Which categories contain the highest-value products?

**Insight**

Identifies premium product categories.

---

## Visual 3

### Product Distribution Across Price Segments

**Business Question**

Where are most products positioned within the pricing spectrum?

**Insight**

Illustrates the marketplace's pricing structure.

---

## Visual 4

### Leading Brands by Product Count

**Business Question**

Which brands contribute the highest number of catalogue listings?

**Insight**

Shows catalogue representation rather than market leadership.

---

## Visual 5

### Average Discount (%) by Main Category

**Business Question**

Do discount strategies vary across categories?

**Insight**

Supports comparison of promotional intensity.

---

## Visual 6

### Average Discount (%) by Price Bucket

**Business Question**

Do cheaper or premium products receive larger discounts?

**Insight**

Highlights pricing behaviour across market segments.

---

## Visual 7

### Retail Price vs Discount Percentage

**Business Question**

Is there a relationship between product price and discount level?

**Insight**

Allows users to identify pricing patterns and potential outliers.

---

# 7. Dashboard Interactions

The dashboard supports cross-filtering between visuals.

Selecting any category, brand, or price bucket updates all related KPIs and charts.

This enables users to perform interactive exploratory analysis without writing queries.

---

# 8. Business Story

The dashboard follows a logical analytical flow.

Step 1

Understand the overall catalogue through KPIs.

↓

Step 2

Identify dominant categories.

↓

Step 3

Analyze pricing behaviour.

↓

Step 4

Evaluate discount strategies.

↓

Step 5

Explore brand participation.

↓

Step 6

Assess catalogue quality.

↓

Step 7

Support pricing and catalogue management decisions.

---

# 9. Dashboard Limitations

The dashboard reflects catalogue listings rather than transactional sales.

Therefore:

- Listing counts should not be interpreted as sales volume.
- Discounts do not indicate promotional success.
- Brand representation does not imply market share.
- Revenue cannot be estimated.
- Customer satisfaction analysis is limited due to sparse rating data.

---

# 10. Intended Users

This dashboard is designed for:

- Business Analysts
- Data Analysts
- Pricing Analysts
- Category Managers
- Business Intelligence Teams
- Product Managers
- Senior Management

---

# 11. Dashboard Usage Guide

Users can explore the dashboard by:

1. Selecting a product category.
2. Filtering by price segment.
3. Filtering by brand.
4. Comparing pricing behaviour.
5. Reviewing discount strategies.
6. Identifying premium categories.
7. Monitoring catalogue quality indicators.

---

# 12. Dashboard Conclusion

The dashboard provides an interactive overview of Flipkart's catalogue structure, pricing behaviour, and discount strategies.

It supports exploratory business analysis while highlighting important data quality limitations that should be considered before making strategic decisions.