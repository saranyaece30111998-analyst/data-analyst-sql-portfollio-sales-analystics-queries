

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
<img width="512" height="486" alt="Screenshot 2026-06-06 230214" src="https://github.com/user-attachments/assets/67642ca8-98a6-402a-a4a4-d95d219e79d9" />


2. Retrieve distinct product categories from Products.**  
```sql
SELECT DISTINCT Category FROM Products;
```
<img width="825" height="257" alt="Screenshot 2026-06-06 230317" src="https://github.com/user-attachments/assets/b0ef4399-3c90-4c8b-83a5-6446e3bd35e0" />

---

###  SELECT + ALIAS (AS)
3. Display customer names and email IDs renamed as Customer_Name and Email_ID.**  
```sql
SELECT CustomerName AS Customer_Name, Email AS Email_ID FROM Customers;
```
<img width="646" height="552" alt="Screenshot 2026-06-06 230354" src="https://github.com/user-attachments/assets/1056287b-5a3e-448c-9242-0cf795ec6e85" />


** 4. Show product name, price, and (Price × 2) as DoublePrice.**  
```sql
SELECT ProductName, Price, Price*2 AS DoublePrice FROM Products;
```
<img width="841" height="516" alt="Screenshot 2026-06-06 230456" src="https://github.com/user-attachments/assets/8ded9de5-880b-485a-bdd9-20a6bfc31c64" />


** 5. Show product name and price after adding a 10% tax.**  
```sql
SELECT ProductName, Price, Price*1.1 AS PriceWithTax FROM Products;
```
<img width="776" height="505" alt="Screenshot 2026-06-06 230545" src="https://github.com/user-attachments/assets/d66340e8-8a9f-4d21-a783-33dbe5729257" />


---

###  WHERE Clause with Operators
** 6. Find all customers who live in Hyderabad.
 - <img width="635" height="328" alt="Screenshot 2026-06-06 230615" src="https://github.com/user-attachments/assets/561b76fd-6725-4862-abd2-b4ffff34164b" />
** 7. Show all products priced above 10,000.
- <img width="647" height="302" alt="Screenshot 2026-06-06 230644" src="https://github.com/user-attachments/assets/278e8407-96b7-449a-8f85-1276067ad564" />
** 8. List all orders placed after 2025-01-12.
- <img width="667" height="516" alt="Screenshot 2026-06-06 230726" src="https://github.com/user-attachments/assets/4371e577-8828-4cb8-8590-4ad19e25e99d" />
** 9. Find products whose price is NOT equal to 1500.
- <img width="452" height="437" alt="Screenshot 2026-06-06 230810" src="https://github.com/user-attachments/assets/b5fe2c93-9644-4cc6-ad55-307d2289fafa" />
** 10. Find customers whose Email is NULL.
- <img width="576" height="245" alt="Screenshot 2026-06-06 230848" src="https://github.com/user-attachments/assets/6555ead6-d59b-4946-9935-4ef30767f5bd" />
** 11. List all orders where quantity is NOT NULL.
  - <img width="720" height="493" alt="Screenshot 2026-06-06 230922" src="https://github.com/user-attachments/assets/ee913ffc-7c44-43a8-a979-fdfb64bc4094" />


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

### Built‑in Functions + Aggregation


---

###  Window Functions


---

###  Date & Time Functions


---

###  Subqueries (Single, Multi, Correlated)


---

## 🚀 How to Use
1. Clone the repository.  
2. Run queries on the **Sales_Analytics** database.  
3. Save query results as screenshots (`.png`) inside the `/screenshots` folder.  
4. Replace placeholders in README with actual screenshots.  

---









