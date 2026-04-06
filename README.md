## Dataset Description

This project uses a synthetic retail transactions dataset containing 500 records generated programmatically with NumPy and pandas. The data represents customer purchase activity across five product categories — Electronics, Clothing, Groceries, Beauty, and Sports — spanning the full year 2022. Each transaction records a unique Transaction ID, the date of sale, a Customer ID, the customer's gender and age, the product category, quantity purchased, unit price, and the total sale value. The dataset was intentionally seeded with real-world data quality issues including inconsistent date formats, missing values in Gender, Age, and Quantity columns, age outliers (implausible values such as 5, 120, and 150), and deliberate mismatches between Total_Amount and the product of Quantity × Price_Per_Unit.


**What Was Done**

1. **Task 1 — Python Basics & Logic:** Loaded the dataset, wrote a `classify_sale()` function to categorise each transaction as High, Medium, or Low based on Total_Amount, performed a manual dictionary-based count of each class, and detected 7 rows where Total_Amount did not match the expected calculation.

2. **Task 2 — Data Cleaning:** Produced a full missing-value audit, imputed Gender nulls with 'Unknown', Age and Quantity nulls with their respective medians, standardised all date formats to YYYY-MM-DD using `pd.to_datetime()`, and replaced four implausible age outliers (outside the 18–80 range) with the valid-age median.

3. **Task 3 — EDA & Visualization:** Created four charts: a bar chart of total revenue by category (Groceries and Beauty lead), a histogram of customer age distribution, a scatter plot of Age vs Total_Amount (showing near-zero correlation of r ≈ 0.01), and a stacked proportional bar chart showing Sale Class composition within each product category.

4. **Task 4 — Interpretation:** Summarised the dataset in plain language, identified three key findings (category revenue rankings, lack of age-spend correlation, and the impact of 30% missing gender data), and recommended prioritising Groceries and Beauty in inventory and promotion strategy.


s from top to bottom. The dataset is generated in the first code cell — no external file download is needed.
4. Required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn` (all available in standard Anaconda/pip environments).
