# 📊 data-analyst-sql-portfollio-sales-analystics-queries

This repository contains a comprehensive set of SQL queries for the **Sales_Analytics** database.  
It covers **fundamental to advanced SQL concepts** with placeholders
This repository offers a well‑structured collection of SQL queries designed for the Sales_Analytics database. It spans from fundamental to advanced concepts, making it useful for learners and professionals alike. Each query is accompanied by placeholders where screenshots of the results can be added, ensuring the documentation is both practical and visually informative.
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

** 37. Find the top 5 customers by total purchase amount.
- <img width="670" height="492" alt="Screenshot 2026-06-06 233217" src="https://github.com/user-attachments/assets/b28f895d-e3ef-40ab-8dfb-32d24201e2d2" />

** 38. Show each Salesperson’s region and the total sales value.
- <img width="725" height="442" alt="Screenshot 2026-06-06 233302" src="https://github.com/user-attachments/assets/5fd4faa0-43f2-4021-891b-0671b941ba56" />

** 39. Find the most sold product with total quantity.
- <img width="590" height="382" alt="Screenshot 2026-06-06 233359" src="https://github.com/user-attachments/assets/a57b48d8-18ac-4ab1-b4ac-ee0cfbdd1382" />

** 40. Show the earliest (minimum) and latest (maximum) order date.
- <img width="751" height="295" alt="Screenshot 2026-06-06 233456" src="https://github.com/user-attachments/assets/000d291f-ec10-42c8-90c8-990ce93b4389" />



---

###  Window Functions
** 41.	Display each order with the total number of orders placed by that customer using a window function.
- <img width="1032" height="555" alt="Screenshot 2026-06-06 233719" src="https://github.com/user-attachments/assets/51cf0419-0834-456b-a158-2355f3276343" />

** 42.	Show each product with its price and the average price of all products.
- <img width="817" height="542" alt="Screenshot 2026-06-06 233846" src="https://github.com/user-attachments/assets/64cc464b-4189-45e8-a5c7-4f3195fbc59e" />
** 43.	Rank all products based on price from highest to lowest using a window function.
- <img width="923" height="592" alt="Screenshot 2026-06-06 233936" src="https://github.com/user-attachments/assets/c80d44c8-422e-4d20-baa5-4f1d5b1f6400" />
** 44.	Display each order with the total quantity ordered by that salesperson.
- <img width="825" height="558" alt="Screenshot 2026-06-06 234039" src="https://github.com/user-attachments/assets/607cf25b-a893-4d88-8c26-80dd6183e5b6" />

**45.	Rank salespersons based on the total sales amount they generated.
- <img width="787" height="488" alt="Screenshot 2026-06-06 234126" src="https://github.com/user-attachments/assets/0f06cb36-e6b5-414b-92a7-6e74852cabc6" />

**46.	Show product price ranking within each category using PARTITION BY.
- <img width="903" height="597" alt="Screenshot 2026-06-06 234234" src="https://github.com/user-attachments/assets/d61853f3-0a7b-4d7b-87c0-8da4b813ce2a" />

**47.	Display the previous order date for each customer using LAG() function.
- <img width="836" height="572" alt="Screenshot 2026-06-06 234339" src="https://github.com/user-attachments/assets/d9f72abc-d768-4c76-8568-f773072ec8f5" />

**48.	Display the next order date for each customer using LEAD() function.
- <img width="921" height="596" alt="Screenshot 2026-06-06 234443" src="https://github.com/user-attachments/assets/4f9431c4-576f-4c72-b7f9-f3228054d612" />
** 49.	Calculate the running total of sales amount by order date.
- <img width="811" height="561" alt="Screenshot 2026-06-06 234537" src="https://github.com/user-attachments/assets/68c627db-c58e-4aad-9899-292cea1f7a54" />

** 50.	Display the top 3 most expensive products using DENSE_RANK()
- <img width="782" height="468" alt="Screenshot 2026-06-06 234934" src="https://github.com/user-attachments/assets/52aa6f1d-be9b-4558-98d2-dbe4b4f7aebb" />




---

###  Date & Time Functions
**51.Find all orders placed in January 2025.
- <img width="653" height="568" alt="Screenshot 2026-06-06 235320" src="https://github.com/user-attachments/assets/d6ab2b85-5901-431e-a004-199707668aa5" />

**52. List orders week-wise (show week number and total orders).
- <img width="763" height="396" alt="Screenshot 2026-06-06 235412" src="https://github.com/user-attachments/assets/bcff9716-72b0-4ab0-af77-0641451cf1a7" />

**53. Display orders along with the day name (Monday, Tuesday, etc.).
- <img width="720" height="597" alt="Screenshot 2026-06-06 235528" src="https://github.com/user-attachments/assets/0d97c888-f757-4717-896f-e2e6fd4b8975" />

**54. Extract day name and display total sales amount and quantity per day of week (ordered Monday → Sunday).
- <img width="1115" height="562" alt="Screenshot 2026-06-06 235719" src="https://github.com/user-attachments/assets/befb65ac-6ee4-4889-9b34-fb357c5f751c" />



---

###  Subqueries 
 ### SINGLE ROW SUBQUERIES

