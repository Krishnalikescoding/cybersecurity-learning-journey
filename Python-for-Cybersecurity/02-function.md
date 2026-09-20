# Python Functions in Cybersecurity – Notes

## What is a Function?
- A **function** is a reusable section of code within a program.
- Helps automate repetitive tasks — useful in cybersecurity for repeated processes like scanning security logs.
- **Example use case**: defining a function that takes a log as input and returns potentially malicious logins — reusable across multiple logs.

## Built-in vs. User-Defined Functions
- **Built-in functions**: exist within Python already (e.g., `print()`).
- **User-defined functions**: created by programmers for specific needs.

## Defining a Function

### Function Header
- Starts with the `def` keyword, followed by the function name, parentheses `()`, and a colon `:`.

```python
def display_investigation_message():
```

- **Pro tip**: name functions based on what they do, so they're easy to recall later.

### Function Body
- Indented block of code after the header — defines what the function does.
- Indentation separates the function definition from the rest of the code.

```python
def display_investigation_message():
    print("investigate activity")
```

## Calling a Function
- After defining a function, you can **call** it (use it) as many times as needed.
- To call it: write the function name followed by parentheses.

```python
display_investigation_message()
```

### Example: Calling a Function Within Conditionals
```python
def display_investigation_message():
    print("investigate activity")

application_status = "potential concern"
email_status = "okay"

if application_status == "potential concern":
    print("application_log:")
    display_investigation_message()

if email_status == "potential concern":
    print("email log:")
```
- Only the first condition (`application_status`) is True → prints "application_log:" and calls the function.
- The second condition (`email_status`) is False → nothing prints for it.
- Functions can be called from many different places in code, including inside conditionals.

## Caution: Infinite Loops
- Calling a function **inside its own definition** (recursion) without a stopping condition creates an **infinite loop**.

```python
def func1():
    func1()   # calls itself forever — infinite loop
```

## Key Takeaways
- Functions require two essential parts: **function header** and **function body**.
- Defining a function once lets you **call** it repeatedly wherever needed.
- Functions improve efficiency, especially for repetitive cybersecurity tasks like log analysis.