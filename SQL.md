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

## QUERYING FROM MULTIPLE TABLES

```SQL
SELECT c1, c2
FROM t1
INNER JOIN t2 ON condition;
--Inner join t1 and t2
```

```SQL
SELECT c1, c2
FROM t1
LEFT JOIN t2 ON condition;
--Left join t1 and t1
```

```SQL
SELECT c1, c2
FROM t1
RIGHT JOIN t2 ON condition;
--Right join t1 and t2
```

```SQL
SELECT c1, c2
FROM t1
FULL OUTER JOIN t2 ON condition;
--Perform full outer join
```

```SQL
SELECT c1, c2
FROM t1
CROSS JOIN t2;
--Produce a Cartesian product of rows in tables
```

```SQL
SELECT c1, c2
FROM t1, t2;
--Another way to perform cross join
```

```SQL
SELECT c1, c2
FROM t1 A
INNER JOIN t2 B ON condition;
--Join t1 to itself using INNER JOIN clause
```

## USING SQL OPERATORS

```SQL
SELECT c1, c2 FROM t1
UNION [ALL]
SELECT c1, c2 FROM t2;
--Combine rows from two queries
```

```SQL
SELECT c1, c2 FROM t1
INTERSECT
SELECT c1, c2 FROM t2;
--Return the intersection of two queries
```

```SQL
SELECT c1, c2 FROM t1
MINUS
SELECT c1, c2 FROM t2;
--Subtract a result set from another result set
```

```SQL
SELECT c1, c2 FROM t1
WHERE c1 [NOT] LIKE pattern;
--Query rows using pattern matching %, _
```

```SQL
SELECT c1, c2 FROM t
WHERE c1 [NOT] IN value_list;
--Query rows in a list
```

```SQL
SELECT c1, c2 FROM t
WHERE c1 BETWEEN low AND high;
--Query rows between two values
```

```SQL
SELECT c1, c2 FROM t
WHERE c1 IS [NOT] NULL;
--Check if values in a table is NULL or not
```
