# Automating Security Tasks in Python: Core Components

## Core Idea
- **Automation** = using technology to reduce manual effort on common, repetitive tasks.
- Security analysts mainly use Python to automate tasks (investigating logins, managing access, updating devices).

## Components You Need

| Component | What it is | Why it helps automation |
|---|---|---|
| **Variables** | Containers that store data | No need to rewrite values for every action |
| **Conditional statements** | Code that checks if conditions are met | Check first, then act, instead of judging each item by hand |
| **Iterative statements** | Code that repeats instructions | Same action many times without retyping |
| **Functions** | Reusable blocks of code | Define once, call anywhere |
| **String techniques** | Working with text data | Strings are very common in security data |
| **List techniques** | Working with collections | Lists are also very common |

### Iterative Statements
- **for loop**: repeats based on a **sequence**.
- **while loop**: repeats based on a **condition**.

### Functions
- Can write your own, or use built-in ones.
- Reduce repeated code in a program.

### Strings
- Bracket notation to access characters by index.
- Useful: `str()`, `len()`, `.index()`

### Lists
- Bracket notation to access elements by index.
- Useful: `.insert()`, `.remove()`, `.append()`, `.index()`

## Example: Counting Logins by a Flagged User
Goal: count how many times a flagged user logged in today, given a list of usernames from all login attempts.

Steps:
1. **for loop** to go through every username in the list.
2. **if statement** inside the loop to check if the username matches the flagged user.
3. If True, **increment a counter variable**.
4. Wrap it in a **function** for reuse:
   - Parameters: flagged username and the list of usernames.
   - Returns: the counter (number of logins).

```python
def count_logins(flagged_user, login_list):
    count = 0
    for username in login_list:
        if username == flagged_user:
            count += 1
    return count
```

## Working with Files
- Security data is often first found in **log files**.
- **Log** = a record of events in an organization's systems. New lines are usually appended over time.

### Common formats: .txt and .csv
- Both are **plain text** files: no images, fonts, colors, or spacing info.
- **.csv** (comma-separated values): values separated by commas.
- **.txt**: no fixed format. Values may be separated by spaces or other ways.
- Data can be easily extracted from both and converted to other formats.

## Key Takeaways
- Automating tasks is a key skill for security analysts.
- Needs: variables, conditionals, iterative statements, string and list techniques.
- Working with files is also essential.

## Quick Memory Hook
**for** = loop over a sequence | **while** = loop until a condition changes | **.txt** = free format | **.csv** = comma-separated