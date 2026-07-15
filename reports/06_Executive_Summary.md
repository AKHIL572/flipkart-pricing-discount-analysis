# Executive Summary

## Project

**Flipkart Product Pricing & Discount Analysis**

---

# Project Background

Flipkart maintains a large product catalogue consisting of thousands of products across multiple categories and brands. Understanding how products are priced, discounted, and distributed across categories can help pricing teams optimize promotional strategies and improve catalogue management.

This project analyzes Flipkart's publicly available product catalogue (2015–2016) to identify pricing trends, discount patterns, category distribution, and data quality issues using Python and Power BI.

---

# Business Objective

The primary objective of this project was to analyze the product catalogue to answer the following business questions:

- Which categories dominate the marketplace?
- Which categories contain the highest-priced products?
- How are products distributed across different price ranges?
- How consistently are discounts applied across categories?
- Which brands have the greatest catalogue presence?
- What data quality issues may impact business reporting?

---

# Dataset Overview

| Attribute | Value |
|------------|-------|
| Source | Flipkart Product Catalogue |
| Original Records | 20,000 |
| Records After Cleaning | 15,827 |
| Main Categories | 251 |
| Identified Brands | 3,486 (including Unknown) |
| Analysis Tools | Python & Power BI |

---

# Project Approach

The project followed a structured analytics workflow:

1. Business Problem Definition
2. Data Understanding
3. Data Cleaning
4. Feature Engineering
5. Exploratory Data Analysis (EDA)
6. Business Insight Generation
7. Interactive Dashboard Development
8. Business Recommendations
9. Project Documentation

---

# Key Findings

### Catalogue Composition

- Clothing accounts for approximately **31%** of all product listings, making it the largest category.
- The catalogue primarily targets budget-conscious customers, with nearly **47%** of products priced below ₹500.

---

### Pricing Strategy

- The average retail price is approximately **₹3,325**.
- Furniture has the highest average retail price, representing the premium segment of the catalogue.

---

### Discount Strategy

- The average product discount is **39.4%**.
- Discount levels remain relatively consistent across major categories, suggesting a standardized promotional strategy.
- Lower-priced products generally receive higher percentage discounts than premium products.

---

### Brand Analysis

- Over **3,400** brands are represented in the catalogue.
- Approximately **29%** of products originally lacked brand information, limiting brand-level analysis.

---

### Customer Feedback

Only **10.2%** of products contain numerical ratings, making customer satisfaction analysis unreliable for this dataset.

---

# Business Recommendations

Based on the analysis, the following recommendations are proposed:

- Develop category-specific pricing strategies rather than relying on uniform discount levels.
- Review products with unusually high discounts to identify possible MRP inflation.
- Improve catalogue quality by reducing missing brand information.
- Encourage customer reviews to strengthen future analytical capabilities.
- Prioritize pricing optimization in high-value categories such as Furniture while maintaining competitiveness in high-volume categories like Clothing.

---

# Business Limitations

The analysis is limited to product catalogue data.

The dataset does **not** include:

- Sales transactions
- Revenue
- Profit
- Customer purchases
- Inventory
- Seller performance

Therefore, the project focuses on catalogue analysis rather than business performance analysis.

---

# Project Deliverables

The completed project includes:

- Data Cleaning using Python
- Exploratory Data Analysis
- Feature Engineering
- Interactive Power BI Dashboard
- Business Insights Report
- Executive Summary
- Technical Documentation
- GitHub Repository

---

# Skills Demonstrated

This project demonstrates practical skills in:

- Data Cleaning
- Data Validation
- Exploratory Data Analysis
- Feature Engineering
- Business Intelligence
- Data Visualization
- Power BI Dashboard Development
- DAX
- Business Storytelling
- Technical Documentation
- Business Recommendation Development

---

# Project Outcome

The project successfully transformed a raw product catalogue into an interactive analytical solution that provides actionable insights into pricing behavior, discount strategies, and catalogue composition.

The resulting dashboard and supporting reports enable business users to explore pricing trends, identify catalogue patterns, and understand the limitations of the available data before making strategic decisions.

---

# Executive Conclusion

This project demonstrates a complete end-to-end data analytics workflow, beginning with raw data preparation and concluding with business-focused insights and an interactive Power BI dashboard.

While the absence of transactional sales data limits commercial performance analysis, the project provides a strong foundation for catalogue analytics and illustrates how structured data analysis can support pricing strategy, catalogue management, and informed business decision-making.