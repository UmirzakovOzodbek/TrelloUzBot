# Task 1
## Question
**From the following table, write a SQL query to calculate total purchase amount of all orders. Return total purchase amount.**
### Written code
```sql
SELECT sum(purch_amt) FROM orders
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221368891-61bb0177-87ab-4f42-84eb-7296e9335cfa.png)

____

# Task 2
## Question
**From the following table, write a SQL query to calculate the average purchase amount of all orders. Return average purchase amount.**
### Written code
```sql
SELECT avg(purch_amt) FROM orders
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221368921-08b3f35d-85b8-4eff-9393-52df864298c1.png)

____

# Task 3
## Question
**From the following table, write a SQL query that counts the number of unique salespeople. Return number of salespeople.**
### Written code
```sql
SELECT count(DISTINCT salesman_id) FROM orders
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221368956-697c2b66-0fa1-4d66-9f8c-5457942cacd1.png)

____

# Task 4
## Question
**From the following table, write a SQL query to count the number of customers. Return number of customers.**
### Written code
```sql
SELECT count(*) FROM customer
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369009-2eaf7b05-2577-4d65-af3b-8c10590bc1af.png)

____

# Task 5
## Question
**From the following table, write a SQL query to determine the number of customers who received at least one grade for their activity.**
### Written code
```sql
SELECT count(ALL grade) FROM customer
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369075-ce325117-9606-45f6-9da5-187ec9a0404e.png)

____

# Task 6
## Question
**From the following table, write a SQL query to find the maximum purchase amount.**
### Written code
```sql
SELECT max(purch_amt) FROM orders
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369102-73158b32-8e31-4f17-bfe7-8a27db03dc77.png)

____

# Task 7
## Question
**From the following table, write a SQL query to find the minimum purchase amount.**
### Written code
```sql
SELECT min(purch_amt) FROM orders
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369138-9d3e22c5-014d-415b-b3b7-21db7d19e3c5.png)

____

# Task 8
## Question
**From the following table, write a SQL query to find the highest grade of the customers in each city. Return city, maximum grade.**
### Written code
```sql
SELECT city, max(grade) FROM customer 
GROUP BY city
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369164-470561cb-ec91-4ddc-87c2-5cf698a3070d.png)

____

# Task 9
## Question
**From the following table, write a SQL query to find the highest purchase amount ordered by each customer. Return customer ID, maximum purchase amount.**
### Written code
```sql
SELECT customer_id, max(purch_amt) FROM orders 
GROUP BY customer_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369242-eafb409b-afd0-40f8-9b8e-fa969b7f41ea.png)

____

# Task 10
## Question
**From the following table, write a SQL query to find the highest purchase amount ordered by each customer on a particular date. Return, order date and highest purchase amount**
### Written code
```sql
SELECT customer_id, ord_date, max(purch_amt) FROM orders 
GROUP BY customer_id, ord_date
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369309-bcdce939-46d5-43cc-b9d6-126fe95a7162.png)

____

# Task 11
## Question
**From the following table, write a SQL query to find the highest purchase amount ordered by each customer on a particular date. Return, order date and highest purchase amount**
### Written code
```sql
SELECT salesman_id, max(purch_amt) FROM orders 
WHERE ord_date = '2012-08-17' 
GROUP BY salesman_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369347-40e3090a-d0ac-47bf-acbe-8b8a8d13df75.png)

____

# Task 12
## Question
**From the following table, write a SQL query to find the highest purchase amount ordered by each customer on a particular date. Return, order date and highest purchase amount**
### Written code
```sql
SELECT customer_id, ord_date, max(purch_amt) FROM orders 
GROUP BY customer_id, ord_date 
HAVING max(purch_amt) > 2000.00
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369399-c906710b-c2f4-49d1-9ade-be6afc8300e1.png)

____

# Task 13
## Question
**From the following table, write a SQL query to find the maximum order (purchase) amount in the range 2000 - 6000 (Begin and end values are included.) by combination of each customer and order date. Return customer id, order date and maximum purchase amount.**
### Written code
```sql
SELECT customer_id, ord_date, max(purch_amt) FROM orders 
GROUP BY customer_id, ord_date 
HAVING max(purch_amt) BETWEEN 2000 AND 6000
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369452-5a3f428c-1edd-4dcf-8a5a-389a7a677604.png)

____

# Task 14
## Question
**From the following table, write a SQL query to find the maximum order (purchase) amount based on the combination of each customer and order date. Filter the rows for maximum order (purchase) amount is either 2000, 3000, 5760, 6000. Return customer id, order date and maximum purchase amount.**
### Written code
```sql
SELECT customer_id, ord_date, max(purch_amt) FROM orders 
GROUP BY customer_id, ord_date 
HAVING max(purch_amt) IN (2000, 3000, 5760, 6000)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369566-94e4068a-3fe0-464f-8148-45693678e75b.png)

