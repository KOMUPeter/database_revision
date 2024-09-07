markdown
Copy code
# Basic SQL Commands

## 1. SELECT: Retrieving Data from a Database

**Definition:** The `SELECT` statement is used to retrieve data from one or more tables in a database.

**Syntax:**
```sql
SELECT column1, column2, ...
FROM table_name;
Examples

Retrieve all columns from a table named Employees:

sql
Copy code
SELECT * 
FROM Employees;
The * wildcard selects all columns from the table.

Retrieve specific columns, such as FirstName and LastName, from the Employees table:

sql
Copy code
SELECT FirstName, LastName 
FROM Employees;
This query selects only the FirstName and LastName columns.

2. WHERE: Filtering Data
The WHERE clause filters records based on specified conditions. It allows you to narrow down the results returned by the SELECT statement.

Syntax:

sql
Copy code
SELECT column1, column2, ...
FROM table_name
WHERE condition;
Examples

Retrieve all employees whose Age is greater than 30:

sql
Copy code
SELECT * 
FROM Employees
WHERE Age > 30;
This query returns employees with an age greater than 30.

Find employees with the last name 'Smith':

sql
Copy code
SELECT * 
FROM Employees
WHERE LastName = 'Smith';
This query returns employees whose last name is 'Smith'.

3. ORDER BY: Sorting Data
The ORDER BY clause sorts the result set by one or more columns. You can specify the sorting order as ascending (ASC) or descending (DESC).

Syntax:

sql
Copy code
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 [ASC|DESC], column2 [ASC|DESC], ...;
Examples

Retrieve all employees sorted by LastName in ascending order:

sql
Copy code
SELECT * 
FROM Employees
ORDER BY LastName ASC;
This query sorts the results by LastName in ascending order.

Sort employees by Age in descending order:

sql
Copy code
SELECT * 
FROM Employees
ORDER BY Age DESC;
This query sorts the results by Age in descending order.

4. LIMIT: Limiting the Number of Results
The LIMIT clause restricts the number of records returned by the SELECT statement.

Syntax:

sql
Copy code
SELECT column1, column2, ...
FROM table_name
LIMIT number;
Examples

Retrieve the first 5 records from the Employees table:

sql
Copy code
SELECT * 
FROM Employees
LIMIT 5;
This query returns only the first 5 rows from the table.

Get the top 10 oldest employees:

sql
Copy code
SELECT * 
FROM Employees
ORDER BY Age DESC
LIMIT 10;
This query sorts the employees by Age in descending order and returns the top 10 results.