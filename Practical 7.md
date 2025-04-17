-- Creating the DATABASE table
CREATE TABLE DATABASE (
    NAME VARCHAR(50),
        ROLL_NO INT PRIMARY KEY,
            LOCATION VARCHAR(50),
                PHONE_NUMBER VARCHAR(15)
                );

                -- Creating the STUDENT table
                CREATE TABLE STUDENT (
                    NAME VARCHAR(50),
                        ROLL_NO INT PRIMARY KEY,
                            SECTION CHAR(1)
                            );

                            -- Inserting data into DATABASE table
                            INSERT INTO DATABASE (NAME, ROLL_NO, LOCATION, PHONE_NUMBER) VALUES
                            ('Ram', 101, 'Chennai', '9988775566'),
                            ('Raj', 102, 'Coimbatore', '8877665544'),
                            ('Sasi', 103, 'Madurai', '7766553344'),
                            ('Ravi', 104, 'Salem', '8989898989'),
                            ('Sumathi', 105, 'Kanchipuram', '8989856868');

                            -- Inserting data into STUDENT table
                            INSERT INTO STUDENT (NAME, ROLL_NO, SECTION) VALUES
                            ('Ravi', 104, 'A'),
                            ('Sumathi', 105, 'B'),
                            ('Raj', 102, 'A');

                            -- Query 1: Display NAME, LOCATION, PHONE_NUMBER of students from DATABASE table whose section is 'A'
                            SELECT NAME, LOCATION, PHONE_NUMBER
                            FROM DATABASE
                            WHERE ROLL_NO IN (SELECT ROLL_NO FROM STUDENT WHERE SECTION = 'A');

                            -- Creating the Student1 table
                            CREATE TABLE Student1 (
                                NAME VARCHAR(50),
                                    ROLL_NO INT PRIMARY KEY,
                                        LOCATION VARCHAR(50),
                                            PHONE_NUMBER VARCHAR(15)
                                            );

                                            -- Creating the Student2 table
                                            CREATE TABLE Student2 (
                                                NAME VARCHAR(50),
                                                    ROLL_NO INT PRIMARY KEY,
                                                        LOCATION VARCHAR(50),
                                                            PHONE_NUMBER VARCHAR(15)
                                                            );

                                                            -- Inserting data into Student1 table
                                                            INSERT INTO Student1 (NAME, ROLL_NO, LOCATION, PHONE_NUMBER) VALUES
                                                            ('Ram', 101, 'Chennai', '9988773344'),
                                                            ('Raju', 102, 'Coimbatore', '9090909090'),
                                                            ('Ravi', 103, 'Salem', '8989898989');

                                                            -- Inserting data into Student2 table
                                                            INSERT INTO Student2 (NAME, ROLL_NO, LOCATION, PHONE_NUMBER) VALUES
                                                            ('Raj', 111, 'Chennai', '8787878787'),
                                                            ('Sai', 112, 'Mumbai', '6565656565'),
                                                            ('Sri', 113, 'Coimbatore', '7878787878');

                                                            -- Query 2: Insert all data from Student2 into Student1
                                                            INSERT INTO Student1 SELECT * FROM Student2;

                                                            -- Query 3: Delete students from Student2 table whose ROLL_NO matches with Student1 and LOCATION is 'Chennai'
                                                            DELETE FROM Student2
                                                            WHERE ROLL_NO IN (SELECT ROLL_NO FROM Student1 WHERE LOCATION = 'Chennai');

                                                            -- Query 4: Update the names in Student2 to 'MYName' where LOCATION matches Raju or Ravi in Student1
                                                            UPDATE Student2
                                                            SET NAME = 'MYName'
                                                            WHERE LOCATION IN (SELECT LOCATION FROM Student1 WHERE NAME IN ('Raju', 'Ravi'));