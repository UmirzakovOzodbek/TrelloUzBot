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
SELECT dir_fname, dir_lname, gen_title, count(gen_title)
FROM director
NATURAL JOIN movie_direction
NATURAL JOIN movie_genres
NATURAL JOIN genres
GROUP BY dir_fname, dir_lname, gen_title
ORDER BY dir_fname, dir_lname
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222102211-788c4579-77ff-4a37-892c-3ade02fb4727.png)

____

# Task 7
### Written code
```sql
SELECT mov_title, mov_year, gen_title
FROM movie
NATURAL JOIN movie_genres
NATURAL JOIN genres
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222102422-791241ad-fa50-420c-a126-12c48d354e7a.png)

____

# Task 8
### Written code
```sql
SELECT mov_title, mov_year, gen_title, dir_fname, dir_lname
FROM movie
NATURAL JOIN movie_genres
NATURAL JOIN genres
NATURAL JOIN movie_direction
NATURAL JOIN director
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222102584-888da76b-bb6c-49ce-88ab-3088969aa802.png)

____

# Task 9
### Written code
```sql
SELECT movie.mov_title, mov_year, mov_dt_rel, mov_time,dir_fname, dir_lname 
FROM movie
JOIN  movie_direction 
ON movie.mov_id = movie_direction.mov_id
JOIN director 
ON movie_direction.dir_id = director.dir_id
WHERE mov_dt_rel < '1989/01/01'
ORDER BY mov_dt_rel desc
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222103208-79350075-6701-422b-a44d-2bed59214353.png)

____

# Task 10
### Written code
```sql
SELECT gen_title, avg(mov_time), count(gen_title) 
FROM movie
NATURAL JOIN  movie_genres
NATURAL JOIN  genres
GROUP BY gen_title
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222103480-6866cc71-14ef-4c4d-a84c-f7c143cbfd0c.png)

____

# Task 11
### Written code
```sql
SELECT mov_title, mov_year, dir_fname, dir_lname, act_fname, act_lname, role 
FROM movie
NATURAL JOIN movie_direction
NATURAL JOIN movie_cast
NATURAL JOIN director
NATURAL JOIN actor
WHERE mov_time = (SELECT min(mov_time) FROM movie)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222103805-8502a42d-b139-49e1-85e3-69b114105a14.png)

____

# Task 12
### Written code
```sql
SELECT DISTINCT mov_year FROM movie
INNER JOIN rating 
ON movie.mov_id = rating.mov_id
WHERE rev_stars IN (3, 4)
ORDER BY mov_year
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222104055-54f40fe1-fb80-4ac0-9f59-e1523c249c13.png)

____

# Task 13
### Written code
```sql
SELECT rev_name, mov_title, rev_stars FROM movie 
NATURAL JOIN rating 
NATURAL JOIN reviewer
WHERE rev_name IS NOT NULL
ORDER BY rev_name, mov_title, rev_stars
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222104290-9e66645e-7783-4500-a88d-cf67b588017f.png)

____

# Task 14
### Written code
```sql
SELECT mov_title, max(rev_stars)
FROM movie
INNER JOIN rating USING (mov_id)
GROUP BY mov_title 
HAVING max(rev_stars) > 0
ORDER BY mov_title
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222104705-f4c7695e-7110-4edd-b53f-adb0cac9f9c8.png)

____

# Task 15
### Written code
```sql
SELECT mov_title, dir_fname,dir_lname, rev_stars
FROM movie
JOIN movie_direction USING(mov_id)
JOIN director USING (dir_id)
LEFT JOIN rating USING (mov_id)
WHERE rev_stars IS NOT NULL
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222105158-0107ce1d-2a8a-4e9c-b0b4-be287175cb4e.png)

____

# Task 16
### Written code
```sql
SELECT mov_title, act_fname, act_lname, role
FROM movie 
JOIN movie_cast 
ON movie_cast.mov_id = movie.mov_id 
JOIN actor 
ON movie_cast.act_id = actor.act_id
WHERE actor.act_id IN (SELECT act_id FROM movie_cast 
GROUP BY act_id HAVING count(*) >= 2)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222105796-c775519a-c72f-462d-a989-c170b641409d.png)

