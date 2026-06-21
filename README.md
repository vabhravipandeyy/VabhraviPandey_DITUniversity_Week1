Basic Data Exploration and Cleaning using Pandas
Course: Data Engineering 003 — Week 1: Python Basics
Platform: Celebal Technologies CSI Portal
Dataset: Shopping Dataset — Kaggle

Objective
Learn Python basics and perform basic data exploration and cleaning using Pandas on a real-world shopping transactions dataset.

Steps Covered
Step	Task
1	Load a CSV dataset into a Pandas DataFrame
2	Explore data — head(), tail(), shape, columns, dtypes, describe()
3	Handle missing values — identify, fill with median / placeholder
4	Perform basic operations — filter rows, select columns
5	Remove duplicate rows
6	Create a derived column: total_amount = price × quantity
7	Save the cleaned dataset as a new CSV file

Dataset Schema
Column	Type	Description
customer_id	string	Unique customer identifier
age	float	Customer age
gender	string	Male / Female / Other
product	string	Product name
category	string	Electronics / Clothing / Food / Books / Sports
price	float	Unit price (₹)
quantity	int	Units purchased
rating	float	Customer rating (1–5)
purchase_date	string	Date of purchase
total_amount (derived)	float	price × quantity

Cleaning Summary
Issue	Details	Fix Applied
Missing values	age (15), rating (10), gender (8)	Filled with median / 'Unknown'
Duplicate rows	4 duplicates found	Removed with drop_duplicates()
Derived column	total_amount not in raw data	Created as price × quantity
Raw dataset: 204 rows × 9 columns
Cleaned dataset: 200 rows × 10 columns
Missing values after cleaning: 0

Key Findings
Grand total revenue across all purchases: ₹3,68,042.60
Top category by revenue: Electronics
Most common rating: 3.0 (median)
Price range: ₹5 (Food) to ₹2,000 (Electronics)

How to Run
Clone this repository:

git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
Install dependencies:

pip install pandas numpy jupyter
Launch Jupyter Notebook:

jupyter notebook Shopping_Data_Exploration.ipynb
Run all cells from top to bottom (Kernel → Restart & Run All)

Make sure shopping_dataset.csv is in the same folder as the notebook before running.

Tech Stack
Python 3.x
Pandas 3.x
NumPy
Jupyter Notebook

Author
Name: VABHRAVI PANDEY
Course: Celebal Technologies — Data Engineering week-1
