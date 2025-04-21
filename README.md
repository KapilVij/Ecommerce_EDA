# E-Commerce Data Analysis

This project analyzes the **complete lifecycle of over 100,000 e-commerce orders**, covering everything from **purchase and payment** to **delivery and customer reviews**. The aim is to extract actionable insights into customer behavior, product performance, logistics, and overall marketplace efficiency.

---

## Goal and Process

The objective of this analysis is to **identify key business patterns** within a real-world e-commerce environment using a comprehensive dataset. Insights are drawn to support smarter decision-making in areas like logistics, marketing, and customer experience.

**Data preparation** steps included:
- Merging multiple CSV files into relevant dataframes
- Parsing and formatting datetime columns
- Handling null or missing values
- Engineering time-based and location-based features

The project utilizes 9 datasets including:
- Orders, customers, and sellers information  
- Product metadata and category translations  
- Payment and review records  
- Geolocation details

**Libraries Used**
- pandas – For data loading, cleaning, merging, and manipulation.
- numpy – For numerical operations and array handling.
- matplotlib.pyplot – For creating basic visualizations and custom plots.
- seaborn – For statistical and aesthetically appealing plots like countplots and boxplots.
- scikit-learn – For building and evaluating the Random Forest regression model.

---

## Approach

Instead of creating a single, large merged dataset, this project follows a **modular, question-driven approach**. Specific combinations of datasets were merged as needed to analyze distinct business areas. This strategy mirrors real-world scenarios where:
- Analysts must selectively join datasets to preserve clarity  
- Inconsistencies across data sources require careful management  
- Multiple perspectives (e.g., customer, seller, product) must be evaluated independently

This method enabled flexible and meaningful exploration of trends at various levels of granularity.

---

## Key Analysis Areas

This project spans several core dimensions of the e-commerce pipeline:

### 1. Order Processing and Fulfillment
- Assessed order lifecycle times: approval, shipping, and delivery  
- Compared timely vs. delayed deliveries  
- Identified delays and bottlenecks in logistics

### 2. Payment Analysis
- Visualized distribution of payment types  
- Found credit cards dominate (73% of transactions)  
- Explored payment methods by order value

### 3. Geographic Insights
- Ranked top states and cities by order volume and revenue  
- Identified geographic patterns in consumer behavior  
- Inferred potential regions for marketing or logistic investment

### 4. Customer Satisfaction
- Analyzed review scores and feedback trends  
- Linked delivery delays with poor review scores  
- Flagged product categories with low satisfaction rates

### 5. Product Category Performance
- Ranked categories by order count and sales volume  
- Compared shipping cost vs. product price  
- Examined trends in category popularity over time

### 6. Shipping and Logistics
- Measured average delivery speeds across categories  
- Highlighted categories with frequent delays  
- Inferred opportunities for shipping process improvements

### 7. Seller Distribution and Performance
- Investigated seller distribution across categories  
- Evaluated fulfillment times and delivery efficiency by seller  
- Identified categories with high seller saturation

### 8. Data Merging Strategy
- Created modular data views (e.g., customer-payment-order, order-product-seller)  
- Avoided flattening the data unnecessarily to retain scalability and focus

---
# Hypothesis Testing 

- **Goal**: To determine if late deliveries are associated with poor customer reviews.
- **Hypothesis:**
    - **Null Hypothesis (Ho)**: Late delivery does not increase poor reviews.
    - **Alternative Hypothesis (H1)**: Late delivery increases poor reviews.

## Z-Test Results
- **Z-statistic**: 92.30  
- **P-value**: ~0.0000

### Interpretation
- **Evidence**: The low p-value and high Z-score strongly indicate a link between late deliveries and poor reviews.
- **Business Insight**: Improving on-time delivery can significantly boost customer satisfaction.

---

## Basic - Shipping Cost Prediction Model

A **Random Forest Regressor** was developed to predict shipping costs based on product features and geographic variables.

### Model Overview
- **R² Score:** 0.69 — explains ~69% of variance in shipping cost  
- **RMSE:** ~$9.09 — average prediction error

### Top Predictive Features
- **Product Volume & Weight** — strongest predictors  
- **Same-State Shipping** — reduces cost  
- **Product Price & Density** — minor contributors  
- **Large Item Flag** — accounts for special handling

### Insights
- Physical dimensions are key drivers of shipping cost  
- Geographic proximity significantly impacts expenses  
- Useful for optimizing logistics, pricing, and delivery strategy

---

## Final Thoughts

Throughout the analysis, emphasis was placed on:
- Clean and modular data preparation  
- Intuitive and insightful visualizations (bar charts, pie charts, time series, etc.)  
- Clear storytelling through data-backed trends and patterns

The result is a comprehensive, business-focused view of how data can power better decisions in a competitive e-commerce landscape.
