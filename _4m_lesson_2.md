# Task 1
## Question
**Categories jadval barcha ustun ma’lumotlarini bilan qaytaring.**
### Query
```python
SELECT * FROM categories
```
# Result
![Снимок экрана_20230223_180352](https://user-images.githubusercontent.com/122611764/220935002-3ddbb7f9-afe1-4051-ad2c-a911f5e405a9.png)
 
 ____
 
# Task 2
## Question
**Categories jadval category_name va description ustun ma’lumotlarini qaytaring**
### Query
```python
SELECT category_name, description FROM categories
```
# Result

 ____
 
# Task 3
## Question
**Categories jadval barcha ustun ma’lumotlari olishda ustun nomlarini o’zbekcha tarjimada
qaytaring. M-n: category_name=Nomi**
### Query
```python
SELECT category_name as kategoriya_nomi, description as tavsifi, picture as rasm FROM categories
```
# Result

 ____
 
# Task 4
## Question
**Categories jadvaldan kategoriya nomi ’Confections’ ga teng bo’lgan ma’lumotlarni
qaytaring**
### Query
```python
SELECT * FROM categories
WHERE category_name = 'Confections'
```
# Result

 ____
 
# Task 5
## Question
**Categories jadvaldan kategoriya nomi ‘Produce’ yoki ‘Seafood’ bo’lgan ma’lumotlarni
qaytaring**
### Query
```python
SELECT * FROM categories
WHERE category_name = 'Produce' OR category_name = 'Seafood'
```
# Result

 ____
 
# Task 6
## Question
**Categories jadvaldan quyida belgilangan ma’lumotlarni qaytaring.**
![Снимок экрана_20230223_200704](https://user-images.githubusercontent.com/122611764/220946142-77ace279-47d3-48a8-8e30-5d6dfa1eacd7.png)

### Query
```python
SELECT * FROM categories
WHERE category_id BETWEEN 6 AND 8
```
# Result

 ____
 
# Task 7
## Question
**Categories jadvaldan ma’lumotlarni description alifbo bo’yicha Z-A tartibida chiqaring.**
### Query
```python
SELECT * FROM categories
ORDER BY description DESC -- ASC (A - Z)
```
# Result

 ____
 
# Task 8
## Question
**Customers jadvalidan barcha ma’lumotlarni oling.**
### Query
```python
SELECT * FROM customers
```
# Result

 ____
 
# Task 9
## Question
**Customers jadvalida ustun nomlarini o’zbekcha holatda oling.**
### Query
```python
SELECT customer_id AS mijoz_id,
       company_name AS kompaniya_nomi,
       contact_name AS kontak_nomi,
       contact_title AS kontak_sarlavhasi,
       address AS adres,
       city AS shahar,
       region AS hudud,
       postal_code AS pochta_kodi,
       country AS shahar,
       phone AS telefon,
       fax AS faks
FROM customers
```
# Result

 ____
 
# Task 10
## Question
**Customers jadvalidan contact_title ‘Owner’ bo’lgan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM customers
WHERE contact_title = 'Owner'
```
# Result

 ____
 
# Task 11
## Question
**Customers jadvalidan city ‘London’ bo’lgan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM customers
WHERE city = 'London'
```
# Result

 ____
 
# Task 12
## Question
**Customers jadvalidan region ustun NULL bo’lgan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM customers
WHERE region IS NULL
```
# Result

 ____
 
# Task 13
## Question
**Customers jadvalidan region ustun NULL bo’lmagan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM customers
WHERE region IS NOT NULL
```
# Result

 ____
 
# Task 14
## Question
**Customers jadvalidan country ustun Germany bo’lgan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM customers
WHERE country = 'Germany'
```
# Result

 ____
 
# Task 15
## Question
**Customers jadvalidan country ustun Germany bo’lgan qatorlar sonini qaytaring.**
### Query
```python
SELECT count(*) FROM customers
WHERE NOT country = 'Germany'
```
# Result

 ____
 
# Task 16
## Question
**Customers jadvalidan fax ustun NULL bo’lmalgan ma’lumotlarni contact_name ustun
alifbo tartiba tartiblab qaytaring.**
### Query
```python
SELECT * FROM customers
WHERE fax IS NOT NULL
ORDER BY contact_name
```
# Result

 ____
 
# Task 17
## Question
**Employees jadvaldan barcha ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM employees
```
# Result

 ____
 
# Task 18
## Question
**Employees jadval ustun nomlarini o’zbekcha qaytaring.**
### Query
```python
SELECT employee_id AS xodim_id,
       first_name AS ismi,
       last_name AS familiyasi,
       title AS sarlavhasi,
       address AS adres,
       title_of_courtesy AS xushmuomalalik_unvoni,
       birth_date AS "tug'ilgan sanasi",
       hire_date AS "ishga qabul qilish sanasi",
       address AS adres,
       city AS shahar,
       region AS hudud,
       postal_code AS pochta_kodi,
       country AS viloyat,
       home_phone AS "uy telefoni",
       extension AS kengaytma,
       photo AS rasm,
       photo_path AS "fotosurat yo'li",
       notes AS eslatmalar
FROM employees
```
# Result

 ____
 
# Task 19
## Question
**Employess jadvaldan title_of_courtest ‘Mr’ bo’lgan xodimlarni firts_name alifbo tartibida qaytaring.**
### Query
```python
SELECT * FROM employees
WHERE title_of_courtesy = 'Mr.'
ORDER BY first_name ASC
```
# Result

 ____
 
# Task 20
## Question
**Employes jadvalda title ‘Sales Representative’ bo’lgan xodimlar sonini qaytaring.**
### Query
```python
SELECT count(*) FROM employees
WHERE title = 'Sales Representative'
```
# Result

 ____
 
# Task 21
## Question
**Employes jadvalda hire_date 1994-yilda bo’lgan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM employees
WHERE hire_date BETWEEN '1994-01-01' AND '1994-12-31'
```
# Result

 ____
 
# Task 22
## Question
**Employes jadvaldan region NULL bo’lmagan xodimlarni first_name, last_name, title, city,
home_phone ma’lumotlarini first_name Z-A alifbo tartibida qaytaring.**
### Query
```python
SELECT first_name, last_name, title,city, home_phone FROM employees
ORDER BY first_name DESC
```
# Result

 ____
 
# Task 23
## Question
**Orders jadvaldan customer_id ‘VINET’ bo’lgan buyurtmalarni qaytaring.**
### Query
```python
SELECT * FROM orders
WHERE customer_id = 'VINET'
```
# Result

 ____
 
# Task 24
## Question
**Orders jadvaldan order_date ustuni orqali 1996-yildagi ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM orders
WHERE order_date BETWEEN '1996-01-01' AND '1996-12-31'
```
# Result

 ____
 
# Task 25
## Question
**Orders jadvaldan ship_region ustun NULL bo’lmagan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM orders
WHERE ship_region IS NOT NULL
```
# Result

 ____
 
# Task 26
## Question
**Orders jadvaldan order_id 10300 va 10400 orasida bo’lgan ma’lumotlarni qaytaring.**
### Query
```python
SELECT * FROM orders
WHERE order_id BETWEEN 10300 AND 10400
```
# Result

 ____
 
# Task 27
## Question
**Order Details jadvaldan unit_price ustun umumiy qiymatini qaytaring.**
### Query
```python
SELECT sum(unit_price) FROM order_details
```
# Result