____

# Task 15
## Question
**From the following table, write a SQL query to determine the maximum order amount for each customer. The customer ID should be in the range 3002 and 3007(Begin and end values are included.). Return customer id and maximum purchase amount.**
### Written code
```sql
SELECT customer_id, max(purch_amt) FROM orders 
WHERE customer_id BETWEEN 3002 and 3007 
GROUP BY customer_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369609-6f8523e7-e819-4fe4-ab75-d8bfaf862b89.png)

____

# Task 16
## Question
**From the following table, write a SQL query to find the maximum order (purchase) amount for each customer. The customer ID should be in the range 3002 and 3007(Begin and end values are included.). Filter the rows for maximum order (purchase) amount is higher than 1000. Return customer id and maximum purchase amount.**
### Written code
```sql
SELECT customer_id, max(purch_amt) FROM orders 
WHERE customer_id BETWEEN 3002 and 3007 
GROUP BY customer_id 
HAVING max(purch_amt) > 1000
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369722-e7744e96-adc1-45cd-af71-ebffc6dbae1c.png)

____

# Task 17
## Question
**From the following table, write a SQL query to determine the maximum order (purchase) amount generated by each salesperson. Filter the rows for the salesperson ID is in the range 5003 and 5008 (Begin and end values are included.). Return salesperson id and maximum purchase amount.**
### Written code
```sql
SELECT salesman_id, max(purch_amt) FROM orders 
GROUP BY salesman_id 
HAVING salesman_id BETWEEN 5003 AND 5008
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369780-3789a1bf-a59f-40d2-9dcc-d5903a6023bf.png)

____

# Task 18
## Question
**From the following table, write a SQL query to count all the orders generated on '2012-08-17'. Return number of orders.**
### Written code
```sql
SELECT count(*) FROM orders 
WHERE ord_date='2012-08-17'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369819-acfc8fc7-e664-47a5-bf10-d1a52bcf64ae.png)

____

# Task 19
## Question
**From the following table, write a SQL query to count the number of salespeople in a city. Return number of salespeople.**
### Written code
```sql
SELECT count(*) FROM salesman 
WHERE city IS NOT NULL
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369846-c9d14fcf-54b2-4f9f-9720-cf4fbc8a9224.png)

____

# Task 20
## Question
**From the following table, write a SQL query to count the number of orders based on the combination of each order date and salesperson. Return order date, salesperson id.**
### Written code
```sql
SELECT ord_date, salesman_id, count(*) FROM orders 
GROUP BY ord_date,salesman_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369943-720472c1-a582-4c64-8aff-59da2ee872ba.png)

____

# Task 21
## Question
**From the following table, write a SQL query to calculate the average product price. Return average product price.**
### Written code
```sql
SELECT avg(pro_price) AS "Average Price" FROM item_mast
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221369973-e532c366-fb0c-4e18-9a64-709ae867a027.png)

____

# Task 22
## Question
**From the following table, write a SQL query to count the number of products whose price are higher than or equal to 350. Return number of products.**
### Written code
```sql
SELECT count(*) FROM item_mast 
WHERE pro_price >= 350
```
# Result
![Снимок экрана_20230225_222055](https://user-images.githubusercontent.com/122611764/221370763-b9ae7c60-b12c-40df-ac76-f006090dfa1c.png)

____

# Task 23
## Question
**From the following table, write a SQL query to compute the average price for unique companies. Return average price and company id.**
### Written code
```sql
SELECT avg(pro_price) AS "Average Price", pro_com AS "Company ID" FROM item_mast
GROUP BY pro_com
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221370980-7913f6ef-685c-4ae4-a3e4-a4c7fd642a5f.png)

____

# Task 24
## Question
**From the following table, write a SQL query to compute the sum of the allotment amount of all departments. Return sum of the allotment amount.**
### Written code
```sql
SELECT sum(dpt_allotment) FROM emp_department
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221371107-22a150b2-09e9-4d9f-9e4f-ce49f586683f.png)

____

# Task 25
## Question
**From the following table, write a SQL query to count the number of employees in each department. Return department code and number of employees**
### Written code
```sql
SELECT emp_dept, count(*) FROM emp_details 
GROUP BY emp_dept
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221371179-43890179-39b8-463d-a975-3201fc9e6493.png)



