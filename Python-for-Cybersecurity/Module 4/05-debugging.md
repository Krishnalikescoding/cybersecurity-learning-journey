# Python Debugging 
 
## The three types of errors
 
| Type | What it is | Error message? |
|------|-----------|----------------|
| **Syntax error** | Invalid use of Python itself | Yes, with line number |
| **Logic error** | Code runs, but gives the wrong result | No |
| **Exception** | Valid syntax, but can't be executed | Yes |
 
---
 
## Syntax errors
 
Mistakes in the Python syntax itself, such as a missing quote, bracket, or colon.
 
- Output shows the **line number**, part of the affected code, and a description
- Label starts with `SyntaxError:`
- `IndentationError` is a subclass, caused by incorrect indentation
```python
message = "You are debugging a syntax error
print(message)
```
 
Error: `SyntaxError: EOL while scanning string literal`
Fix: add the missing closing quotation mark.
 
---
 
## Logic errors
 
The code is valid, so Python runs it without complaint, but the result isn't what you intended.
 
Common causes:
- Wrong logical operator (e.g. `>=` instead of `<`)
- Wrong value assigned in a condition
- Indentation that changes how a line executes
```python
login_attempts = 5
if login_attempts >= 5:   # should be: login_attempts < 5
    print("User has not reached maximum number of login attempts.")
else:
    print("User has reached maximum number of login attempts.")
```
 
The output says the user hasn't hit the limit, but they have.
 
---
 
## Exceptions
 
Code is syntactically correct but can't be executed.
 
| Exception | Cause |
|-----------|-------|
| `NameError` | Using a variable that hasn't been assigned, or a function that hasn't been defined |
| `IndexError` | Using an index that doesn't exist in the sequence |
| `TypeError` | Using the wrong data type (e.g. adding a string to an integer) |
| `FileNotFound` | Opening a file that doesn't exist at the given location |
 
Example of an `IndexError`:
 
```python
usernames = ["bmoreno", "tshah", "elarson"]   # indices: 0, 1, 2
print(usernames[3])                           # no index 3
```
 
---
 
## Debugging strategies
 
**Good to know:** if there are multiple errors, Python reports them **one at a time**, starting with the first one it hits. Fix it, re-run, and the next one appears.
 
Syntax error messages are usually enough to fix the problem. Logic errors and exceptions often need extra strategies.
 
### 1. Debuggers
 
- An **IDE** (Integrated Development Environment) is software for writing code with editing and error-correction tools.
- A **debugger** helps locate the source of an error and assess its causes.
- **Breakpoints** mark lines where you want execution to pause, so you can narrow down the problem area.
- Many debuggers let you watch **variable values change** as the code runs, which is especially useful for logic errors.
**AI coding assistants** (e.g. Gemini Code Assist) can analyze code, find errors, and suggest fixes. Always review and validate their output, since it may not be accurate, optimal, or secure. Treat them as a co-pilot, not the final authority.
 
### 2. Print statements
 
Add temporary `print()` statements at key points to see which parts of the code actually run.
 
**Problem:** `"bmoreno"` gets added to the list twice, even though the code says it's already there.
 
```python
new_users = ["sgilmore", "bmoreno"]
approved_users = ["bmoreno", "tshah", "elarson"]
def add_users():
    for user in new_users:
        print("line 5 - inside for loop")
        if user in approved_users:
            print("line 7 - inside if statement")
            print(user, "already in list")
        print("line 9 - before .append method")
        approved_users.append(user)
add_users()
print(approved_users)
```
 
**What the prints reveal:**
- "inside for loop" prints **twice**, as expected (two new users)
- "inside if statement" prints **once**, as expected (only one duplicate)
- "before .append method" prints **twice**, which is the problem: `.append()` runs for every user
**Fix:** put `approved_users.append(user)` inside an `else` block so it only runs when the user is *not* already in the list.
 
```python
for user in new_users:
    if user in approved_users:
        print(user, "already in list")
    else:
        approved_users.append(user)
```
 
---
 
## Key takeaways
 
- **Syntax errors:** invalid Python; the error message points you to the fix
- **Logic errors:** valid code, wrong result; no error message
- **Exceptions:** valid syntax, but can't run; the error message names the type
- Use **debuggers** (breakpoints, variable tracking) and **print statements** to track down logic errors and tricky exceptions
