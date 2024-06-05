# Data Cleaning in MySQL

This repository contains scripts and instructions for cleaning a dataset on layoffs in 2022 using MySQL. The dataset is sourced from [Kaggle](https://www.kaggle.com/datasets/swaptr/layoffs-2022). The main objectives are to remove duplicates, standardize the data, handle null or blank values, and remove any unnecessary columns.

## Table of Contents

- [Dataset](#dataset)
- [To Do](#to-do)
  - [1. Remove Duplicates](#1-remove-duplicates)
  - [2. Standardize the Data](#2-standardize-the-data)
  - [3. Handle Null or Blank Values](#3-handle-null-or-blank-values)
  - [4. Remove Unnecessary Columns](#4-remove-unnecessary-columns)
- [Usage](#usage)
- [License](#license)

## Dataset

The dataset used in this project can be found on Kaggle: [Layoffs 2022 Dataset](https://www.kaggle.com/datasets/swaptr/layoffs-2022). Please download the dataset and place it in the root directory of this repository.

## To Do

### 1. Remove Duplicates

Duplicates in the dataset can skew analysis and lead to incorrect conclusions. We will use SQL queries to identify and remove duplicate rows.

Example SQL Query:
```sql
DELETE FROM layoffs
WHERE id NOT IN (
    SELECT MIN(id)
    FROM layoffs
    GROUP BY company, date, employees_laid_off
);

### 2. Standardize the Data

Data standardization ensures consistency in data format and representation across all fields. This step involves converting data into a uniform format where necessary.

Example SQL Query:
```sql
UPDATE layoffs
SET company = UPPER(company),
    date = DATE_FORMAT(date, '%Y-%m-%d'),
    reason = CONCAT(UCASE(LEFT(reason, 1)), LCASE(SUBSTRING(reason, 2)));
