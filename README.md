# oppy-github-retail-analytics-customer-intelligence
Customer insights project showing how retail transaction data can be turned into clear customer segments, spending patterns, and business-ready insights to support marketing, retention, and commercial decision-making.



Retail Customer Analytics — Supermarket Transactions (2013–2015)

Introduction

This project analyzes three years of supermarket transaction data to turn millions of daily sales records into clear, business-ready customer insights. The work focuses on understanding how customers shop, which groups drive the most value, how sales change across the year, and whether promotions meaningfully increase purchasing. The goal is to support practical decisions around marketing, retention, staffing, and sales planning.


Data
The dataset covers supermarket operations from 2013 to 2015, with each trading day stored as a separate file (public holidays excluded). After consolidation, the dataset contains approximately 37.4 million transaction lines and 14 columns describing each receipt-line item, including sale date, receipt number, customer ID, quantities, sales value, department, and promotion status.

Key scale indicators (2014):

Unique customers: ~10,650

Unique shopping trips: ~768,000

Departments: Grocery, dairy, fresh meat, fruit & vegetables, and more

To preserve accuracy, the full dataset was processed without downsampling. Item barcodes were treated as text to avoid misclassification of alphanumeric product codes.


Data Cleaning and Manipulation

The raw transaction data was transformed into a customer-centric structure suitable for analysis:

Regular customer filter: Focused on customers active in 2013, 2014, and 2015 to remove one-time or system-generated activity.

Missing IDs removed: Transactions without customer identifiers were excluded to ensure reliable customer-level metrics.

Trip construction: Individual receipt lines were grouped into complete shopping trips using a combined receipt number and date, creating one row per store visit.

Feature aggregation: Each trip was summarized into total spend, total items, and number of departments visited.

Outlier handling: Extreme spending cases (e.g., bulk or corporate purchases) were identified using the IQR method and removed to prevent skewed results.

This process reduced millions of raw records into a clean dataset of realistic, comparable customer profiles that reflect true shopping behavior.


Analysis Performed

The project applies a structured, end-to-end analytical pipeline:

Behavioral patterns: Trips analyzed by day of week, month, and quarter to identify peak demand and seasonal trends.

Customer profiling: Creation of customer-level metrics such as total spend, visit frequency, basket size, and shopping breadth.

RFM segmentation: Customers scored and grouped based on how recently they shopped, how often they visited, and how much they spent.

Unsupervised clustering: K-means clustering used to identify natural customer groups based on spend, basket size, and department variety.

Sales forecasting: Monthly sales modeled using historical drivers (trips, customers, items, basket size) to predict early 2016 performance.

Promotion impact testing: Statistical comparison of transactions with and without offers to measure changes in items purchased.


Findings

Key business insights include:

Customer value concentration: A smaller group of high-value customers drives a disproportionate share of total revenue.


Three clear segments:

Light Shoppers — low spend, infrequent visits, limited department range.

Steady Shoppers — the largest group, consistent and reliable contributors.

Premium Bulk Buyers — smaller in number but high spend and large baskets.

Seasonality: Sales and trips peak mid-year and in December, with noticeably lower activity toward the end of the year.

Promotions: Offers slightly increase items per transaction. The per-visit uplift is modest, but meaningful at scale across millions of transactions.


Conclusions

This analysis demonstrates how large-scale transaction data can be converted into practical, decision-ready insights. Loyal and high-value customers play a critical role in sustaining revenue, while a sizeable low-engagement group presents opportunities for reactivation. Seasonal sales patterns highlight when staffing, stock, and promotions should be adjusted, and promotional testing confirms that small behavioural changes can compound into significant business impact.

Overall, the project shows a complete analytics workflow — from raw data ingestion and cleaning to customer segmentation, forecasting, and business interpretation — designed to support real-world retail strategy and planning.

Governance

This repository does not contain raw or proprietary data. All examples use schema references or synthetic structures to demonstrate the analytical approach without exposing confidential datasets.
