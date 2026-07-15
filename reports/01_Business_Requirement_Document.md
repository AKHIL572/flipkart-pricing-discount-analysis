# Business Requirement Document (BRD)

# Flipkart Product Pricing & Discount Analysis

---

# 1. Project Information

| Item | Details |
|------|----------|
| Project Name | Flipkart Product Pricing & Discount Analysis |
| Project Type | Data Analytics |
| Domain | E-Commerce |
| Status | Completed |
| Analyst | Akhil T V |
| Tools Used | Python, Pandas, NumPy, Matplotlib, Seaborn, Power BI |
| Dataset | Flipkart Product Catalogue Dataset (2015–2016) |

---

# 2. Business Background

Flipkart is one of India's largest e-commerce platforms, offering products across hundreds of categories and thousands of brands. As the product catalogue grows, maintaining consistent pricing strategies, competitive discounts, and accurate catalogue information becomes increasingly challenging.

Pricing decisions directly influence customer purchasing behavior, product competitiveness, and overall business performance. Understanding how prices and discounts vary across categories and brands can help business teams optimize catalogue strategy and improve customer experience.

This project analyzes Flipkart's publicly available product catalogue (2015–2016) to identify pricing patterns, discount strategies, category distribution, and catalogue quality issues using Python and Power BI.

---

# 3. Business Problem

The Pricing and Category Management teams lack a consolidated view of how products are distributed across categories, brands, price ranges, and discount levels.

Without these insights, business teams may struggle to:

- identify categories receiving excessive discounts,
- understand pricing variations across product categories,
- evaluate catalogue distribution across price segments,
- identify data quality issues affecting analysis,
- support pricing decisions with data-driven evidence.

The objective of this project is to transform raw catalogue data into meaningful business insights that support pricing optimization and catalogue management.

---

# 4. Business Objectives

The primary objectives of this project are to:

- Analyze the overall product catalogue structure.
- Understand pricing distribution across product categories.
- Measure discount patterns across categories and price segments.
- Identify the most represented brands and categories.
- Evaluate catalogue data quality.
- Develop an interactive dashboard for business users.
- Provide actionable business recommendations based on analytical findings.

---

# 5. Stakeholders

This analysis is designed to support the following stakeholders:

| Stakeholder | Business Need |
|-------------|---------------|
| Pricing Manager | Understand pricing and discount strategies across categories. |
| Category Manager | Monitor product distribution and category performance. |
| Marketing Team | Identify categories with promotional opportunities. |
| Business Intelligence Team | Build reporting and monitor catalogue health. |
| Senior Management | Obtain a high-level overview of catalogue composition and pricing trends. |

---

# 6. User Stories

### User Story 1
As a Pricing Manager, I want to identify categories offering the highest discounts so that pricing strategies can be reviewed and optimized.

### User Story 2
As a Category Manager, I want to understand how products are distributed across categories so that inventory and assortment planning can be improved.

### User Story 3
As a Marketing Manager, I want to compare discounts across price segments so that promotional campaigns can be targeted effectively.

### User Story 4
As a Business Intelligence Analyst, I want to identify data quality issues such as missing brand information and missing product ratings so that reporting reliability can be improved.

### User Story 5
As Senior Management, I want a single interactive dashboard summarizing catalogue performance for faster business decision-making.

---

# 7. Project Scope

## In Scope

- Product catalogue analysis
- Pricing analysis
- Discount analysis
- Category analysis
- Brand analysis
- Price segmentation
- Product rating availability analysis
- Data quality assessment
- Dashboard development
- Business recommendations

## Out of Scope

This project does **not** include:

- Sales analysis
- Revenue analysis
- Customer behaviour analysis
- Order history analysis
- Profitability analysis
- Inventory analysis
- Time-series analysis
- Demand forecasting
- Predictive modelling

These analyses require transactional business data that is not available in the provided dataset.

---

# 8. Assumptions

The following assumptions were made during the analysis:

- Retail prices represent the original listed prices.
- Discounted prices represent the selling prices displayed on the platform.
- Products with different prices are treated as separate catalogue listings.
- Missing brand information is considered unavailable rather than incorrect.
- Product ratings marked as "No rating available" indicate the absence of customer ratings.
- The dataset accurately represents Flipkart's catalogue during the 2015–2016 period.

---

# 9. Constraints

The analysis is subject to the following limitations:

- The dataset contains catalogue information only.
- Sales and revenue information are unavailable.
- Customer demographics are unavailable.
- Order-level transactions are unavailable.
- Profit margins cannot be calculated.
- Inventory information is unavailable.
- Approximately 29% of products have missing brand information.
- Approximately 90% of products do not contain usable product ratings.
- The dataset represents a historical snapshot (2015–2016) and does not reflect current catalogue conditions.

---

# 10. Success Metrics

The project will be considered successful if it can:

- Successfully clean and prepare the raw dataset.
- Generate meaningful pricing and discount insights.
- Identify major product categories and brands.
- Highlight catalogue data quality issues.
- Produce an interactive Power BI dashboard.
- Deliver business recommendations supported by data.
- Present findings in a clear and professional format.

---

# 11. Expected Business Outcomes

The expected outcomes of this analysis include:

- Improved visibility into product pricing across categories.
- Better understanding of discount strategies.
- Identification of catalogue distribution across price ranges.
- Increased awareness of catalogue data quality issues.
- Support for data-driven pricing and category management decisions.
- A reusable dashboard for exploratory catalogue analysis.

---

# 12. Deliverables

The project delivers the following outputs:

- Cleaned dataset
- Python data analysis notebook
- Exploratory Data Analysis (EDA)
- Engineered analytical features
- Power BI dashboard
- Business insights and recommendations
- Project documentation
- GitHub repository