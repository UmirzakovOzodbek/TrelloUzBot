# Task 1
## Question
**From the following table, write a SQL query to find the details of those salespeople who come from the 'Paris' City or 'Rome' City. Return salesman_id, name, city, commission.**
### Written code
```sql
SELECT * FROM salesman 
WHERE city = 'Paris' OR city = 'Rome'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221371919-c4ad95b6-d2e5-4f52-a1f8-74dba0d4375e.png)

____

# Task 2
## Question
**From the following table, write a SQL query to find the details of the salespeople who come from either 'Paris' or 'Rome'. Return salesman_id, name, city, commission.**
### Written code
```sql
SELECT * FROM salesman 
WHERE city IN('Paris','Rome')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221371956-988e90e3-8e70-4f0d-8deb-e4a067567c27.png)

____

# Task 3
## Question
**From the following table, write a SQL query to find the details of those salespeople who live in cities other than Paris and Rome. Return salesman_id, name, city, commission.**
### Written code
```sql
SELECT * FROM salesman 
WHERE city NOT IN('Paris','Rome')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221372034-43102e53-5483-470d-9060-9ac988aac0e5.png)

____

# Task 4
## Question
**From the following table, write a SQL query to retrieve the details of all customers whose ID belongs to any of the values 3007, 3008 or 3009. Return customer_id, cust_name, city, grade, and salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE customer_id IN (3007,3008,3009)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221372219-449dd90c-7325-4476-bed9-4b9fd27cf02f.png)

____

# Task 5
## Question
**From the following table, write a SQL query to find salespeople who receive commissions between 0.12 and 0.14 (begin and end values are included). Return salesman_id, name, city, and commission.**
### Written code
```sql
SELECT * FROM salesman 
WHERE commission BETWEEN 0.12 AND 0.14
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221372256-b17c2d42-453f-4844-900e-a75cb1f25475.png)

____

# Task 6
## Question
**From the following table, write a SQL query to select orders between 500 and 4000 (begin and end values are included). Exclude orders amount 948.50 and 1983.43. Return ord_no, purch_amt, ord_date, customer_id, and salesman_id.**
### Written code
```sql
SELECT * FROM orders 
WHERE (purch_amt BETWEEN 500 AND 4000) AND NOT purch_amt IN (948.50, 1983.43)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373511-33b67e40-60a6-45c1-b367-b834adc90b78.png)

____

# Task 7
## Question
**From the following table, write a SQL query to retrieve the details of the salespeople whose names begin with any letter between 'A' and 'L' (not inclusive). Return salesman_id, name, city, commission.**
### Written code
```sql
SELECT * FROM salesman 
WHERE name BETWEEN 'A' and 'L'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373529-eb379f79-15f2-4622-828f-a159fa58df86.png)

____

# Task 8
## Question
**From the following table, write a SQL query to find the details of all salespeople except those whose names begin with any letter between 'A' and 'L' (not inclusive). Return salesman_id, name, city, commission.**
### Written code
```sql
SELECT * FROM salesman 
WHERE name NOT BETWEEN 'A' and 'L'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373552-492100b5-e6bf-4703-9267-7c5259451295.png)

____

# Task 9
## Question
**From the following table, write a SQL query to retrieve the details of the customers whose names begins with the letter 'B'. Return customer_id, cust_name, city, grade, salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE cust_name LIKE 'B%'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373580-2270c7db-6757-4193-ad70-a30949d69572.png)

____

# Task 10
## Question
**From the following table, write a SQL query to find the details of the customers whose names end with the letter 'n'. Return customer_id, cust_name, city, grade, salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE cust_name LIKE '%n'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373653-1141da9b-8bb5-4c9d-a03b-ea631c48760c.png)

____

# Task 11
## Question
**From the following table, write a SQL query to find the details of those salespeople whose names begin with ‘N’ and the fourth character is 'l'. Rests may be any character. Return salesman_id, name, city, commission.**
### Written code
```sql
SELECT * FROM salesman 
WHERE name LIKE 'N__l%'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373680-5ce09856-bc6c-442c-9274-3da322ba5bc4.png)

____

# Task 12
## Question
**From the following table, write a SQL query to find those rows where col1 contains the escape character underscore ( _ ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 LIKE '%/_%' ESCAPE '/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373729-53968d84-fd02-4b00-9d76-9dfecd478a12.png)

____

# Task 13
## Question
**From the following table, write a SQL query to identify those rows where col1 does not contain the escape character underscore ( _ ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 NOT LIKE '%/_%' ESCAPE '/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373857-3027af1f-3d0b-4352-884e-c711213e104a.png)

____

# Task 14
## Question
**From the following table, write a SQL query to find rows in which col1 contains the forward slash character ( / ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 LIKE '%//%' ESCAPE '/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373886-0380a337-2370-4bab-ad39-cdb4d3dfcbb1.png)

____

# Task 15
## Question
**From the following table, write a SQL query to identify those rows where col1 does not contain the forward slash character ( / ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 NOT LIKE '%//%' ESCAPE '/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373910-b9951f85-4436-483b-9f8e-f2038fa98206.png)

____

# Task 16
## Question
**From the following table, write a SQL query to find those rows where col1 contains the string ( _/ ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 LIKE '%/_//%' ESCAPE '/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373945-52831fa9-ef9a-45ca-b65e-aae3e388eefa.png)

____

# Task 17
## Question
**From the following table, write a SQL query to find those rows where col1 does not contain the string ( _/ ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 NOT LIKE '%/_//%' ESCAPE '/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221373976-63aa95db-6124-4378-b5a6-3e2b9dac4c6e.png)

____

# Task 18
## Question
**From the following table, write a SQL query to find those rows where col1 contains the character percent ( % ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 LIKE '%/%%' ESCAPE'/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221374030-263f764e-661e-42ef-953f-af2f17f6eb6d.png)

____

# Task 19
## Question
**From the following table, write a SQL query to find those rows where col1 does not contain the character percent ( % ). Return col1.**
### Written code
```sql
SELECT * FROM testtable 
WHERE col1 NOT LIKE '%/%%' ESCAPE'/'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221374050-193e9e0a-6366-4f38-9949-1c4314279377.png)

____

# Task 20
## Question
**From the following table, write a SQL query to find all those customers who does not have any grade. Return customer_id, cust_name, city, grade, salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE grade IS NULL
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221374088-0e4b1612-7bda-4228-b618-87bc8bdb73e3.png)

____

# Task 21
## Question
**From the following table, write a SQL query to locate all customers with a grade value. Return customer_id, cust_name,city, grade, salesman_id.**
### Written code
```sql
SELECT * FROM customer 
WHERE NOT grade IS NULL
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221374104-8ffd2baa-77e9-4ab2-8703-0eb0298481d1.png)

____

# Task 22
## Question
**From the following table, write a SQL query to locate the employees whose last name begins with the letter 'D'. Return emp_idno, emp_fname, emp_lname and emp_dept.**
### Written code
```sql
SELECT * FROM emp_details 
WHERE emp_lname LIKE 'D%'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221374124-62b46951-4dd0-447a-b148-44840ef35112.png)

