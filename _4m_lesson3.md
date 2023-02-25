# Task 1
## Question
**Write a SQL statement that displays all the information about all salespeople**
### Written code
```sql
SELECT * FROM salesman
```
# Result
![Снимок экрана_20230225_193218](https://user-images.githubusercontent.com/122611764/221362568-d16da7f3-dcb1-4d0d-b2b1-1cef8964bdbd.png)

____

# Task 2
## Question
**Write a SQL statement to display a string "This is SQL Exercise, Practice and Solution".**
### Written code
```sql
SELECT "This is SQL Exercise, Practice and Solution"
```
# Result
![Снимок экрана_20230225_193638](https://user-images.githubusercontent.com/122611764/221362957-a9f72277-c2b6-415c-b92c-59e715cf6389.png)


____

# Task 3
## Question
**Write a SQL query to display three numbers in three columns.**
### Written code
```sql
SELECT 10, 20, 30
```
# Result
![Снимок экрана_20230225_193847](https://user-images.githubusercontent.com/122611764/221362967-b9e0a2e5-8ddb-4815-a4eb-2a2f42751be0.png)

____

# Task 4
## Question
**Write a SQL query to display the sum of two numbers 10 and 15 from the RDBMS server.**
### Written code
```sql
SELECT 10 + 15
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221362949-9a8e0d66-77bb-4252-a49e-573c2c9f0dc4.png)

____

# Task 5
## Question
**Write an SQL query to display the result of an arithmetic expression. **
### Written code
```sql
SELECT 12 + 20 - 6 * 2
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363055-6cd3dbd2-e905-4ee1-bb3f-0da44403051f.png)

____

# Task 6
## Question
**Write a SQL statement to display specific columns such as names and commissions for all salespeople.**
### Written code
```sql
SELECT name, commission FROM salesman
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363447-1592b330-4e02-47f4-b1db-a9134aa8176c.png)

____

# Task 7
## Question
**Write a query to display the columns in a specific order, such as order date, salesman ID, order number, and purchase amount for all orders.**
### Written code
```sql
SELECT ord_date, salesman_id, ord_no, purch_amt FROM orders
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363497-32fa952d-a8b8-4854-bebf-0db83197f918.png)

____

# Task 8
## Question
**From the following table, write a SQL query to identify the unique salespeople ID. Return salesman_id.**
### Written code
```sql
SELECT DISTINCT salesman_id FROM orders
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363531-007359b1-8fd2-4884-aeff-1cb115e3957c.png)

____

# Task 9
## Question
**From the following table, write a SQL query to locate salespeople who live in the city of 'Paris'. Return salesperson's name, city.**
### Written code
```sql
SELECT name,city FROM salesman 
WHERE city='Paris'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363561-75a822bd-252e-4611-a2b2-72cc51f39420.png)

____

# Task 10
## Question
**From the following table, write a SQL query to find customers whose grade is 200. Return customer_id, cust_name, city, grade, salesman_id.**
### Written code
```sql
SELECT *FROM customer 
WHERE grade=200
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363603-8af888e2-8bed-4e14-8f61-5c3e32abbfb1.png)

____

# Task 11
## Question
**From the following table, write a SQL query to find orders that are delivered by a salesperson with ID. 5001. Return ord_no, ord_date, purch_amt.**
### Written code
```sql
SELECT ord_no, ord_date, purch_amt FROM orders 
WHERE salesman_id=5001
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363636-c996a976-eb92-4340-ab56-ddce96bad318.png)

____

# Task 12
## Question
**From the following table, write a SQL query to find the Nobel Prize winner(s) for the year 1970. Return year, subject and winner. **
### Written code
```sql
SELECT year,subject,winner FROM nobel_win 
WHERE year=1970
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221363672-57bcbba3-32cd-4c20-b86d-bc545e043f4b.png)

____

# Task 13
## Question
**From the following table, write a SQL query to find the Nobel Prize winner in ‘Literature’ for 1970. Return winner.**
### Written code
```sql
SELECT winner FROM nobel_win 
WHERE year = 1970 AND subject = 'Literature'
```
# Result
![Снимок экрана_20230225_195713](https://user-images.githubusercontent.com/122611764/221364016-4b6edae4-67dd-42ee-b62b-06bfe5f03fbd.png)

____

# Task 14
## Question
**From the following table, write a SQL query to locate the Nobel Prize winner ‘Dennis Gabor'. Return year, subject.**
### Written code
```sql
SELECT year, subject FROM nobel_win 
WHERE winner = 'Dennis Gabor'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364030-1a3fbe31-d27d-48e5-81ce-ed22c403f538.png)

