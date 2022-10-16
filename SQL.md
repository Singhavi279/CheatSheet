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

## MANAGING TABLES

```SQL
CREATE TABLE t (
id INT PRIMARY KEY,
name VARCHAR NOT NULL,
price INT DEFAULT 0
);
--Create a new table with three columns
```

```SQL
DROP TABLE t ;
Delete the table from the database
```

```SQL
ALTER TABLE t ADD column;
--Add a new column to the table
```

```SQL
ALTER TABLE t DROP COLUMN c ;
--Drop column c from the table
```

```SQL
ALTER TABLE t ADD constraint;
--Add a constraint
```

```SQL
ALTER TABLE t DROP constraint;
--Drop a constraint
```

```SQL
ALTER TABLE t1 RENAME TO t2;
--Rename a table from t1 to t2
```

```SQL
ALTER TABLE t1 RENAME c1 TO c2 ;
--Rename column c1 to c2
```

```SQL
TRUNCATE TABLE t;
--Remove all data in a table
```

## USING SQL CONSTRAINTS

```SQL 
  CREATE TABLE t(c1 INT,c2 INT,C3 VARCHAR, PRIMARY KEY(c1,c2));
  --Set c1 and c2 as a primary key
```

```SQL
CREATE TABLE t1(c1 INT PRIMARY KEY,c2 INT,FOREIGN KEY (c2) REFERENCES t2(c2));
--Set c2 column as a foreign key
```

```SQL
CREATE TABLE t(c1 INT, c1 INT,UNIQUE(c2,c3));
--Make the values in c1 and c2 unique
```

```SQL
CREATE TABLE t(c1 INT, c2 INT,CHECK(c1> 0 AND c1 >= c2));
--Ensure c1 > 0 and values in c1 >= c2
```

```SQL
CREATE TABLE t(c1 INT PRIMARY KEY,c2 VARCHAR NOT NULL);
--Set values in c2 column not NULL
```

## MODIFYING DATA


```SQL
INSERT INTO t(column_list)
VALUES(value_list);
--Insert one row into a table
```

```SQL
INSERT INTO t(column_list)
VALUES (value_list),
(value_list), ….;
--Insert multiple rows into a table
```

```SQL
INSERT INTO t1(column_list) SELECT column_list FROM t2;
--Insert rows from t2 into t1
```

```SQL
UPDATE t
SET c1 = new_value;
--Update new value in the column c1 for all rows
```

```SQL
UPDATE t
SET c1 = new_value, c2 = new_value WHERE condition;
--Update values in the column c1, c2 that match the condition
```

```SQL
DELETE FROM t;
--Delete all data in a table
```

```SQL
DELETE FROM t
WHERE condition;
--Delete subset of rows in a table
```



