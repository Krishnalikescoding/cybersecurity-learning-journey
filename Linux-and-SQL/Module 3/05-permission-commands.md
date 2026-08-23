# Linux File and Directory Permissions

## Overview

Linux uses permissions to control who can access files and directories and what actions they can perform.

Understanding permissions is important for security analysts because improperly configured permissions can allow users to access or modify resources beyond what they need.

Linux permissions are represented using a **10-character string**.

## Permission Types

Linux uses three basic permissions:

| Permission | Files | Directories |
|---|---|---|
| **Read (`r`)** | Read the contents of the file | Read the contents of the directory, including files and subdirectories |
| **Write (`w`)** | Modify the file contents | Create new files in the directory |
| **Execute (`x`)** | Execute the file if it is a program | Enter the directory and access its files |

## Permission Owner Types

Permissions are assigned to three types of users:

- **User (`u`):** The owner of the file.
- **Group (`g`):** A group that the file owner belongs to.
- **Other (`o`):** All other users on the system.

## Understanding the 10-Character Permission String

A Linux permission string contains 10 characters.

Example:

```text
drwxrwxrwx
```

The first character represents the **file type**, while the remaining nine characters represent permissions for the user, group, and other.

```text
d r w x r w x r w x
│ │ │ │ │ │ │ │ │ │
│ └─┴─┘ └─┴─┘ └─┴─┘
│  User   Group   Other
│
│
└── File type
```

### Permission Positions

| Position | Example | Meaning |
|---:|---|---|
| 1 | `d` | File type |
| 2 | `r` | Read permission for user |
| 3 | `w` | Write permission for user |
| 4 | `x` | Execute permission for user |
| 5 | `r` | Read permission for group |
| 6 | `w` | Write permission for group |
| 7 | `x` | Execute permission for group |
| 8 | `r` | Read permission for other |
| 9 | `w` | Write permission for other |
| 10 | `x` | Execute permission for other |

### File Type

The first character identifies the type of filesystem object.

- `d` = Directory
- `-` = Regular file

For example:

```text
drwxrwxrwx
```

The first character `d` indicates that this is a directory.

A regular file might appear as:

```text
-rwxrwxrwx
```

### Permission Symbols

For each permission:

- `r` = Permission is granted
- `w` = Permission is granted
- `x` = Permission is granted
- `-` = Permission is not granted

For example:

```text
-rw-r-----
```

This indicates:

- User: read and write
- Group: read
- Other: no permissions

## Exploring Existing Permissions

The `ls` command can be used to investigate file and directory permissions.

### `ls -a`

```bash
ls -a
```

Displays hidden files.

Hidden files typically begin with a period (`.`).

### `ls -l`

```bash
ls -l
```

Displays detailed information about files and directories, including:

- Permissions
- Owner
- Group
- File size
- Last modification time

### `ls -la`

```bash
ls -la
```

Displays detailed information, including hidden files.

It combines the functionality of `-l` and `-a`.

## Principle of Least Privilege

**Principle of Least Privilege:** The concept of granting only the minimum access and authorization required to complete a task or function.

Users should not have privileges beyond what is necessary for their responsibilities.

Failing to follow the principle of least privilege can create security risks by allowing users to access or modify resources they do not need.

## Changing Permissions with `chmod`

The **`chmod`** command changes permissions on files and directories.

The basic structure is:

```bash
chmod <permission_changes> <file_or_directory>
```

### Adding Permissions

To add read, write, and execute permissions for the user, group, and other:

```bash
chmod u+rwx,g+rwx,o+rwx login_sessions.txt
```

This adds all three permissions to each owner type.

### Removing Permissions

To remove all permissions from the user, group, and other:

```bash
chmod u-rwx,g-rwx,o-rwx login_sessions.txt
```

### Assigning Exact Permissions

The `=` operator assigns permissions exactly as specified.

For example:

```bash
chmod u=r,g=r,o=r login_sessions.txt
```

This gives read permission to the user, group, and other.

It also **overwrites existing permissions**.

For example, if the user previously had write permission, that permission is removed because only `r` is specified.

## `chmod` Symbols

The first argument of `chmod` uses specific characters to identify the owner type and permission changes.

| Symbol | Description |
|---|---|
| `u` | User permissions |
| `g` | Group permissions |
| `o` | Other permissions |
| `+` | Adds permissions |
| `-` | Removes permissions |
| `=` | Assigns permissions exactly as specified |

When modifying multiple owner types, separate the changes with commas and do not add spaces.

Example:

```bash
chmod u+r,g-w,o-r file.txt
```

## Principle of Least Privilege in Action

Consider a file named `bonuses.txt` inside a `compensation` directory.

The file belongs to a Human Resources employee with the username `hrrep1`.

The employee needs access to the file, but other members of the HR group do not need access because the file contains confidential information.

First, the permissions can be checked using:

```bash
ls -l
```

Suppose the file has the following permissions:

```text
-rw-rw----
```

These permissions indicate:

- User: read and write
- Group: read and write
- Other: no permissions

The group has more access than necessary, which violates the **principle of least privilege**.

The unnecessary group permissions can be removed with:

```bash
chmod g-rw bonuses.txt
```

This removes read and write permissions from the group while leaving the user's permissions unchanged.

The result is:

```text
-rw-------
```

Now only the file owner has read and write access.

## Key Takeaways

- Linux permissions control access to files and directories.
- Permissions include **read (`r`)**, **write (`w`)**, and **execute (`x`)**.
- Permissions are assigned to the **user**, **group**, and **other**.
- The first character of a 10-character permission string identifies the file type.
- `ls -l` displays detailed file and directory permissions.
- `ls -la` displays detailed permissions, including hidden files.
- **`chmod`** is used to modify file and directory permissions.
- `+` adds permissions, `-` removes permissions, and `=` assigns permissions exactly.
- The **principle of least privilege** requires users to receive only the access necessary for their tasks.
- Properly managing permissions helps reduce unauthorized access and security risks.