# Python Variables 

## What is a Variable?
- A **variable** is a container that stores data (like a kitchen storage container/labeled box — the label/name stays the same even when the contents change).
- Named storage location in memory that holds a value of a particular data type (integer, string, Boolean, etc.).
- The value stored can change, but the variable name stays the same.
- Security analysts commonly use variables for things like login attempts, allow lists, and addresses.

## Assigning a Variable
- Creating a variable = **assignment**: `name = value`.
- Best practice: give variables names relevant to what they store.
- Python automatically assigns the data type based on the value.

```python
device_ID = "h32rb17"
```

## Calling (Using) a Variable
- To use a variable, type its name — this is called **calling** it.
- No quotation marks needed when printing a variable (unlike printing a plain string).

```python
device_ID = "h32rb17"
print(device_ID)          # prints: h32rb17
print("m50pi31")           # prints a string directly: m50pi31
```

## Why Use Variables?
- Makes code cleaner and easier to read.
- Useful for long strings/numbers used repeatedly — avoids retyping them.
- Variables can store **any data type**, and their type matches whatever value they currently hold.

## The `type()` Function
- Returns the data type of its input.
- Useful when you're unsure what type a variable is storing.

```python
device_ID = "h32rb17"
data_type = type(device_ID)
print(data_type)          # prints: <class 'str'>
```

## Type Errors
- A **type error** occurs when incompatible data types are combined (e.g., adding a string + integer).
- Python can only add two strings together, or two numbers together — not a mix.

```python
device_ID = "h32rb17"
number = 5
print(device_ID + number)  # TypeError: can only concatenate str (not "int") to str
```

## Reassignment
- Variables can be **reassigned** — the object stored inside can change after creation.
- Reassignment works just like the original assignment: `name = new_value`.

```python
username = "nzhao"
print(username)           # prints: nzhao

username = "zhao2"        # reassigned
print(username)           # prints: zhao2
```
- A variable can even be reassigned to a **different data type** (e.g., string → integer).

```python
device_ID = "h32rb17"     # string
device_ID = 132            # reassigned to integer
print(device_ID)           # prints: 132
```

## Assigning a Variable to Another Variable
- One variable's value can be copied into a new variable.

```python
username = "nzhao"
old_username = username    # old_username now also holds "nzhao"

username = "zhao2"         # reassign username
print(old_username)        # still prints: nzhao
print(username)            # prints: zhao2
```

## Best Practices for Naming Variables

### Syntax rules (must follow)
- Use only **letters, numbers, and underscores** — e.g., `date_3`, `username`, `interval2`.
- Names are **case-sensitive** — `time`, `Time`, `TIME`, `timE` are all different variables.
- Don't use Python's built-in keywords/functions as names — e.g., avoid `True`, `False`, `if`.

### Style guidelines (recommended)
- Separate multiple words with underscores — e.g., `login_attempts`, `invalid_user`.
  - Alternative convention: camelCase — e.g., `loginAttempt`.
- Avoid similar-looking names that could be confused — e.g., `start_time` vs. `starting_time` vs. `time_starting`.
- Avoid unnecessarily long names — e.g., don't use `variable_that_equals_3`.
- Names should **describe the data**, not be random words — e.g., `num_login_attempts`, `device_id`, `invalid_usernames`.

## Key Takeaways
- Variables store data and can be **created**, **called**, and **reassigned**.
- Use `type()` to check a variable's current data type.
- Mixing incompatible data types in operations causes a **type error**.
- Clear, consistent naming makes code more readable for you and other analysts.