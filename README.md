# SQL-Data-Cleaning

This repository contains a structured SQL-based data cleaning project focused on handling messy datasets, specifically layoff-related data from various companies. The objective is to prepare clean, consistent, and analysis-ready data using SQL.

## 📁 Dataset
1. Source: layoffs.layoffs table (raw data)
2. Staging Table: A copy of the original dataset is made as layoffs_staging to safely clean the data.

## 🔧 Steps Performed
1. Created a Staging Table:
   Created a working copy of the original table to preserve raw data.
2. Removed Duplicates:
   Identified duplicates using ROW_NUMBER() and deleted extra rows.
   Verified specific cases (e.g., Yahoo) to prevent accidental data loss.
3. Standardized Data:
   Cleaned inconsistent text entries (industry, country).
   Replaced blank strings with NULL for better handling.
   Standardized date formats using STR_TO_DATE().
4. Handled Missing Values:
   Used self-joins to populate missing industry values where possible.
   Retained essential NULLs for better EDA handling.
5. Removed Irrelevant Rows/Columns:
   Deleted rows with both total_laid_off and percentage_laid_off as NULL.
   Dropped helper columns like row_num after use.

## 📌 Key SQL Concepts Used
1. ROW_NUMBER() and CTE for deduplication
2. UPDATE, JOIN, and TRIM for standardization
3. STR_TO_DATE() and ALTER TABLE for date formatting
4. Conditional deletion of rows

## 🛠️ Tools & Technologies
1. MySQL / SQL
2. Data Wrangling Techniques
3. Schema Design Best Practices
