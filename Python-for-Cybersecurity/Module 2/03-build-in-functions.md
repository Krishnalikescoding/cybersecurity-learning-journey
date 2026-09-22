# Python Built-in Functions 

## `print()`
- Outputs specified object(s) to the screen.
- Accepts **any number of arguments**, separated by commas — prints all of them together.

```python
month = "September"
print("Investigate failed login attempts during", month, "if more than", 100)
```

## `type()`
- Returns the **data type** of its argument.
- Helps track variable data types to avoid errors.
- Accepts **only one argument**.

```python
print(type("security"))   # <class 'str'>
print(type(7))             # <class 'int'>
```

### Passing One Function Into Another
- A function can be passed directly as an argument to another function.
- The inner function is processed **first**, and its output becomes the argument for the outer function.

```python
print(type("This is a string"))
# Output: <class 'str'>
```

## `max()` and `min()`
- **`max()`**: returns the largest numeric input.
- **`min()`**: returns the smallest numeric input.
- Both accept multiple numeric values or an iterable (like a list).

**Cybersecurity use case**: finding the longest/shortest login session.

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(min(time_list))   # 2
print(max(time_list))   # 57
```

## `sorted()`
- Sorts elements of a list (or any iterable, like a string).
- Default order: **ascending**.
  - Numeric data → smallest to largest.
  - String data → alphabetical order.

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(sorted(time_list))   # [2, 12, 14, 19, 22, 32, 57]
```

- **Does NOT modify the original list** — returns a new sorted list.

```python
time_list = [12, 2, 32, 19, 57, 22, 14]
print(sorted(time_list))   # sorted output
print(time_list)           # original, unsorted list unchanged
```

- **Limitation**: cannot sort a list/iterable with **mixed data types** (e.g., `[1, 2, "hello"]` will error).

## Key Takeaways
- **`print()`** – outputs data to the screen.
- **`type()`** – returns the data type of a value.
- **`min()` / `max()`** – return smallest/largest values in an iterable.
- **`sorted()`** – returns a sorted version of an iterable (original stays unchanged).

## Further Resources
- [Python Standard Library documentation](https://docs.python.org/3/library/functions.html) — full list of built-in functions.