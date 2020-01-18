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
IN (...) | clo_name IN (1, 3, 5)
NOT IN (...) | col_name NOT IN (1, 3, 5)


## FATAL
1. fatal: pathspec 'remote' did not match any files
解决方法：
```
git pull origin master --allow-unrelated-histories
```
