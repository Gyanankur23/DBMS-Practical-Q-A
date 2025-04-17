-- Create the Students table
CREATE TABLE Students (
    RollNo INT,
        Last_Name VARCHAR(50),
            First_Name VARCHAR(50),
                Address VARCHAR(100),
                    City VARCHAR(50)
                    );

                    -- Insert sample data into the Students table
                    INSERT INTO Students (RollNo, Last_Name, First_Name, Address, City) VALUES
                    (1, 'Pawar', 'Ramesh', 'Bytco', 'Nashik'),
                    (2, 'Patil', 'Sachin', 'Juhu', 'Mumbai'),
                    (3, 'Shah', 'Nayana', 'Nashik Road', 'Nashik'),
                    (4, 'Hussein', 'Zakir', 'Cidco', 'Nashik'),
                    (5, 'Jain', 'Kavita', 'Shivaginagar', 'Pune'),
                    (6, 'Mishra', 'Ravi', 'Pune Station', 'Pune');

                    -- Sample Queries Demonstrating Functions

                    -- Using SUBSTRING function
                    SELECT SUBSTR(Last_Name, 3) AS Substring_Result FROM Students WHERE Last_Name = 'Hussein';

                    -- Using TRIM function
                    SELECT TRIM(' Sample ') AS Trim_Result FROM dual;

                    -- Using LENGTH function
                    SELECT LENGTH(Last_Name) AS Length_Result FROM Students WHERE Last_Name = 'Hussein';

                    -- Using REPLACE function
                    SELECT REPLACE(Last_Name, 'til', 'tel') AS Replace_Result FROM Students WHERE Last_Name = 'Patil';

                    -- Using CONCAT function
                    SELECT CONCAT(Last_Name, ' ', First_Name) AS FullName FROM Students WHERE Last_Name = 'Hussein';

                    -- Using LEFT and RIGHT functions
                    SELECT LEFT(Last_Name, 3) AS Left_Result, RIGHT(Last_Name, 3) AS Right_Result FROM Students WHERE Last_Name = 'Shah';

                    -- Using REPLICATE function
                    SELECT REPEAT(Last_Name, 2) AS Replicate_Result FROM Students WHERE Last_Name = 'Shah';

                    -- Using UPPER and LOWER functions
                    SELECT UPPER(Last_Name) AS Upper_Result, LOWER(Last_Name) AS Lower_Result FROM Students WHERE Last_Name = 'Shah';

                    -- Using DATE functions
                    SELECT TO_DATE('2024-01-02', 'YYYY-MM-DD') + 31 AS Future_Date FROM dual;
                    SELECT TO_DATE('2024-02-01', 'YYYY-MM-DD') - TO_DATE('2024-02-27', 'YYYY-MM-DD') AS Day_Difference FROM dual;

                    -- Using Math functions
                    SELECT ABS(-6) AS Absolute_Value FROM dual;
                    SELECT CEIL(5.7) AS Ceiling_Value FROM dual;
                    SELECT FLOOR(5.7) AS Floor_Value FROM dual;
                    SELECT MOD(9, 5) AS Mod_Result FROM dual;
                    SELECT POWER(2, 5) AS Power_Result FROM dual;
                    SELECT SQRT(9) AS Square_Root FROM dual;
                    SELECT ROUND(5.7) AS Rounded_Value FROM dual;