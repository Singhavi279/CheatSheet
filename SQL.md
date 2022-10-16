# SQL Cheat Sheet

The SQL cheat sheet provides you with the most commonly used SQL statements for your reference.

## QUERYING DATA FROM A TABLE

```SQL
SELECT c1, c2 FROM t;
--Query data in columns c1, c2 from a table
```

```SQL
SELECT * FROM t;
--Query all rows and columns from a table
```

```SQL 
SELECT c1, c2 FROM t
WHERE condition;
--Query data and filter rows with a condition
```

```SQL
SELECT c1, c2 FROM t
ORDER BY c1 ASC [DESC];
--Sort the result set in ascending or descending order
```

```SQL
SELECT c1, c2 FROM t
ORDER BY c1
LIMIT n OFFSET offset;
--Skip offset of rows and return the next n rows 
```

```SQL
SELECT c1, aggregate(c2)
FROM t
GROUP BY c1;
--Group rows using an aggregate function
```

```SQL
SELECT c1, aggregate(c2)
FROM t
GROUP BY c1
HAVING condition;
--Filter groups using HAVING clause
```

