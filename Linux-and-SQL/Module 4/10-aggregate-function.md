# SQL Aggregate Functions

## Overview

**Aggregate functions** are functions that perform a calculation over multiple data points and return the result of that calculation. The underlying raw data is not returned — only the calculated result.

## Key Concepts

### Common Aggregate Functions

- **`COUNT`**: Returns a single number representing the number of rows returned from a query.
- **`AVG`**: Returns a single number representing the average of the numerical data in a column.
- **`SUM`**: Returns a single number representing the sum of the numerical data in a column.

### Aggregate Function Syntax

To use an aggregate function, place its keyword after `SELECT`, followed by the target column in parentheses.

**Example:** Finding the total number of customers using `COUNT` (excludes `NULL` values):

```sql
SELECT COUNT(firstname)
FROM customers;
```

This returns a table with one column, `COUNT(firstname)`, and one row containing the count.

A filter can be added to narrow the count:

```sql
SELECT COUNT(firstname)
FROM customers
WHERE country = 'USA';
```

This returns a lower count, limited to records where `country` is `'USA'`.

> Other aggregate functions (e.g., `SUM`, `AVG`) follow the same syntax pattern as `COUNT` — placed after `SELECT`.

## Key Takeaways

- Aggregate functions (`COUNT`, `SUM`, `AVG`, etc.) perform calculations across multiple rows and return a single summarized result.
- `COUNT` excludes `NULL` values when counting rows.
- Filters (`WHERE`) can be combined with aggregate functions to calculate results over a specific subset of data.
- SQL has many additional keywords and applications beyond aggregate functions, worth continuing to explore for practical use as a security analyst.