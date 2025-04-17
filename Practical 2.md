-- Step 1: Create the EMP table
CREATE TABLE EMP123 (
  EMPNO NUMBER(6) PRIMARY KEY,
    ENAME VARCHAR2(20) NOT NULL,
      JOB VARCHAR2(10) NOT NULL,
        DEPTNO NUMBER(3),
          SAL NUMBER(7,2)
          );

          -- Step 2: Insert data into EMP123 table
          INSERT INTO EMP123 VALUES (101, 'Sam', 'Supervisor', 30, 45000);
          INSERT INTO EMP123 VALUES (102, 'Ram', 'Sales', 20, 35000);
          INSERT INTO EMP123 VALUES (103, 'Rajesh', 'HR', 10, 50000);

          -- Step 3: Perform vertical selection
          SELECT EMPNO, ENAME, SAL 
          FROM EMP123;

          -- Step 4: Perform horizontal selection with conditions
          SELECT EMPNO, ENAME, SAL 
          FROM EMP123 
          WHERE SAL > 25000;

          SELECT EMPNO, ENAME, SAL 
          FROM EMP123 
          WHERE ENAME LIKE 'R%';

          SELECT EMPNO, ENAME, SAL 
          FROM EMP123 
          WHERE ENAME NOT LIKE 'R%';

          SELECT EMPNO, ENAME, SAL 
          FROM EMP123 
          WHERE SAL < 50000 OR ENAME LIKE 'S%';

          -- Step 5: Alter the table to add a new column
          ALTER TABLE EMP123 ADD DOB DATE;

          -- Step 6: Display the updated table structure
          DESCRIBE EMP123;

          -- Step 7: Display all records in the table
          SELECT * 
          FROM EMP123;