# Day 27 - 16.01.2025
**Protocol writer:** Martin Volman  

---

## Introduction to SQL JOINs and CTEs

In this session, we focused on understanding and applying the **JOIN** function and **Common Table Expressions (CTEs)** in SQL.

---

## JOIN in SQL

Using **JOIN** allows you to combine two or more tables in SQL.  
Here are the main types of JOINs:

### 1. INNER JOIN  
Returns only the rows with matching values in both tables.  
```sql
SELECT * 
FROM table1
INNER JOIN table2
ON table1.id = table2.id;
```

### 2. LEFT JOIN  
Returns all rows from the left table and the matched rows from the right table.  
```sql
SELECT * 
FROM table1
LEFT JOIN table2
ON table1.id = table2.id;
```

### 3. RIGHT JOIN  
Returns all rows from the right table and the matched rows from the left table.  
```sql
SELECT * 
FROM table1
RIGHT JOIN table2
ON table1.id = table2.id;
```

### 4. FULL JOIN  
Returns all rows when there is a match in either the left or the right table.  
```sql
SELECT * 
FROM table1
FULL JOIN table2
ON table1.id = table2.id;
```

---

## SQL Syntax Order of Operations

When writing SQL queries, the logical order of operations is as follows:
1. **SELECT**  
2. **FROM**  
3. **WHERE**  
4. **GROUP BY**  
5. **HAVING**  
6. **ORDER BY**  
7. **LIMIT**  

---

## Common Table Expressions (CTEs)

**CTE** stands for **Common Table Expression**.  
It functions as a temporary table or a subquery that exists only during the query execution.

### Why use CTEs?
- **Improves readability**: Makes queries easier to understand.
- **Simplifies complex queries**: Breaks down queries into smaller, manageable parts.
- **Reusability**: Useful when running the same query multiple times.

### Syntax Example:
```sql
WITH MonthlySales AS (
    SELECT
        Year,
        Month,
        SUM(TotalSales) AS TotalMonthlySales
    FROM SalesData
    GROUP BY Year, Month
)
SELECT *
FROM MonthlySales;
```

---

## Useful Links

- [Learn about JOIN](https://www.scaler.com/topics/sql/foreign-key-in-sql/)  
- [Introduction to CTEs](https://www.datacamp.com/tutorial/cte-sql)  

