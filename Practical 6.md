-- Create the 'emp112' table
CREATE TABLE emp112 (
    eid INT PRIMARY KEY,
        ename VARCHAR2(20) NOT NULL,
            Deptno INT,
                FOREIGN KEY (Deptno) REFERENCES dept111(Deptno)
                );

                -- Insert values into 'emp112'
                INSERT INTO emp112 VALUES (100, 'AAA', 01);
                INSERT INTO emp112 VALUES (101, 'BBB', 05);
                INSERT INTO emp112 VALUES (102, 'CCC', 02);
                INSERT INTO emp112 VALUES (104, 'EEE', 03);
                INSERT INTO emp112 VALUES (105, 'FFF', 05);

                -- Create the 'dept111' table
                CREATE TABLE dept111 (
                    Deptno INT PRIMARY KEY,
                        dname CHAR(20)
                        );

                        -- Insert values into 'dept111'
                        INSERT INTO dept111 VALUES (01, 'Sales');
                        INSERT INTO dept111 VALUES (02, 'Marketing');
                        INSERT INTO dept111 VALUES (03, 'Lecturer');
                        INSERT INTO dept111 VALUES (04, 'ASP');
                        INSERT INTO dept111 VALUES (05, 'HR');

                        -- INNER JOIN: Display the employee details and departments that are the same in both tables
                        SELECT * 
                        FROM emp112 
                        INNER JOIN dept111 
                        ON emp112.Deptno = dept111.Deptno;

                        -- LEFT OUTER JOIN: Display all employees and the departments
                        SELECT * 
                        FROM emp112 
                        LEFT OUTER JOIN dept111 
                        ON emp112.Deptno = dept111.Deptno;

                        -- RIGHT OUTER JOIN: Display all employees and the departments
                        SELECT * 
                        FROM emp112 
                        RIGHT OUTER JOIN dept111 
                        ON emp112.Deptno = dept111.Deptno;

                        -- FULL OUTER JOIN: Display all employees and the departments
                        SELECT * 
                        FROM emp112 
                        FULL OUTER JOIN dept111 
                        ON emp112.Deptno = dept111.Deptno;