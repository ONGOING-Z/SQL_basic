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
BETWEEN ... AND ... | clo_name BETWEEN 0.5 AND 1.5
NOT BETWEEN ... AND ... | clo_name NOT BETWEEN 2000 AND 2010
IN (...) | clo_name IN (1, 3, 5)
NOT IN (...) | col_name NOT IN (1, 3, 5)
<center>表1</center>

Operator | Condition | Example
:-: | :-: | :-:
LIKE | Case insensitive exact string comparison | col_name **LIKE** 'abc'
NOT LIKE | Case insensitive exact string inequality comparison | col_name **NOT LIKE ** 'abc'**
% | Match(only with LIKE or NOT LIKE | col_name LIKE '%hello%'
_ | Used to match a single character(only with LIKE or NOT LIKE) | col_name LIKE "AN_"
IN (...) | String exists in a list | col_name IN ("A", "B")
NOT IN (...) | String does not exit in a list | col_name NOT IN ("C", "E")
<center>表2</center>

```
SELECT column,...
FORM table
WHERE condition
  AND/OR another_condition
```

