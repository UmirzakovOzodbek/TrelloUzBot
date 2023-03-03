# Task 1
### Written code
```sql
SELECT e.first_name, e.last_name, e.department_id, d.department_name 
FROM employees e 
JOIN departments d 
ON e.department_id = d.department_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221925319-53375a5f-88e6-4f76-a2d9-10cba865a1a1.png)

____

# Task 2
### Written code
```sql
SELECT e.first_name, e.last_name, d.department_name, l.city, l.state_province 
FROM employees e 
JOIN departments d ON e.department_id = d.department_id 
JOIN locations l ON d.location_id = l.location_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221927110-fac49b0a-97b4-4df7-8e75-5e801e6cdfdd.png)

____

# Task 3
### Written code
```sql
SELECT e.first_name, e.last_name, e.salary, j.grade_level 
FROM employees e 
JOIN job_grades j 
ON e.salary BETWEEN j.lowest_sal AND j.highest_sal
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221927666-fbebe294-811c-4969-ab5b-ccc3fbbe0798.png)

____

# Task 4
### Written code
```sql
SELECT e.first_name, e.last_name, e.department_id,  d.department_name 
FROM employees e 
JOIN departments d 
ON e.department_id = d.department_id AND e.department_id IN (80, 40) 
ORDER BY e.last_name
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221928168-d10b7214-3c6e-4f88-81df-2bfd70875ad9.png)

____

# Task 5
### Written code
```sql
SELECT e.first_name, e.last_name, d.department_name, l.city, l.state_province 
FROM employees e 
JOIN departments d  ON e.department_id = d.department_id 
JOIN locations l ON d.location_id = l.location_id 
WHERE e.first_name LIKE '%z%'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221928704-d6746818-96a4-417f-8986-65b5882f79e4.png)

____

# Task 6
### Written code
```sql
SELECT e.first_name, e.last_name, d.department_id, d.department_name 
FROM employees e 
RIGHT OUTER JOIN departments d 
ON e.department_id = d.department_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221929577-17c1a6d3-cb72-4ec1-b613-2ee454d1f2ab.png)

____

# Task 7
### Written code
```sql
SELECT e.first_name, e.last_name, e.salary 
FROM employees e 
JOIN employees emp ON e.salary < emp.salary AND emp.employee_id = 182
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221931056-7e747102-3abd-4caa-8526-f1993e89e775.png)

____

# Task 8
### Written code
```sql
SELECT e.first_name AS "Employee Name", emp.first_name AS "Manager name" FROM employees e 
JOIN employees emp ON e.manager_id = emp.employee_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221932135-48c4ff88-32f2-45bc-a456-9ac88371de88.png)

____

# Task 9
### Written code
```sql
SELECT d.department_name, l.city, l.state_province 
FROM  departments d 
JOIN locations l ON  d.location_id = l.location_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221932389-d857b8f0-a758-4392-9dea-56939f743707.png)

____

# Task 10
### Written code
```sql
SELECT e.first_name, e.last_name, e.department_id, d.department_name 
FROM employees e 
LEFT OUTER JOIN departments d ON e.department_id = d.department_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221933563-3feca6d4-bd9e-4a89-8cff-3a3a3112a7d2.png)

____

# Task 11
### Written code
```sql
SELECT e.first_name AS "Employee Name", emp.first_name AS "Manager name" 
FROM employees e 
LEFT OUTER JOIN employees emp ON e.manager_id = emp.employee_id   
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221934923-77b30700-32b2-407d-b21f-807a3717d788.png)

____

# Task 12
### Written code
```sql
SELECT e.first_name, e.last_name, e.department_id 
FROM employees e 
JOIN employees emp ON e.department_id = emp.department_id AND emp.last_name = 'Taylor'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221935348-61be3e00-635b-4721-bf51-571440e03dc6.png)

____

# Task 13
### Written code
```sql
SELECT job_title, department_name, first_name || ' ' || last_name AS Employee_name, start_date 
FROM job_history 
JOIN jobs USING (job_id) 
JOIN departments USING (department_id) 
JOIN  employees USING (employee_id) 
WHERE start_date >= '1993-01-01' AND start_date <= '1997-08-31'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221936266-b77c09a2-ffc0-4bc4-97d5-43a425f3a461.png)

____

# Task 14
### Written code
```sql
SELECT job_title, first_name || ' ' || last_name AS Employee_name, max_salary-salary AS salary_difference 
FROM employees 
NATURAL JOIN jobs
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221938630-f13631ae-aa89-49e9-8bf8-682021b03e72.png)

