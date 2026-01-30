# Retail Customer Intelligence — Executive Summary

## Business Context
This project analyses three years of supermarket transaction data to understand how customers shop, what drives repeat visits, and how different customer groups contribute to overall revenue. The goal is to translate raw transaction records into clear, actionable customer insights that can support marketing, retention, and commercial planning decisions.

## Data Overview
The dataset represents daily transaction records from a national supermarket chain across three years. Each record includes customer identifiers (where available), transaction totals, items purchased, and department information.  
To ensure realistic business analysis, transactions were reviewed for missing identifiers, duplicate receipts, and non-customer records (such as system or supplier transactions), which were excluded from customer-level modelling.

## Analytical Approach
The analysis was structured as an end-to-end pipeline:
- Created a customer-level view from individual shopping trips
- Engineered spending, visit frequency, basket size, and department coverage metrics
- Grouped customers into practical segments based on recent activity, visit behaviour, and total value
- Identified natural customer groupings to validate and complement rule-based segments

## Key Insights
- A small group of high-value customer accounts for a disproportionate share of total revenue
- Regular customers show consistent visit patterns and broader department engagement
- Infrequent customers tend to have smaller baskets and lower long-term value, indicating strong potential for targeted re-engagement strategies

## Business Applications
This framework can be used to:
- Design targeted marketing campaigns by customer type
- Prioritise retention efforts on high-value segments
- Improve promotional planning based on shopping behaviour patterns
- Support store and category planning using department-level engagement trends

## Governance and Data Ethics
This repository does not contain raw or proprietary data. All data structures are represented using schema examples or synthetic samples to demonstrate methodology without exposing confidential or institutional datasets.
