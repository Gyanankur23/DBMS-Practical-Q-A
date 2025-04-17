-- Create the EMP table with constraints
CREATE TABLE EMP (
      EMPNO NUMBER(6) PRIMARY KEY,
        ENAME VARCHAR2(20) NOT NULL,
          JOB VARCHAR2(10) NOT NULL,
            DEPTNO NUMBER(3),
              SAL NUMBER(7,2)
);

-- Insert records into the EMP table
INSERT INTO EMP VALUES (101, 'Sam', 'Supervisor', 30, 45000);
INSERT INTO EMP VALUES (102, 'Ram', 'Sales', 20, 35000);
INSERT INTO EMP VALUES (103, 'Rajesh', 'HR', 10, 50000);
INSERT INTO EMP VALUES (104, 'Nina', 'Manager', 40, 60000);
INSERT INTO EMP VALUES (105, 'Anita', 'Executive', 50, 55000);

-- Display all contents of the EMP table
SELECT * 
FROM EMP;
)