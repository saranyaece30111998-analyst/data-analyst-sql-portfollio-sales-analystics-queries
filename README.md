

---

# 📊 data-analyst-sql-portfollio-sales-analystics-queries

This repository contains a comprehensive set of SQL queries for the **Sales_Analytics** database.  
It covers **fundamental to advanced SQL concepts** with placeholders for screenshots of query results.

---

## 🗂 Database Schema
- **Customers**: CustomerID, CustomerName, City, Gender, Email  
- **Products**: ProductID, Name, Category, Price  
- **Orders**: OrderID, CustomerID, ProductID, Quantity, OrderDate, SalespersonID  
- **Salespersons**: SalespersonID, Name, Region, Target  

---



###  SELECT + DISTINCT
1. List all distinct cities where customers live.**  
```sql
SELECT DISTINCT City FROM Customers;
```


2. Retrieve distinct product categories from Products.**  
```sql
SELECT DISTINCT Category FROM Products;
```

---

###  SELECT + ALIAS (AS)
3. Display customer names and email IDs renamed as Customer_Name and Email_ID.**  
```sql
SELECT CustomerName AS Customer_Name, Email AS Email_ID FROM Customers;
```


** 4. Show product name, price, and (Price × 2) as DoublePrice.**  
```sql
SELECT ProductName, Price, Price*2 AS DoublePrice FROM Products;
```


**5. Show product name and price after adding a 10% tax.**  
```sql
SELECT ProductName, Price, Price*1.1 AS PriceWithTax FROM Products;
```


---

###  WHERE Clause with Operators

 

---

###  ORDER BY & LIMIT


---

###  Aggregate Functions

```sql
SELECT COUNT(*) AS TotalCustomers FROM Customers;
```

---

###  GROUP BY & HAVING


---

###  JOINs
 


---

### 8. Built‑in Functions + Aggregation
*(Total sales amount, top 5 customers, earliest/latest order date, etc.)*  
📸 Example: `screenshots/total_sales_per_order.png`

---

### 9. Window Functions
*(Ranking products, running totals, lag/lead examples, etc.)*  
📸 Example: `screenshots/product_price_rank.png`

---

### 10. Date & Time Functions
*(Orders in January 2025, week-wise totals, day names, etc.)*  
📸 Example: `screenshots/orders_january2025.png`

---

### 11. Subqueries (Single, Multi, Correlated)
*(Customers in same city as Arjun Kumar, products > average price, etc.)*  
📸 Example: `screenshots/subquery_same_city.png`

---

## 🚀 How to Use
1. Clone the repository.  
2. Run queries on the **Sales_Analytics** database.  
3. Save query results as screenshots (`.png`) inside the `/screenshots` folder.  
4. Replace placeholders in README with actual screenshots.  

---









