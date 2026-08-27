# SQL Filtering: Numeric and Date/Time Operators

## Overview

Security analysts work with more than just string data (ordered sequences of characters). This topic covers how to filter **numeric data** and **date and time data** in SQL using comparison operators and the `BETWEEN` operator.

## Key Concepts

### Numeric Data

Numeric data consists of numbers. Examples relevant to security analysis include:

- Number of login attempts
- Count of a specific type of log entry
- Volume of data sent from a source
- Volume of data sent to a destination

### Date and Time Data

Date and time data represents a date and/or time. Logs generally timestamp every record. Other examples include:

- Login dates
- Login times
- Dates for patches
- Duration of a connection

### Comparison Operators

Comparison operators are used in filters (typically within a `WHERE` clause) to return only the rows needed.

| Operator | Use                       |
|----------|----------------------------|
| `<`      | Less than                  |
| `>`      | Greater than                |
| `=`      | Equal to                    |
| `<=`     | Less than or equal to       |
| `>=`     | Greater than or equal to    |
| `<>`     | Not equal to                |

> **Note:** `!=` can also be used as an alternative operator for "not equal to."

### Exclusive vs. Inclusive Operators

- **Exclusive operator**: An operator that does not include the value being compared against (e.g., `>`).
- **Inclusive operator**: An operator that includes the value being compared against (e.g., `>=`).

**Example:** A query filtering the `birthdate` column with `>` and `'1970-01-01'` returns employees born *after*, but not on, January 1, 1970. Using `>=` instead would also include employees born exactly on that date.

```sql
SELECT firstname, lastname, birthdate
FROM employees
WHERE birthdate > '1970-01-01';
```

### BETWEEN Operator

`BETWEEN` filters for numbers or dates within a range. It works for both numeric data and date/time data.

**Example:** Finding employees hired between January 1, 2002 and January 1, 2003 uses `BETWEEN` on the `hiredate` column.

```sql
SELECT firstname, lastname, hiredate
FROM employees
WHERE hiredate BETWEEN '2002-01-01' AND '2003-01-01';
```

> **Note:** `BETWEEN` is inclusive — records with a `hiredate` of exactly January 1, 2002 or January 1, 2003 are included in the results.

## Key Takeaways

- Security analysts frequently filter both numeric data and date/time data.
- Comparison operators (`<`, `>`, `=`, `<=`, `>=`, `<>`/`!=`) are used in the `WHERE` clause to filter results.
- `<` and `>` are **exclusive**; `<=` and `>=` are **inclusive**.
- `BETWEEN` is an **inclusive** operator used to filter numeric or date/time data within a range.