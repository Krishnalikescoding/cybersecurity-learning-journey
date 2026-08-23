# Linux File and Directory Management

## Overview

Linux provides several commands for creating, modifying, moving, copying, and deleting files and directories.

Important commands covered in this section include:

- `mkdir`
- `rmdir`
- `touch`
- `rm`
- `mv`
- `cp`
- `nano`

Linux also provides **standard output redirection** using:

- `>`
- `>>`

## Creating and Modifying Directories

### `mkdir`

The **`mkdir`** command creates a new directory.

A directory can be specified using either:

- **Absolute path:** Starts from the root directory (`/`)
- **Relative path:** Starts from the current working directory

#### Using an Absolute Path

```bash
mkdir /home/analyst/logs/network
```

This creates a directory named `network` inside `/home/analyst/logs`.

#### Using a Relative Path

If you are already in `/home/analyst/logs`, you can use:

```bash
mkdir network
```

The `ls` command can be used to verify that the directory was created:

```bash
ls
```

### `rmdir`

The **`rmdir`** command removes an empty directory.

Example:

```bash
rmdir /home/analyst/logs/network
```

This removes the `network` directory.

> **Note:** `rmdir` cannot remove directories that contain files or subdirectories.

For example:

```bash
rmdir /home/analyst
```

will return an error if `/home/analyst` contains files or subdirectories.

## Creating and Modifying Files

### `touch`

The **`touch`** command creates a new empty file.

For example, if the current directory is `/home/analyst/reports`:

```bash
touch permissions.txt
```

This creates an empty file named `permissions.txt`.

You can verify that the file was created using:

```bash
ls
```

### `rm`

The **`rm`** command removes a file.

Example:

```bash
rm permissions.txt
```

> **Warning:** Use `rm` carefully because files deleted with `rm` can be difficult to recover.

You can verify that the file was removed using:

```bash
ls
```

## Moving and Copying Files

### `mv`

The **`mv`** command moves a file or directory to a new location.

Syntax:

```bash
mv <source> <destination>
```

Example:

```bash
mv permissions.txt /home/analyst/logs
```

This moves `permissions.txt` into the `/home/analyst/logs` directory.

Moving a file removes it from its original location.

### `cp`

The **`cp`** command copies a file or directory to a new location.

Syntax:

```bash
cp <source> <destination>
```

Example:

```bash
cp permissions.txt /home/analyst/logs
```

This creates a copy of `permissions.txt` in `/home/analyst/logs` while keeping the original file in its current location.

### `mv` vs `cp`

| Command | Function | Original Remains? |
|---|---|---|
| `mv` | Moves a file or directory | No |
| `cp` | Copies a file or directory | Yes |

### Renaming Files with `mv`

The `mv` command can also be used to rename files.

Example:

```bash
mv permissions.txt perm.txt
```

This renames `permissions.txt` to `perm.txt`.

## Nano Text Editor

**`nano`** is a command-line text editor available by default in many Linux distributions.

It can be used to:

- Create files
- Open existing files
- Modify file contents

Nano is commonly used by beginners and is also widely used in the security profession.

### Opening an Existing File

If you are in the directory containing the file:

```bash
nano permissions.txt
```

This opens `permissions.txt` for editing.

You can also specify the absolute path:

```bash
nano /home/analyst/reports/permissions.txt
```

### Creating a New File

You can create and open a new file directly with `nano`:

```bash
nano authorized_users.txt
```

If the file does not exist, nano creates it when the file is saved.

### Saving and Exiting Nano

Nano does not automatically save changes.

Important keyboard shortcuts:

| Shortcut | Function |
|---|---|
| `Ctrl + O` | Save the file |
| `Ctrl + X` | Exit nano |

When saving with `Ctrl + O`, nano prompts you to confirm the filename.

Other popular command-line text editors include:

- Vim
- Emacs

## Standard Output Redirection

Linux allows command output to be redirected into files.

**Standard input:** Information received by the operating system through the command line.

**Standard output:** Information returned by the operating system through the shell.

In addition to piping (`|`), Linux provides two important output redirection operators:

- `>`
- `>>`

### `>` Operator

The **`>`** operator redirects standard output to a file.

If the file already exists, its contents are **overwritten**.

Example:

```bash
echo "time" > permissions.txt
```

This replaces the existing contents of `permissions.txt` with:

```text
time
```

> **Warning:** Use `>` carefully because existing file contents can be overwritten and may be difficult to recover.

### `>>` Operator

The **`>>`** operator redirects standard output to the end of a file without overwriting its existing contents.

Example:

```bash
echo "last updated date" >> permissions.txt
```

This adds `last updated date` to the end of `permissions.txt`.

### `>` vs `>>`

| Operator | Function | Existing Contents |
|---|---|---|
| `>` | Writes output to a file | Overwrites existing contents |
| `>>` | Appends output to a file | Preserves existing contents |

Both operators will create a new file if the specified file does not already exist.

## Command Summary

| Command / Operator | Purpose |
|---|---|
| `mkdir` | Creates a directory |
| `rmdir` | Removes an empty directory |
| `touch` | Creates an empty file |
| `rm` | Removes a file |
| `mv` | Moves or renames a file or directory |
| `cp` | Copies a file or directory |
| `nano` | Opens or creates a file for editing |
| `>` | Redirects output and overwrites existing file contents |
| `>>` | Redirects output and appends to existing file contents |
| `|` | Sends output from one command to another as input |

## Key Takeaways

- Linux provides commands for managing files and directories directly from the command line.
- `mkdir` creates directories, while `rmdir` removes empty directories.
- `touch` creates empty files, and `rm` removes files.
- `mv` moves or renames files and directories.
- `cp` creates copies while preserving the original.
- `nano` is a command-line text editor used to create and modify files.
- `>` redirects output to a file and **overwrites** existing contents.
- `>>` redirects output and **appends** to existing contents.
- Security analysts need to understand Linux file-system management because many security tasks involve creating, modifying, analyzing, and managing files.