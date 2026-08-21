# Shell Communication Basics

## Overview

Communicating with a computer through the shell works like a conversation: one party sends a message, and the other responds. Shell communication happens in one of three ways: **input**, **output**, or **error**.

## Key Concepts

### Standard Input

**Standard Input**: Information received by the operating system (OS) via the command line, typed from the keyboard into the shell.

- Equivalent to asking a question in a conversation.
- If the shell can interpret the input, it requests the necessary resources from the kernel to execute the task.

### Standard Output

**Standard Output**: The information returned by the OS through the shell in response to a command.

- Equivalent to receiving an answer in a conversation.
- Output is what the user receives after a command is successfully executed.

### Standard Error

**Standard Error**: Error messages returned by the OS through the shell when a command cannot be processed.

- Equivalent to a friend indicating they cannot answer a question.
- Common causes:
  - Misspelled commands
  - The system not recognizing the command
  - Insufficient permissions to perform the command

## Examples

### Example: Standard Input and Output

The `echo` command outputs a specified string of text. A **string** is data consisting of an ordered sequence of characters.

```bash
echo hello
```

**Output:**

```text
hello
```

Here, `echo hello` is the input sent to the OS. Pressing Enter sends the command, and the shell immediately returns the output `hello`.

### Example: Standard Error

Intentionally misspelling `echo` as `eco` demonstrates an error response:

```bash
eco hello
```

Pressing Enter produces an error message, since `eco` is not a recognized command.

## Key Takeaways

- Shell communication occurs in three forms: **input**, **output**, and **error**.
- **Standard input** is data sent from the keyboard to the shell.
- **Standard output** is the response returned by the OS after successful command execution.
- **Standard error** is returned when a command cannot be processed (e.g., misspelling, unrecognized command, or lack of permissions).