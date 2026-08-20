# Task11 — Cleaned Company Employee Dataset

This project cleans a messy company employee dataset using **Python and Pandas**.

## Objective

Load and inspect the raw employee data, identify missing values, inconsistent categorical entries, incorrect data types, and duplicate records, clean the issues using appropriate Pandas techniques, verify the results, and export the cleaned dataset.

## Files

- `Cleaned_Company_Employee.ipynb` — Complete step-by-step cleaning workflow.
- `Cleaned_Company_Employee.csv` — Final cleaned employee dataset.
- `Cleaning_Summary.txt` — Brief summary of the cleaning decisions.
- `Day11_Messy_Company_Employee_Dataset.csv` — Original messy dataset.

## Cleaning Performed

- Inspected the dataset using Pandas.
- Quantified missing values with `isnull()` / `isna()`.
- Trimmed unnecessary whitespace.
- Standardized inconsistent values in categorical columns such as Department, Gender, and Work Mode.
- Converted numeric columns to appropriate numeric data types.
- Used **median imputation** for missing numeric values.
- Used **mode imputation** for missing categorical values.
- Converted `Joining_Date` to a proper datetime type.
- Removed duplicate records with `drop_duplicates()`.
- Verified missing values, duplicates, data types, and dataset dimensions after cleaning.
- Exported the final dataset as a CSV.

## Why These Methods?

- **Median imputation:** suitable for numeric employee attributes because it is less affected by unusually high or low values than the mean.
- **Mode imputation:** suitable for categorical fields because it replaces missing categories with the most common valid category.
- **drop_duplicates():** removes repeated employee records without discarding unique information.
- **dropna() / forward fill:** considered but not used indiscriminately. Dropping rows would unnecessarily remove usable employee data, and forward filling is not appropriate for this non-time-series employee dataset.

## Tools

- Python
- Pandas
- Jupyter Notebook

## Result

The final CSV contains cleaned, standardized employee records with missing values and exact duplicate rows addressed, and with dates stored using an appropriate datetime type.
