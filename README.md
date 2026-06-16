# Task-1-Data-Cleaning-and-Preprocessing
Objective: Clean and prepare a raw dataset (with nulls, duplicates, inconsistent formats).  Tools: Excel / Python (Pandas)  Deliverables: Cleaned dataset + short summary of changes 

## Data Cleaning and Preprocessing Summary: Netflix Movies and TV Shows Dataset

### 1. Dataset Acquisition

We downloaded the **“Netflix Movies and TV Shows”** dataset from Kaggle to perform data cleaning and preprocessing for future analysis.

### 2. Missing Values Identification and Handling

We identified missing values in several columns of the dataset:

* **director**: 2,634 missing values
* **cast**: 825 missing values
* **country**: 831 missing values
* **date_added**: 10 missing values
* **rating**: 4 missing values
* **duration**: 3 missing values

To handle these missing values:

* Missing values in **director**, **cast**, and **country** were replaced with **“Unknown”** to preserve the records while maintaining consistency.
* Rows containing missing values in **date_added**, **rating**, and **duration** were removed because these fields were considered essential for analysis.

### 3. Duplicate Values Check

We checked the dataset for duplicate records to ensure data integrity and consistency. No significant duplicate issues were found in the dataset.

### 4. Leading and Trailing Spaces Detection

We checked all string-based columns for **leading and trailing spaces**. We found that only the **date_added** column contained values with extra spaces, such as:

* “ August 4, 2017”
* “ December 23, 2018”
* “ December 15, 2018”
* “ July 1, 2017”
* “ July 26, 2019”

We removed leading and trailing spaces from all text columns to ensure consistency and avoid formatting issues during analysis.

### 5. Multi-Value Columns Handling

To simplify future analysis, we handled multi-value columns by extracting only the **primary (first) value** from:

* **country**
* **listed_in**

This ensured more consistent categorical analysis later.

### 6. Date Format Standardization

We converted date values from formats such as:

**“September 24, 2021” → “2021-09-24”**

to ensure a **consistent date format** suitable for analysis and modeling.

### 7. Column Header Verification

We verified the column names and found that the headers were already **clean, standardized, and uniform**, so no modifications were required.

### 8. Data Type Verification

Finally, we checked the **data types of all columns** to ensure that each variable had the appropriate format for future analysis and preprocessing tasks.
