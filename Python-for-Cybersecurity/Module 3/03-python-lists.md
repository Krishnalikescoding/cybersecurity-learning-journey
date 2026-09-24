# Python Lists: Indices, Slicing & Methods 

## List Data in a Security Setting
- **List data**: a data structure holding a collection of data in sequential form.
- Can store multiple elements (and multiple data types) in a single variable.
- Common security uses: usernames, IP addresses, URLs, device IDs.
- Often paired with `for` loops and conditionals to process list items (e.g., iterating through device IDs, checking conditions).

## Indices in Lists
- Indices start at **0**, just like strings.

**Example**: `["elarson", "fgarcia", "tshah", "sgilmore"]`

| element | index |
|---------|-------|
| "elarson" | 0 |
| "fgarcia" | 1 |
| "tshah" | 2 |
| "sgilmore" | 3 |

## Bracket Notation

### Extracting an Element
```python
username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
print(username_list[2])   # tshah
```

### Extracting a Slice (Sublist)
- Extracts more than one element → returns a new list called a **sublist**.
- Needs two indices: `[start:stop]` — start included, stop excluded.

```python
username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
print(username_list[0:2])   # ['elarson', 'fgarcia']
```

### Changing an Element
- Unlike strings (immutable), **lists are mutable** — elements can be reassigned directly.

```python
username_list = ["elarson", "fgarcia", "tshah", "sgilmore"]
print("Before changing an element:", username_list)
username_list[1] = "bmoreno"
print("After changing an element:", username_list)
```

## List Methods

### `.insert()`
- Adds an element at a specific position.
- Two parameters: **index** to insert at, and the **element** to insert.
- Existing elements shift right by one position.

```python
username_list = ["elarson", "bmoreno", "tshah", "sgilmore"]
username_list.insert(2, "wjaffrey")
print(username_list)   # ['elarson', 'bmoreno', 'wjaffrey', 'tshah', 'sgilmore']
```

### `.remove()`
- Removes the **first occurrence** of a specified element.
- One parameter: the element itself.

```python
username_list = ["elarson", "bmoreno", "wjaffrey", "tshah", "sgilmore"]
username_list.remove("elarson")
print(username_list)   # ['bmoreno', 'wjaffrey', 'tshah', 'sgilmore']
```
- Note: only removes the **first** instance if duplicates exist.

### `.append()`
- Adds an element to the **end** of a list.
- One parameter: the element to add.

```python
username_list = ["bmoreno", "wjaffrey", "tshah", "sgilmore"]
username_list.append("btang")
print(username_list)   # [..., 'btang']
```

- Commonly used with `for` loops to build a list from scratch:

```python
numbers_list = []
for i in range(10):
    numbers_list.append(i)
print(numbers_list)   # [0, 1, 2, ..., 9]
```

### `.index()`
- Finds the **first occurrence** of an element and returns its index.
- Similar to the string `.index()` method, but a **separate method** defined for lists.

```python
username_list = ["bmoreno", "wjaffrey", "tshah", "sgilmore", "btang"]
username_index = username_list.index("tshah")
print(username_index)   # 2
```
- Returns only the index of the **first** matching occurrence if duplicates exist.

## Key Takeaways
- **Bracket notation** extracts elements/slices and can also **modify** list elements (lists are mutable).
- **`.insert(index, element)`** — adds without replacing, shifts others right.
- **`.remove(element)`** — deletes first matching element.
- **`.append(element)`** — adds to the end of the list.
- **`.index(element)`** — finds index of first occurrence.