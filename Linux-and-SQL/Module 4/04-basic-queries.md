# Basic SQL Queries and Sorting

## Why We Use a Ready-Made Database

Creating a database from scratch requires setting up rules for:

- How information is stored
- How data is protected from being lost
- How data can be located efficiently
- How tables and relationships are structured

Instead of building a database from scratch, this course uses the **Chinook database** so learners can focus on querying and analyzing data.

## Chinook Database

The **Chinook database** is a sample database used throughout the course for practicing SQL queries.

It contains data that might be created by a digital media company.

The database contains **11 tables**, including:

- `employees`
- `customers`
- `invoices`

These tables contain information such as names and addresses.

## Basic SQL Query

Two essential SQL keywords used to query a database are:

- **`SELECT`**: Specifies which columns to return.
- **`FROM`**: Specifies which table to query.

### Example

```sql
SELECT employee_id, device_id
FROM employees;
```

This query returns the `employee_id` and `device_id` columns from the `employees` table.

## `SELECT`

The **`SELECT`** keyword specifies the columns to return.

### Selecting One Column

```sql
SELECT customerid
```

This selects the `customerid` column.

### Selecting Multiple Columns

Multiple columns are separated by commas.

```sql
SELECT customerid, city
```

This selects both the `customerid` and `city` columns.

### Selecting All Columns

The asterisk (`*`) can be used to return all columns.

```sql
SELECT *
```

For example:

```sql
SELECT *
FROM customers;
```

This returns all columns from the `customers` table.

> **Note:** Although `SELECT *` is convenient for small tables, it may not be advisable for large databases. Returning every column can make the output difficult to understand and may cause queries to run more slowly.

## `FROM`

The **`FROM`** keyword specifies which table the query should retrieve data from.

Example:

```sql
SELECT *
FROM customers;
```

Here:

- `SELECT *` specifies that all columns should be returned.
- `FROM customers` specifies that the data should come from the `customers` table.

### Semicolons

A semicolon (`;`) marks the end of an SQL query.

```sql
SELECT *
FROM customers;
```

The semicolon tells SQL that the statement is complete.

### SQL Line Breaks

Line breaks are not required in SQL queries.

The following queries are equivalent:

```sql
SELECT *
FROM customers;
```

```sql
SELECT * FROM customers;
```

Line breaks are commonly used because they make longer queries easier to read.

## `ORDER BY`

The **`ORDER BY`** keyword organizes the records returned by a query based on one or more specified columns.

It can sort data in:

- Ascending order
- Descending order

### Sorting in Ascending Order

By default, `ORDER BY` sorts results in **ascending order**.

Example:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY city;
```

This returns the selected columns from `customers` and sorts the records alphabetically by `city`.

For numeric data, ascending order means:

```text
Smallest → Largest
```

For alphabetic data, ascending order means:

```text
A → Z
```

### Sorting in Descending Order

The **`DESC`** keyword specifies descending order.

Example:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY city DESC;
```

For numeric data, descending order means:

```text
Largest → Smallest
```

For alphabetic data, descending order means:

```text
Z → A
```

### Sorting by Multiple Columns

SQL can sort records using multiple columns.

For example:

```sql
SELECT customerid, city, country
FROM customers
ORDER BY country, city;
```

SQL first sorts the records by `country`.

If multiple records have the same country, SQL then sorts those records by `city`.

This allows data to be organized using multiple levels of sorting.

## SQL Query Structure

A basic query using `SELECT`, `FROM`, and `ORDER BY` follows this structure:

```sql
SELECT column1, column2
FROM table_name
ORDER BY column1;
```

For descending order:

```sql
SELECT column1, column2
FROM table_name
ORDER BY column1 DESC;
```

For multiple sorting columns:

```sql
SELECT column1, column2
FROM table_name
ORDER BY column1, column2;
```

## Command Summary

| SQL Keyword | Purpose |
|---|---|
| `SELECT` | Specifies the columns to return |
| `FROM` | Specifies the table to query |
| `ORDER BY` | Sorts the returned records |
| `DESC` | Sorts records in descending order |
| `*` | Selects all columns |
| `;` | Marks the end of an SQL statement |

## Key Takeaways

- The **Chinook database** is a sample database used to practice SQL queries.
- **`SELECT`** specifies which columns to return.
- **`FROM`** specifies which table to query.
- The asterisk (`*`) selects all columns.
- SQL queries commonly end with a semicolon (`;`).
- Line breaks are optional but can improve query readability.
- **`ORDER BY`** organizes query results based on one or more columns.
- By default, `ORDER BY` sorts results in **ascending order**.
- **`DESC`** sorts results in descending order.
- Multiple columns can be specified with `ORDER BY` to create multi-level sorting.