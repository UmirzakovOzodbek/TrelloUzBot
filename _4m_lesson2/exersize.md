# Task 1
## Question
**Categories jadval barcha ustun ma’lumotlarini bilan qaytaring.**
### Written code
```python
SELECT * FROM categories
```
# Result
![Снимок экрана_20230223_180352](https://user-images.githubusercontent.com/122611764/220935002-3ddbb7f9-afe1-4051-ad2c-a911f5e405a9.png)
  
 ____
 
# Task 2
## Question
**Categories jadval category_name va description ustun ma’lumotlarini qaytaring**
### Written code
```python
SELECT category_name, description FROM categories
```
# Result
![Снимок экрана_20230223_180539](https://user-images.githubusercontent.com/122611764/220952695-6eea2ccb-2ab6-47d4-b274-efae84e39cff.png)

 ____
 
# Task 3
## Question
**Categories jadval barcha ustun ma’lumotlari olishda ustun nomlarini o’zbekcha tarjimada
qaytaring. M-n: category_name=Nomi**
### Written code
```python
SELECT category_name as kategoriya_nomi, description as tavsifi, picture as rasm FROM categories
```
# Result
![Снимок экрана_20230223_181007](https://user-images.githubusercontent.com/122611764/220952976-669cb089-7937-47f4-9db2-f93d56499977.png)

 ____

# Task 4
## Question
**Categories jadvaldan kategoriya nomi ’Confections’ ga teng bo’lgan ma’lumotlarni
qaytaring**
### Written code
```python
SELECT * FROM categories
WHERE category_name = 'Confections'
```
# Result
![Снимок экрана_20230223_181135](https://user-images.githubusercontent.com/122611764/220953217-e5c60968-77ad-431d-99dc-8f504f6565fb.png)

 ____
 
# Task 5
## Question
**Categories jadvaldan kategoriya nomi ‘Produce’ yoki ‘Seafood’ bo’lgan ma’lumotlarni
qaytaring**
### Written code
```python
SELECT * FROM categories
WHERE category_name = 'Produce' OR category_name = 'Seafood'
```
# Result
![Снимок экрана_20230223_181502](https://user-images.githubusercontent.com/122611764/220953287-a9b3585e-0e54-4b5d-ade2-24ef74e2ab2c.png)

 ____
 
# Task 6
## Question
**Categories jadvaldan quyida belgilangan ma’lumotlarni qaytaring.**
![Снимок экрана_20230223_200704](https://user-images.githubusercontent.com/122611764/220946142-77ace279-47d3-48a8-8e30-5d6dfa1eacd7.png)

### Written code
```python
SELECT * FROM categories
LIMIT 3 OFFSET 5
```
# Result
![Снимок экрана_20230223_181647](https://user-images.githubusercontent.com/122611764/220953381-8684ae55-0152-4377-80be-807cb3956eaf.png)

 ____
 
# Task 7
## Question
**Categories jadvaldan ma’lumotlarni description alifbo bo’yicha Z-A tartibida chiqaring.**
### Written code
```python
SELECT * FROM categories
ORDER BY description DESC -- ASC (A - Z)
```
# Result
![Снимок экрана_20230223_181807](https://user-images.githubusercontent.com/122611764/220953480-d5f0b761-2020-4953-9130-2f6e69296e19.png)

 ____
 
# Task 8
## Question
**Customers jadvalidan barcha ma’lumotlarni oling.**
### Written code
```python
SELECT * FROM customers
```
# Result
![Снимок экрана_20230223_182040](https://user-images.githubusercontent.com/122611764/220953553-acd33167-223f-4f49-b365-1f3b69d2fd19.png)

 ____
 
# Task 9
## Question
**Customers jadvalida ustun nomlarini o’zbekcha holatda oling.**
### Written code
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
![Снимок экрана_20230223_182601](https://user-images.githubusercontent.com/122611764/220953742-d39b1f04-6575-486c-963a-088527d05ebb.png)
![Снимок экрана_20230223_182618](https://user-images.githubusercontent.com/122611764/220953775-19346c0d-ce29-4cea-a764-149935c20999.png)

 ____
 
# Task 10
## Question
**Customers jadvalidan contact_title ‘Owner’ bo’lgan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM customers
WHERE contact_title = 'Owner'
```
# Result
![Снимок экрана_20230223_182849](https://user-images.githubusercontent.com/122611764/220953928-36ee2c5f-a72c-4d3b-b532-8605aeeeaeed.png)

 ____
 
# Task 11
## Question
**Customers jadvalidan city ‘London’ bo’lgan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM customers
WHERE city = 'London'
```
# Result
![Снимок экрана_20230223_183119](https://user-images.githubusercontent.com/122611764/220954258-4ac09bd9-5eff-44aa-ad38-c676861fae07.png)

 ____
 
# Task 12
## Question
**Customers jadvalidan region ustun NULL bo’lgan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM customers
WHERE region IS NULL
```
# Result
![Снимок экрана_20230223_183240](https://user-images.githubusercontent.com/122611764/220954294-a42210ef-f3bc-4c7d-b16d-5f4b1ea1e0af.png)

 ____
 
# Task 13
## Question
**Customers jadvalidan region ustun NULL bo’lmagan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM customers
WHERE region IS NOT NULL
```
# Result
![Снимок экрана_20230223_183551](https://user-images.githubusercontent.com/122611764/220954352-3f96b833-4b19-4b8a-97eb-d3d1b5909539.png)

 ____
 
# Task 14
## Question
**Customers jadvalidan country ustun Germany bo’lgan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM customers
WHERE country = 'Germany'
```
# Result
![Снимок экрана_20230223_183756](https://user-images.githubusercontent.com/122611764/220954432-196107c7-69ab-4403-83bf-a74d014b4c64.png)

 ____
 
# Task 15
## Question
**Customers jadvalidan country ustun Germany bo’lgan qatorlar sonini qaytaring.**
### Written code
```python
SELECT count(*) FROM customers
WHERE country = 'Germany'
```
# Result
![Снимок экрана_20230223_203351](https://user-images.githubusercontent.com/122611764/220954759-2263d969-5734-474a-af17-3df4346a346e.png)

 ____
 
# Task 16
## Question
**Customers jadvalidan fax ustun NULL bo’lmalgan ma’lumotlarni contact_name ustun
alifbo tartiba tartiblab qaytaring.**
### Written code
```python
SELECT * FROM customers
WHERE fax IS NOT NULL
ORDER BY contact_name
```
# Result
![Снимок экрана_20230223_184718](https://user-images.githubusercontent.com/122611764/220955392-ee49e63e-b89e-42b5-933c-b12074b84841.png)
![Снимок экрана_20230223_185012](https://user-images.githubusercontent.com/122611764/220955407-0db35679-ace9-48ba-90a8-77b91f2c0e5d.png)

 ____
 
# Task 17
## Question
**Employees jadvaldan barcha ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM employees
```
# Result
![Снимок экрана_20230223_185143](https://user-images.githubusercontent.com/122611764/220959854-36b910e8-3d23-479c-bbf3-29bd928ca552.png)


 ____
 
# Task 18
## Question
**Employees jadval ustun nomlarini o’zbekcha qaytaring.**
### Written code
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
![Снимок экрана_20230223_190116](https://user-images.githubusercontent.com/122611764/220956344-cb42a01b-12cf-4e02-8ef3-bf73ed644bd8.png)
![Снимок экрана_20230223_190136](https://user-images.githubusercontent.com/122611764/220956361-1aeba49d-7cbb-40c4-9644-d8aeaabdbedf.png)

 ____
 
# Task 19
## Question
**Employess jadvaldan title_of_courtest ‘Mr’ bo’lgan xodimlarni firts_name alifbo tartibida qaytaring.**
### Written code
```python
SELECT * FROM employees
WHERE title_of_courtesy = 'Mr.'
ORDER BY first_name ASC
```
# Result
![Снимок экрана_20230223_190550](https://user-images.githubusercontent.com/122611764/220956413-46c317cd-2990-47c8-8d93-91b27a88d70e.png)

 ____
 
# Task 20
## Question
**Employes jadvalda title ‘Sales Representative’ bo’lgan xodimlar sonini qaytaring.**
### Written code
```python
SELECT count(*) FROM employees
WHERE title = 'Sales Representative'
```
# Result
![Снимок экрана_20230223_190753](https://user-images.githubusercontent.com/122611764/220956767-dfdbfce8-2c81-4392-ab39-a07ab2a68cf5.png)

 ____
 
# Task 21
## Question
**Employes jadvalda hire_date 1994-yilda bo’lgan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM employees
WHERE hire_date BETWEEN '1994-01-01' AND '1994-12-31'
```
# Result
![Снимок экрана_20230223_190928](https://user-images.githubusercontent.com/122611764/220956933-7bf90f0f-68b2-4d99-bf4e-af2a537d560e.png)

 ____
 
# Task 22
## Question
**Employes jadvaldan region NULL bo’lmagan xodimlarni first_name, last_name, title, city,
home_phone ma’lumotlarini first_name Z-A alifbo tartibida qaytaring.**
### Written code
```python
SELECT first_name, last_name, title,city, home_phone FROM employees
ORDER BY first_name DESC
```
# Result
![Снимок экрана_20230223_191034](https://user-images.githubusercontent.com/122611764/220957028-05ecdea7-6e0e-4a7d-a325-427055c2db5d.png)

 ____
 
# Task 23
## Question
**Orders jadvaldan customer_id ‘VINET’ bo’lgan buyurtmalarni qaytaring.**
### Written code
```python
SELECT * FROM orders
WHERE customer_id = 'VINET'
```
# Result
![Снимок экрана_20230223_191224](https://user-images.githubusercontent.com/122611764/220957081-22648604-325f-4e18-b8ff-4d25c2c62e13.png)

 ____
 
# Task 24
## Question
**Orders jadvaldan order_date ustuni orqali 1996-yildagi ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM orders
WHERE order_date BETWEEN '1996-01-01' AND '1996-12-31'
```
# Result
![Снимок экрана_20230223_191329](https://user-images.githubusercontent.com/122611764/220957256-5b728c5e-ba5b-4a28-8026-577032476da3.png)
![Снимок экрана_20230223_205646](https://user-images.githubusercontent.com/122611764/220961023-a2445f5b-06d1-4ac6-818b-11ad51ffe14d.png)

 ____
 
# Task 25
## Question
**Orders jadvaldan ship_region ustun NULL bo’lmagan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM orders
WHERE ship_region IS NOT NULL
```
# Result
![Снимок экрана_20230223_191517](https://user-images.githubusercontent.com/122611764/220957324-23828241-276f-4424-a5c5-48952648558f.png)

 ____
 
# Task 26
## Question
**Orders jadvaldan order_id 10300 va 10400 orasida bo’lgan ma’lumotlarni qaytaring.**
### Written code
```python
SELECT * FROM orders
WHERE order_id BETWEEN 10300 AND 10400
```
# Result
![Снимок экрана_20230223_204624](https://user-images.githubusercontent.com/122611764/220958102-69c77e42-bb18-472c-8be0-5cbf3b7bc78e.png)
![Снимок экрана_20230223_191704](https://user-images.githubusercontent.com/122611764/220957792-22330f3c-c1d9-4120-a933-b616765dc1cc.png)

 ____
 
# Task 27
## Question
**Order Details jadvaldan unit_price ustun umumiy qiymatini qaytaring.**
### Written code
```python
SELECT sum(unit_price) FROM order_details
```
# Result
![Снимок экрана_20230223_191934](https://user-images.githubusercontent.com/122611764/220958176-5b16bc3c-0713-49de-8ddc-d6d275b60b35.png)

