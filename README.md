# 📊 Elevate Labs – Day 7 Internship Task  

## 🎯 Objective  
Analyze sales data from a SQLite database using Python, SQL, and Matplotlib to extract key business insights.  

## 📂 Dataset Info  
- **Database:** `sales_data.db`  
- **Table:** `sales`  
- **Columns:**  
  - `id` – Transaction ID  
  - `product` – Product name  
  - `quantity` – Units sold  
  - `price` – Price per unit  
  - `date` – Date of sale  

## 🛠 Steps Performed  
1. **Database Connection** – Connected to `sales_data.db` using `sqlite3`.  
2. **SQL Query Execution** –  
   - Top products by quantity sold  
   - Daily revenue trends  
3. **Data Loading** – Fetched query results directly into Pandas DataFrames.  
4. **Data Visualization** – Created a horizontal bar chart for top products using Matplotlib.  
5. **Chart Saving** – Exported chart as `sales_chart.png`.  

## 📊 SQL Queries Used  
```sql
-- Top Products by Quantity Sold
SELECT product, SUM(quantity) AS total_quantity
FROM sales
GROUP BY product
ORDER BY total_quantity DESC;

-- Daily Revenue
SELECT date, SUM(quantity * price) AS daily_revenue
FROM sales
GROUP BY date
ORDER BY date;
````

## 📈 Outputs

* **Console:** Printed aggregated query results.
* **Chart:** Horizontal bar chart of top-selling products (`sales_chart.png`).

## 🛠 Tools Used

* Python (`sqlite3`, `pandas`, `matplotlib`)
* SQLite Database

## 👨‍💻 Author

**Saloora Vaibhav**

