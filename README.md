# Data-Cleaning-in-SQL

## Overview
This SQL project demonstrates advanced data cleaning and exploratory data analysis (EDA) techniques applied to a real-world dataset of global layoffs from 2020 to 2023. The goal is to uncover employment trends and transform raw data into a reliable dataset for actionable insights. By processing the data in MySQL, the project showcases best practices in data pipeline creation, non-destructive workflows, and systematic validation, highlighting proficiency in SQL for data manipulation and analysis.

## Key Features
- **Data Cleaning**: Removes duplicates, standardizes formats, handles null/blank values, and eliminates unnecessary data while preserving raw data integrity.
- **Exploratory Data Analysis (EDA)**: Uses advanced SQL techniques to identify trends, such as the most affected industries and countries, and rankings of companies by layoffs.
- **Best Practices**: Implements a non-destructive workflow using staging tables and systematic validation to ensure data reliability.

## Methodology
The project processes a global layoffs dataset in MySQL within a `world_layoffs` schema, following a structured pipeline:
1. **Data Import**: Imports raw data into MySQL and creates staging tables to preserve original data.
2. **Data Cleaning**:
   - Removes duplicates using `ROW_NUMBER()` window functions.
   - Standardizes industry labels (e.g., unifying "crypto" and "cryptocurrency" with `TRIM` and pattern matching).
   - Handles missing values via self-joins (e.g., populating missing industry data for companies like Airbnb).
   - Eliminates unnecessary columns or rows for a lean dataset.
3. **Exploratory Data Analysis**:
   - Uses Common Table Expressions (CTEs) for modular analysis.
   - Applies window functions (`DENSE_RANK`, `SUM OVER`) for time-series and ranking analytics.
   - Converts date formats to enable temporal analysis.
4. **Validation**: Ensures data integrity through systematic checks at each cleaning stage.

## Key Outcomes
The analysis reveals significant employment trends:
- **Industry and Country Impact**: Identifies sectors (e.g., tech) and countries most affected by layoffs.
- **Company Rankings**: Ranks companies by annual layoffs, highlighting major players like Google and Amazon.
- **Layoff Progression**: Computes rolling totals to show the temporal evolution of layoffs from 2020 to 2023.
These insights demonstrate the ability to transform raw data into actionable business intelligence, suitable for informing workforce strategies or economic policy.
