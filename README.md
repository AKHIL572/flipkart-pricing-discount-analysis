# 🛒 Flipkart Product Pricing & Discount Analysis

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)
![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-EDA-black?logo=pandas)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

## 📌 Project Overview

This project analyzes Flipkart's product catalogue (2015–2016) to understand pricing strategies, discount patterns, category distribution, and catalogue quality.

The project follows an end-to-end data analytics workflow starting from raw data cleaning in Python, performing Exploratory Data Analysis (EDA), engineering analytical features, and finally building an interactive Power BI dashboard for business decision-making.

The objective is not simply to visualize the data but to answer practical business questions related to pricing optimization, product positioning, and catalogue quality.

---

# 🎯 Business Problem

Flipkart maintains a catalogue containing thousands of products spread across hundreds of categories and brands.

The business wants to understand:

- Which product categories dominate the catalogue?
- Which categories receive the highest discounts?
- How are products distributed across price segments?
- Do expensive products receive larger discounts?
- Which brands have the largest catalogue presence?
- How complete and reliable is the catalogue information?

Answering these questions helps improve pricing strategy, merchandising decisions, and catalogue standardization.

---

# 🎯 Project Objectives

- Clean and prepare raw Flipkart catalogue data
- Handle missing values and duplicate listings
- Engineer useful analytical features
- Perform Exploratory Data Analysis
- Discover pricing and discount patterns
- Evaluate catalogue quality
- Build an interactive Power BI dashboard
- Generate business insights and recommendations

---

# 📂 Dataset Information

**Dataset Name**

Flipkart Product Catalogue Dataset

**Source**

Public Flipkart catalogue dataset (2015–2016)

**Original Records**

20,000

**Final Cleaned Records**

15,827

**Features Used**

- Brand
- Product Name
- Product Category Tree
- Product Rating
- Retail Price
- Discounted Price

---

# 📁 Project Structure

```text
Flipkart_Product_Analysis/
│
├── data/
│   ├── flipkart_dataset.csv
│   └── cleaned_flipkart_dataset.csv
│
├── notebooks/
│   ├── 01_Data_Understanding_&_Cleaning.ipynb
│   ├── 02_Exploratory_Data_Analysis.ipynb
│   └── 03_Feature_Engineering.ipynb
│
├── dashboard/
│   ├── Flipkart_Dashboard.pbix
│   ├── Dashboard.pdf
│   └── Dashboard.png
│
├── reports/
│   ├── 01_Business_Requirement_Document.md
│   ├── 02_Data_Cleaning_Report.md
│   ├── 03_EDA_Report.md
│   ├── 04_Business_Insights_Report.md
│   ├── 05_Dashboard_Documentation.md
│   ├── 06_Executive_Summary.md
│   ├── 07_Final_Project_Report.md
│   └── 08_Data_Dictionary.md
│
├── README.md
├── requirements.txt
└── LICENSE
```

---

# ⚙️ Tools & Technologies

### Programming

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn

### BI Tool

- Power BI

### Other

- DAX
- Git
- GitHub

---

# 🧹 Data Cleaning Process

The raw dataset was cleaned through several preprocessing steps.

### Removed

- Exact duplicate records
- Rows with missing price information

### Missing Values

Brand

- Filled using **Unknown**

Product Rating

- Converted to numeric
- "No rating available" converted to NaN

### Feature Engineering

Created:

- Discount Percentage
- Main Category
- Sub Category
- Price Bucket

---

# 📊 Exploratory Data Analysis

EDA was performed to understand:

- Product distribution
- Category dominance
- Brand distribution
- Retail price distribution
- Discount distribution
- Rating availability
- Pricing vs discount relationship
- Price segmentation
- Brand diversity

Several statistical summaries and visualizations were created before dashboard development.

---

# 📈 Dashboard Features

The Power BI dashboard includes interactive filters and business-focused visualizations.

## KPI Cards

- Total Products
- Average Discount (%)
- Average Retail Price
- Total Identified Brands

## Filters

- Main Category
- Price Bucket
- Brand

## Visualizations

- Top Categories by Product Listings
- Average Price by Category
- Product Distribution by Price Range
- Top Brands by Listings
- Average Discount by Category
- Average Discount by Price Range
- Price vs Discount Relationship (Scatter Plot)

## Data Quality Section

- Unknown Brand %
- Products with Rating %
- Total Categories

## Business Insight Cards

- Category competition
- Mass-market pricing
- Discount concentration
- Missing brand information
- Rating data limitation

---

# 📊 Key Findings

- Cleaned catalogue contains **15,827 products**
- Average discount is **39.41%**
- Clothing is the largest product category
- Nearly half of the products are priced below ₹500
- Furniture has the highest average retail price
- Around **29%** of products have missing brand information
- Only around **10%** of products contain rating data
- Discount percentages remain relatively consistent across categories

---

# 💼 Business Recommendations

- Improve catalogue quality by enriching missing brand information.
- Standardize product metadata across categories.
- Investigate categories offering unusually high discounts.
- Use category-level pricing strategies rather than uniform discounting.
- Collect additional customer behaviour data (orders, sales, reviews) for more advanced analytics.

---

# 📌 Business Value

This project demonstrates how descriptive analytics can support:

- Pricing optimization
- Product positioning
- Catalogue quality assessment
- Category performance analysis
- Business decision making

---

# 📸 Dashboard Preview

> *(Insert dashboard screenshot here)*

Example:

```
dashboard/Dashboard.png
```

---

# 🚀 Future Improvements

Potential extensions include:

- Sales analysis
- Customer segmentation
- Inventory optimization
- Time-series pricing trends
- Predictive pricing models
- Interactive Tableau dashboard
- Streamlit deployment
- SQL integration

---

# 🎓 Skills Demonstrated

- Data Cleaning
- Data Wrangling
- Exploratory Data Analysis
- Feature Engineering
- Data Visualization
- Dashboard Design
- Business Analytics
- DAX
- Power BI
- Python Programming
- GitHub Project Documentation

---

# 👨‍💻 Author

**Akhil T V**

Aspiring Data Analyst | Python | SQL | Power BI | Tableau | Machine Learning

GitHub : https://github.com/AKHIL572

LinkedIn : https://www.linkedin.com/in/akhil-t-v/

---

# ⭐ If you found this project useful, consider giving this repository a Star.