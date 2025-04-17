# DBMS-Practical-Q-A
The following repository contains all 7 practicals of DBMS for Sem 2 and probable questions that can come in the exam.


# DBMS Practicals 🚀

## Practical 1: Create table `student` and perform operations ✍️

**Q1. How to create the `student` table?**

```sql
CREATE TABLE student(rno int, name varchar(20), class varchar(10), marks int);
```

**Q2. How to insert values into the `student` table?**

```sql
INSERT INTO student VALUES(1,'Ajay','FYBSc',450);
INSERT INTO student VALUES(2,'Vijay','FYBSc',390);
INSERT INTO student VALUES(3,'Ravi','SYBSc',410);
INSERT INTO student VALUES(4,'Kiran','SYBSc',395);
INSERT INTO student VALUES(5,'Reena','TYBSc',430);
```

**Q3. How to display all records from the `student` table?**

```sql
SELECT * FROM student;
```

**Q4. How to display students having marks greater than 400?**

```sql
SELECT * FROM student WHERE marks > 400;
```

**Q5. How to display students whose name starts with ‘R’?**

```sql
SELECT * FROM student WHERE name LIKE 'R%';
```

**Q6. How to display students of `SYBSc` class?**

```sql
SELECT * FROM student WHERE class = 'SYBSc';
```

**Q7. How to display all records in descending order of marks?**

```sql
SELECT * FROM student ORDER BY marks DESC;
```

**Q8. How to update marks of the student whose `rno` is 2 to 410?**

```sql
UPDATE student SET marks = 410 WHERE rno = 2;
```

**Q9. How to delete the record of the student whose `rno` is 4?**

```sql
DELETE FROM student WHERE rno = 4;
```

**Q10. How to add the column `email` to the `student` table?**

```sql
ALTER TABLE student ADD email varchar(50);
```

---

## Practical 2: Create table `company` and perform operations 🏢

**Q1. How to create the `company` table?**

```sql
CREATE TABLE company(c_id int, c_name varchar(30), location varchar(20), no_of_employees int);
```

**Q2. How to insert values into the `company` table?**

```sql
INSERT INTO company VALUES(101,'TCS','Pune',200);
INSERT INTO company VALUES(102,'Infosys','Mumbai',250);
INSERT INTO company VALUES(103,'Wipro','Pune',150);
INSERT INTO company VALUES(104,'TechM','Hyderabad',300);
INSERT INTO company VALUES(105,'Capgemini','Mumbai',275);
```

**Q3. How to display all companies located in Pune?**

```sql
SELECT * FROM company WHERE location = 'Pune';
```

**Q4. How to display companies having more than 200 employees?**

```sql
SELECT * FROM company WHERE no_of_employees > 200;
```

**Q5. How to display all records from the `company` table?**

```sql
SELECT * FROM company;
```

**Q6. How to display records in ascending order of company name?**

```sql
SELECT * FROM company ORDER BY c_name ASC;
```

**Q7. How to update `no_of_employees` for the company with `c_id` 103 to 180?**

```sql
UPDATE company SET no_of_employees = 180 WHERE c_id = 103;
```

**Q8. How to delete the record where `c_id` is 104?**

```sql
DELETE FROM company WHERE c_id = 104;
```

**Q9. How to add the column `revenue` to the `company` table?**

```sql
ALTER TABLE company ADD revenue int;
```

**Q10. How to change the data type of `c_name` to `varchar(50)`?**

```sql
ALTER TABLE company MODIFY c_name varchar(50);
```

---

## Practical 3: Create table `employee` and perform operations 👔

**Q1. How to create the `employee` table?**

```sql
CREATE TABLE employee(emp_id int, name varchar(30), dept varchar(20), salary int);
```

**Q2. How to insert values into the `employee` table?**

```sql
INSERT INTO employee VALUES(1,'Ajay','sales',25000);
INSERT INTO employee VALUES(2,'Vijay','marketing',30000);
INSERT INTO employee VALUES(3,'Ravi','sales',28000);
INSERT INTO employee VALUES(4,'Kiran','accounts',22000);
INSERT INTO employee VALUES(5,'Reena','marketing',27000);
```

**Q3. How to display all employee records?**

```sql
SELECT * FROM employee;
```

**Q4. How to display employees of the `sales` department?**

```sql
SELECT * FROM employee WHERE dept = 'sales';
```

**Q5. How to display employees having a salary between 25000 and 30000?**

```sql
SELECT * FROM employee WHERE salary BETWEEN 25000 AND 30000;
```

**Q6. How to display employees whose name ends with ‘i’?**

```sql
SELECT * FROM employee WHERE name LIKE '%i';
```

**Q7. How to display employees in descending order of salary?**

```sql
SELECT * FROM employee ORDER BY salary DESC;
```

**Q8. How to update the salary of the employee with `emp_id` 2 to 32000?**

```sql
UPDATE employee SET salary = 32000 WHERE emp_id = 2;
```

**Q9. How to delete the record of the employee with `emp_id` 4?**

```sql
DELETE FROM employee WHERE emp_id = 4;
```

**Q10. How to add the column `experience` to the `employee` table?**

```sql
ALTER TABLE employee ADD experience int;
```

---

## Practical 4: Perform Alter table operations 🔧

**Q1. How to add the column `gender` to the `student` table?**

```sql
ALTER TABLE student ADD gender varchar(10);
```

**Q2. How to modify the column `marks` to `float` in the `student` table?**

```sql
ALTER TABLE student MODIFY marks float;
```

**Q3. How to rename the column `name` to `student_name`?**

```sql
ALTER TABLE student RENAME COLUMN name TO student_name;
```

**Q4. How to drop the column `email` from the `student` table?**

```sql
ALTER TABLE student DROP COLUMN email;
```

