Superstore Sales Analysis

Tools used: SQL (MySQL), Excel, Tableau

Overview

This project analyzes four years of sales data (2014–2018) from a fictional retail superstore, using SQL for data cleaning and analysis and Tableau to build an interactive dashboard.

Data Cleaning

The raw CSV failed to import into MySQL due to a non-ASCII character (a dagger symbol, †) embedded in one product name, MySQL's import process rejected the entire file because of it. I traced the issue to the specific byte causing the error, replaced it with a plain hyphen, and validated the full file before successfully re-importing all 9,994 rows.

SQL Analysis

Using MySQL, I wrote queries to find: revenue and profit by region, the top 10 products by sales, monthly sales trends, and the least profitable product sub-categories.

Dashboard

These findings were built into a four panel interactive Tableau dashboard, combining regional sales, top products, monthly trends, and sub-category profitability into one visual view.

Key Findings
-West led all regions in both sales ($725K) and profit ($108K).
-Central had higher sales than South but lower profit — a sign of inefficiency, likely from discounting.
-Tables and Bookcases were the only sub-categories losing money, with Tables alone down nearly $18,000.
-Sales consistently spike in November and December each year.
-The Canon imageCLASS 2200 Copier was the single highest-revenue product despite low unit volume.
