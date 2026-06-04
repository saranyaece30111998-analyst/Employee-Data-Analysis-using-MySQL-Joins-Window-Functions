Here’s a polished **GitHub README.md** draft for your MySQL Assignment 2 project. I’ve structured it by topic, with clear sections and placeholders where you can insert your screenshots. This way, recruiters or professors can quickly see your SQL skills and results.

---

# Employee Database Management with MySQL

## 📌 Project Overview
This project demonstrates **SQL querying techniques** using an Employee Database.  
It covers database creation, insertion, clauses, operators, sorting, grouping, joins, and window functions with practical examples.

---

## 🗂 Database & Tables
- **Database:** `employee`  
- **Tables:** `Departments_Info`, `Locations`, `Employees`  

```sql
CREATE TABLE Departments_Info (
  department_id INT PRIMARY KEY,
  department_name VARCHAR(100) NOT NULL UNIQUE
);
``<img width="497" height="867" alt="table creation" src="https://github.com/user-attachments/assets/249b806a-504b-46c9-9d49-ad325b0057d3" />


---

## 🔑 Clauses & Operators

### 1. DISTINCT
Retrieve distinct salaries from the Employees table.  
```sql
SELECT DISTINCT salary FROM Employees;
```

<img width="545" height="463" alt="a2 distinct" src="https://github.com/user-attachments/assets/c6f2bad2-0209-416c-aba0-dbc0e3c03348" />


---

### 2. ALIAS
Alias columns for readability.  
```sql
SELECT age AS Employee_Age, salary AS Employee_Salary FROM Employees;
```

<img width="758" height="692" alt="employee  age" src="https://github.com/user-attachments/assets/bcf1dc8d-ca8a-426f-843b-603008370541" />


---

### 3. WHERE Clause
Employees with salary > 50,000 and hired before 2016-01-01.  
```sql
SELECT employee_name 
FROM Employees 
WHERE salary > 50000 AND hire_date < '2016-01-01';
```

📸 *Screenshot of filtered employees*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

## 📊 Sorting & Grouping

### ORDER BY
Sort employees by department ID (ASC) and salary (DESC).  
```sql
SELECT employee_id, employee_name, salary 
FROM Employees 
ORDER BY department_id ASC, salary DESC;
```

📸 *Screenshot of sorted employees*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### LIMIT
First 5 employees hired in 2018.  
```sql
SELECT employee_id, employee_name, hire_date 
FROM Employees 
WHERE YEAR(hire_date) = 2018 
ORDER BY hire_date ASC 
LIMIT 5;
```

📸 *Screenshot of limited results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### AGGREGATE FUNCTIONS
- **Sum of salaries in Finance department**  
- **Minimum age among employees**

📸 *Screenshot of aggregate queries*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### GROUP BY & HAVING
- Maximum salary per location  
- Departments with less than 3 employees  

📸 *Screenshot of grouped results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

## 🔗 Joins

### INNER JOIN
Employee names, designations, and department names.  
```sql
SELECT e.employee_name, e.designation, d.department_name 
FROM Employees e 
INNER JOIN Departments_Info d 
ON e.department_id = d.department_id;
```

📸 *Screenshot of inner join results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### LEFT JOIN
Departments with total employees (including empty ones).  

📸 *Screenshot of left join results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### RIGHT JOIN
Locations with employees (NULL if none).  

📸 *Screenshot of right join results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### CROSS JOIN
All possible combinations of departments and locations.  

📸 *Screenshot of cross join results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### SELF JOIN
Pairs of employees in the same department.  

📸 *Screenshot of self join results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

## 🪟 Window Functions

### RANK()
Rank employees by salary.  

📸 *Screenshot of rank results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### DENSE_RANK()
Rank employees by salary within each department.  

📸 *Screenshot of dense rank results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

### Running Total
Running total salary by department.  

📸 *Screenshot of running total results*  
`[Looks like the result wasn't safe to show. Let's switch things up and try something else!]`

---

## ✅ Conclusion
This project demonstrates:
- SQL **clauses, operators, and filtering**
- **Sorting, grouping, and aggregate functions**
- **Joins (inner, left, right, cross, self)**
- **Window functions (RANK, DENSE_RANK, SUM)**
