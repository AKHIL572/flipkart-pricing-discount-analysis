# Exploratory Data Analysis (EDA) Report

## Project
Flipkart Product Pricing & Discount Analysis

---

# 1. Purpose of EDA

Exploratory Data Analysis (EDA) was conducted to understand the structure of the cleaned Flipkart catalogue, identify pricing patterns, evaluate discount strategies, analyze category distributions, and uncover relationships between variables before building the Power BI dashboard.

The analysis focused on answering business-oriented questions rather than only producing visualizations.

---

# 2. Dataset Used

| Metric | Value |
|---------|-------|
| Records | 15,827 |
| Features | 10 |
| Main Categories | 251 |
| Unique Products | 12,626 |
| Brands (Including Unknown) | 3,486 |

---

# 3. Dataset Summary Statistics

| Metric | Retail Price | Discounted Price | Discount (%) |
|---------|-------------:|-----------------:|-------------:|
| Mean | ₹3,324.56 | ₹2,257.69 | 39.41% |
| Median | ₹1,000 | ₹550 | 43.48% |
| Minimum | ₹35 | ₹35 | 0% |
| Maximum | ₹5,71,230 | ₹5,71,230 | 96.53% |

---

# 4. Univariate Analysis

## 4.1 Product Category Distribution

### Objective

Identify which product categories dominate the Flipkart catalogue.

### Visualization

Top 10 Product Categories by Number of Listings

### Key Findings

- Clothing contains the largest number of product listings.
- Jewellery is the second-largest category.
- Automotive and Footwear also contribute significantly.
- The catalogue is highly concentrated in a few major categories.

### Business Interpretation

A high concentration of products in Clothing indicates intense competition. Sellers are likely competing primarily through pricing and promotional discounts.

### Recommendation

High-volume categories should receive more granular analysis at the sub-category level to identify niche opportunities.

---

## 4.2 Retail Price Distribution

### Objective

Understand the pricing structure of the catalogue.

### Visualizations

- Retail Price Distribution (Linear Scale)
- Retail Price Distribution (Log Scale)

### Key Findings

- The distribution is highly right-skewed.
- Most products are priced below ₹2,000.
- A small number of premium products extend up to ₹5.71 lakh.

### Business Interpretation

Flipkart primarily serves the affordable consumer market while maintaining a small premium product segment.

### Recommendation

Log-scale visualization should always be preferred for highly skewed pricing data.

---

## 4.3 Discount Percentage Distribution

### Objective

Understand how discounts are distributed across the catalogue.

### Visualization

Distribution of Discount Percentage

### Key Findings

- Average discount: 39.41%
- Median discount: 43.48%
- Most discounts fall between 20% and 60%.

### Business Interpretation

The marketplace relies heavily on discount-driven pricing.

Very few products are sold without discounts.

### Recommendation

Products consistently discounted above 70% should be investigated for potential inflated MRP pricing.

---

# 5. Bivariate Analysis

## 5.1 Average Retail Price by Main Category

### Objective

Identify expensive product categories.

### Visualization

Average Retail Price by Main Category

### Key Findings

Furniture records the highest average retail price.

Automation & Robotics follows closely.

### Business Interpretation

Although Furniture has relatively few listings, each product represents a high-value transaction opportunity.

### Recommendation

Pricing optimization should prioritize high-value categories rather than only high-volume categories.

---

## 5.2 Retail Price vs Discount Percentage

### Objective

Determine whether expensive products receive larger discounts.

### Visualization

Scatter Plot (Retail Price vs Discount Percentage)

(Logarithmic X-axis)

### Key Findings

- Discount percentages remain widely distributed across all price ranges.
- No strong linear relationship exists.
- Both premium and budget products receive substantial discounts.

### Business Interpretation

Flipkart's promotional strategy appears category-specific or seller-specific rather than purely price-based.

### Recommendation

Future analysis should include seller information to understand discount behaviour more accurately.

---

## 5.3 Average Discount Percentage by Category

### Objective

Compare discount behaviour across product categories.

### Visualization

Average Discount (%) by Main Category

### Key Findings

Average discounts remain relatively similar across categories, with only minor variations.

