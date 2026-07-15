# Final Project Report

# Flipkart Product Pricing & Discount Analysis

---

# 1. Project Overview

## Project Title

Flipkart Product Pricing & Discount Analysis

---

## Project Type

End-to-End Data Analytics Project

---

## Domain

E-Commerce Analytics

---

## Duration

Self-initiated portfolio project

---

## Objective

The objective of this project was to analyze Flipkart's product catalogue to understand:

- Catalogue composition
- Pricing behaviour
- Discount strategies
- Brand representation
- Category distribution
- Data quality

The project aimed to convert raw catalogue data into meaningful business insights that could support pricing strategy and catalogue management.

---

# 2. Business Problem

Flipkart hosts thousands of products across hundreds of categories.

Without structured analysis, it is difficult to answer questions such as:

- Which categories dominate the marketplace?
- Which categories contain premium-priced products?
- How are discounts distributed?
- Which brands contribute most to the catalogue?
- Are current discount strategies consistent?
- What data quality issues affect reporting?

The objective was to answer these questions through exploratory data analysis and interactive business intelligence.

---

# 3. Dataset Overview

| Attribute | Value |
|------------|-------|
| Source | Flipkart Product Catalogue (2015–2016) |
| Original Records | 20,000 |
| Cleaned Records | 15,827 |
| Main Categories | 251 |
| Brands | 3,486 (including Unknown) |

### Columns Used

- Brand
- Product Name
- Product Category Tree
- Product Rating
- Retail Price
- Discounted Price

---

# 4. Project Workflow

The project followed a structured analytics workflow:

Business Problem Definition

↓

Data Understanding

↓

Data Cleaning

↓

Feature Engineering

↓

Exploratory Data Analysis

↓

Business Insight Generation

↓

Dashboard Development

↓

Business Recommendations

↓

Project Documentation

---

# 5. Data Cleaning Summary

The following preprocessing steps were performed:

- Filtered only columns relevant to the business problem.
- Converted product ratings from text to numeric.
- Replaced `"No rating available"` with `NaN`.
- Removed rows with missing retail and discounted prices.
- Filled missing brand values with `"Unknown"`.
- Removed duplicate product listings.
- Standardized category information.
- Created helper columns:
  - Discount Percentage
  - Main Category
  - Sub Category
  - Price Bucket

---

# 6. Exploratory Data Analysis

The following analyses were performed:

- Dataset overview
- Missing value analysis
- Duplicate analysis
- Category distribution
- Brand distribution
- Retail price distribution
- Discount percentage distribution
- Price segmentation
- Category pricing comparison
- Category discount comparison
- Brand comparison
- Product rating analysis
- Scatter analysis between retail price and discounts

---

# 7. Dashboard Development

An interactive Power BI dashboard was developed to visualize:

- Total products
- Average retail price
- Average discount
- Total brands
- Unknown brand percentage
- Rating availability
- Total categories
- Category distribution
- Price distribution
- Brand analysis
- Discount comparison
- Retail price vs discount relationship

Interactive slicers allow filtering by:

- Main Category
- Brand
- Price Bucket

---

# 8. Key Business Findings

## Catalogue Composition

- Clothing represents approximately **31%** of all listings.
- The catalogue spans **251** main product categories.

---

## Pricing

- Average retail price is approximately **₹3,325**.
- Furniture has the highest average product price.

---

## Discounts

- Average discount equals **39.4%**.
- Discount percentages remain relatively consistent across categories.
- Budget products generally receive higher discounts than premium products.

---

## Product Distribution

- Nearly **47%** of products fall below ₹500.
- Premium-priced products represent a relatively small share of the catalogue.

---

## Brand Analysis

- Over **3,400** brands are represented.
- Approximately **29%** of products originally lacked brand information.

---

## Product Ratings

Only **10.2%** of products contain numerical ratings.

Therefore, customer satisfaction analysis remains limited.

---

# 9. Business Recommendations

Based on the findings, the following recommendations are proposed:

### Recommendation 1

Adopt category-specific pricing strategies instead of applying similar discounts across all product groups.

---

### Recommendation 2

Review products with unusually high discounts to identify possible MRP inflation.

---

### Recommendation 3

Improve catalogue completeness by reducing missing brand information.

---

### Recommendation 4

Encourage customers to submit ratings and reviews.

---

### Recommendation 5

Prioritize pricing optimization in high-value categories such as Furniture.

---

### Recommendation 6

Integrate sales and customer transaction data for more comprehensive business intelligence.

---

# 10. Project Limitations

Several limitations should be considered.

The dataset does not contain:

- Customer information
- Orders
- Sales revenue
- Profit
- Inventory
- Seller performance
- Time-series pricing

Therefore:

- Sales performance cannot be evaluated.
- Revenue cannot be calculated.
- Customer behaviour cannot be analysed.
- Market share cannot be estimated.

---

# 11. Skills Demonstrated

This project demonstrates practical knowledge of:

- Python
- Pandas
- NumPy
- Data Cleaning
- Data Validation
- Feature Engineering
- Exploratory Data Analysis
- Data Visualization
- Power BI
- DAX
- Business Intelligence
- Dashboard Design
- Business Storytelling
- Technical Documentation

---

# 12. Deliverables

The project includes:

- Raw Dataset
- Cleaned Dataset
- Jupyter Notebook
- Power BI Dashboard (.pbix)
- Dashboard PDF
- Business Requirement Document
- Data Cleaning Report
- EDA Report
- Business Insights Report
- Dashboard Documentation
- Executive Summary
- Final Project Report
- Data Dictionary
- README

---

# 13. Lessons Learned

This project reinforced several important analytics concepts:

- Business understanding should guide technical analysis.
- Data quality significantly impacts analytical reliability.
- Effective dashboards require a clear business narrative.
- Documentation is essential for reproducibility.
- Business recommendations should always acknowledge dataset limitations.

---

# 14. Future Improvements

If additional data becomes available, the project can be expanded to include:

- Revenue analysis
- Sales performance analysis
- Customer segmentation
- RFM analysis
- Market basket analysis
- Time-series pricing analysis
- Demand forecasting
- Dynamic pricing models
- Seller performance analytics
- Inventory optimization

---

# 15. Conclusion

This project demonstrates a complete end-to-end data analytics workflow, beginning with raw catalogue data and progressing through data preparation, exploratory analysis, dashboard development, and business reporting.

Although the absence of transactional data limits commercial performance analysis, the project provides valuable insights into catalogue composition, pricing behaviour, discount strategies, and data quality.

The project highlights the importance of combining technical analysis with business context to support informed decision-making and serves as a strong foundation for more advanced e-commerce analytics projects.