# 🧹 Data Cleaning Pipeline for SaaS Dataset

A Python-based **SaaS Customer Data Cleaning Pipeline** developed as part of the Python Module End Assessment.

## 📌 Project Overview

This project demonstrates how raw SaaS customer data can be cleaned, validated, analyzed, and exported using Python.

The dataset contains customer information such as:

* Customer ID
* Name
* Signup Date
* Plan
* Monthly Fee
* Usage Hours

## 🔧 Key Tasks

### 1. Display Customer Data

Uses a `for` loop to display customer records in a readable format.

```python
for i in range(len(saas_data["customer_id"])):
    print(f"ID: {saas_data['customer_id'][i]}")
```

### 2. Add New Customers

New customer records are added using user input with **auto-increment Customer IDs**.

```python
new_id = max_id + 1
saas_data["customer_id"].append(new_id)
```

### 3. OOP Data Validation

A `SaasCustomer` class is used to validate and display customer data.

```python
class SaasCustomer:
    def validate_data(self):
        # Validate and clean customer data
        pass
```

### 4. Data Cleaning Pipeline

The pipeline handles:

* Missing values
* Invalid numeric values
* Duplicate Customer IDs
* Inconsistent date formats

```python
dirty_data = handle_missing_values(dirty_data)
dirty_data = remove_duplicates(dirty_data)
dirty_data = standardize_dates(dirty_data)
```

### 5. Summary Statistics

Calculates:

* Total customers
* Average monthly fee
* Total usage hours
* Plan distribution

### 6. Low-Usage Customers

Identifies customers with:

```python
usage_hours < 50
```

### 7. Unique Plan Types

Uses `set()` and `sorted()` to extract unique plans alphabetically.

```python
plans = sorted(set(cleaned_data["plan"]))
```

### 8. Export Cleaned Data

Creates two output files:

* `saas_customers_cleaned.csv`
* `plan_summary.txt`

File operations are handled using `try`, `except`, `else`, and `finally`.

## 🛠️ Technologies

**Python | OOP | Functions | Lists | Dictionaries | Sets | CSV | File Handling | Exception Handling**

## 🎯 Objective

To transform raw SaaS customer data into **clean, standardized, validated, and analysis-ready data** using practical Python programming concepts.

## 📂 Project Files

```text
M1A1_Data_Cleaning_Pipeline_for_SaaS_Dataset.ipynb
saas_customers_cleaned.csv
plan_summary.txt

## 👤 Author

**Sathyabama Rajaram**  
Data Science Learner
README.md
```
