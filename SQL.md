# SQL Notes

## What is SQL?
SQL (Structured Query Language) is used to manage and manipulate relational databases.

---

## Database Commands

### Create Database
```sql
CREATE DATABASE college;
```

### Use Database
```sql
USE college;
```

### Drop Database
```sql
DROP DATABASE college;
```

---

## Table Commands

### Create Table
```sql
CREATE TABLE Student (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
```

### View Tables
```sql
SHOW TABLES;
```

### Describe Table
```sql
DESC Student;
```

### Drop Table
```sql
DROP TABLE Student;
```

---

## DML Commands

### Insert Data
```sql
INSERT INTO Student VALUES (1, 'Anandhu', 20);
```

### View Data
```sql
SELECT * FROM Student;
```

### Select Specific Columns
```sql
SELECT name, age FROM Student;
```

### Update Data
```sql
UPDATE Student
SET age = 21
WHERE id = 1;
```

### Delete Data
```sql
DELETE FROM Student
WHERE id = 1;
```

---

## WHERE Clause

```sql
SELECT * FROM Student
WHERE age > 18;
```

### Operators

```sql
=   Equal
!=  Not Equal
>   Greater Than
<   Less Than
>=  Greater Than Equal
<=  Less Than Equal
```

---

## ORDER BY

### Ascending
```sql
SELECT * FROM Student
ORDER BY age ASC;
```

### Descending
```sql
SELECT * FROM Student
ORDER BY age DESC;
```

---

## Aggregate Functions

### Count
```sql
SELECT COUNT(*) FROM Student;
```

### Sum
```sql
SELECT SUM(age) FROM Student;
```

### Average
```sql
SELECT AVG(age) FROM Student;
```

### Maximum
```sql
SELECT MAX(age) FROM Student;
```

### Minimum
```sql
SELECT MIN(age) FROM Student;
```

---

## GROUP BY

```sql
SELECT department, COUNT(*)
FROM Employee
GROUP BY department;
```

---

## HAVING

```sql
SELECT department, COUNT(*)
FROM Employee
GROUP BY department
HAVING COUNT(*) > 5;
```

---

## LIKE Operator

### Starts With A
```sql
SELECT * FROM Student
WHERE name LIKE 'A%';
```

### Ends With a
```sql
SELECT * FROM Student
WHERE name LIKE '%a';
```

### Contains n
```sql
SELECT * FROM Student
WHERE name LIKE '%n%';
```

---

## Joins

### INNER JOIN
```sql
SELECT *
FROM Student s
INNER JOIN Course c
ON s.id = c.student_id;
```

### LEFT JOIN
```sql
SELECT *
FROM Student s
LEFT JOIN Course c
ON s.id = c.student_id;
```

### RIGHT JOIN
```sql
SELECT *
FROM Student s
RIGHT JOIN Course c
ON s.id = c.student_id;
```

---

## Constraints

```sql
PRIMARY KEY
FOREIGN KEY
UNIQUE
NOT NULL
CHECK
DEFAULT
```

Example:
```sql
CREATE TABLE Employee(
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    salary INT CHECK(salary > 0)
);
```

---

## Practice Queries

### Find all students older than 18
```sql
SELECT * FROM Student
WHERE age > 18;
```

### Count students
```sql
SELECT COUNT(*) FROM Student;
```

### Find highest age
```sql
SELECT MAX(age) FROM Student;
```

### Sort by age
```sql
SELECT * FROM Student
ORDER BY age DESC;
```
