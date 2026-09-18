# Python Data Types – Notes

## Core Data Types

### String
- Ordered sequence of characters (letters, numbers, symbols, spaces).
- Placed within quotation marks (single `''` or double `""`).
- Examples: `"updates needed"`, `"20%"`, `""` (empty string).
- Displayed using `print()`.
- Consistency in quote style improves readability.

```python
username = "krishna"
print(username)
print("Alert: " + username + " logged in")
```

### List
- Data structure holding a collection of items in sequential order.
- Can contain any data type (strings, integers, Booleans, even other lists).
- Elements placed in **square brackets `[]`**, separated by commas.
- Examples: `[12, 36, 54, 1, 7]`, `[15, "approved", True, 45.5, False]`, `[]` (empty list).

```python
blocked_ips = ["192.168.1.5", "10.0.0.3", "172.16.0.9"]
print(blocked_ips)
print(blocked_ips[0])  # first item
```

### Integer
- Whole number, no decimal point.
- Not placed in quotation marks.
- Examples: `-100`, `0`, `500`.
- Can be used in math operations via `print()`.

```python
failed_attempts = 3
max_attempts = 5
print(max_attempts - failed_attempts)  # remaining attempts
```

### Float
- Number with a decimal point.
- Not placed in quotation marks.
- Examples: `-2.2`, `0.0`, `0.34`.
- Dividing with `/` always returns a float (e.g., `1/4` → `0.25`).
- Dividing with `//` rounds down:
  - `1//4` → `0` (integer)
  - `1.0//4.0` → `0.0` (float)

```python
cpu_usage = 78.5
print(cpu_usage / 100)   # true division -> float
print(cpu_usage // 10)   # floor division -> 7.0
```

### Boolean
- Only two possible values: `True` or `False`.
- Not placed in quotation marks.
- Can result from comparisons (e.g., `9 > 10` → `False`).

```python
is_authenticated = True
print(is_authenticated)
print(10 > 15)  # False
```

## Additional Data Types

### Tuple
- Collection of data that **cannot be changed** (immutable).
- Can hold mixed data types, like a list.
- Placed in **parentheses `()`** instead of brackets.
- Examples: `("wjaffrey", "arutley", "dkot")`, `("wjaffrey", 13, True)`.
- **Cybersecurity use case**: storing software identifiers in a tuple ensures they can't be altered — useful for reliable access control lists.
- **Pro tip**: more memory-efficient than lists — good for large datasets.

```python
approved_software = ("firewall_v2", "antivirus_v5", "vpn_client")
print(approved_software)
print(approved_software[1])
```

### Dictionary
- Data consisting of **key-value pairs**.
- Syntax: `{key: value, key: value}` — colon between key/value, commas between pairs, curly brackets `{}`.
- Useful for predictable storage/retrieval.
- Example: `{1: "East", 2: "West", 3: "North", 4: "South"}`.

```python
user_roles = {"krishna": "admin", "mayuri": "editor", "guest01": "viewer"}
print(user_roles["krishna"])
```

### Set
- **Unordered** collection of **unique values** (no duplicates allowed).
- Placed in curly brackets `{}`, separated by commas.
- Can contain any data type.
- Example: `{"jlanksy", "drosas", "nmason"}`.

```python
logged_in_users = {"krishna", "mayuri", "krishna"}  # duplicate ignored
print(logged_in_users)
```

## Key Takeaways
- Core types used in this course: **string, list, integer, float, Boolean**.
- Additional types: **tuple, dictionary, set** — each with its own syntax and use case.
- Understanding these is essential for security analysts who program in Python.