____

# Task 15
### Written code
```sql
SELECT department_name, avg(salary), count(commission_pct) 
FROM departments 
JOIN employees USING (department_id) 
GROUP BY department_name
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221939506-deb42634-4661-4271-90e8-17c6a3ac7385.png)

____

# Task 16
### Written code
```sql
SELECT job_title, first_name || ' ' || last_name AS Employee_name, max_salary-salary AS salary_difference 
FROM employees 
NATURAL JOIN jobs 
WHERE department_id = 80
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221939727-20544688-fb2a-4dcb-a0f0-e3e2417607b3.png)

____

# Task 17
### Written code
```sql
SELECT country_name,city, department_name 
FROM countries 
JOIN locations USING (country_id) 
JOIN departments USING (location_id)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221940167-e491f8c3-9f19-43c5-8939-814aee19bc31.png)

____

# Task 18
### Written code
```sql
SELECT department_name, first_name || ' ' || last_name AS "Manager name" 
FROM departments d 
JOIN employees e ON d.manager_id = e.employee_id
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221940846-42642a35-8350-453e-b3a4-bd9c5f6ef7ad.png)

____

# Task 19
### Written code
```sql
SELECT job_title, avg(salary) FROM employees 
NATURAL JOIN jobs 
GROUP BY job_title
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221941081-62c78ebf-40a6-42f0-ae19-8eca3a0e6d81.png)

____

# Task 20
### Written code
```sql
SELECT job.* FROM job_history job 
JOIN employees emp ON job.employee_id = emp.employee_id 
WHERE salary >= 12000
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221941496-1cd1ec37-492d-48d1-a7b5-e5a6b5c9aef6.png)

____

# Task 21
### Written code
```sql
SELECT country_name, city, count(department_id) 
FROM countries 
JOIN locations USING (country_id) 
JOIN departments USING (location_id) 
WHERE department_id IN 
    (SELECT department_id 
		FROM employees 
	 GROUP BY department_id 
	 HAVING COUNT(department_id)>=2)
GROUP BY country_name, city
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221942038-f6b3a051-d06e-4024-94c3-c115c88efab6.png)

____

# Task 22
### Written code
```sql
SELECT department_name, first_name || ' ' || last_name AS "Manager name", city 
FROM departments d 
JOIN employees e ON d.manager_id = e.employee_id 
JOIN locations l USING (location_id)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221942495-39b21ed6-980e-4f16-87b9-12deaa776c14.png)

____

# Task 23
### Written code
```sql
SELECT employee_id, job_title, end_date-start_date days
FROM job_history 
NATURAL JOIN jobs 
WHERE department_id = 80
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221942798-c42d2fad-2e91-4133-9b79-7e44c1983608.png)

____

# Task 24
### Written code
```sql
SELECT first_name || ' ' || last_name AS Employee_name, salary 
FROM employees 
JOIN departments USING (department_id) 
JOIN  locations USING (location_id) 
WHERE city = 'London'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221943106-d2cc2b65-a641-4f78-9d40-7a73eaf38f5a.png)

____

# Task 25
### Written code
```sql
SELECT CONCAT(e.first_name, ' ', e.last_name) AS Employee_name,
       j.job_title,
       h.*
FROM employees e
JOIN
  (SELECT MAX(start_date),
          MAX(end_date),
          employee_id
   FROM job_history
   GROUP BY employee_id) h ON e.employee_id=h.employee_id
JOIN jobs j ON j.job_id=e.job_id
WHERE e.commission_pct = 0
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221943958-50200001-8e82-4168-90ac-ba6a8e6e886c.png)

____

# Task 26
### Written code
```sql
SELECT d.department_name, e.*
FROM departments d
JOIN
  (SELECT count(employee_id),
          department_id
   FROM employees
   GROUP BY department_id) e USING (department_id)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221944241-673a11d9-df12-4802-a925-fb441b68f831.png)

____

# Task 27
### Written code
```sql
SELECT first_name || ' ' || last_name AS Employee_name, employee_id, country_name 
FROM employees 
JOIN departments USING (department_id) 
JOIN locations USING (location_id) 
JOIN countries USING (country_id)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221944833-38afbdc6-552a-4ab8-a487-2d771117d86c.png)


