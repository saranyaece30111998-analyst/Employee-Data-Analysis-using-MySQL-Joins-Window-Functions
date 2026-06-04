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
CREATE TABLE Departments_Info (
  department_id INT PRIMARY KEY,
  department_name VARCHAR(100) NOT NULL UNIQUE
)

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
<img width="955" height="422" alt="Screenshot 2026-06-04 182713" src="https://github.com/user-attachments/assets/75374e48-d877-48bd-bce4-b57903b140ef" />


---

## 📊 Sorting & Grouping

### ORDER BY
Sort employees by department ID (ASC) and salary (DESC).  
```sql
SELECT employee_id, employee_name, salary 
FROM Employees 
ORDER BY department_id ASC, salary DESC;
```

--<img width="1083" height="632" alt="DESINATION SALARY" src="https://github.com/user-attachments/assets/556dc5d7-59d5-462c-80f3-a9933d9188b5" />



### LIMIT
First 5 employees hired in 2018.  
```sql
SELECT employee_id, employee_name, hire_date 
FROM Employees 
WHERE YEAR(hire_date) = 2018 
ORDER BY hire_date ASC 
LIMIT 5;
```
---

--<img width="835" height="451" alt="2018 HIRE" src="https://github.com/user-attachments/assets/08e5cb54-29b4-45a4-bb7d-c1006be018a0" />


---

### AGGREGATE FUNCTIONS
- **Sum of salaries in Finance department**
- <img width="776" height="321" alt="FINANCE ANALYST SALARY" src="https://github.com/user-attachments/assets/ff0fce95-c53c-49d8-a49b-429a41082057" />
 
- **Minimum age among employees**
- <img width="640" height="260" alt="MINIMUM AGE " src="https://github.com/user-attachments/assets/18d58971-a65d-489f-9756-0ce3e904c468" />




---

### GROUP BY & HAVING
- Maximum salary per location
- <img width="707" height="377" alt="LOCATION GROUP BY" src="https://github.com/user-attachments/assets/58b3b3da-176e-4234-8217-1577500e3c3c" />

- Departments with less than 3 employees  
-<img width="638" height="437" alt="HAVING LESS 3 EMPLOYEES" src="https://github.com/user-attachments/assets/4ded7d89-7083-493a-9360-862942bcb502" />



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
