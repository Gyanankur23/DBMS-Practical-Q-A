-- Creating the EMP table with specified structure
CREATE TABLE EMP (
    EMPNO NUMBER(6) PRIMARY KEY,
        ENAME VARCHAR2(20) NOT NULL,
            JOB VARCHAR2(10) NOT NULL,
                DEPTNO NUMBER(3),
                    SAL NUMBER(7,2)
                    );

                    -- Listing all aggregate functions with examples
                    SELECT COUNT(*) FROM emp123;
                    SELECT MAX(SAL) FROM emp123;
                    SELECT MIN(SAL) FROM emp123;
                    SELECT SUM(SAL) FROM emp123;
                    SELECT AVG(SAL) FROM emp123;

                    -- Displaying total salary spent for each job category
                    SELECT SUM(SAL), JOB FROM emp123 GROUP BY JOB;
                    SELECT SUM(SAL), DEPTNO FROM emp123 GROUP BY DEPTNO;

                    -- Displaying count of employees who work in the same department
                    SELECT COUNT(*), JOB FROM emp123 GROUP BY JOB;

                    -- Displaying maximum salary spent for each job category
                    SELECT MAX(SAL), JOB FROM emp123 GROUP BY JOB;

                    -- Displaying minimum salary spent for each job category
                    SELECT MIN(SAL), JOB FROM emp123 GROUP BY JOB;

                    -- Calculating the total and average salary amount in the EMP table
                    SELECT SUM(SAL), AVG(S BY DEPTNO;

                    -- Determining the max and min salary with renamed columns
                    SELECT MIN(SAL) AS MIN_SALARY, MAX(SAL) AS MAX_SALARY FROM emp123;

                    -- Finding how many job titles are available in the EMP table
                    SELECT JOB FROM emp123 GROUP BY JOB;