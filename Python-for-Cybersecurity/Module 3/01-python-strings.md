# Python Operations

## String Recap
- **String**: data consisting of an ordered sequence of characters.
- Written between quotation marks (single or double — this course uses double).

```python
my_string = "security"
```

## Converting to a String: `str()`
- Built-in function that converts an object into a string.
- Useful because some operations (like removing/reordering elements) are only possible on strings, not integers.

```python
new_string = str(123)
print(type(new_string))   # <class 'str'>
```

## Basic String Operations

### `len()` — Length Function
- Returns the number of characters (elements) in a string.
- **Cybersecurity use case**: IPv4 addresses have a max of 15 characters — `len()` can check if an address is valid.

```python
print(len("Hello"))   # 5
```

### String Concatenation
- Joining two strings together using the **`+`** operator.
- No automatic spacing added.

```python
print("Hello" + "world")   # Helloworld
```
- Note: other operators (like `-`) don't work on strings.

## String Methods
- A **method** is a function that belongs to a specific data type — using it on the wrong type causes an error.
- Syntax: `string.method()` — placed **after** the string with a dot.

### `.upper()`
- Returns a copy of the string in all uppercase.

```python
print("Hello".upper())   # HELLO
```

### `.lower()`
- Returns a copy of the string in all lowercase.

```python
print("Hello".lower())   # hello
```

## Key Takeaways
- Strings can be created directly or converted from other data types using `str()`.
- `len()` returns character count — useful for validation tasks (e.g., IP address length).
- `+` concatenates strings; other math operators don't apply.
- String methods (`.upper()`, `.lower()`) are called with dot notation after the string.
- Coming up: indexing and splitting strings.