# 🛍️ Shopping Dataset — Project Summary

## Overview
This project demonstrates Python & Pandas fundamentals through a complete
data exploration and cleaning workflow on a shopping transactions dataset.

---

## Files Delivered

| File | Description |
|------|-------------|
| `Shopping_Data_Exploration.ipynb` | Jupyter Notebook with all 7 steps, comments, and analysis |
| `shopping_dataset.csv` | Raw dataset (204 rows × 9 columns) with intentional missing values & duplicates |
| `shopping_cleaned.csv` | Cleaned & enriched dataset (200 rows × 10 columns) |

---

## Dataset Schema

| Column | Type | Description |
|--------|------|-------------|
| `customer_id` | string | Unique customer identifier |
| `age` | float | Customer age (years) |
| `gender` | string | Male / Female / Other / Unknown |
| `product` | string | Product name |
| `category` | string | Electronics / Clothing / Food / Books / Sports |
| `price` | float | Unit price (₹) |
| `quantity` | int | Units purchased |
| `rating` | float | Customer rating (1–5) |
| `purchase_date` | string | Date of purchase (YYYY-MM-DD) |
| `total_amount` *(derived)* | float | `price × quantity` |

---

## Steps Completed

### Step 1 — Load CSV
- Used `pd.read_csv()` to load the dataset
- Verified shape: **204 rows × 9 columns**

### Step 2 — Explore Data
- `df.head()` / `df.tail()` — inspect first/last rows
- `df.shape` — dimensions of the dataset
- `df.columns` — column names
- `df.dtypes` — data type of each column
- `df.describe()` — statistical summary (mean, std, min, max)
- `df['category'].value_counts()` — category distribution

### Step 3 — Handle Missing Values
| Column | Missing Count | Strategy |
|--------|--------------|----------|
| `age` | 15 | Filled with **median age** |
| `rating` | 10 | Filled with **median rating** |
| `gender` | 8 | Filled with **'Unknown'** |
- After cleaning: **0 missing values**

### Step 4 — Filter & Select
- Selected specific columns using `df[['col1', 'col2']]`
- Filtered Electronics: `df[df['category'] == 'Electronics']`
- Filtered high-value: `df[df['price'] > 500]`
- Multi-condition: Female customers with rating ≥ 4
- Sorted top 5 most expensive purchases

### Step 5 — Remove Duplicates
- Detected: **4 duplicate rows**
- Removed using `df.drop_duplicates()`
- Final row count: **200 rows**

### Step 6 — Derived Column
- Created `total_amount = price × quantity`
- Grand total revenue: **₹368,042.60**
- Top category by revenue: **Electronics**

### Step 7 — Save Cleaned CSV
- Exported to `shopping_cleaned.csv`
- Final shape: **200 rows × 10 columns**
- Zero missing values confirmed

---

## Key Concepts Learned
- Loading and inspecting DataFrames
- Identifying and handling missing data (median fill, placeholder fill)
- Boolean indexing for filtering rows
- Column selection and creation
- Deduplication
- Exporting cleaned data

---
*Project completed using Python 3 + Pandas 3.x*