**Q5. How to add the column `gender` to the `employee` table?**

```sql
ALTER TABLE employee ADD gender varchar(10);
```

**Q6. How to modify the column `salary` to `float` in the `employee` table?**

```sql
ALTER TABLE employee MODIFY salary float;
```

**Q7. How to rename the column `name` to `emp_name` in the `employee` table?**

```sql
ALTER TABLE employee RENAME COLUMN name TO emp_name;
```

**Q8. How to drop the column `experience` from the `employee` table?**

```sql
ALTER TABLE employee DROP COLUMN experience;
```

**Q9. How to add the column `company_name` to the `employee` table?**

```sql
ALTER TABLE employee ADD company_name varchar(30);
```

**Q10. How to change the data type of `company_name` to `varchar(50)`?**

```sql
ALTER TABLE employee MODIFY company_name varchar(50);
```

---


## Practical 5: SQL Clauses (WHERE, ORDER BY, GROUP BY, HAVING) 🛠️

**Q1. How to display employee details where salary > 20,000?**

```sql
SELECT * FROM employee WHERE salary > 20000;
```

**Q2. How to display employee details where department = 'sales'?**

```sql
SELECT * FROM employee WHERE dept = 'sales';
```

**Q3. How to display employee details in ascending order of name?**

```sql
SELECT * FROM employee ORDER BY name ASC;
```

**Q4. How to display employee details in descending order of salary?**

```sql
SELECT * FROM employee ORDER BY salary DESC;
```

**Q5. How to display total salary paid to employees?**

```sql
SELECT SUM(salary) AS Total_Salary FROM employee;
```

**Q6. How to display department-wise total salary?**

```sql
SELECT dept, SUM(salary) AS Total_Salary FROM employee GROUP BY dept;
```

**Q7. How to display department-wise maximum salary?**

```sql
SELECT dept, MAX(salary) AS Max_Salary FROM employee GROUP BY dept;
```

**Q8. How to display department-wise minimum salary?**

```sql
SELECT dept, MIN(salary) AS Min_Salary FROM employee GROUP BY dept;
```

**Q9. How to display department-wise total salary having total > 25,000?**

```sql
SELECT dept, SUM(salary) AS Total_Salary
FROM employee
GROUP BY dept
HAVING SUM(salary) > 25000;
```

**Q10. How to count the number of employees in each department?**

```sql
SELECT dept, COUNT(*) AS No_of_Employees FROM employee GROUP BY dept;
```

---

## Practical 6: Subqueries and Joins 🔗

**Q1. How to display employee names whose salary is greater than the average salary?**

```sql
SELECT name FROM employee
WHERE salary > (SELECT AVG(salary) FROM employee);
```

**Q2. How to display employee details whose department is the same as the employee with `emp_id` 102?**

```sql
SELECT * FROM employee
WHERE dept = (SELECT dept FROM employee WHERE emp_id = 102);
```

**Q3. How to create the `department` table (did, dname)?**

```sql
CREATE TABLE department (
    did INT PRIMARY KEY,
    dname VARCHAR(30)
);
```

**Q4. How to insert values into the `department` table?**

```sql
INSERT INTO department VALUES (1, 'sales');
INSERT INTO department VALUES (2, 'marketing');
INSERT INTO department VALUES (3, 'accounts');
```

**Q5. How to add the column `did` in the `employee` table?**

```sql
ALTER TABLE employee ADD did INT;
```

**Q6. How to update `did` values in the `employee` table?**

```sql
UPDATE employee SET did = 1 WHERE dept = 'sales';
UPDATE employee SET did = 2 WHERE dept = 'marketing';
UPDATE employee SET did = 3 WHERE dept = 'accounts';
```

**Q7. How to display employee name and department name using a join?**

```sql
SELECT e.name, d.dname
FROM employee e
JOIN department d ON e.did = d.did;
```

**Q8. How to display all employees with their department name using a left join?**

```sql
SELECT e.name, d.dname
FROM employee e
LEFT JOIN department d ON e.did = d.did;
```

**Q9. How to display all departments and their employees using a right join?**

```sql
SELECT e.name, d.dname
FROM employee e
RIGHT JOIN department d ON e.did = d.did;
```

**Q10. How to display employee name and department name using aliases?**

```sql
SELECT e.name AS Employee_Name, d.dname AS Department_Name
FROM employee AS e, department AS d
WHERE e.did = d.did;
```

---

## Practical 7: Views and Indexes 👓

**Q1. How to create a view of `employee` (emp_id, name) for the `sales` department?**

```sql
CREATE VIEW sales_emp AS
SELECT emp_id, name FROM employee
WHERE dept = 'sales';
```

**Q2. How to display the contents of the view?**

```sql
SELECT * FROM sales_emp;
```

**Q3. How to add a new employee to the `sales_emp` view?**

```sql
INSERT INTO sales_emp VALUES (106, 'Meena');
```

**Q4. How to delete a record from the view?**

```sql
DELETE FROM sales_emp WHERE emp_id = 106;
```

**Q5. How to drop the view?**

```sql
DROP VIEW sales_emp;
```

**Q6. How to create a unique index on `emp_id`?**

```sql
CREATE UNIQUE INDEX idx_emp_id ON employee(emp_id);
```

**Q7. How to create a non-unique index on `name`?**

```sql
CREATE INDEX idx_emp_name ON employee(name);
```

**Q8. How to display all indexes on the `employee` table?**

```sql
SHOW INDEX FROM employee;
```

**Q9. How to drop the index on `name`?**

```sql
DROP INDEX idx_emp_name ON employee;
```

**Q10. How to drop the index on `emp_id`?**

```sql
DROP INDEX idx_emp_id ON employee;
```

---

