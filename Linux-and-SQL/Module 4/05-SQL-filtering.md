# SQL Filtering with `WHERE`, `LIKE`, and Wildcards

## Overview

Security analysts often work with large and complex security logs. SQL filtering helps analysts narrow down large datasets and retrieve only the information relevant to an investigation.

For example, SQL filters can be used to:

- Find login attempts from a specific user
- Identify login attempts made during a security incident
- Find devices running a specific version of an application
- Search for records that match a particular pattern

## `WHERE`

The **`WHERE`** keyword is used to create a filter in SQL.

It specifies the condition that records must meet to be included in the query results.

### Example

Suppose an organization needs to identify employees whose job title is `IT Staff`.

A query can use:

```sql
SELECT *
FROM employees
WHERE title = 'IT Staff';
```

The `WHERE` clause tells SQL to return only records where the `title` column contains exactly `IT Staff`.

The **equals sign (`=`)** is used to specify an exact match.

> **Note:** The semicolon (`;`) should be placed at the end of the complete query, after the `WHERE` condition.

## Filtering for Patterns

SQL can also filter data based on patterns rather than exact values.

Pattern matching requires:

- The **`LIKE`** operator
- A **wildcard**

Two commonly used SQL wildcards are:

- Percentage sign (`%`)
- Underscore (`_`)

## Wildcards

A **wildcard** is a special character that can represent one or more unknown characters when searching for patterns.

### Percentage Sign (`%`)

The **`%`** wildcard represents **any number of characters**, including zero characters.

For example:

```text
a%
```

can match:

- `apple123`
- `art`
- `a`

The `%` wildcard can be placed before, after, or on both sides of a string.

### Underscore (`_`)

The **`_`** wildcard represents **exactly one character**.

For example:

```text
a_
```

can match:

- `as`
- `an`
- `a7`

It cannot match `apple` because the pattern only allows one character after `a`.

## Wildcard Examples

| Pattern | Example Results |
|---|---|
| `'a%'` | `apple123`, `art`, `a` |
| `'a_'` | `as`, `an`, `a7` |
| `'a__'` | `ant`, `add`, `a1c` |
| `'%a'` | `pizza`, `Z6ra`, `a` |
| `'_a'` | `ma`, `1a`, `Ha` |
| `'%a%'` | `Again`, `back`, `a` |
| `'_a_'` | `Car`, `ban`, `ea7` |

## `LIKE`

The **`LIKE`** operator is used with `WHERE` to search for patterns in a column.

When using wildcards, use `LIKE` instead of the equals sign (`=`).

### Example: Finding IT Employees

Suppose you want to find employees whose titles begin with `IT`.

You can use:

```sql
SELECT *
FROM employees
WHERE title LIKE 'IT%';
```

The pattern:

```text
'IT%'
```

means that the value must begin with `IT`, followed by zero or more characters.

This can return titles such as:

- `IT Staff`
- `IT Manager`

## Using the Underscore Wildcard

Suppose the `invoices` table contains a `state` column and you want to find states with abbreviations that begin with `N` and contain exactly one additional character.

You can use:

```sql
SELECT *
FROM invoices
WHERE state LIKE 'N_';
```

The pattern:

```text
'N_'
```

means:

- The first character must be `N`.
- The second character can be any single character.

This can match state abbreviations such as:

- `NY`
- `NV`
- `NS`
- `NT`

## `%` vs. `_`

| Wildcard | Meaning | Example |
|---|---|---|
| `%` | Any number of characters, including zero | `'IT%'` matches `IT Staff` and `IT Manager` |
| `_` | Exactly one character | `'N_'` matches two-character values beginning with `N` |

## `=` vs. `LIKE`

| Operator | Purpose | Example |
|---|---|---|
| `=` | Matches an exact value | `WHERE title = 'IT Staff'` |
| `LIKE` | Matches a pattern | `WHERE title LIKE 'IT%'` |

Use `=` when you know the exact value you want to match.

Use `LIKE` when you need to search for a pattern.

## Key Takeaways

- **`WHERE`** is used to filter SQL query results based on a condition.
- The **`=`** operator can be used to search for an exact value.
- **`LIKE`** is used with `WHERE` to search for patterns.
- The **`%`** wildcard represents any number of characters, including zero.
- The **`_`** wildcard represents exactly one character.
- Wildcards can appear before, after, or around a search pattern.
- SQL filtering is an important skill for security analysts because it helps narrow large datasets and security logs to relevant information.