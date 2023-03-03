# Task 1
## Question
**Universitet ma'lumotar bazasini ishlab chiqishda Departments, Staffs, Teachers, Students, Groups, Subjects, Regions jadvallari va mos ustunlarini yarating. Har bir jadvalga ma'lumotlar qo'shing.**
### Departments
```python
CREATE TABLE Departments(
  dept_id INT PRIMARY KEY,
  dept_name VARCHAR(50) NOT NULL,
  department_head VARCHAR(255),
  faculty_id INT NOT NULL
);

INSERT INTO Departments(dept_id, dept_name, department_head, faculty_id) VALUES
(1, 'Computer Science', 'Feb 2016 - Present9 years 2 months', 6),
(2, 'Mathematics', 'Feb 2019 - Present7 years 4 months', 7),
(3, 'Physics', 'Feb 2006 - Present12 years 5 months', 8)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222699731-8acdd846-0139-48ba-b747-2f609d4843b6.png)

____

# Task 2
## Question
**Universitet ma'lumotar bazasini ishlab chiqishda Departments, Staffs, Teachers, Students, Groups, Subjects, Regions jadvallari va mos ustunlarini yarating. Har bir jadvalga ma'lumotlar qo'shing.**
### Staffs
```python
CREATE TABLE Staffs(
  staff_id INT PRIMARY KEY,
  staff_name VARCHAR(50) NOT NULL,
  dept_id INT NOT NULL
);

INSERT INTO Staffs(staff_id, staff_name, dept_id) VALUES
(1, 'John Smith', 1),
(2, 'Jane Doe', 2),
(3, 'Bob Johnson', 3)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222700738-ef6cd2b4-cfc1-4b8f-9cce-1b0a15afaf76.png)

____

# Task 3
## Question
**Universitet ma'lumotar bazasini ishlab chiqishda Departments, Staffs, Teachers, Students, Groups, Subjects, Regions jadvallari va mos ustunlarini yarating. Har bir jadvalga ma'lumotlar qo'shing.**
### Teachers
```python
CREATE TABLE Teachers(
  teacher_id INT PRIMARY KEY,
  teacher_name VARCHAR(50) NOT NULL,
  dept_id INT NOT NULL,
  FOREIGN KEY (dept_id) REFERENCES Departments(dept_id)
);

INSERT INTO Teachers(teacher_id, teacher_name, dept_id) VALUES
(1, 'Alice Brown', 1),
(2, 'Bill White', 2),
(3, 'Charlie Green', 3)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222700814-7c429317-f6b2-4047-bbc5-f615cb52e201.png)

____

# Task 4
## Question
**Universitet ma'lumotar bazasini ishlab chiqishda Departments, Staffs, Teachers, Students, Groups, Subjects, Regions jadvallari va mos ustunlarini yarating. Har bir jadvalga ma'lumotlar qo'shing.**
### Students
```python
CREATE TABLE Students(
  student_id INT PRIMARY KEY,
  student_name VARCHAR(50) NOT NULL,
  group_id INT NOT NULL
);

INSERT INTO Students(student_id, student_name, group_id) VALUES
(1, 'Tom Jones', 1),
(2, 'Amy Smith', 1),
(3, 'Joe Davis', 2),
(4, 'Sara Lee', 3),
(5, 'Mike Johnson', 3)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222700945-144e768f-7221-4be0-9151-8ea6fc5e008a.png)

____

# Task 5
## Question
**Universitet ma'lumotar bazasini ishlab chiqishda Departments, Staffs, Teachers, Students, Groups, Subjects, Regions jadvallari va mos ustunlarini yarating. Har bir jadvalga ma'lumotlar qo'shing.**
### Groups
```python
CREATE TABLE Groups(
  group_id INT PRIMARY KEY,
  group_name VARCHAR(50) NOT NULL,
  dept_id INT NOT NULL,
  teacher_id INT NOT NULL,
  FOREIGN KEY (dept_id) REFERENCES Departments(dept_id),
  FOREIGN KEY (teacher_id) REFERENCES Teachers(teacher_id)
);

INSERT INTO Groups(group_id, group_name, dept_id, teacher_id) VALUES
(1, 'CS101', 1, 1),
(2, 'MATH201', 2, 2),
(3, 'PHY301', 3, 3)
```
# Result
![Снимок экрана 2023-03-03 154720](https://user-images.githubusercontent.com/122611764/222701221-7e50eaa4-7060-45f0-857e-70fe6328f29f.png)

____

# Task 6
## Question
**Universitet ma'lumotar bazasini ishlab chiqishda Departments, Staffs, Teachers, Students, Groups, Subjects, Regions jadvallari va mos ustunlarini yarating. Har bir jadvalga ma'lumotlar qo'shing.**
### Subjects
```python
CREATE TABLE Subjects(
  subject_id INT PRIMARY KEY,
  subject_name VARCHAR(50) NOT NULL,
  dept_id INT NOT NULL,
  teacher_id INT NOT NULL,
  FOREIGN KEY (dept_id) REFERENCES Departments(dept_id),
  FOREIGN KEY (teacher_id) REFERENCES Teachers(teacher_id)
);

INSERT INTO Subjects(subject_id, subject_name, dept_id, teacher_id) VALUES
(1, 'Introduction to Computer Science', 1, 1),
(2, 'Calculus I', 2, 2),
(3, 'Mechanics', 3, 3)
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222701488-e8f10068-7b08-4123-9247-c9e7554a546e.png)

____

# Task 7
## Question
**Universitet ma'lumotar bazasini ishlab chiqishda Departments, Staffs, Teachers, Students, Groups, Subjects, Regions jadvallari va mos ustunlarini yarating. Har bir jadvalga ma'lumotlar qo'shing.**
### Regions
```python
CREATE TABLE Regions(
  region_id INT PRIMARY KEY,
  region_name VARCHAR(50) NOT NULL
);

INSERT INTO Regions(region_id, region_name) VALUES
(1, 'North America'),
(2, 'Europe'),
(3, 'Asia')
```
# Result
![image](https://user-images.githubusercontent.com/122611764/222701584-dc5c17c4-f458-42f4-8c75-fbe98bdf3d27.png)



