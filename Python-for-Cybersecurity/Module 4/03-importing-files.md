# Working with Files in Python 

## Why Files Matter
- Analysts often work with **logs** (records of events in a system).
- Examples:
  - Login attempt log: spot unusual activity from a malicious actor.
  - Software issue log: find applications being attacked or having problems.
- Analysts also **write** files, e.g. a new allow list of approved usernames, or edits to meet standardization policies.

## Opening a File

```python
with open("update_log.txt", "r") as file:
```

| Part | Role |
|---|---|
| `with` | Handles errors and manages resources. Closes the file automatically after the block. |
| `open()` | Opens the file. Takes 2 parameters: file name/path and mode. |
| `as file` | Assigns a variable to reference the opened file inside the block. |
| `:` | Required at the end of the line. |

- Without `with`, you must close the file yourself.

### File Paths
- Same directory as the Python file: file name is enough.
  - `open("update_log.txt", "r")`
- Different directory: use the **absolute file path** (starts from the root).
  - `open("/home/analyst/logs/access_log.txt", "r")`
- Paths are strings, so keep them in quotation marks.

### Modes (second parameter)

| Mode | Meaning |
|---|---|
| `"r"` | Read |
| `"w"` | Write (replaces existing contents, or creates a new file) |
| `"a"` | Append (adds to the end, keeps existing contents) |

## Reading a File

```python
with open("update_log.txt", "r") as file:
    updates = file.read()

print(updates)
```

- `.read()` converts the file into a **string**.
- Then you can use normal string operations: `.index()`, `len()`, etc.

## Writing to a File
Use `"w"` or `"a"` with the `.write()` method.

- `"w"` on an existing file: contents are **replaced**.
- `"w"` on a new name: **creates** the file.
  - `with open("update_log2.txt", "w") as file:`
- `"a"`: new data is added to the **end**, nothing deleted.

```python
line = "jrafael,192.168.243.140,4:56:27,True"

with open("access_log.txt", "a") as file:
    file.write(line)
```

- `.write()` writes **string** data to the file.
- Always use `with`, otherwise the data may not be fully written if the file isn't closed properly.

## Key Takeaways
- Import files with `with` + `open()` + `as`.
- Read with `.read()`, write with `.write()`.
- Modes: `"r"` read, `"w"` write/replace, `"a"` append.

## Quick Memory Hook
**r** = read | **w** = wipe and write | **a** = add to the end