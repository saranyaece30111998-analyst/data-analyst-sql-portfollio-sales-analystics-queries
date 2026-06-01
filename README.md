

---

# 📊 Sales_Analytics: Database Schema, Sample Data & Query Examples

## 1. Overview
This project creates a **Sales Analytics Database** to manage customers, products, salespersons, and orders.  
It includes **sample data inserts** and a wide range of **SQL queries** demonstrating filtering, grouping, ordering, aggregation, and advanced window functions.

---

## 2. Database Schema

### **Customers Table**
- Stores customer details.  
- **Columns:** `CustomerID`, `CustomerName`, `Gender`, `City`, `Email`  
- **Sample Data:** 30 customers across multiple cities.

### **Products Table**
- Stores product details.  
- **Columns:** `ProductID`, `ProductName`, `Category`, `Price`  
- **Sample Data:** Electronics & Furniture items.

### **Salespersons Table**
- Stores salesperson details.  
- **Columns:** `SalespersonID`, `SalespersonName`, `Region`, `TargetAmount`

### **Orders Table**
- Stores order transactions.  
- **Columns:** `OrderID`, `CustomerID`, `SalespersonID`, `ProductID`, `Quantity`, `OrderDate`  
- **Relationships:**  
  - `CustomerID` → Customers  
  - `SalespersonID` → Salespersons  
  - `ProductID` → Products  

---

## 3. Sample Queries

### **Basic Retrieval**
- Distinct cities from Customers  
- Distinct product categories  
- Customer names & emails (renamed as `Customer_Name`, `Email_ID`)  
- Products with tax, double price, or price filters  

### **Filtering**
- Customers from Hyderabad  
- Products priced above 10,000  
- Orders placed after `2025-01-12`  
- Female customers in Chennai  
- Products not in Electronics/Furniture  

### **Ordering & Limiting**
- Customers ordered by name  
- Top 3 products by price  
- Top 3 expensive products > 5000  
- Customers in Chennai/Pune/Hyderabad sorted by name  

### **Aggregation & Grouping**
- Number of customers in each city  
- Number of customers by gender  
- Cities with customer count > 2  
- Customers with more than 3 orders  
- Average price per category (only > 5000)  

### **Window Functions**
- Earliest & latest order dates  
- Total orders per customer using `COUNT OVER`  
- Product price ranking using `RANK()`  
- Ranking within each category using `PARTITION BY`
- Perfect — let’s add **code snippets with sample outputs** to your README so it looks more complete and professional. Here are some ready‑to‑use examples based on your *Sales Analytics* project:

---

## 💻 Example SQL Queries & Results

### 1. Distinct Cities from Customers
```sql
SELECT DISTINCT city FROM Customers;
```
**Result:**
| city       |
|------------|
| Chennai    |
| Bangalore  |
| Hyderabad  |
| Mumbai     |
| Delhi      |
| Kochi      |
| Pune       |

---

### 2. Products Priced Above ₹10,000
```sql
SELECT name, category, price FROM Products WHERE price > 10000;
```
**Result:**
| name       | category     | price   |
|------------|--------------|---------|
| Laptop     | Electronics  | 55000   |
| Sofa       | Furniture    | 25000   |
| Smartphone | Electronics  | 30000   |

---

### 3. Average Product Price per Category
```sql
SELECT category, AVG(price) AS avg_price FROM Products GROUP BY category;
```
**Result:**
| category     | avg_price |
|--------------|-----------|
| Electronics  | 28,500    |
| Furniture    | 18,200    |

---

### 4. Total Orders per Customer (Window Function)
```sql
SELECT customer_id, COUNT(*) OVER(PARTITION BY customer_id) AS total_orders
FROM Orders;
```
**Result:**
| customer_id | total_orders |
|-------------|--------------|
| C001        | 5            |
| C002        | 3            |
| C003        | 7            |

---

### 5. Ranking Products by Price (Global & Category)
```sql
SELECT name, category,
       RANK() OVER(ORDER BY price DESC) AS rank_global,
       RANK() OVER(PARTITION BY category ORDER BY price DESC) AS rank_category
FROM Products;
```
**Result:**
| name       | category     | rank_global | rank_category |
|------------|--------------|-------------|---------------|
| Laptop     | Electronics  | 1           | 1             |
| Smartphone | Electronics  | 2           | 2             |
| Sofa       | Furniture    | 3           | 1             |
| Chair      | Furniture    | 4           | 2             |

---

✅ These **code + result blocks** make your README much more engaging and portfolio‑ready.  

Would you like me to also prepare a **sample ER diagram screenshot placeholder section** so recruiters can visually see the schema relationships?

---

## 4. Key Highlights
- Demonstrates **SQL fundamentals**: `SELECT`, `WHERE`, `ORDER BY`, `GROUP BY`, `HAVING`.  
- Uses **aggregate functions**: `COUNT`, `AVG`, `MIN`, `MAX`.  
- Applies **window functions**: `RANK()`, `COUNT() OVER`.  
- Provides **realistic sample data** for analytics scenarios.  

---

✅ This README makes your project **professional and portfolio-ready**.  
Would you like me to also create a **visual ER diagram (Entity-Relationship)** for this schema so you can include it in your documentation?
