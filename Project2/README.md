# Real-World Data Wrangling: Income Analysis
## Project Overview

### This project analyzes the relationship between self-employment income and wage or salary income across various households. By exploring the distribution of these income types, we aim to identify patterns and differences between self-employment and salaried earnings.
Problem Statement

### The goal is to analyze and compare income distributions for self-employment versus wage or salary income, addressing questions such as:

   ### How do self-employment and salary incomes vary?
  ###  Are there identifiable patterns in income types across different households?

### Datasets
1. Self-Employment Income

    Source: UCI Machine Learning Repository
    Format: CSV
    Main Variables:
        SERIALNO: Household serial number
        PUMA: Public use microdata area code
        PINCP: Total person's income (past 12 months)

2. Wage or Salary Income

    Source: Western Pennsylvania Regional Data Center
    Format: CSV
    Main Variables:
        SERIALNO: Household serial number
        PUMA: Public use microdata area code
        WAGP: Wage or salary income (past 12 months)

### Project Steps
1. Data Collection

    Self-Employment Income: Downloaded directly as a CSV.
    Salary Income: Fetched from an online URL provided by the data source.

2. Data Assessment

    Quality Issues:
        Missing Values: Checked for null values and handled them by filling missing values in numeric columns with the column mean.
        Inaccurate Data: Identified outliers and inconsistencies using summary statistics.
    Tidiness Issues:
        Redundant Columns: Removed irrelevant columns (e.g., SERIALNO, PUMA) for a focused analysis.
        Inconsistent Data Types: Ensured correct data types, converting necessary columns to strings.

3. Data Cleaning

    Handle Missing Values: Filled numeric columns' missing values with mean values; filled non-numeric columns with "Unknown."
    Remove Redundant Columns: Dropped unnecessary columns.
    Convert Data Types: Ensured numerical columns were treated as numeric, and unique identifiers were strings.

4. Data Storage

    Cleaned datasets were saved as SelfEmploymentIncome_cleaned.csv and SalaryIncome_cleaned.csv for further analysis.

5. Data Analysis

    Research Question: Calculate and compare the average incomes from self-employment and salaries to identify trends.
    Findings:
        Self-employment income was generally lower and more volatile compared to salary income.
        Salary income was higher on average and showed a less skewed distribution.

6. Visualizations

    Created histograms for each income type, revealing that self-employment income was highly skewed with a few high outliers, while salary income had a more uniform spread.