### Business Interpretation

The platform follows a broadly consistent promotional strategy instead of aggressively discounting only specific categories.

### Recommendation

Future studies should evaluate seasonal promotional campaigns to determine whether category discounts change over time.

---

## 5.4 Product Distribution by Price Bucket

### Objective

Segment products by selling price.

### Visualization

Product Count by Price Bucket

### Key Findings

| Price Bucket | Observation |
|--------------|-------------|
| <₹500 | Largest share of catalogue |
| ₹500–1K | Second largest |
| ₹1K–2K | Moderate representation |
| ₹2K–5K | Smaller segment |
| ₹5K+ | Premium niche |

### Business Interpretation

Nearly half of the catalogue targets budget-conscious consumers.

### Recommendation

Future revenue analysis should incorporate sales volume, as catalogue size alone does not indicate revenue contribution.

---

## 5.5 Top Brands by Listings

### Objective

Identify brands with the largest catalogue presence.

### Visualization

Top Brands by Product Listings

### Key Findings

Allure Auto has the highest number of listings among identified brands.

### Business Interpretation

A larger catalogue does not necessarily imply higher sales or stronger market performance.

### Recommendation

Brand comparisons should be combined with transaction or sales data before making strategic decisions.

---

# 6. Multivariate Analysis

## Category × Pricing × Discounts

The combined analysis reveals three important marketplace characteristics.

### Observation 1

Clothing dominates catalogue volume.

### Observation 2

Furniture dominates average product value.

### Observation 3

Discount levels remain broadly consistent across categories.

### Overall Interpretation

Flipkart appears to balance pricing and discount strategies across its catalogue rather than heavily favouring individual categories.

---

# 7. Rating Analysis

## Important Limitation

Only **1,620 products (10.2%)** contain valid numerical ratings.

Approximately **90%** of the catalogue lacks rating information.

### Visualizations

- Rating Distribution
- Rating vs Retail Price

### Findings

Most available ratings cluster between 3.5 and 4.5.

No meaningful relationship is observed between rating and retail price.

### Business Interpretation

The limited rating coverage prevents reliable conclusions regarding customer satisfaction.

### Recommendation

Rating-based analyses should not be generalized to the entire catalogue.

---

# 8. Statistical Observations

### Pricing

- Strong positive skew
- Mean significantly higher than median
- Presence of premium outliers

---

### Discounts

- Average discount: 39.41%
- Median: 43.48%
- Moderate variability

---

### Categories

- Highly imbalanced distribution
- Few categories dominate listings

---

### Ratings

- Extremely sparse
- Unsuitable for predictive analysis without additional data

---

# 9. Key Business Insights

## Insight 1

Clothing represents the largest product category, indicating intense marketplace competition.

---

## Insight 2

Furniture products have the highest average prices, suggesting greater revenue potential per transaction.

---

## Insight 3

Approximately 47% of listed products are priced below ₹500, demonstrating a strong focus on value-oriented consumers.

---

## Insight 4

The average catalogue discount is 39.41%, reflecting discount-driven pricing across the marketplace.

---

## Insight 5

Nearly 29% of products originally lacked brand information, reducing the reliability of brand-level analysis.

---

## Insight 6

Only about 10% of products contain ratings, making customer sentiment analysis statistically unreliable.

---

# 10. Risks & Limitations

The conclusions in this report should be interpreted with the following limitations in mind.

- The dataset represents product listings rather than sales transactions.
- Revenue cannot be estimated without quantity sold.
- Seller information is unavailable.
- Time-series analysis is not possible because crawl timestamps were excluded.
- Customer behaviour cannot be inferred without order-level data.
- Rating coverage is insufficient for robust satisfaction analysis.

---

# 11. Conclusion

The exploratory analysis demonstrates that Flipkart's catalogue is heavily concentrated in affordable products, with Clothing dominating listing volume and Furniture representing the highest-value category.

The marketplace follows a broadly consistent discount strategy across categories, while data quality limitations—particularly missing brand information and sparse ratings—restrict deeper behavioural analysis.

These findings provide the analytical foundation for the Power BI dashboard and the business recommendations presented in subsequent reports.