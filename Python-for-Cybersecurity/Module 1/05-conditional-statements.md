# Python Conditional Statements 

## What is a Conditional Statement?
- Evaluates code to check whether it meets a specific condition.
- Condition met → evaluates to **True** → runs specified action(s).
- Condition not met → evaluates to **False** → skips the action(s).

## Comparison Operators
| Operator | Meaning |
|----------|---------|
| `>`  | greater than |
| `<`  | less than |
| `>=` | greater than or equal to |
| `<=` | less than or equal to |
| `==` | equal to |
| `!=` | not equal to |

- `==` and `!=` also work for comparing strings.

## `if` Statements
- `if` starts a conditional statement — a required component.
- Structure: **header** (condition + colon) + **body** (indented action).

```python
if status == 200:
    print("OK")
```

- Parentheses around the condition are optional (can improve readability):
```python
if (status == 200):
    print("OK")
```
- The header **must** end with a colon `:`.
- The body **must be indented** consistently — otherwise Python throws an error.

## `else` Statements
- Runs only when **all preceding conditions** evaluate to False.
- Requires a colon and indented body, just like `if`.

```python
if status == 200:
    print("OK")
else:
    print("check other status")
```

## `elif` Statements
- Used for **multiple alternative conditions**.
- Only evaluated if the previous condition(s) were False.
- You can chain multiple `elif` statements (unlike `else`, which can only appear once).

```python
if status == 200:
    print("OK")
elif status == 400:
    print("Bad Request")
elif status == 500:
    print("Internal Server Error")
else:
    print("check other status")
```

- **Important behavior difference**: 
  - Once an `elif` evaluates to True, Python **skips the rest** of the `elif` chain.
  - Multiple separate `if` statements are **all checked independently**, regardless of earlier results.

## Logical Operators for Multiple Conditions

### `and`
- **Both** conditions must be True.

```python
if status >= 200 and status <= 226:
    print("successful response")
```

### `or`
- **Only one** condition needs to be True.

```python
if status == 100 or status == 102:
    print("informational response")
```

### `not`
- **Negates** a condition — True becomes False, and False becomes True.

```python
if not(status >= 200 and status <= 226):
    print("check status")
```
- Parentheses matter here — Python evaluates the condition inside parentheses first, then applies `not` to the whole result.

## Key Takeaways
- `if` is required to start any conditional statement.
- `else` and `elif` allow for additional/alternative actions.
- `and`, `or`, and `not` help build more complex conditions.