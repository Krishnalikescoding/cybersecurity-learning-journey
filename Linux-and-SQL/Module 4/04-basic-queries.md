# Basic SQL Queries

## Overview

Security analysts can use SQL queries to retrieve specific information from databases.

A common security-related task is determining which computer has been assigned to a particular employee. This can be done by querying an `employees` table and selecting the relevant columns.

## `SELECT` and `FROM`

Two important SQL keywords used in basic queries are:

- **`SELECT`**: Specifies the columns to return.
- **`FROM`**: Specifies the table to query.

### Basic Syntax

```sql
SELECT column1, column2
FROM table_name;
```

For example, if the `employees` table contains `employee_id` and `device_id`, a query can return only those two columns:

```sql
SELECT employee_id, device_id
FROM employees;
```

This query:

1. Uses `SELECT` to specify the `employee_id` and `device_id` columns.
2. Uses `FROM` to specify the `employees` table.
3. Uses a comma to separate the columns being selected.
4. Uses a semicolon (`;`) to mark the end of the SQL statement.

## SQL Syntax

**Syntax** refers to the rules that determine how statements must be structured in a programming or query language.

### SQL Keywords

SQL keywords are **not case-sensitive**.

For example, these queries are equivalent:

```sql
SELECT employee_id, device_id
FROM employees;
```

```sql
select employee_id, device_id
from employees;
```

Uppercase keywords are commonly used because they make SQL queries easier to read and distinguish from table and column names.

### Semicolons

SQL statements commonly end with a semicolon (`;`).

Example:

```sql
SELECT employee_id, device_id
FROM employees;
```

## Selecting All Columns

Sometimes an analyst needs to retrieve all columns from a table rather than selecting specific columns.

The asterisk (`*`) can be used to select all columns.

This is commonly referred to as **select all**.

### Example

```sql
SELECT *
FROM employees;
```

This query returns all columns and rows from the `employees` table.

For example, if the table contains:

- `employee_id`
- `device_id`
- `username`
- `department`
- `office`

the query returns all five columns.

## Specific Columns vs. All Columns

| Query | Result |
|---|---|
| `SELECT employee_id, device_id FROM employees;` | Returns only `employee_id` and `device_id` |
| `SELECT * FROM employees;` | Returns all columns from `employees` |

## Example: Employee and Device Information

Suppose the `employees` table contains information about employees and the computers assigned to them.

To retrieve only employee and device information:

```sql
SELECT employee_id, device_id
FROM employees;
```

If additional information is needed, such as the employee's department, username, or office, all columns can be retrieved:

```sql
SELECT *
FROM employees;
```

## Key Takeaways

- **`SELECT`** specifies which columns to return.
- **`FROM`** specifies which table to query.
- Multiple columns in a `SELECT` statement are separated by commas.
- SQL keywords are not case-sensitive, but uppercase keywords can improve readability.
- SQL statements commonly end with a semicolon (`;`).
- The asterisk (`*`) selects all columns from a table.
- Security analysts can use basic SQL queries to retrieve information such as employee IDs, device IDs, usernames, departments, and office locations.