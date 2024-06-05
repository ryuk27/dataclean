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

## Dataset

The dataset used in this project can be found on Kaggle: [Layoffs 2022 Dataset](https://www.kaggle.com/datasets/swaptr/layoffs-2022). Please download the dataset and place it in the root directory of this repository.

## To Do

### 1. Remove Duplicates

Duplicates in the dataset can skew analysis and lead to incorrect conclusions. We will use SQL queries to identify and remove duplicate rows.

### 2. Standardize the Data

Data standardization ensures consistency in data format and representation across all fields. This step involves converting data into a uniform format where necessary.

### 3. Handle Null or Blank Values

Null or blank values can affect analysis and computations. We will handle these values appropriately, either by replacing them with meaningful defaults or by removing the corresponding rows.

### 4. Remove Unnecessary Columns

Removing unnecessary columns streamlines the dataset and focuses analysis on relevant attributes.

## Usage

1. Setup: Download the dataset from Kaggle and place it in the root directory of this repository.
2. Run Scripts: Execute the provided MySQL scripts in your MySQL environment, following the order specified in the scripts/ directory.
3. Review Results: After running each script, review the cleaned dataset to ensure accuracy and completeness.
