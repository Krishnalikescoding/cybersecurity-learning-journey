# Python Loops 

## What is an Iterative Statement?
- Code that repeatedly executes a set of instructions.
- Executes **zero or more times**, depending on the criteria.
- Two main types: **for loops** and **while loops**.

## `for` Loops
- Used to iterate through a **specified sequence** (list, string, range, etc.).

```python
usernames = ["nzhao", "jdoe", "krishna"]
for i in usernames:
    print(i)
```

- **Loop header**: `for i in usernames:`
  - `for` starts the loop.
  - `i` is the **loop variable** (controls each iteration).
  - `in` tells Python to iterate over every item in the sequence.
  - Header must end with a colon `:`.
- **Loop body**: indented code — what to do each iteration (e.g., `print(i)`).
- Note: `in` is also used in conditional statements to check membership:
```python
if "elarson" in ["tshah", "bmoreno", "elarson"]:
    print("found")  # True, since "elarson" is in the list
```

### Looping Through a List
```python
computer_assets = ["laptop01", "desktop20", "smartphone03"]
for asset in computer_assets:
    print(asset)
```
- On each iteration, `asset` takes the value of the next list item.

### Looping Through a String
```python
for letter in "security":
    print(letter)
```
- Iterates through each character one by one.

### Using `range()`
- Generates a sequence of numbers: `range(start, stop, step)`.
- **Start is inclusive**, **stop is exclusive**.

```python
for i in range(0, 5, 1):
    print(i)   # prints 0, 1, 2, 3, 4 (5 excluded)
```

- If start = 0 and step = 1 (defaults), they can be omitted:
```python
for i in range(5):
    print(i)   # same result: 0, 1, 2, 3, 4
```
- If start ≠ 0 or step ≠ 1, both must be specified explicitly.

## `while` Loops
- Iterates based on a **condition**, not a fixed sequence.
- Continues while condition is **True**; exits when **False**.
- Loop variable is assigned **outside** the loop (unlike `for` loops).

```python
i = 1
while i < 5:
    print(i)
    i += 1
```

- Header: `while i < 5:` — uses same comparison operators as conditionals.
- Body must update the loop variable, or the loop never ends.

### Integer-Based Condition Example
```python
login_attempts = 0
while login_attempts < 5:
    print(login_attempts)
    login_attempts += 1
# Prints 0 through 4; stops before printing 5
```

### Boolean-Based Condition Example
```python
count = 0
login_status = True
while login_status:
    print("try again")
    count += 1
    if count == 4:
        login_status = False
```
- Loop exits once `login_status` becomes `False` (prints "try again" 4 times).

## Managing Loops: `break` and `continue`
- Both are used inside an `if` statement within the loop body.

### `break`
- **Exits the loop entirely** when a condition is True.

```python
computer_assets = ["laptop01", "desktop20", "smartphone03"]
for asset in computer_assets:
    if asset == "desktop20":
        break
    print(asset)
# Only prints "laptop01" — loop exits before printing the rest
```

### `continue`
- **Skips the current iteration** and moves to the next one.

```python
computer_assets = ["laptop01", "desktop20", "smartphone03"]
for asset in computer_assets:
    if asset == "desktop20":
        continue
    print(asset)
# Prints "laptop01" and "smartphone03" — skips "desktop20" only
```

## Infinite Loops
- A loop that never exits = **infinite loop**.
- Stop manually with `CTRL-C` or `CTRL-Z`.
- Can happen intentionally in services that run continuously (e.g., web servers).

## Key Takeaways
- **`for` loops**: iterate a predetermined number of times (through lists, strings, or ranges).
- **`while` loops**: iterate based on a condition evaluating to True.
- **`break`** and **`continue`** give finer control over loop execution.