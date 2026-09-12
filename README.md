# E-Commerce Revenue Analytics — VirtuBox Data Analyst Assessment

## Project Overview
This project was completed as part of the Data Analyst Assessment for VirtuBox Infotech Private Limited. The objective was to analyze online retail transaction data, identify business trends and performance gaps, and provide actionable, data-driven recommendations to management.

## Dataset
- **Name:** Online Retail II
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
- **Size:** 1,067,371 raw transaction records (Dec 2009 – Dec 2011)

## Tools Used
Python (Pandas, NumPy), Jupyter Notebook, Google Sheets, Google Looker Studio, Microsoft PowerPoint

## Methodology

### Data Cleaning
- Combined both yearly datasets into one dataframe
- Removed rows with missing Customer ID (243,007 rows)
- Removed duplicate transactions (26,479 rows)
- Removed zero-price entries (70 rows)
- Flagged (not removed) cancelled orders and quantity outliers (IQR method)
- Created `Revenue` (Quantity × Price), `Year`, `Month`, and `YearMonth` fields
- **Final dataset:** 797,815 clean rows

### Key Insights
- United Kingdom generates **91%+** of total revenue (£13.48M)
- Top 20% of customers generate **77.38%** of total revenue (Pareto pattern)
- Revenue consistently peaks **September–November** each year
- Overall cancellation rate: **2.31%**

### Dashboard
An interactive Google Looker Studio dashboard was built with KPI cards, revenue trends, and country/product breakdowns for management reporting.
🔗 [View Dashboard](https://datastudio.google.com/reporting/2fe020e5-2833-4075-9fb0-bfa3d8ed9284)

## Files in This Repository
- `VirtuBox_DataAnalyst_Cleaning.ipynb` — Python data cleaning & analysis code
- `Revenue_Drivers_Presentation.pptx` — Management presentation

## Note
The full processed dataset (797,815 rows) is used for all analysis in Python. Due to Google Sheets' import limits, the Looker Studio dashboard uses a representative 10,000-row sample for visualization only.
