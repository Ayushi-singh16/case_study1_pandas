# Customer Data Cleaning and Transformation Project

## Overview

This project focuses on cleaning and transforming raw customer data using Python and Pandas.
The dataset contains common real-world data quality issues such as missing values, inconsistent formats, and incorrect data types.

The objective is to prepare a structured and reliable dataset for further analysis.

---

## Dataset Description

The dataset includes the following columns:

* `customer_id`: Unique identifier for each customer
* `name`: Customer name (contains missing values and inconsistent formatting)
* `age`: Age values with mixed data types
* `city`: Customer city with inconsistent casing and missing values
* `salary`: Monthly salary containing symbols such as "k", "rs", and commas
* `experience`: Work experience with both text and numeric formats
* `join_date`: Joining date with multiple formats and invalid entries
* `is_active`: Membership status represented inconsistently (Yes/No formats)

---

## Data Issues Identified

* Presence of missing values across multiple columns
* Inconsistent text formatting (uppercase, lowercase, extra spaces)
* Mixed data types within columns
* Invalid and non-standard entries (e.g., "twenty", "five", "invalid")
* Special characters in numeric fields

---

## Data Cleaning Steps

### 1. Handling Missing Values

* Removed rows where `customer_id` was missing
* Filled missing values in categorical columns (`name`, `city`)
* Imputed numeric columns (`age`, `salary`) using statistical measures (median/mean)

### 2. Data Type Conversion

* Converted `age`, `salary`, and `experience` to numeric types
* Converted `join_date` to datetime format
* Handled invalid values using `errors='coerce'`

### 3. Text Standardization

* Removed extra spaces using string methods
* Converted text columns to lowercase for consistency
* Standardized categorical values (e.g., Yes/No to 1/0)

### 4. Cleaning Numeric Fields

* Removed symbols such as "k", "rs", and commas from salary
* Converted shorthand values (e.g., 60k → 60000)
* Replaced invalid entries with appropriate values

### 5. Handling Dates

* Standardized multiple date formats into a single datetime format
* Removed rows with invalid or missing dates

### 6. Feature Engineering

* Created `salary_per_year` by multiplying monthly salary by 12
* Created `age_group` column based on defined age ranges

### 7. Removing Duplicates

* Identified and removed duplicate records

---

## Technologies Used

* Python
* Pandas


---

## Key Learnings

* Handling missing data using `dropna()` and `fillna()`
* Converting and cleaning mixed data types
* Working with string operations in Pandas
* Applying transformations using `apply()` and lambda functions
* Managing real-world messy datasets

---

## Conclusion

## This project demonstrates a complete data cleaning workflow, transforming raw and inconsistent data into a structured format suitable for analysis. The techniques used here are directly applicable to real-world data preprocessing tasks in data analysis and data science.

## How to Run

1. Install required libraries:

   ```bash
   pip install pandas numpy
   ```

2. Run the Python script or Jupyter Notebook containing the code.

---