55.	Find customers who live in the same city as 'Arjun Kumar'.
-<img width="732" height="485" alt="Screenshot 2026-06-06 235917" src="https://github.com/user-attachments/assets/fe34a243-3f66-494d-b249-b38289d6c49d" />
    
56.	Find products that are more expensive than the average product price.
- <img width="887" height="445" alt="Screenshot 2026-06-07 000014" src="https://github.com/user-attachments/assets/4e2c9338-cc37-47e9-9a49-cdbf31cd9960" />

57.	Find products belonging to the same category as 'Laptop'.
- <img width="642" height="553" alt="Screenshot 2026-06-07 000111" src="https://github.com/user-attachments/assets/a539468c-cc4e-412e-b13e-efeb96e1aa0d" />

58.	Find customers who have placed more orders than the customer with CustomerID = 5.
- <img width="933" height="545" alt="Screenshot 2026-06-07 000219" src="https://github.com/user-attachments/assets/e1c4fc02-1f95-47ee-93da-09f6ed14df19" />


59.	Find products that are priced higher than the product with ProductID = 3.
- <img width="892" height="455" alt="Screenshot 2026-06-07 000307" src="https://github.com/user-attachments/assets/6fd67c57-f884-446c-834b-1e796cad7dde" />

60.	Find customers who placed an order on the same date as OrderID = 1.
- <img width="886" height="406" alt="Screenshot 2026-06-07 000424" src="https://github.com/user-attachments/assets/f3eaf2fc-f011-46d8-b37b-ec89fac3c9fa" />

61.	Find the salesperson whose target amount is higher than the average target.
- <img width="941" height="453" alt="Screenshot 2026-06-07 000511" src="https://github.com/user-attachments/assets/dfe36fbe-75ec-4f76-9c30-1af2ef3eb163" />

### MULTI ROW SUBQUERIES

62.	Find customers who have ordered any product in the 'Electronics' category.
- <img width="962" height="542" alt="Screenshot 2026-06-07 000706" src="https://github.com/user-attachments/assets/dbf47af1-8cf7-4262-b646-84c6db947c4b" />

63.	Find products that were ordered by customers from Chennai.
 - <img width="837" height="492" alt="Screenshot 2026-06-07 000759" src="https://github.com/user-attachments/assets/aa66d4ee-0a72-4199-b14f-381a2abd69f1" />

64.	Find salespersons who handled orders for customers from Bangalore.
 - <img width="815" height="537" alt="Screenshot 2026-06-07 000855" src="https://github.com/user-attachments/assets/3e08c54a-33d4-4645-884a-77914b4e80f7" />

65.	Find products whose price is greater than ALL products in the Furniture category.
 - <img width="1041" height="448" alt="Screenshot 2026-06-07 000942" src="https://github.com/user-attachments/assets/e051b8b2-88a9-419f-b751-c4667f97c010" />

66.	Find products whose price is greater than ANY Electronics product.
 - <img width="887" height="577" alt="Screenshot 2026-06-07 001033" src="https://github.com/user-attachments/assets/c11f46e5-f2bc-4ae4-b2f3-7d8dce916eac" />

67.	Find customers who purchased products costing more than 10000.
- <img width="798" height="543" alt="Screenshot 2026-06-07 001109" src="https://github.com/user-attachments/assets/b62dcacd-ea36-40bd-b235-1d71131266e5" />

### CORRELATED SUBQUERIES

68.	Find customers who have placed at least one order.
 -<img width="777" height="511" alt="Screenshot 2026-06-07 001445" src="https://github.com/user-attachments/assets/d837d824-cb77-4e8d-9c6e-a2c421946fd6" />

69.	Find customers who have placed more than 2 orders.
 - <img width="720" height="518" alt="Screenshot 2026-06-07 001540" src="https://github.com/user-attachments/assets/f7f83aba-0f5a-4c96-819f-141e278897fb" />

70.	Find products that have been ordered more than once.
 - <img width="855" height="510" alt="Screenshot 2026-06-07 001643" src="https://github.com/user-attachments/assets/8093e996-3c95-4cce-be13-15fdabb1aa35" />

71.	Find salespersons who have handled more than 3 orders.
 - <img width="842" height="582" alt="Screenshot 2026-06-07 001733" src="https://github.com/user-attachments/assets/f11c5053-c8a1-4d29-89a6-8c7c133dd63f" />

72.	Find customers who have purchased products more expensive than the average product price in that category.
- <img width="1178" height="638" alt="Screenshot 2026-06-07 001841" src="https://github.com/user-attachments/assets/aa1af903-8e0a-4dc3-ac8f-2366d2446f59" />

73.	Find products whose price is greater than the average price of their category.
- <img width="1047" height="497" alt="Screenshot 2026-06-07 001950" src="https://github.com/user-attachments/assets/3d36ec20-2d5d-4a5e-8f54-443961afc382" />

74.	Find customers whose total orders are greater than the average number of orders placed by customers.
- <img width="1102" height="513" alt="Screenshot 2026-06-07 002122" src="https://github.com/user-attachments/assets/4efeac21-024e-4c0b-b823-60d8215c4f17" />


________________________________________



---

## 🚀 How to Use
1. Clone the repository.  
2. Run queries on the **Sales_Analytics** database.  
3. Save query results as screenshots (`.png`) inside the `/screenshots` folder.  
4. Replace placeholders in README with actual screenshots.  

---









