

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
** 12. List the female customers who live in Chennai.
  - <img width="776" height="560" alt="Screenshot 2026-06-06 231027" src="https://github.com/user-attachments/assets/c59da254-a57f-466d-9191-208edcfce8fe" />

** 13. Display customers who live in (‘Chennai’, ‘Bangalore’, ‘Hyderabad’).
- <img width="842" height="491" alt="Screenshot 2026-06-06 231107" src="https://github.com/user-attachments/assets/d90a9094-2693-4f5e-932a-c27e8dcccbcc" />

** 14. Show products whose category is NOT IN (‘Electronics’, ‘Furniture’)
- <img width="970" height="237" alt="Screenshot 2026-06-06 231145" src="https://github.com/user-attachments/assets/c2114d46-b872-440d-be81-ee2703a3d607" />




###  ORDER BY & LIMIT
** 15. List all customers ordered by their Customer Name in ascending order.
- <img width="922" height="513" alt="Screenshot 2026-06-06 231219" src="https://github.com/user-attachments/assets/bb50dda0-3134-479b-9d57-bf0aeebbad8e" />

** 16. Display the top 3 products by price.
- <img width="667" height="367" alt="Screenshot 2026-06-06 231301" src="https://github.com/user-attachments/assets/8367a9a6-27da-4cc0-a2a5-37b8461364d3" />

** 17. List the top 3 most expensive products whose price is > 5,000, ordered by price DESC.
- <img width="986" height="335" alt="Screenshot 2026-06-06 231337" src="https://github.com/user-attachments/assets/d3738c76-1e8f-49e7-a227-9efce2601380" />

** 18. Show the number of customers in each city and order the result by customer count DESC.
- <img width="1082" height="527" alt="Screenshot 2026-06-06 231410" src="https://github.com/user-attachments/assets/3afd4d7e-6a23-49f9-8ea9-7ff0de15ca3a" />

** 19. Retrieve customers in (‘Chennai’, ‘Pune’, ‘Hyderabad’) and sort by name.
 - <img width="966" height="480" alt="Screenshot 2026-06-06 231436" src="https://github.com/user-attachments/assets/7056e683-52e3-4a1a-89ec-5949f896497c" />

** 20. Retrieve customers in given cities, display City + CustomerName, sorted by city and name.
- <img width="997" height="491" alt="Screenshot 2026-06-06 231505" src="https://github.com/user-attachments/assets/be19f2ac-1fc4-4d5d-af24-6b93266e68f5" />

** 21. List customers whose name starts with ‘A’ and sort by CustomerID.
- <img width="771" height="357" alt="Screenshot 2026-06-06 231534" src="https://github.com/user-attachments/assets/5c50a0fa-473e-4174-b02d-de7e64216e25" />



---

###  Aggregate Functions

```sql
SELECT COUNT(*) AS TotalCustomers FROM Customers;
```
**22. Find the total number of customers in the Customers table.
 - <img width="842" height="282" alt="Screenshot 2026-06-06 231601" src="https://github.com/user-attachments/assets/d150516e-3496-4921-a8a5-1a93cbe2ffad" />

---

###  GROUP BY & HAVING
** 23.Show the number of customers in each city.
- <img width="673" height="522" alt="Screenshot 2026-06-06 231629" src="https://github.com/user-attachments/assets/d3e56aa2-5bdf-4d01-95bd-276e20d69630" />
** 24.Show the total number of customers in each gender group.
- <img width="771" height="297" alt="Screenshot 2026-06-06 231707" src="https://github.com/user-attachments/assets/3994d2df-b6c9-4b55-9047-bb49e53db845" />
** 25.Display City and Customer Name grouped by city. 
- <img width="722" height="506" alt="Screenshot 2026-06-06 231741" src="https://github.com/user-attachments/assets/0a82cb96-4967-4bb3-b237-8cecc17df9f2" />
** 26.Show only those cities where customer count is greater than 2.
- <img width="802" height="355" alt="Screenshot 2026-06-06 231846" src="https://github.com/user-attachments/assets/a6c3ac95-6615-46c5-bde2-c41f7858a93d" />
** 27.Total orders per customer, but show only customers with more than 3 orders.
- <img width="902" height="316" alt="Screenshot 2026-06-06 231916" src="https://github.com/user-attachments/assets/57aa6cda-453e-46c9-8467-82199d35307a" />
** 28.Product ID and total quantity sold, but only products where total quantity is between 5 and 10
- <img width="1147" height="473" alt="Screenshot 2026-06-06 232002" src="https://github.com/user-attachments/assets/d7c46529-e530-4336-a735-713aa38570eb" />
** 29.Each category and its average price, but only categories where average price is greater than 5000.
- <img width="1083" height="325" alt="Screenshot 2026-06-06 232034" src="https://github.com/user-attachments/assets/dc67088b-45eb-41a6-8470-897df8c44279" />


 
---

###  JOINs
 ** 30. List all orders along with the customer names.
 - <img width="810" height="630" alt="Screenshot 2026-06-06 232206" src="https://github.com/user-attachments/assets/99d4c627-a56e-4034-ae31-018d603c5c80" />
** 31. Show all customers and their orders using LEFT JOIN.
- <img width="832" height="632" alt="Screenshot 2026-06-06 232536" src="https://github.com/user-attachments/assets/054d0480-c6d6-4905-b66d-560a54c89bcc" />
** 32.Show salesperson name and orders assigned to them (RIGHT JOIN).
- <img width="892" height="612" alt="Screenshot 2026-06-06 232630" src="https://github.com/user-attachments/assets/454e3d03-4ced-4f7f-85fe-f9913ff9d959" />
** 33.List all orders with Customer Name, Product Name, Quantity, and Order Date (ordered by OrderID).
- <img width="978" height="635" alt="Screenshot 2026-06-06 232757" src="https://github.com/user-attachments/assets/f26bb4bb-b8c8-4f6c-837b-f30a72b9415d" />
** 34.Display all orders from ‘Chennai’ customers with the product details.
- <img width="757" height="552" alt="Screenshot 2026-06-06 232843" src="https://github.com/user-attachments/assets/4296ae8a-bd81-430b-9223-8c155e1dd23b" />
** 35.Display all customers who purchased “Laptop”.
- <img width="672" height="458" alt="Screenshot 2026-06-06 232922" src="https://github.com/user-attachments/assets/b7ebfc4c-4c09-4880-bcb1-f8e59ae58099" />

---

### Built‑in Functions + Aggregation
** 36.Show total sales amount (Price × Quantity) for each order.
- <img width="735" height="605" alt="Screenshot 2026-06-06 233120" src="https://github.com/user-attachments/assets/336097a1-a9a2-4e86-bb8b-29431fd0fb0f" />

8. Find the top 5 customers by total purchase amount.
9. Show each Salesperson’s region and the total sales value.
10. Find the most sold product with total quantity.
11. Show the earliest (minimum) and latest (maximum) order date.


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









