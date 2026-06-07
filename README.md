

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

## ✅ Queries with Screenshots

### 1. SELECT + DISTINCT
**Q1. List all distinct cities where customers live.**  
```sql
SELECT DISTINCT City FROM Customers;
```
📸 *Screenshot:* `screenshots/distinct_cities.png`

**Q2. Retrieve distinct product categories from Products.**  
```sql
SELECT DISTINCT Category FROM Products;
```
📸 *Screenshot:* `screenshots/distinct_categories.png`

---

### 2. SELECT + ALIAS (AS)
**Q3. Display customer names and email IDs renamed as Customer_Name and Email_ID.**  
```sql
SELECT CustomerName AS Customer_Name, Email AS Email_ID FROM Customers;
```
📸 *Screenshot:* `screenshots/customer_email_alias.png`

**Q4. Show product name, price, and (Price × 2) as DoublePrice.**  
```sql
SELECT ProductName, Price, Price*2 AS DoublePrice FROM Products;
```
📸 *Screenshot:* `screenshots/double_price.png`

**Q5. Show product name and price after adding a 10% tax.**  
```sql
SELECT ProductName, Price, Price*1.1 AS PriceWithTax FROM Products;
```
📸 *Screenshot:* `screenshots/price_with_tax.png`

---

### 3. WHERE Clause with Operators
*(Hyderabad customers, products > 10,000, orders after 2025-01-12, etc.)*  
Each query has its own screenshot placeholder, e.g.:  
📸 `screenshots/customers_hyderabad.png`  
📸 `screenshots/products_above_10000.png`  

---

### 4. ORDER BY & LIMIT
*(Top 3 products, sorted customers, etc.)*  
📸 Example: `screenshots/top3_products.png`

---

### 5. Aggregate Functions
**Q8. Find the total number of customers.**  
```sql
SELECT COUNT(*) AS TotalCustomers FROM Customers;
```
📸 *Screenshot:* `screenshots/total_customers.png`

---

### 6. GROUP BY & HAVING
*(Customer count per city, gender grouping, etc.)*  
📸 Example: `screenshots/customers_per_city.png`

---

### 7. JOINs
*(Orders with customer names, LEFT JOIN, RIGHT JOIN, etc.)*  
📸 Example: `screenshots/orders_with_customers.png`

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



---

## 🗂 Database Schema
- **Customers**: CustomerID, CustomerName, City, Gender, Email  
- **Products**: ProductID, Name, Category, Price  
- **Orders**: OrderID, CustomerID, ProductID, Quantity, OrderDate, SalespersonID  
- **Salespersons**: SalespersonID, Name, Region, Target  

---

## ✅ Queries with Screenshots

### 1. SELECT + DISTINCT
**Q1. List all distinct cities where customers live.**  
```sql
SELECT DISTINCT City FROM Customers;
```
📸 *Screenshot:* `screenshots/distinct_cities.png`

**Q2. Retrieve distinct product categories from Products.**  
```sql
SELECT DISTINCT Category FROM Products;
```
📸 *Screenshot:* `screenshots/distinct_categories.png`

---

### 2. SELECT + ALIAS (AS)
**Q3. Display customer names and email IDs renamed as Customer_Name and Email_ID.**  
```sql
SELECT CustomerName AS Customer_Name, Email AS Email_ID FROM Customers;
```
📸 *Screenshot:* `screenshots/customer_email_alias.png`

**Q4. Show product name, price, and (Price × 2) as DoublePrice.**  
```sql
SELECT ProductName, Price, Price*2 AS DoublePrice FROM Products;
```
📸 *Screenshot:* `screenshots/double_price.png`

**Q5. Show product name and price after adding a 10% tax.**  
```sql
SELECT ProductName, Price, Price*1.1 AS PriceWithTax FROM Products;
```
📸 *Screenshot:* `screenshots/price_with_tax.png`

---

### 3. WHERE Clause with Operators
*(Hyderabad customers, products > 10,000, orders after 2025-01-12, etc.)*  
Each query has its own screenshot placeholder, e.g.:  
📸 `screenshots/customers_hyderabad.png`  
📸 `screenshots/products_above_10000.png`  

---

### 4. ORDER BY & LIMIT
*(Top 3 products, sorted customers, etc.)*  
📸 Example: `screenshots/top3_products.png`

---

### 5. Aggregate Functions
**Q8. Find the total number of customers.**  
```sql
SELECT COUNT(*) AS TotalCustomers FROM Customers;
```
📸 *Screenshot:* `screenshots/total_customers.png`

---

### 6. GROUP BY & HAVING
*(Customer count per city, gender grouping, etc.)*  
📸 Example: `screenshots/customers_per_city.png`

---

### 7. JOINs
*(Orders with customer names, LEFT JOIN, RIGHT JOIN, etc.)*  
📸 Example: `screenshots/orders_with_customers.png`

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

👉 This README now includes **all questions, all queries, and screenshot placeholders**.  

Would you like me to **expand every single question with its exact SQL code block + screenshot placeholder** (so you don’t have to add them manually), or keep it summarized by section with examples?
