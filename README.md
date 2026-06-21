# Basic Data Exploration and Cleaning using Pandas

**Course:** Data Engineering 003 — Week 1: Python Basics

**Platform:** Celebal Technologies CSI Portal

**Dataset:** Shopping Dataset (Kaggle)

---

## 📌 Project Objective

The goal of this project is to master Python basics and perform essential data exploration and cleaning techniques using **Pandas** on a real-world shopping transactions dataset.

---

## 🛠️ Tech Stack

* **Language:** Python 3.x
* **Libraries:** Pandas 3.x, NumPy
* **Environment:** Jupyter Notebook

---

## 📋 Steps Covered

1. **Load Data:** Import a CSV dataset into a Pandas DataFrame.
2. **Explore Data:** Inspect structural attributes using `head()`, `tail()`, `shape`, `columns`, `dtypes`, and `describe()`.
3. **Handle Missing Values:** Identify gaps and fill them using medians or structural placeholders.
4. **Basic Operations:** Apply row filtering and column selection.
5. **Deduplication:** Locate and remove duplicate records.
6. **Feature Engineering:** Create a derived column: $\text{total\_amount} = \text{price} \times \text{quantity}$.
7. **Export Data:** Save the final, cleaned dataset into a fresh CSV file.

---

## 🗂️ Dataset Schema

| Column | Type | Description |
| --- | --- | --- |
| `customer_id` | string | Unique customer identifier |
| `age` | float | Customer age |
| `gender` | string | Male / Female / Other |
| `product` | string | Product name |
| `category` | string | Electronics / Clothing / Food / Books / Sports |
| `price` | float | Unit price (₹) |
| `quantity` | int | Units purchased |
| `rating` | float | Customer rating (1–5) |
| `purchase_date` | string | Date of purchase |
| `total_amount` *(Derived)* | float | Calculated dynamically as `price` $\times$ `quantity` |

---

## 🧹 Cleaning Summary

* **Shape Transformation:**
* *Raw Dataset:* 204 rows × 9 columns
* *Cleaned Dataset:* 200 rows × 10 columns


* **Missing Values:** Resolved all gaps (0 missing values remaining).
* `age` (15 missing) & `rating` (10 missing) $\rightarrow$ Filled with column **median**
* `gender` (8 missing) $\rightarrow$ Filled with placeholder **'Unknown'**


* **Duplicate Rows:** 4 duplicate rows identified $\rightarrow$ Removed via `drop_duplicates()`.
* **Derived Feature:** Added `total_amount` column ($\text{price} \times \text{quantity}$) to compute true order totals.

---

## 📈 Key Findings

> 💰 **Grand Total Revenue:** ₹3,68,042.60 generated across all transactions.
> 🛒 **Top Performing Category:** **Electronics** drove the highest revenue.
> ⭐️ **Typical Customer Rating:** **3.0** (Median).
> | 🏷️ **Price Range spectrum:** Ranges from a minimum of **₹5** (Food) up to a maximum of **₹2,000** (Electronics).

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

```

### 2. Install Dependencies

```bash
pip install pandas numpy jupyter

```

### 3. Open and Execute the Notebook

Ensure that your raw `shopping_dataset.csv` file is placed directly in the same folder directory as the notebook before launching:

```bash
jupyter notebook Shopping_Data_Exploration.ipynb

```

*Once open, click **Kernel** $\rightarrow$ **Restart & Run All** to run all cells sequentially.*

---

## 🧑‍💻 Author

* **Name:** VABHRAVI PANDEY
* **Program:** Celebal Technologies — Data Engineering (Week 1 Assignment)
