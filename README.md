# SQL Project: Data Cleaning

## Overview
This project focuses on data cleaning operations performed on a dataset about layoffs across different companies and industries around the world. The objective is to enhance the dataset by removing duplicates, standardizing data formats, and ensuring consistency for effective analysis.

## Key Features
- *Duplicate Handling*: Identifies and removes duplicate records in the dataset using ROW_NUMBER() and partitioning techniques.
- *Standardization*: Formats date fields and trims unnecessary characters from textual data.
- *Null Value Management*: Handles null or empty values in critical fields like industry and total_laid_off.
- *Data Cleaning with CTEs*: Utilizes Common Table Expressions (CTEs) for simplifying complex DELETE operations.
- *Data Transformation*: Consolidates and updates inconsistent categories like "CryptoCurrency" and "Crypto" into a unified format.

## Dataset
The dataset includes the following key fields:
- company: Name of the company.
- location: Location of the company.
- industry: Industry the company operates in.
- total_laid_off: Total number of employees laid off.
- percentage_laid_off: Percentage of employees laid off.
- date: Layoff date.
- stage: Stage of the company (e.g., startup).
- country: Country of operation.
- funds_raised_millions: Amount of funds raised by the company.

## Scripts
### Data Cleaning Process
1. *Staging Tables*:
   - Create a staging table to preserve the original data.
   - Populate the staging table with the dataset.
2. *Duplicate Removal*:
   - Identify duplicates using ROW_NUMBER() and remove them.
3. *Null & Empty Fields*:
   - Standardize NULL and empty values in critical fields (e.g., industry).
4. *Field Updates*:
   - Correct inconsistencies like trimming country values and standardizing date formats.
5. *Finalize Clean Data*:
   - Store the cleaned data in a dedicated table (layoffs_staging2) for further analysis.

## SQL Commands
Scripts include:
- Staging table creation.
- Data insertion and duplicate removal.
- Null value handling and field updates.
- Date field formatting and country field cleaning.

## How to Run
1. Set up a database (world_layoffs) on your SQL server.
2. Execute the provided SQL scripts in the following order:
   - Create staging tables.
   - Populate tables and clean data.
3. Run SELECT queries to validate the final cleaned data.

## Requirements
- SQL Server or compatible database management system.
- Basic understanding of SQL syntax and operations.

