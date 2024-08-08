## SQL Queries

1. **Rename Column in a Table**:
    ```sql
    ALTER TABLE table_name RENAME COLUMN old_column_name TO new_column_name;
    ```

2. **Add AUTO_INCREMENT in Existing Table**:
    ```sql
    ALTER TABLE table_name MODIFY COLUMN column_name INT AUTO_INCREMENT;
    ```

3. **Change Column Data Type**:
    ```sql
    ALTER TABLE employee MODIFY COLUMN salary INT;
    ```

4. **Find Maximum Salary**:
    ```sql
    SELECT MAX(salary) FROM employee;
    ```

5. **Find Minimum Salary**:
    ```sql
    SELECT MIN(salary) FROM employee;
    ```

6. **Find Average Salary**:
    ```sql
    SELECT AVG(salary) AS average_salary FROM employee;
    ```

7. **Find Distinct Addresses**:
    ```sql
    SELECT DISTINCT address FROM employee;
    ```

8. **Count of Last Names**:
    ```sql
    SELECT COUNT(last_name) FROM employee;
    ```

9. **Find Second Highest Salary**:
    ```sql
    SELECT MAX(salary) FROM employee WHERE salary < (SELECT MAX(salary) FROM employee);
    ```

10. **Set Default Value in a Table**:
    ```sql
    ALTER TABLE table_name ALTER COLUMN column_name SET DEFAULT default_value;
    ```

11. **Find Distinct Values where ID is Even**:
    ```sql
    SELECT DISTINCT state FROM employee WHERE id % 2 = 0;
    ```

12. **Find Difference Between Total CITY Entries and Distinct CITY Entries**:
    ```sql
    SELECT COUNT(city) - COUNT(DISTINCT city) FROM station;
    ```

13. **Select Multiple Characters that Start with Specific Letters**:
    ```sql
    SELECT first_name FROM employee WHERE first_name LIKE 'a%' OR first_name LIKE 'e%' OR first_name LIKE 'i%';
    ```

14. **Select Distinct CITY with Specific Conditions**:
    ```sql
    SELECT DISTINCT city FROM station WHERE LOWER(SUBSTR(city, 1, 1)) NOT IN ('a', 'e', 'i', 'o', 'u') OR LOWER(SUBSTR(city, LENGTH(city), 1)) NOT IN ('a', 'e', 'i', 'o', 'u');
    ```

15. **Find ASCII Value of Specific Column**:
    ```sql
    SELECT ASCII(column_name) AS column_name FROM table_name;
    ```

16. **Find String Length**:
    ```sql
    SELECT LENGTH(column_name) AS string_length FROM table_name;
    ```

17. **Find Max Salary When Employee is Unknown**:
    ```sql
    SELECT salary FROM company ORDER BY salary DESC LIMIT 1 OFFSET 4;
    ```

18. **Find Second Highest Salary from a Table**:
    ```sql
    SELECT salary FROM company ORDER BY salary DESC LIMIT 1 OFFSET 1;
    ```

19. **Find Even ID Numbers**:
    ```sql
    SELECT * FROM company WHERE id % 2 = 0;
    ```

20. **Find Odd ID Numbers**:
    ```sql
    SELECT * FROM company WHERE id % 2 != 0;
    ```

21. **Insert Multiple Rows in a Single Column**:
    ```sql
    UPDATE company SET Incoming = CASE id
        WHEN 1 THEN '10:30'
        WHEN 2 THEN '8:30'
        ELSE Incoming
    END WHERE id IN (1, 2);
    ```

22. **Add Column After Another Column in Table**:
    ```sql
    ALTER TABLE company ADD COLUMN holidays VARCHAR(30) AFTER outgoing;
    ```

23. **Add Primary Key with AUTO_INCREMENT in Existing Table**:
    ```sql
    ALTER TABLE table_name ADD PRIMARY KEY (id), MODIFY id INT AUTO_INCREMENT;
    ```

24. **Cross Join**:
    ```sql
    SELECT * FROM table1_name CROSS JOIN table2_name;
    ```

25. **Find Distinct Values where ID is Odd**:
    ```sql
    SELECT DISTINCT state FROM employee WHERE id % 2 != 0;
    ```

26. **Find Total Number of Records in a Table**:
    ```sql
    SELECT COUNT(*) FROM table_name;
    ```

27. **Find Records with NULL Values in a Specific Column**:
    ```sql
    SELECT * FROM table_name WHERE column_name IS NULL;
    ```

28. **Update Multiple Columns Based on Condition**:
    ```sql
    UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
    ```

29. **Delete Records Based on Condition**:
    ```sql
    DELETE FROM table_name WHERE condition;
    ```

30. **Add a New Column to a Table**:
    ```sql
    ALTER TABLE table_name ADD COLUMN new_column_name data_type;
    ```
30. ** how to find department with group a Table**:
    ```sql
     select department,count(*) as tech_mahindra from mahindra group by department;
    