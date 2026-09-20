# Python Functions: Parameters, Arguments, Return & Scope 

## Parameters vs. Arguments

### Parameters
- Variables included in a **function definition**, used within the function.
- Defined in the function header.

```python
def remaining_login_attempts(maximum_attempts, total_attempts):
    print(maximum_attempts - total_attempts)
```
- `maximum_attempts` and `total_attempts` are **parameters**.

### Arguments
- The actual **data passed into a function** when it's called.

```python
remaining_login_attempts(3, 2)
```
- `3` and `2` are **arguments** — passed by position (`3` → `maximum_attempts`, `2` → `total_attempts`).

## Return Statements
- `return` sends information back out of a function.
- No parentheses after `return` (it's a keyword, not a function).

```python
def remaining_login_attempts(maximum_attempts, total_attempts):
    return maximum_attempts - total_attempts
```

- Useful for storing a function's output in a variable for later use:

```python
def remaining_login_attempts(maximum_attempts, total_attempts):
    return maximum_attempts - total_attempts

remaining_attempts = remaining_login_attempts(3, 3)
if remaining_attempts <= 0:
    print("Your account is locked")
```
- Prints the lockout message since `3 - 3 = 0`.

- **Note**: Once Python hits a `return` statement, it exits the function immediately — any code after `return` inside that function won't run.

## Global vs. Local Variables

### Global Variables
- Assigned **outside** any function.
- Accessible **anywhere** in the program (inside or outside functions).

```python
device_id = "7ad2130bd"
```

### Local Variables
- Assigned **inside** a function (including parameters).
- Only exist **while the function is running** — deleted from memory afterward.
- Cannot be accessed outside the function.

```python
def greet_employee(name):
    total_string = "Welcome" + name
    return total_string
```
- `name` and `total_string` are both **local variables**.
- Trying to use `total_string` outside this function → error.

## Best Practices for Global & Local Variables

### Functions can read global variables:
```python
username = "elarson"
def identify_user():
    print(username)
identify_user()
# prints: elarson
```
- Works, but not ideal — to handle different usernames, it's better to use a **parameter** instead of relying on a global variable.

### Reusing a global variable's name inside a function creates a separate local variable:
```python
username = "elarson"
print("1:" + username)   # prints: 1:elarson

def greet():
    username = "bmoreno"  # this is a NEW local variable
    print("2:" + username)  # prints: 2:bmoreno

greet()
print("3:" + username)   # prints: 3:elarson (global unchanged)
```
- The local `username` inside `greet()` does **not** affect the global `username`.
- Best practice: **avoid mixing global and local variables with the same name** — it creates confusing, hard-to-track behavior.

## Key Takeaways
- **Parameter** = variable defined in a function's header.
- **Argument** = actual value passed in when calling the function.
- **`return`** sends a value back and immediately exits the function.
- **Global variables** are accessible everywhere; **local variables** exist only within their function.
- Keep global and local variable names distinct to avoid confusion and bugs.