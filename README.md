Project Title:
Exploratory Data Analysis of Customer Transaction Data

Objective

This notebook implements a comprehensive exploratory data analysis (EDA) pipeline to extract actionable insights from a customer transaction dataset. The primary objectives are to understand data distributions, identify patterns and trends, detect outliers, and generate visual summaries to support data-driven decision-making.

Methodology

The analysis is executed in seven sequential phases:

1. Data Loading and Inspection
Loads the dataset from an Excel file (Dataset for Data Analytics.xlsx, sheet Sheet1) using pandas.

Displays initial dataset overview including shape, first 5 rows, column data types, and missing value counts.

Establishes a foundation for subsequent analysis by verifying data integrity.

2. Basic Statistical Analysis
Computes key descriptive statistics for numerical columns (Quantity, UnitPrice, TotalPrice):

Count, mean, median, minimum, maximum, and standard deviation

Generates a comprehensive statistical summary using df.describe().

Key Finding: The median order value (624)is substantially lower than the mean( 1,178), indicating a right-skewed distribution.

3. Categorical Variable Analysis
Analyzes the following categorical dimensions:

Product Distribution: Identifies top 5 products by order count (Printer, Tablet, Chair, Laptop, Desk)

Order Status: Calculates distribution across Cancelled, Returned, Pending, Shipped, and Delivered statuses

Payment Methods: Evaluates usage frequency of Online, Cash, Credit Card, Debit Card, and Gift Card

Referral Sources: Assesses customer acquisition channels (Instagram, Email, Google, Facebook, Referral)

Coupon Usage: Quantifies percentage of orders utilizing promotional codes (74.2%)

Key Finding: Approximately 41.4% of orders are either cancelled or returned, suggesting potential quality or delivery issues requiring investigation.

4. Trend and Pattern Analysis
Performs temporal and product-based trend analysis:

Temporal Trends:

Total sales aggregated by year (2023–2025)

Average monthly sales computed to identify seasonal patterns

Product Performance:

Total revenue by product category

Average order value by product category

Key Findings:

Chairs generate the highest total revenue ($195,620.11)

Laptops have the highest average order value ($1,110.56)

5. Outlier Detection
Implements the Interquartile Range (IQR) Method to identify statistical outliers:

Calculates Q1 (25th percentile), Q3 (75th percentile), and IQR

Defines outlier boundaries as Q1 - 1.5×IQR and Q3 + 1.5×IQR

Results:

Quantity and UnitPrice: 0 outliers detected

TotalPrice: 8 outliers (0.7% of data), with maximum value of $3,456.40

6. Data Visualization
Generates a comprehensive suite of visualizations using matplotlib and seaborn:

Visualization Type	Purpose
Histogram (Total Price)	Examine distribution shape and skewness
Boxplot (Price by Product)	Compare price distributions across product categories
Bar Chart (Order Status)	Visualize order fulfillment rates
Line Chart (Monthly Sales)	Identify seasonal sales patterns
Bar Chart (Top 5 Products by Revenue)	Highlight top revenue-generating products
Pie Chart (Payment Methods)	Show payment method market share
Boxplot (Outlier View)	Emphasize extreme value detection
Bar Chart (Referral Source Effectiveness)	Compare average order value by acquisition channel
7. Summary of Key Observations
Consolidates findings into a structured executive summary covering:

Dataset overview and scope

Basic statistical insights

Order status analysis with actionable recommendations

Product performance rankings

Outlier characterization

Temporal and channel-specific trends
