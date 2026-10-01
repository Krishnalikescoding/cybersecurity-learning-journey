# Parsing File Data in Python: `.split()` and `.join()`

## What is Parsing?
- **Parsing** = converting data into a more readable or usable format.
- Why it helps:
  - Some code needs data in a specific format so Python can process it.
  - Programmers need to read and understand the results.
- Main methods: `.split()` and `.join()`.

## `.split()`: String to List
- Splits a string into a list at a chosen character (the argument).
- **No argument** = splits at every whitespace (spaces, newlines, etc.).

```python
approved_users = "elarson,bmoreno,tshah,sgilmore,eraab"
approved_users = approved_users.split(",")
# ['elarson', 'bmoreno', 'tshah', 'sgilmore', 'eraab']
```

### Using `.split()` on Files
Read the file into a string first, then split it into a list. Useful for looping with a `for` loop.

```python
with open("update_log.txt", "r") as file:
    updates = file.read()
updates = updates.split()
```

- The `.split()` line is **outside** the `with` block, so the file closes as soon as it is no longer needed. This keeps code readable.

## `.join()`: List to String
- Joins the elements of an iterable into one string.
- **Syntax differs**: you append `.join()` to the **separator**, and pass the **list** as the argument.

```python
approved_users = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]
approved_users = ",".join(approved_users)
# 'elarson,bmoreno,tshah,sgilmore,eraab'
```

- Use `"\n"` as the separator to put each element on a new line.

### Using `.join()` on Files
`.write()` only accepts strings, so convert the list back first.

```python
updates = " ".join(updates)
with open("update_log.txt", "w") as file:
    file.write(updates)
```

- `" ".join(updates)` separates the elements with a space.
- `"w"` overwrites the old file contents.

## Full Flow (Read, Modify, Write)
1. `open(..., "r")` and `.read()` to get a **string**
2. `.split()` to get a **list**
3. Work on the list (loops, `.remove()`, `.append()`, etc.)
4. `.join()` to get a **string** again
5. `open(..., "w")` and `.write()` to save

## Key Takeaways
- `.split()`: string to list.
- `.join()`: list to string.
- Both are used to parse file data.

## Quick Memory Hook
**split** = break apart (string to list) | **join** = glue together (list to string)
`separator.join(list)` and `string.split(separator)`