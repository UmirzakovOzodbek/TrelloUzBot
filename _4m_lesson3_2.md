# Task 1
## Question
**From the following table, write a SQL query to locate the details of customers with grade values above 100. Return customer_id, cust_name, city, grade, and salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE grade > 100
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365553-bd487d7b-072e-4a0a-97ff-82fb517a0efc.png)

____

# Task 2
## Question
**From the following table, write a SQL query to find all the customers in ‘New York’ city who have a grade value above 100. Return customer_id, cust_name, city, grade, and salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE city = 'New York' AND grade > 100
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365706-00adb03e-7916-46c9-83a7-8a1f2aa90a64.png)

____

# Task 3
## Question
**From the following table, write a SQL query to find all the customers in ‘New York’ city who have a grade value above 100. Return customer_id, cust_name, city, grade, and salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE city = 'New York' OR grade > 100
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365754-75b91273-c225-4bff-9b19-143be3410c28.png)

____

# Task 4
## Question
**From the following table, write a SQL query to find customers who are either from the city 'New York' or who do not have a grade greater than 100. Return customer_id, cust_name, city, grade, and salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE city = 'New York' OR NOT grade > 100
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365819-4657eb21-a78e-4aad-b760-ec16ca1799cb.png)

____

# Task 5
## Question
**From the following table, write a SQL query to identify customers who do not belong to the city of 'New York' or have a grade value that exceeds 100. Return customer_id, cust_name, city, grade, and salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE NOT (city = 'New York' OR grade > 100)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365859-0a31729d-c8c8-41be-965c-7d1632addfbe.png)

____

# Task 6
## Question
**From the following table, write a SQL query to find details of all orders excluding those with ord_date equal to '2012-09-10' and salesman_id higher than 5005 or purch_amt greater than 1000.Return ord_no, purch_amt, ord_date, customer_id and salesman_id.**
### Written code
```sql
SELECT * FROM  orders 
WHERE NOT ((ord_date = '2012-09-10' AND salesman_id > 5005) OR purch_amt > 1000.00)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365894-1c631d2b-e1d8-400c-bc8d-22ad5b80fcf3.png)

____

# Task 7
## Question
**From the following table, write a SQL query to find the details of those salespeople whose commissions range from 0.10 to0.12. Return salesman_id, name, city, and commission.**
### Written code
```sql
SELECT salesman_id, name,city, commission FROM salesman 
WHERE (commission > 0.10 AND commission < 0.12)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365939-528efb5e-ef92-46fb-8208-afcc5a97bbf0.png)

____

# Task 8
## Question
**From the following table, write a SQL query to find details of all orders with a purchase amount less than 200 or exclude orders with an order date greater than or equal to '2012-02-10' and a customer ID less than 3009. Return ord_no, purch_amt, ord_date, customer_id and salesman_id.**
### Written code
```sql
SELECT * FROM  orders 
WHERE(purch_amt < 200 OR NOT(ord_date >= '2012-02-10' AND customer_id < 3009))
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365973-140187cb-80d8-4b74-923b-6a1689879975.png)

____

# Task 9
## Question
**From the following table, write a SQL query to find all orders that meet the following conditions. Exclude combinations of order date equal to '2012-08-17' or customer ID greater than 3005 and purchase amount less than 1000.**
### Written code
```sql
SELECT * FROM  orders 
WHERE NOT((ord_date = '2012-08-17' OR customer_id > 3005) AND purch_amt < 1000)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221366020-cb548fb1-f0af-4fb7-bb26-0c2d74912b27.png)

____

# Task 10
## Question
**Write a SQL query that displays order number, purchase amount, and the achieved and unachieved percentage (%) for those orders that exceed 50% of the target value of 6000.**
### Written code
```sql
SELECT ord_no, purch_amt,
    100 * purch_amt / 6000 AS "Achieved%",
    100 - (100 * purch_amt / 6000) AS "Unachieved%"
FROM orders
WHERE purch_amt > 0.5 * 6000
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221366072-be96c95a-7eaa-4d88-85c5-5b7224952ff1.png)

____

# Task 11
## Question
**From the following table, write a SQL query to find the details of all employees whose last name is ‘Dosni’ or ‘Mardy’. Return emp_idno, emp_fname, emp_lname, and emp_dept.**
### Written code
```sql
SELECT *  FROM emp_details  
WHERE emp_lname = 'Dosni' OR emp_lname = 'Mardy'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221366297-bdefaf20-5ab6-499d-84a6-4a39eb1f6a8c.png)

____

# Task 12
## Question
**From the following table, write a SQL query to find the employees who work at depart 47 or 63. Return emp_idno, emp_fname, emp_lname, and emp_dept.**
### Written code
```sql
SELECT * FROM emp_details 
WHERE emp_dept = 47 OR emp_dept = 63
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221366347-77e468c3-82c1-41ed-9ae9-dbb750d4a704.png)
