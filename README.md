# RetailPulse — Retail Sales & Data Quality Analysis

RetailPulse is a retail sales analytics project focused on understanding sales performance while improving the quality and reliability of the underlying data.

The dataset contains retail orders from **January to June 2026**. The project follows a practical analytics workflow:

**Raw Data → Data Quality Checks → Data Cleaning → Validation → Exploratory Analysis → Business Insights**

## Business Objective

The goal of this project is to:

* Clean and validate raw retail transaction data
* Analyze revenue across products, categories, and cities
* Compare weekday and weekend purchasing behavior
* Analyze payment methods and average order value
* Examine discount and quantity patterns
* Identify data-quality issues that could affect business decisions

## Key Business Questions

1. Which product categories generate the most revenue?
2. Which cities contribute the most to overall revenue?
3. How does purchasing behavior differ between weekdays and weekends?
4. Which payment methods are most commonly used?
5. Which payment methods have the highest average order value?
6. Is there an observable relationship between discounts and quantity purchased?
7. What data-quality issues need to be addressed before analysis?

## Dataset

The original dataset contains retail transaction-level information including:

* Order ID
* Order Date
* City
* Category
* Product Name
* Quantity
* Unit Price
* Discount
* Payment Method
* Customer Age
* Customer Rating

After cleaning, the dataset contains **1,800 records and 13 columns**.

## Data Cleaning

Several data-quality issues were identified and addressed:

* **25 duplicate records** were removed
* City names were standardized
* Missing quantities were imputed using the median
* Missing unit prices were imputed using product-level median prices
* Missing discounts were treated as 0%
* Missing payment methods were labelled as `Unknown`
* Missing customer ages were imputed using the median
* Missing customer ratings were retained because missing ratings can represent a meaningful absence of feedback
* Extreme unit-price values were investigated and four apparent data-entry errors were replaced using product-level median prices
* Four unrealistic quantity values of **999** were replaced using product-level median quantities

The cleaned dataset was validated before being used for analysis.

## Analysis

The exploratory analysis covers:

### Revenue Performance

* Total revenue
* Revenue by product category
* Revenue by city
* Top-performing products

### Customer & Purchasing Behavior

* Weekday vs weekend sales
* Average order value
* Payment method usage
* Customer rating availability

### Discount Analysis

* Distribution of discount levels
* Quantity sold across discount levels
* Relationship between discount percentage and quantity purchased

## Key Findings

* Total revenue was approximately **₹3.24 million**
* **Electronics** generated the highest category revenue at approximately **₹1.39 million**
* **Mumbai** generated the highest city revenue at approximately **₹741.5K**
* **Smart Watch** was the highest-revenue individual product at approximately **₹542.9K**
* Weekend orders had a higher average order value than weekday orders
* **UPI** was the most frequently used payment method
* The correlation between discount percentage and quantity purchased was approximately **0.003**, indicating almost no linear relationship in this dataset

## Tools Used

* **Python**

  * Pandas
  * NumPy
  * Matplotlib
* **Jupyter Notebook**
* **Git & GitHub**

## Project Structure

```text
retailpulse-retail-analytics/
│
├── README.md
├── requirements.txt
│
├── data/
│   └── retailpulse_orders_cleaned.csv
│
├── notebooks/
│   └── RetailPulse_Analysis.ipynb
│
├── reports/
│   ├── Data_Cleaning_Notes.pdf
│   └── Summary_of_Findings.pdf
│
└── visuals/
```

## Repository Contents

**RetailPulse_Analysis.ipynb**
Complete analysis workflow covering data quality checks, cleaning, validation, exploratory analysis, and visualizations.

**Data_Cleaning_Notes.pdf**
Detailed documentation of the data-quality issues identified and the decisions made during cleaning.

**Summary_of_Findings.pdf**
Summary of the major analytical findings and business observations.

**retailpulse_orders_cleaned.csv**
The cleaned dataset used for the final analysis.

## What This Project Demonstrates

This project demonstrates a practical approach to data analysis rather than focusing only on visualization.

Key skills demonstrated include:

* Data cleaning and validation
* Exploratory data analysis
* Data quality assessment
* Business-oriented analysis
* Aggregation and comparison of metrics
* Data visualization
* Documenting analytical decisions
* Reproducible analysis using Python and Jupyter

---

**Project:** RetailPulse
**Focus:** Retail Sales & Data Quality Analysis
**Tools:** Python, Pandas, NumPy, Matplotlib, Jupyter Notebook