____

# Task 15
## Question
**From the following table, write a SQL query to locate the Nobel Prize winner ‘Dennis Gabor'. Return year, subject.**
### Written code
```sql
SELECT winner FROM nobel_win 
WHERE year>=1950 AND subject='Physics'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364091-80206675-423d-408e-b3a0-a4c926731f21.png)

____

# Task 16
## Question
**From the following table, write a SQL query to find the Nobel Prize winners in ‘Chemistry’ between the years 1965 and 1975. Begin and end values are included. Return year, subject, winner, and country.**
### Written code
```sql
SELECT year, subject, winner, country FROM nobel_win 
WHERE subject = 'Chemistry' AND year >= 1965 AND year <= 1975
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364155-785d0641-95c9-42ee-bf84-0d355cc0cc71.png)

____

# Task 17
## Question
**Write a SQL query to display all details of the Prime Ministerial winners after 1972 of Menachem Begin and Yitzhak Rabin.**
### Written code
```sql
SELECT * FROM nobel_win 
WHERE year >1972 AND winner IN ('Menachem Begin','Yitzhak Rabin')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364240-5082fe9c-038c-4203-ae55-b8a31d33d2f1.png)

____

# Task 18
## Question
**Write a SQL query to display all details of the Prime Ministerial winners after 1972 of Menachem Begin and Yitzhak Rabin.**
### Written code
```sql
SELECT * FROM nobel_win 
WHERE winner LIKE 'Louis%'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364274-8ee23939-6b53-4361-b240-3e2280de974a.png)

____

# Task 19
## Question
**From the following table, write a SQL query that combines the winners in Physics, 1970 and in Economics, 1971. Return year, subject, winner, country, and category.**
### Written code
```sql
SELECT * FROM nobel_win  
WHERE (subject ='Physics' AND year=1970) UNION (SELECT * FROM nobel_win  
WHERE (subject='Economics' AND year=1971))
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364372-d22269f6-4865-41e0-a7f2-26bdc22f8c78.png)

____

# Task 20
## Question
**From the following table, write a SQL query to find the Nobel Prize winners in 1970 excluding the subjects of Physiology and Economics. Return year, subject, winner, country, and category.**
### Written code
```sql
SELECT * FROM nobel_win 
WHERE year=1970 AND subject NOT IN('Physiology','Economics')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364412-9e605050-7d0f-4753-a148-872d4c59a123.png)

____

# Task 21
## Question
**From the following table, write a SQL query to combine the winners in 'Physiology' before 1971 and winners in 'Peace' on or after 1974. Return year, subject, winner, country, and category.**
### Written code
```sql
SELECT * FROM nobel_win 
WHERE (subject ='Physiology' AND year<1971) UNION (SELECT * FROM nobel_win 
WHERE (subject ='Peace' AND year>=1974))
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364755-afab5cf5-76df-4a91-b027-45a004ecb2d2.png)

____

# Task 22
## Question
**From the following table, write a SQL query to find the details of the Nobel Prize winner 'Johannes Georg Bednorz'. Return year, subject, winner, country, and category.**
### Written code
```sql
SELECT * FROM nobel_win 
WHERE winner='Johannes Georg Bednorz'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364813-05f3dcbf-55fc-4f34-8f30-9d1deb2eb860.png)

____

