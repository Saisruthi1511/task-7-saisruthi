# Task 7: Basic Sales Summary using SQLite in Python

##  Overview

This project is part of a Data Analyst Internship task focused on practicing basic SQL within Python using a small SQLite database. The objective was to extract simple sales insights (like total quantity sold and total revenue) and visualize them using a bar chart — all implemented in Google Colab.

##  Tools Used

- **Google Colab** (Python)
- **SQLite** (`sqlite3`)
- **Pandas**
- **Matplotlib**

##  Dataset

A small SQLite database file named `sales_data.db` was used, containing a single `sales` table with sample transactional data.

##  What I Did

- Connected to the SQLite database using Python's `sqlite3` module.
- Ran a SQL query to calculate total quantity and revenue per product:
  ```sql
  SELECT product, 
         SUM(quantity) AS total_qty, 
         SUM(quantity * price) AS revenue 
  FROM sales 
  GROUP BY product;
  ```
- Loaded the results into a Pandas DataFrame.
- Printed the summary table.
- Plotted a bar chart of revenue by product using Matplotlib.
- All work was done inside a Google Colab notebook.

## Output

- A printed DataFrame showing each product’s total quantity sold and revenue.
- A basic bar chart visualizing revenue per product.

## ✅ How to Run

1. Upload `sales_data.db` to your Colab session.
2. Open and run the Colab notebook.
3. The code will connect to the database, query the sales data, and display the results both in tabular and chart form.
