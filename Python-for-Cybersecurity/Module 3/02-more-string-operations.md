# Python Strings: Indices, Slicing & Methods 

## String Data in Security
- **String**: ordered sequence of characters — used for info not meant for math operations.
- Common security examples: IP addresses, usernames, URLs, employee IDs.
- Common tasks: extracting parts of a string, verifying formatting/criteria.

## Indices
- An **index** = the position number assigned to each character in a string.
- Indices start at **0**.

**Example**: `"h32rb17"`

| char | index | neg. index |
|------|-------|------------|
| h | 0 | -7 |
| 3 | 1 | -6 |
| 2 | 2 | -5 |
| r | 3 | -4 |
| b | 4 | -3 |
| 1 | 5 | -2 |
| 7 | 6 | -1 |

- **Negative indices** count backward from the end of the string.

## Bracket Notation
- Used to extract characters from a string via their index.

```python
device_id = "h32rb17"
print("h32rb17"[0])   # h
print(device_id[0])   # h
```

### Slicing
- Extracts **multiple characters** (a substring range) using `[start:stop]`.
- Start index is **included**, stop index is **excluded**.

```python
print("h32rb17"[0:3])   # h32 (indices 0, 1, 2 — index 3 excluded)
```

## String Functions

### `str()`
- Converts an object (e.g., integer) into a string.
- Useful for IDs you want to search/slice but not use mathematically.

```python
string_id = str(19329302)
```

### `len()`
- Returns the number of characters in a string.
- Useful for validating string format (e.g., checking ID length).

```python
device_id_length = len("h32rb17")
if device_id_length == 7:
    print("The device ID has 7 characters.")
```

## String Methods
- A **method** is a function belonging to a specific data type — called with dot notation after the string.

### `.upper()` / `.lower()`
```python
print("Information Technology".upper())   # INFORMATION TECHNOLOGY
print("Information Technology".lower())   # information technology
```

### `.index()`
- Finds the **first occurrence** of a character (or substring) and returns its index.

```python
print("h32rb17".index("r"))   # 3
```

- **Errors if not found**: `"h32rb17".index("a")` → raises an error (no "a" in the string).
- **Only returns the first match** if there are multiple occurrences:

```python
print("r45rt46".index("r"))   # 0 (first "r", not the one at index 3)
```

### Finding Substrings with `.index()`
- Works on substrings too — returns the index of the **first character** of the match.

```python
tshah_index = "tsnow, tshah, bmoreno - updated".index("tshah")
print(tshah_index)   # 7
```

- **Caution**: partial matches can return unexpected results.
```python
"tsnow, tshah, bmoreno - updated".index("ts")   # returns 0 (matches "ts" in "tsnow", not "tshah")
```

## Key Takeaways
- Use **bracket notation** and **slicing** to extract characters/substrings from strings.
- **`str()`** converts to string; **`len()`** returns string length.
- String methods: **`.upper()`**, **`.lower()`**, **`.index()`** — each only work on strings.
- Be careful with `.index()` on substrings — it matches the *first* occurrence, even if part of a longer match.