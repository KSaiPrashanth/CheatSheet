
![header](/images/SQL%20Cheat%20Sheet.webp)

---

### Table of Contents

- [**SQL Cheat Sheet**](#sql-cheat-sheet)
  - [**1. Basic SQL Syntax**](#1-basic-sql-syntax)
  - [**2. Aggregate Functions**](#2-aggregate-functions)
  - [**3. Grouping Data**](#3-grouping-data)
  - [**4. Joins**](#4-joins)
  - [**5. Subqueries**](#5-subqueries)
  - [**6. Data Manipulation**](#6-data-manipulation)
  - [**7. Table Management**](#7-table-management)

## SQL Cheat Sheet

### **1. Basic SQL Syntax**

- **Select All Columns:**
  ```sql
  SELECT * FROM table_name;
  ```

- **Select Specific Columns:**
  ```sql
  SELECT column1, column2 FROM table_name;
  ```

- **Filter Results:**
  ```sql
  SELECT * FROM table_name WHERE condition;
  ```

- **Sort Results:**
  ```sql
  SELECT * FROM table_name ORDER BY column1 ASC|DESC;
  ```

- **Limit Results:**
  ```sql
  SELECT * FROM table_name LIMIT number;
  ```

### **2. Aggregate Functions**

- **Count Rows:**
  ```sql
  SELECT COUNT(*) FROM table_name;
  ```

- **Sum Values:**
  ```sql
  SELECT SUM(column_name) FROM table_name;
  ```

- **Average Values:**
  ```sql
  SELECT AVG(column_name) FROM table_name;
  ```

- **Minimum Value:**
  ```sql
  SELECT MIN(column_name) FROM table_name;
  ```

- **Maximum Value:**
  ```sql
  SELECT MAX(column_name) FROM table_name;
  ```

### **3. Grouping Data**

- **Group By:**
  ```sql
  SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
  ```

- **Having Clause:**
  ```sql
  SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name HAVING COUNT(*) > value;
  ```

### **4. Joins**

- **Inner Join:**
  ```sql
  SELECT columns FROM table1 INNER JOIN table2 ON table1.column = table2.column;
  ```

- **Left Join:**
  ```sql
  SELECT columns FROM table1 LEFT JOIN table2 ON table1.column = table2.column;
  ```

- **Right Join:**
  ```sql
  SELECT columns FROM table1 RIGHT JOIN table2 ON table1.column = table2.column;
  ```

- **Full Join:**
  ```sql
  SELECT columns FROM table1 FULL JOIN table2 ON table1.column = table2.column;
  ```

### **5. Subqueries**

- **Subquery in SELECT:**
  ```sql
  SELECT column1, (SELECT column2 FROM table2 WHERE condition) AS alias FROM table1;
  ```

- **Subquery in WHERE:**
  ```sql
  SELECT column1 FROM table1 WHERE column2 = (SELECT column2 FROM table2 WHERE condition);
  ```

### **6. Data Manipulation**

- **Insert Data:**
  ```sql
  INSERT INTO table_name (column1, column2) VALUES (value1, value2);
  ```

- **Update Data:**
  ```sql
  UPDATE table_name SET column1 = value1 WHERE condition;
  ```

- **Delete Data:**
  ```sql
  DELETE FROM table_name WHERE condition;
  ```

### **7. Table Management**

- **Create Table:**
  ```sql
  CREATE TABLE table_name (
      column1 datatype constraints,
      column2 datatype constraints
  );
  ```

- **Drop Table:**
  ```sql
  DROP TABLE table_name;
  ```

- **Alter Table:**
  ```sql
  ALTER TABLE table_name ADD column_name datatype;
  ALTER TABLE table_name DROP COLUMN column_name;
  ```

This should cover most of the basic and intermediate SQL tasks. Let me know if you need anything more specific!
