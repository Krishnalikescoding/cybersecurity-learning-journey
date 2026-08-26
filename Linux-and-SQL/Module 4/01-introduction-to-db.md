# Databases and Relational Databases

## Overview

Modern organizations work with large amounts of data that often guides important decisions. Databases provide a way to store this information in an organized structure that allows it to be accessed and processed efficiently.

**Database:** An organized collection of information or data.

Security analysts may need to access databases containing information such as:

- Login attempts
- Software and software updates
- Machines and their owners
- Employee information

## Databases vs. Spreadsheets

Databases are often compared to spreadsheets because both can be used to store and organize data.

| Feature | Spreadsheets | Databases |
|---|---|---|
| Typical use | Individual users or small teams | Organizations and multiple users |
| Amount of data | Generally smaller amounts | Can store massive amounts of data |
| Simultaneous access | More limited | Multiple people can access data simultaneously |
| Data operations | Basic to moderately complex | Can perform complex operations while accessing data |

Databases allow large amounts of data to remain organized while making it relatively quick and efficient to access and process.

## Relational Databases

There are many ways to structure a database. This course focuses on **relational databases**.

**Relational Database:** A structured database containing tables that are related to each other.

Relational databases organize information into tables consisting of:

- **Columns**, which represent fields
- **Rows**, which represent records

## Tables, Fields, and Records

### Tables

A **table** stores related information within a relational database.

For example, an organizational database might contain an `employees` table and a `machines` table.

### Fields

**Fields** are individual categories of information stored in a table. Fields are represented as **columns**.

An `employees` table might contain fields such as:

- `employee_id`
- `device_id`
- `username`

### Records

**Records** are individual rows in a table.

Each record contains specific data corresponding to the fields defined by the table.

For example:

| employee_id | department | username |
|---:|---|---|
| 1000 | Marketing | ... |

The row represents one employee record.

## Relationships Between Tables

Relational databases often contain multiple tables.

For example:

- An `employees` table can contain information about employees.
- A `machines` table can contain information about machines assigned to employees.

Two tables can be related when they share a common column.

In this example, the `employee_id` column can be used to establish a relationship between the two tables.

The columns used to establish relationships between tables are called **keys**.

## Types of Keys

There are two important types of keys:

1. **Primary key**
2. **Foreign key**

### Primary Key

**Primary Key:** A column in which every row has a unique value and that is used to uniquely identify each row in a table.

A primary key:

- Must contain unique values
- Cannot contain duplicate values
- Cannot contain null or empty values
- Uniquely identifies each record in a table

For example, `employee_id` can be the primary key of an `employees` table because every employee has a unique ID.

```text
employees

employee_id
-----------
1000
1001
1002
```

Each `employee_id` uniquely identifies an employee.

A table can have only **one primary key**.

### Foreign Key

**Foreign Key:** A column in one table that is a primary key in another table.

Foreign keys are used to establish relationships between tables.

Unlike primary keys, foreign keys:

- Can contain duplicate values
- Can contain empty or null values

For example, if `employee_id` is the primary key in the `employees` table, it can be used as a foreign key in the `machines` table.

```text
employees
-----------
employee_id
1000
1001
1002

        ↓ relationship

machines
-----------
employee_id
1000
1000
1001
```

This allows machines to be associated with their corresponding employees.

A table can have:

- One primary key
- Multiple foreign keys

## Primary Key vs. Foreign Key

| Feature | Primary Key | Foreign Key |
|---|---|---|
| Purpose | Uniquely identifies records | Connects tables |
| Must be unique? | Yes | No |
| Can contain duplicates? | No | Yes |
| Can contain null/empty values? | No | Yes |
| Relationship | Identifies records in its own table | References a primary key in another table |

## Example: Organizational Database

Consider an organization that maintains information about employees and the machines assigned to them.

### Employees Table

| employee_id | username | department |
|---:|---|---|
| 1000 | user1 | Marketing |
| 1001 | user2 | Security |
| 1002 | user3 | Finance |

Here, `employee_id` can serve as the **primary key**.

### Machines Table

| machine_id | employee_id | device_name |
|---:|---:|---|
| 2001 | 1000 | PC-01 |
| 2002 | 1000 | PC-02 |
| 2003 | 1001 | PC-03 |

Here, `employee_id` can serve as a **foreign key** that connects each machine to its corresponding employee.

The same employee can have multiple machines, which is why the foreign key can contain duplicate values.

## SQL

**Structured Query Language (SQL)** is the language used to work with relational databases.

SQL can be used to interact with and retrieve information from relational databases.

Understanding tables, records, fields, primary keys, and foreign keys provides the foundation for learning SQL.

## Key Takeaways

- A **database** is an organized collection of information or data.
- Databases can store large amounts of data and support simultaneous access by multiple users.
- A **relational database** organizes data into related tables.
- **Fields** are represented by columns, while **records** are represented by rows.
- A **primary key** uniquely identifies each record and cannot contain duplicates or null values.
- A **foreign key** references a primary key in another table and establishes relationships between tables.
- Foreign keys can contain duplicate and null values.
- A table can have one primary key and multiple foreign keys.
- **SQL** is the language used to work with relational databases.