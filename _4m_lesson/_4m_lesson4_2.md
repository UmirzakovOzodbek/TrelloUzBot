# Task 1
### Written code
```sql
SELECT rev_name FROM reviewer
INNER JOIN rating USING(rev_id)
WHERE rev_stars IS NULL
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221946584-73934e71-023d-445e-85d2-d0422aa51d70.png)

____

# Task 2
### Written code
```sql
SELECT act_fname,act_lname, role FROM actor 
JOIN movie_cast ON actor.act_id = movie_cast.act_id
JOIN movie ON movie_cast.mov_id = movie.mov_id 
AND movie.mov_title = 'Annie Hall' 
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221947238-baeb6008-5f4a-4dbc-bcd5-e7c1b492f05f.png)

____

# Task 3
### Written code
```sql
SELECT dir_fname, dir_lname, mov_title
FROM director 
NATURAL JOIN movie_direction
NATURAL JOIN movie
NATURAL JOIN movie_cast
WHERE role IS NOT NULL
AND mov_title = 'Eyes Wide Shut'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221947445-08c4d50c-3516-4ba5-ba25-428e35b2690f.png)

____

# Task 4
### Written code
```sql
SELECT dir_fname, dir_lname, mov_title
FROM director 
JOIN movie_direction 
ON director.dir_id = movie_direction.dir_id
JOIN movie 
ON movie_direction.mov_id = movie.mov_id
JOIN movie_cast 
ON movie_cast.mov_id = movie.mov_id
WHERE role = 'Sean Maguire'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221947670-61fa9d50-748e-4ccd-806e-0c81567f0f96.png)

____

# Task 5
### Written code
```sql
SELECT act_fname, act_lname, mov_title, mov_year
FROM actor
JOIN movie_cast 
ON actor.act_id = movie_cast.act_id
JOIN movie 
ON movie_cast.mov_id = movie.mov_id
WHERE mov_year NOT BETWEEN 1990 and 2000
```
# Result
![image](https://user-images.githubusercontent.com/122611764/221947973-3e15aab9-d339-4560-b94f-0ff505dbabbb.png)

____

# Task 6
### Written code
```sql

```
# Result

____

# Task 7
### Written code
```sql

```
# Result
____

# Task 8
### Written code
```sql

```
# Result

____

# Task 9
### Written code
```sql

```
# Result

____

# Task 10
### Written code
```sql

```
# Result

____

# Task 11
### Written code
```sql

```
# Result

____

# Task 12
### Written code
```sql

```
# Result

____

# Task 13
### Written code
```sql

```
# Result
____

# Task 14
### Written code
```sql

```
# Result

____

# Task 15
### Written code
```sql

```
# Result

____

# Task 16
### Written code
```sql

```
# Result

____

# Task 17
### Written code
```sql

```
# Result

____

# Task 18
### Written code
```sql

```
# Result

____

# Task 19
### Written code
```sql

```
# Result

____

# Task 20
### Written code
```sql

```
# Result

____

# Task 21
### Written code
```sql

```
# Result

____

# Task 22
### Written code
```sql

```
# Result

____

# Task 23
### Written code
```sql

```
# Result

____

# Task 24
### Written code
```sql

```
# Result


