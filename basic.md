### 1. SELECT
```
SELECT * FROM table_name;
```

### 2. Queries with constraints
- WHERE clause
```
SELECT column,...
FORM table
WHERE condition
```

Operator | SQL Example
:-: | :-:
BETWEEN ... AND ... | clo_name **BETWEEN** 0.5 **AND** 1.5
NOT BETWEEN ... AND ... | clo_name NOT **BETWEEN** 2000 **AND** 2010
IN (...) | clo_name **IN** (1, 3, 5)
NOT IN (...) | col_name **NOT IN** (1, 3, 5)
<center>表1</center>

Operator | Condition | Example
:-: | :-: | :-:
LIKE | Case insensitive exact string comparison | col_name **LIKE** 'abc'
NOT LIKE | Case insensitive exact string inequality comparison | col_name **NOT LIKE ** 'abc'
% | Match(only with LIKE or NOT LIKE | col_name **LIKE** '%hello%'
_ | Used to match a single character(only with LIKE or NOT LIKE) | col_name **LIKE** "AN_"
IN (...) | String exists in a list | col_name **IN** ("A", "B")
NOT IN (...) | String does not exit in a list | col_name **NOT IN** ("C", "E")
<center>表2</center>

```
SELECT column,...
FORM table
WHERE condition
  AND/OR another_condition
```

### 3. Filtering and sorting Query results
- Unique results
```
SELECT DISTINCT column, another_column, ...
FROM table_name
WHERE condition(s)
```
- Ordering results
```
% Select query with ordered results
SELECT column, another_column, ...
FROM table_name
WHERE condition(s)
ORDER BY column ASC/DESC;
```
- Limiting results to a subset
```sql
% Select query with limited rows
SELECT column, another_column, ...
FROM table_name
WHERE condition(s)
ORDER BY column ASC/DESC
LIMIT num_limit OFFSET num_offset % offset偏移量
```

eg.

> List the last four Pixar movies released (ordered from most recent to least) 

```
SELECT * FROM movies
ORDER BY year DESC
LIMIT 4;
```

![sql_eg_1](images/sql_eg_1.png)

eg.

> List the **next** five Pixar movies sorted alphabetically

```SQL
SELECT * FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;
```

![sql_eg_2](images/sql_eg_2.png)

