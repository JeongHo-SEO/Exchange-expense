# Exchange Student Expense Analysis (Grenoble, France)

This repository provides a detailed analysis of expenses incurred during an exchange semester in **Grenoble, France** from August 22, 2025, to January 31, 2026.  
The project is designed to offer a practical budget reference for students planning their own exchange programs, particularly those coming from South Korea.

## 1. Dataset Introduction

The core dataset, `exchange_expenses_dataset.csv`, originated from a **Notion database** that I meticulously maintained throughout my stay.

- **Purpose**: I am sharing this data to help future exchange students estimate their potential costs for living and traveling in Europe.
- **Privacy**: All personal identification and sensitive details (such as specific transaction descriptions and payer name - me) have been removed to ensure privacy.
- **Data Source**: The original ledger was exported from Notion and converted into a CSV format for processing.

## 2. Data Preprocessing

The raw data from Notion required significant cleaning to be useful for analysis. The workflow is documented in `1. preprocessing.ipynb`:

- **Data Cleaning**: Removed unnecessary columns and handled missing values.
- **Date Standardization**: Used Regular Expressions (Regex) to parse inconsistent date formats and split date ranges into individual `Start Date` and `End Date` columns.
- **Currency Conversion (KRW)**:
  - The original transactions were recorded in various currencies: **EUR, USD, GBP, CHF, and TRY**.
  - I used the `yfinance` library to fetch historical exchange rates for each specific transaction date.
  - All amounts were unified into **Korean Won (KRW)** to provide a clear understanding of the total financial impact.

## 3. Expense Analysis

The analysis, found in `2. analysis.ipynb`, breaks down the spending into several key perspectives:

### Part 1: Overall Overview

- **Total Expenditure**: Calculation of the grand total spent across the entire period in KRW.
- **Spending by Currency**: Insights into how much was spent in local currencies before conversion.
- **Daily Average**: An assessment of the average daily cost of living in France.

### Part 2: Time-Series Trends

- **Monthly Spending**: Visualization of expenditure patterns over the months.
- **Period Analysis**: Comparison of costs incurred "Before" departure (visas, flights) versus "During" the exchange period.

### Part 3: Category & Travel Insights

- **Category Breakdown**: Analysis of spending across categories such as Rent, Groceries, Dining, and Transportation.
- **Travel-Specific Analysis**: A dedicated look at travel expenses, which represent a significant portion of the exchange experience.

***

## Repository Structure
- `1. preprocessing.ipynb`: Jupyter notebook for data cleaning and currency unification.
- `2. analysis.ipynb`: Jupyter notebook for statistical analysis and visualization.
- `exchange_expenses_dataset.csv`: The cleaned, anonymized, and KRW-converted dataset.

*Note: The original raw CSV file containing private descriptions is not included in this repository.*

***

## License & Citation

### License
This dataset and the accompanying analysis are licensed under a **Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0)**.

- **You are free to**: Share and adapt the material.
- **Under the following terms**:
  - **Attribution**: You must give appropriate credit and provide a link to the license.
  - **NonCommercial**: You may not use the material for commercial purposes (including publications for profit).

To view a copy of this license, visit [http://creativecommons.org/licenses/by-nc/4.0/](http://creativecommons.org/licenses/by-nc/4.0/).

### How to Cite
If you use this dataset or analysis for your own project or blog post, please cite it as follows:
**JeongHo SEO. (2026). Exchange Student Expense Analysis (Grenoble, France). GitHub Repository: [https://github.com/JeongHo-SEO/Exchange-expense]**
