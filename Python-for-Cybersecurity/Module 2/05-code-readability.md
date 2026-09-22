# PEP 8 Style Guide & Python Syntax 

## Comments
- A **comment** is a note explaining the intention behind code.
- Improves readability for you and other programmers.
- Best practice: start code with a comment explaining what the program does, then add comments throughout for specific sections.

### Single-Line Comments
- Begin with **`#`**.
- PEP 8 recommends keeping lines (including comments) under **79 characters**.

```python
# Print elements of 'computer_assets' list
computer_assets = ["laptop1", "desktop20", "smartphone03"]
for asset in computer_assets:
    print(asset)
```
- Especially useful for complex code (functions, loops, conditionals); optional for simple code (e.g., variable reassignment).

### Multi-Line Comments
- Needed when a comment exceeds 79 characters.
- **Method 1**: multiple `#` lines.

```python
# remaining_login_attempts() function takes two integer parameters,
# the maximum login attempts allowed and the total attempts made,
# and it returns an integer representing remaining login attempts
def remaining_login_attempts(maximum_attempts, total_attempts):
    return maximum_attempts - total_attempts
```

- **Method 2**: docstrings using triple quotation marks `""" """` (not assigned to a variable).

```python
"""
remaining_login_attempts() function takes two integer parameters,
the maximum login attempts allowed and the total attempts made,
and it returns an integer representing remaining login attempts
"""
```

## Correct Indentation
- Indentation = space at the start of a line; required for conditionals, loops, and function definitions.
- Needed both for Python to interpret code correctly **and** for readability.
- **PEP 8 recommendation**: indent using **4 spaces**.
- Nested blocks indent further (e.g., a conditional inside a loop = 8 spaces total).

```python
count = 0
login_status = True

while login_status == True:
    print("Try again.")
    count = count + 1
    if count == 4:
        login_status = False
```

## Maintaining Correct Syntax
- **Syntax errors** = invalid use of Python language; very common — important to recognize and fix.
- Often caused by mistakes with **data types** or missing **colons** in headers.

### Data Type Syntax Rules
- **Strings** → quotation marks: `username = "bmoreno"`
- **Integers/Floats/Booleans** → no quotation marks: `login_attempts = 5`, `percentage_successful = .8`, `login_status = True`
- **Lists** → brackets, comma-separated: `username_list = ["bmoreno", "tshah"]`

### Colons in Headers
- Required at the end of conditional statements, loops, and function definitions.

```python
def remaining_login_attempts(maximum_attempts, total_attempts):
    return maximum_attempts - total_attempts
```

## Key Takeaways
- PEP 8 provides standards for writing readable, consistent Python code.
- Use **comments** (single-line or multi-line/docstrings) to clarify intent.
- Use **correct indentation** (4 spaces) for proper execution and readability.
- Watch for common **syntax errors**: data type formatting and missing colons.

## Further Resources
- [PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/) (use the table of contents to navigate unfamiliar sections).