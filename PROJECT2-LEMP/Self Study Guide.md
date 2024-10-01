# SQL Syntax and Commonly Used Commands

## Overview of SQL

**SQL (Structured Query Language)** is used to communicate with databases. It is essential for managing and manipulating relational databases. SQL commands are categorized into several types like Data Query Language (DQL), Data Definition Language (DDL), Data Manipulation Language (DML), and Data Control Language (DCL).

---

## 1. SELECT Statement

The `SELECT` statement is used to retrieve data from a database.

```sql
SELECT column1, column2, ...
FROM table_name;
```
## 2. WHERE Clause
The WHERE clause filters records based on specific conditions.

```sql
SELECT column1, column2
FROM table_name
WHERE condition;
```

## 3. INSERT INTO Statement
The INSERT INTO statement is used to add new records to a table.

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

## 4. UPDATE Statement
The UPDATE statement modifies existing records in a table.

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

## 5. DELETE Statement
The DELETE statement removes existing records from a table.

```sql
DELETE FROM table_name
WHERE condition;
```

## 6. CREATE TABLE Statement
The CREATE TABLE statement creates a new table in the database.

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    ...
);
```

## 7. ALTER TABLE Statement
The ALTER TABLE statement modifies an existing table.

### Add a column:
```sql
ALTER TABLE table_name
ADD column_name datatype;
```

### Drop a column:
```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

## 8. DROP TABLE Statement
The DROP TABLE statement deletes an entire table from the database.

```sql
DROP TABLE table_name;
```

## 9. JOIN Clause
The JOIN clause combines rows from two or more tables based on a related column.

### INNER JOIN
```sql
SELECT column1, column2, ...
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

## 10. GROUP BY Clause
The GROUP BY clause groups rows sharing the same values into summary rows.

```sql
SELECT column1, COUNT(*)
FROM table_name
GROUP BY column1;
```
## 11. ORDER BY Clause
The ORDER BY clause sorts the result set in ascending or descending order.

```sql
SELECT column1, column2
FROM table_name
ORDER BY column1 [ASC|DESC];
```

## 12. LIMIT Clause
The LIMIT clause limits the number of records returned by a query.

```sql
SELECT column1, column2
FROM table_name
LIMIT number;
```

## 13. LIKE Operator
The LIKE operator searches for a specified pattern in a column.

```sql
SELECT column1, column2
FROM table_name
WHERE column1 LIKE pattern;
```

### Wildcards:
%: Represents zero or more characters.

_: Represents a single character.

## 14. BETWEEN Operator
The BETWEEN operator filters records within a range of values.

```sql
SELECT column1, column2
FROM table_name
WHERE column1 BETWEEN value1 AND value2;
```

## 15. DISTINCT Keyword
The DISTINCT keyword returns only unique values from a column.

```sql
SELECT DISTINCT column1
FROM table_name;
```


## 16. Subqueries
A subquery is a query inside another query.

```sql
SELECT column1
FROM table_name
WHERE column1 = (SELECT column2 FROM table2 WHERE condition);
```

## 17. PRIMARY KEY and FOREIGN KEY
### PRIMARY KEY
A PRIMARY KEY uniquely identifies each record in a table.

```sql
CREATE TABLE table_name (
    id INT PRIMARY KEY,
    column1 datatype,
    ...
);
```


### FOREIGN KEY
A FOREIGN KEY is a key that links two tables together.

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    FOREIGN KEY (column1) REFERENCES other_table(column_name)
);
```

### 18. Transactions
Transactions ensure that a series of SQL statements are executed successfully or rolled back if one of them fails.

```sql
START TRANSACTION;

UPDATE accounts
SET balance = balance - 100
WHERE account_id = 1;

UPDATE accounts
SET balance = balance + 100
WHERE account_id = 2;

COMMIT;
```

If any statement fails, you can roll back the transaction:

```sql
ROLLBACK;
```

