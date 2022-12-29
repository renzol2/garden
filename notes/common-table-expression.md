---
tags: sql
---

# Common table expression (CTE)

A **common table expression**, or CTE, is a temporary named result in [[sql|SQL]] created from a simple `SELECT` statement that can be used in subsequent `SELECT `statements.

- Each SQL CTE is like a _named query_, whose result is stored in a virtual table to be referenced later

## Example

```sql
WITH my_cte AS (
  SELECT a, b, c
  FROM T1
)
SELECT a, c
FROM my_cte
WHERE ...
```

## Sources

- <https://learnsql.com/blog/what-is-common-table-expression/>