# Task 23
## Question
**From the following table, write a SQL query to find Nobel Prize winners for the subject that does not begin with the letter 'P'. Return year, subject, winner, country, and category. Order the result by year, descending and winner in ascending.**
### Written code
```sql
SELECT * FROM nobel_win 
WHERE subject NOT LIKE 'P%' ORDER BY year DESC, winner
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364861-2e6771c5-6aa9-4ba0-b167-3123b6dde9bc.png)

____

# Task 24
## Question
**From the following table, write a SQL query to find the details of 1970 Nobel Prize winners. Order the results by subject, ascending except for 'Chemistry' and ‘Economics’ which will come at the end of the result set. Return year, subject, winner, country, and category.**
### Written code
```sql
SELECT * FROM nobel_win
WHERE year=1970 
ORDER BY
 CASE
    WHEN subject IN ('Economics','Chemistry') THEN 1
    ELSE 0
 END ASC,
 subject,
 winner
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364947-bf4099a2-e289-49b7-b10a-a6300de71ebf.png)

____

# Task 25
## Question
**From the following table, write a SQL query to find the details of 1970 Nobel Prize winners. Order the results by subject, ascending except for 'Chemistry' and ‘Economics’ which will come at the end of the result set. Return year, subject, winner, country, and category.**
### Written code
```sql
SELECT * FROM item_mast 
WHERE pro_price BETWEEN 200 AND 600
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221364982-1d7d6e40-d585-465f-9fab-0860195c32bc.png)

____

# Task 26
## Question
**From the following table, write a SQL query to find the details of 1970 Nobel Prize winners. Order the results by subject, ascending except for 'Chemistry' and ‘Economics’ which will come at the end of the result set. Return year, subject, winner, country, and category.**
### Written code
```sql
SELECT AVG(pro_price) FROM item_mast 
WHERE pro_com=16
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365014-1a589470-e900-4df4-8286-c0eb9217dba9.png)

____

# Task 27
## Question
**From the following table, write a SQL query to display the pro_name as 'Item Name' and pro_priceas 'Price in Rs.'**
### Written code
```sql
SELECT pro_name as "Item Name", pro_price AS "Price in Rs." FROM item_mast
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365049-5caed0c1-dcdd-4698-b384-dbadbdd247e5.png)

____

# Task 28
## Question
**From the following table, write a SQL query to find the items whose prices are higher than or equal to $250. Order the result by product price in descending, then product name in ascending. Return pro_name and pro_price.**
### Written code
```sql
SELECT pro_name, pro_price FROM item_mast 
WHERE pro_price >= 250 
ORDER BY pro_price DESC, pro_name
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365086-1fabeb4f-c0ca-4645-9490-b312a2f5cf61.png)

____

# Task 29
## Question
**From the following table, write a SQL query to calculate average price of the items for each company. Return average price and company code.**
### Written code
```sql
SELECT AVG(pro_price), pro_com FROM item_mast 
GROUP BY pro_com
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365116-f4aead6b-a1d1-43d6-a1dc-33ddd0d89f1f.png)

____

# Task 30
## Question
**From the following table, write a SQL query to find the cheapest item(s). Return pro_name and, pro_price.**
### Written code
```sql
SELECT pro_name, pro_price FROM item_mast 
WHERE pro_price = (SELECT min(pro_price) FROM item_mast)
```
# Result
![Снимок экрана_20230225_202201](https://user-images.githubusercontent.com/122611764/221365172-b8be369f-7cc6-4cbf-ad71-e81de2a4f1fc.png)

____

# Task 31
## Question
**From the following table, write a SQL query to find the unique last name of all employees. Return emp_lname.**
### Written code
```sql
SELECT DISTINCT emp_lname FROM emp_details
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365219-ae1a8029-5669-4c46-9bd0-43e2119bbfb8.png)

____

# Task 32
## Question
**From the following table, write a SQL query to find the details of employees whose last name is 'Snares'. Return emp_idno, emp_fname, emp_lname, and emp_dept.**
### Written code
```sql
SELECT * FROM emp_details 
WHERE emp_lname= 'Snares'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365239-63664d4e-80e6-4ab5-8764-57549b420fbf.png)

____

# Task 33
## Question
**From the following table, write a SQL query to retrieve the details of the employees who work in the department 57. Return emp_idno, emp_fname, emp_lname and emp_dept.**
### Written code
```sql
SELECT * FROM emp_details 
WHERE emp_dept= 57
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221365265-58234375-839e-4110-a065-bf8c81225e5e.png)

