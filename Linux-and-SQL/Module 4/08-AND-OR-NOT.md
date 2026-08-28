# SQL Filtering: Logical Operators

## Overview

`AND`, `OR`, and `NOT` allow you to filter queries to return specific information relevant to security analysis work. These are known as **logical operators**.

## Key Concepts

### AND

`AND` is used to filter on two conditions, both of which must be met simultaneously.

**Example:** Finding customers handled by support representative ID `5` **and** located in the USA:

```sql
SELECT firstname, lastname, email, country, supportrepid
FROM customers
WHERE supportrepid = 5 AND country = 'USA';
```

This query returns four rows of customer information, which can be used to contact them about a security concern.

### OR

`OR` also connects two conditions, but only requires that either condition be met. It returns results where the first condition, the second condition, or both are true.

**Example:** Finding all customers in the USA **or** Canada to communicate a security update:

```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE country = 'Canada' OR country = 'USA';
```

> **Note:** Even if both conditions reference the same column, each condition must be written out in full — e.g., `WHERE country = 'Canada' OR country = 'USA'`.

### NOT

Unlike `AND` and `OR`, `NOT` works on a single condition. It negates the condition, so SQL returns all records that do **not** match it.

**Example:** Finding all customers who are **not** in the USA (useful when an issue affects only non-USA customers, which is more efficient than listing every other country individually):

```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'USA';
```

> **Pro tip:** The `<>` or `!=` operators can also be used to find values not equal to a specified value. `WHERE country <> 'USA'` and `WHERE country != 'USA'` are equivalent to `WHERE NOT country = 'USA'`.

### Combining Logical Operators

Logical operators can be combined for more specific filters.

**Example:** Finding customers in all countries **except** the USA and Canada:

```sql
SELECT firstname, lastname, email, country
FROM customers
WHERE NOT country = 'Canada' AND NOT country = 'USA';
```

## Key Takeaways

- `AND` requires both conditions to be true simultaneously.
- `OR` requires that either one or both conditions be true.
- `NOT` negates a single condition, returning records that don't match it.
- `<>` and `!=` are alternative ways to express "not equal to."
- Logical operators can be combined to build more precise, targeted queries.