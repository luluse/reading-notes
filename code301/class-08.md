# SQL

Structured Query Language: language designed to allow both technical and non-technical users query, manipulate, and transform data from a relational database.

A **relational database** represents a collection of related (two-dimensional) tables. Each of the tables are similar to an Excel spreadsheet, with a fixed number of named columns (the attributes or properties of the table) and any number of rows of data.

### SQL Lesson 1: SELECT queries 101

To retrieve data from a SQL database, we need to write SELECT statements, which are often colloquially refered to as queries.

Select query for a specific columns:

`SELECT column, another_column, …`

`FROM mytable;`

Select query for all columns:

`SELECT *` 

`FROM mytable;`

### SQL Lesson 2: Queries with constraints

In order to filter certain results from being returned, we need to use a WHERE clause in the query. The clause is applied to each row of data by checking specific column values to determine whether it should be included in the results or not.

`SELECT column, another_column, …`

`FROM mytable`

`WHERE condition`

   `AND/OR another_condition`

   ` AND/OR …;`


- =, !=, < <=, >, >=	Standard numerical operators `col_name != 4`
- BETWEEN … AND …	Number is within range of two values (inclusive)	`col_name BETWEEN 1.5 AND 10.5`
- NOT BETWEEN … AND …	Number is not within range of two values (inclusive)	`col_name NOT BETWEEN 1 AND 10`
- IN (…)	Number exists in a list	`col_name IN (2, 4, 6)`
- NOT IN (…)	Number does not exist in a list	`col_name NOT IN (1, 3, 5)`

### SQL Lesson 3: Queries with constraints

- =	Case sensitive exact string comparison (notice the single equals)	`col_name = "abc"`
- != or <>	Case sensitive exact string inequality comparison	`col_name != "abcd"`
- LIKE	Case insensitive exact string comparison	`col_name LIKE "ABC"`
- NOT LIKE	Case insensitive exact string inequality comparison	`col_name NOT LIKE "ABCD"`
- %	Used anywhere in a string to match a sequence of zero or more characters (only with LIKE or NOT LIKE)	`col_name LIKE "%AT%"
(matches "AT", "ATTIC", "CAT" or even "BATS")`
- _	Used anywhere in a string to match a single character (only with LIKE or NOT LIKE) `col_name LIKE "AN_" (matches "AND", but not "AN")`
- IN (…)	String exists in a list	`col_name IN ("A", "B", "C")`
- NOT IN (…)	String does not exist in a list	`col_name NOT IN ("D", "E", "F")`

All strings must be quoted so that the query parser can distinguish words in the string from SQL keywords.

### SQL Lesson 4: Filtering and sorting Query results

- DISTINCT: SQL provides a convenient way to discard rows that have a duplicate column value by using the DISTINCT keyword. it will blindly remove duplicate rows. `SELECT DISTINCT column, another_column, …`

- ORDER BY: SQL provides a way to sort your results by a given column in ascending or descending order using the ORDER BY clause. `ORDER BY column ASC/DESC;`

- LIMIT: will reduce the number of rows to return

- OFFSET: will specify where to begin counting the number rows from. `LIMIT num_limit OFFSET num_offset;`

### SQL Lesson 13: Inserting rows

INSERT statement declares which table to write into, the columns of data that we are filling, and one or more rows of data to insert.

`INSERT INTO mytable`

`VALUES (value_or_expr, another_value_or_expr, …),`

   `(value_or_expr_2, another_value_or_expr_2, …), …;`

 ###  SQL Lesson 14: Updating rows

 `UPDATE mytable`

`SET column = value_or_expr, other_column = another_value_or_expr, `
    
`WHERE condition;`

### SQL Lesson 15: Deleting rows

`DELETE FROM mytable`

`WHERE condition;`

### SQL Lesson 16: Creating tables


`CREATE TABLE movies (`

 `id INTEGER PRIMARY KEY,`
 `title TEXT,`
 `director TEXT,`
 `year INTEGER, `
 `length_minutes INTEGER`
);

### SQL Lesson 17: Altering tables

update your tables and database schemas by using the ALTER TABLE statement to add, remove, or modify columns and table constraints.

`ALTER TABLE mytable`
`ADD column DataType OptionalTableConstraint `

`ALTER TABLE mytable`
`DROP column_to_be_deleted;`

`ALTER TABLE mytable`
`RENAME TO new_table_name;`

### SQL Lesson 18: Dropping tables

remove an entire table including all of its data and metadata: use the DROP TABLE statement.

`DROP TABLE IF EXISTS mytable;`