____

# Task 17
### Written code
```sql
SELECT dir_fname, dir_lname, mov_title, act_fname, act_lname, role
FROM actor
JOIN movie_cast 
ON actor.act_id = movie_cast.act_id
JOIN movie_direction 
ON movie_cast.mov_id = movie_direction.mov_id
JOIN director 
ON movie_direction.dir_id = director.dir_id
JOIN movie 
ON movie.mov_id = movie_direction.mov_id
WHERE act_fname = 'Claire' AND act_lname = 'Danes'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222106336-b4842dd0-7be8-4c15-9b95-def8ee217d93.png)

____

# Task 18
### Written code
```sql
SELECT act_fname, act_lname, mov_title, role
FROM actor
JOIN movie_cast 
ON actor.act_id = movie_cast.act_id
JOIN movie_direction 
ON movie_cast.mov_id = movie_direction.mov_id
JOIN director 
ON movie_direction.dir_id = director.dir_id
JOIN movie 
ON movie.mov_id = movie_direction.mov_id
WHERE act_fname = dir_fname AND act_lname = dir_lname
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222106663-caa95ba0-48c0-4975-8bb4-0354dd69c23c.png)

____

# Task 19
### Written code
```sql
SELECT a.act_fname, a.act_lname FROM movie_cast mov
JOIN actor a 
ON mov.act_id = a.act_id
WHERE mov_id = (SELECT mov_id FROM movie
WHERE mov_title = 'Chinatown')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222107562-d86a6293-fce1-4f0e-8e8d-1c995e817507.png)

____

# Task 20
### Written code
```sql
SELECT m.mov_title FROM  movie m
JOIN movie_cast mov 
ON m.mov_id = mov.mov_id
WHERE mov.act_id IN (SELECT act_id FROM actor 
WHERE act_fname = 'Harrison' AND act_lname = 'Ford')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222108093-66e9018b-15ae-4376-bea4-1e0ba24d0b4f.png)

____

# Task 21
### Written code
```sql
SELECT mov_title, mov_year, rev_stars, mov_rel_country
FROM movie 
NATURAL JOIN rating
WHERE rev_stars = (SELECT max(rev_stars) FROM rating)
```
# Result
![Снимок экрана_20230301_151352](https://user-images.githubusercontent.com/122611764/222109949-c5d018d7-8be3-47a0-a85b-00b4ffe0d48c.png)

____

# Task 22
### Written code
```sql
SELECT mov_title, mov_year, rev_stars
FROM movie 
NATURAL JOIN movie_genres 
NATURAL JOIN genres 
NATURAL JOIN rating
WHERE gen_title = 'Mystery' AND rev_stars >= ALL (SELECT rev_stars FROM rating 
NATURAL JOIN movie_genres 
NATURAL JOIN genres
WHERE gen_title = 'Mystery')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222110257-6ab3cc69-adc9-487d-ae9d-02d3cd398c44.png)

____

# Task 23
### Written code
```sql
SELECT mov_year, gen_title, count(gen_title), avg(rev_stars)
FROM movie 
NATURAL JOIN movie_genres 
NATURAL JOIN genres
NATURAL JOIN rating
WHERE gen_title = 'Mystery' 
GROUP BY mov_year, gen_title
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222110511-14be0e6f-22a8-46e9-a555-818bb8f83c83.png)

____

# Task 24
### Written code
```sql
SELECT mov_title, act_fname, act_lname, 
mov_year, role, gen_title, dir_fname, dir_lname, 
mov_dt_rel, rev_stars
FROM movie 
NATURAL JOIN movie_cast
NATURAL JOIN actor
NATURAL JOIN movie_genres
NATURAL JOIN genres
NATURAL JOIN movie_direction
NATURAL JOIN director
NATURAL JOIN rating
WHERE act_gender = 'F'
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222110816-8ded1bf6-c314-4d64-b2be-dba71abb3eeb.png)


