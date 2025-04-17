CREATE TABLE Manager1 (
        mgr_id NUMBER PRIMARY KEY,
            mgr_name VARCHAR2(15),
                exp_yr NUMBER
                );

                CREATE TABLE Employee1 (
                    emp_id NUMBER PRIMARY KEY,
                        emp_name VARCHAR2(15),
                            department VARCHAR2(15),
                                salary NUMBER,
                                    manager_id NUMBER CONSTRAINT fk_manager FOREIGN KEY (manager_id) REFERENCES Manager1(mgr_id)
                                    );

                                    INSERT INTO Manager1 (mgr_id, mgr_name, exp_yr) VALUES (302, 'Dave', 3);
                                    INSERT INTO Manager1 (mgr_id, mgr_name, exp_yr) VALUES (303, 'Carol', NULL);

                                    INSERT INTO Employee1 (emp_id, emp_name, department, salary, manager_id) VALUES (204, 'Dan', 'Marketing', 47000, 304);

                                    DELETE FROM Manager1 WHERE mgr_id = 302;

                                    SELECT * FROM Manager1;
                                    SELECT * FROM Employee1;
)