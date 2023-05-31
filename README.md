# SQL Interview Questions And Answers

Most targeted up-to-date SQL interview questions and answers list

# Table of Contents

1. [What is the difference between INNER JOIN and LEFT JOIN in SQL?](#1-what-is-the-difference-between-inner-join-and-left-join-in-sql)
2. [What is a subquery in SQL? Provide an example.](#2-what-is-a-subquery-in-sql-provide-an-example)
3. [How can you find the second highest salary in a table?](#3-how-can-you-find-the-second-highest-salary-in-a-table)
4. [Explain the difference between WHERE and HAVING clauses in SQL.](#4-explain-the-difference-between-where-and-having-clauses-in-sql)
5. [How can you calculate the total count of rows in a table?](#5-how-can-you-calculate-the-total-count-of-rows-in-a-table)
6. [Explain the difference between UNION and UNION ALL operators in SQL.](#6-explain-the-difference-between-union-and-union-all-operators-in-sql)
7. [How can you find the maximum value from a column in SQL?](#7-how-can-you-find-the-maximum-value-from-a-column-in-sql)
8. [Explain the difference between LIKE and IN operators in SQL.](#8-explain-the-difference-between-like-and-in-operators-in-sql)
9. [How can you calculate the average of a column in SQL?](#9-how-can-you-calculate-the-average-of-a-column-in-sql)
10. [Explain the difference between BETWEEN and IN operators in SQL.](#10-explain-the-difference-between-between-and-in-operators-in-sql)
11. [How can you calculate the sum of a column in SQL?](#11-how-can-you-calculate-the-sum-of-a-column-in-sql)
12. [Explain the difference between GROUP BY and ORDER BY clauses in SQL.](#12-explain-the-difference-between-group-by-and-order-by-clauses-in-sql)
- [Whats more?](#whats-more)
- [Contributing](#contributing)
- [License](#license)

## 1. What is the difference between INNER JOIN and LEFT JOIN in SQL?

INNER JOIN returns only the matching rows between two tables based on the join condition, while LEFT JOIN returns all the rows from the left table and the matching rows from the right table.

Example of INNER JOIN:

```sql
SELECT *
FROM table1
INNER JOIN table2 ON table1.id = table2.id;
```

Example of LEFT JOIN:

```sql
SELECT *
FROM table1
LEFT JOIN table2 ON table1.id = table2.id;
```

## 2. What is a subquery in SQL? Provide an example.

A subquery is a query nested within another query, used to retrieve data based on the result of the outer query.

Example:

```sql
SELECT column1
FROM table1
WHERE column2 IN (SELECT column3 FROM table2 WHERE condition);
```

## 3. How can you find the second highest salary in a table?

You can use the ORDER BY and LIMIT clauses to find the second highest salary.

Example:

```sql
SELECT salary
FROM employees
ORDER BY salary DESC
LIMIT 1, 1;
```

## 4. Explain the difference between WHERE and HAVING clauses in SQL.

The WHERE clause is used to filter rows before grouping and aggregating, while the HAVING clause is used to filter groups after grouping and aggregating.

Example of WHERE:

```sql
SELECT *
FROM employees
WHERE salary > 50000;
```

Example of HAVING:

```sql
SELECT department, AVG(salary) as avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;
```

## 5. How can you calculate the total count of rows in a table?

You can use the COUNT() function to calculate the total count of rows in a table.

Example:

```sql
SELECT COUNT(*)
FROM table1;
```

## 6. Explain the difference between UNION and UNION ALL operators in SQL.

UNION combines the result sets of two or more SELECT statements, removing duplicate rows, while UNION ALL includes all rows, including duplicates.

Example of UNION:

```sql
SELECT column1 FROM table1
UNION
SELECT column1 FROM table2;
```

Example of UNION ALL:

```sql
SELECT column1 FROM table1
UNION ALL
SELECT column1 FROM table2;
```

## 7. How can you find the maximum value from a column in SQL?

You can use the MAX() function to find the maximum value from a column.

Example:

```sql
SELECT MAX(salary)
FROM employees;
```

## 8. Explain the difference between LIKE and IN operators in SQL.

The LIKE operator is used for pattern matching with wildcard characters, while the IN operator is used to specify multiple possible values.

Example of LIKE:

```sql
SELECT *
FROM employees
WHERE last_name LIKE 'Sm%';
```

Example of IN:

```sql
SELECT *
FROM employees
WHERE department IN ('HR', 'Marketing');
```

## 9. How can you calculate the average of a column in SQL?

You can use the AVG() function to calculate the average of a column.

Example:

```sql
SELECT AVG(salary)
FROM employees;
```

## 10. Explain the difference between BETWEEN and IN operators in SQL.

The BETWEEN operator is used to specify a range of values, while the IN operator is used to specify multiple possible values.

Example of BETWEEN:

```sql
SELECT *
FROM employees
WHERE salary BETWEEN 50000 AND 80000;
```

Example of IN:

```sql
SELECT *
FROM employees
WHERE department IN ('HR', 'Marketing', 'Finance');
```

## 11. How can you calculate the sum of a column in SQL?

You can use the SUM() function to calculate the sum of a column.

Example:

```sql
SELECT SUM(quantity)
FROM orders;
```

## 12. Explain the difference between GROUP BY and ORDER BY clauses in SQL.

The GROUP BY clause is used to group rows based on specified columns, while the ORDER BY clause is used to sort the result set based on specified columns

Example of GROUP BY:

```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department;
```

Example of ORDER BY:

```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department
ORDER BY AVG(salary) DESC;
```

## What's more?
<a href="https://interviewplus.ai/database-administration/sql/questions">A comprehensive list of questions and answers</a>

## Contributing
We welcome contributions from our users to help make this resource as comprehensive and useful as possible. If you have been recently interviewed and encountered a question that is not currently covered on our website, feel free to suggest it as a new question. Your contributions will be added to our platform, and we will make sure to credit you for your contributions. We appreciate your help in making our platform a valuable tool for all job seekers.

## License
MIT License
