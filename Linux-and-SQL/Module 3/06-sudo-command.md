# Linux Authentication, Authorization, and `sudo`

## Overview

Linux provides commands that allow security analysts to manage **authentication**, **authorization**, users, groups, and file ownership.

The `sudo` command is especially important because it allows authorized users to temporarily perform commands with elevated privileges without directly logging in as the root user.

Important commands covered in this section include:

- `sudo`
- `useradd`
- `usermod`
- `userdel`
- `chown`

## Authentication vs. Authorization

**Authentication:** The process of verifying who someone is.

**Authorization:** The process of determining what resources or actions a user is allowed to access.

These concepts are important when managing users and permissions in Linux.

## The Root User

The **root user**, also called the **superuser**, is a user account with extensive privileges to modify and manage the Linux system.

The root user can perform sensitive administrative tasks, including managing:

- Users
- Groups
- Permissions
- System configurations
- Files and directories

### Risks of Running as Root

Logging in and operating directly as the root user is generally discouraged because:

- A compromised root account can give an attacker extensive control over the system.
- It is easy to make irreversible mistakes.
- Commands run directly as root can be harder to associate with a specific administrator.

Instead, Linux commonly uses `sudo` to provide elevated privileges when they are needed.

## `sudo`

**`sudo`** allows authorized users to temporarily run commands with elevated privileges.

The name comes from **"super user do."**

Example:

```bash
sudo useradd fgarcia
```

Users must be authorized to use `sudo` through the **sudoers configuration**.

### Responsible Use of `sudo`

Although `sudo` is generally preferable to logging in directly as root, it still provides significant privileges.

Users with `sudo` access can be at greater risk if their accounts are compromised.

Best practices include:

- Granting `sudo` access only to users who need it.
- Using `sudo` only when elevated privileges are required.
- Running only the specific commands that require elevated privileges.
- Carefully reviewing commands copied from online sources before running them with `sudo`.

> **Security Note:** Be especially careful when copying commands from the internet. Adding `sudo` to a command can give it elevated privileges and may allow it to bypass normal security controls.

## `useradd`

The **`useradd`** command creates a new user account.

Example:

```bash
sudo useradd fgarcia
```

This creates a user named `fgarcia`.

### `-g`

The `-g` option sets the user's **primary group**.

Example:

```bash
sudo useradd -g security fgarcia
```

This creates `fgarcia` and assigns `security` as the user's primary group.

### `-G`

The `-G` option adds the user to one or more **supplemental groups**.

Example:

```bash
sudo useradd -G finance,admin fgarcia
```

This creates `fgarcia` and adds the user to the existing `finance` and `admin` groups.

## `usermod`

The **`usermod`** command modifies an existing user account.

It supports many of the same options as `useradd`, including `-g` and `-G`.

### Changing the Primary Group

Use `-g` to change an existing user's primary group.

```bash
sudo usermod -g executive fgarcia
```

This changes `fgarcia`'s primary group to `executive`.

### Adding a Supplemental Group

Use `-G` together with `-a` to add a user to a supplemental group without removing their existing supplemental groups.

```bash
sudo usermod -a -G marketing fgarcia
```

Here:

- `-a` = Append the user to the existing supplemental groups
- `-G` = Specify supplemental groups

> **Important:** When using `-G` with `usermod`, omitting `-a` replaces the user's existing supplemental groups with the groups specified in the command. Using `-a` ensures existing supplemental groups are preserved.

### Other `usermod` Options

| Option | Purpose |
|---|---|
| `-g` | Changes the user's primary group |
| `-G` | Specifies supplemental groups |
| `-a` | Appends supplemental groups instead of replacing them |
| `-d` | Changes the user's home directory |
| `-l` | Changes the user's login name |
| `-L` | Locks the user's account |

### Changing a Home Directory

```bash
sudo usermod -d /home/garcia_f fgarcia
```

This changes `fgarcia`'s home directory to `/home/garcia_f`.

### Locking an Account

```bash
sudo usermod -L fgarcia
```

This locks the account and prevents the user from logging in.

## `userdel`

The **`userdel`** command deletes a user account.

Example:

```bash
sudo userdel fgarcia
```

This deletes the `fgarcia` user account.

### Removing the User's Home Directory

By default, `userdel` does not delete the user's files in their home directory.

The `-r` option removes the user's home directory and its files.

```bash
sudo userdel -r fgarcia
```

> **Warning:** Deleting a user's home directory can permanently remove important files. Ensure appropriate backups exist before using `userdel -r`.

### Locking vs. Deleting an Account

Instead of deleting a user account, an administrator may lock it:

```bash
sudo usermod -L fgarcia
```

Locking an account prevents the user from logging in while preserving the account, files, and associated permissions.

This can be useful when an employee leaves an organization because administrators can still identify files owned by that account and transfer ownership when necessary.

## `chown`

The **`chown`** command changes the ownership of a file or directory.

Ownership can be changed for:

- A user
- A group

### Changing User Ownership

To change the owner of `access.txt` to `fgarcia`:

```bash
sudo chown fgarcia access.txt
```

### Changing Group Ownership

To change the group owner of `access.txt` to `security`:

```bash
sudo chown :security access.txt
```

The colon (`:`) indicates that `security` is the group name.

### User and Group Ownership

The general structure can be represented as:

```bash
chown <user>:<group> <file>
```

For example:

```bash
sudo chown fgarcia:security access.txt
```

This changes both the user owner and group owner of `access.txt`.

## Command Summary

| Command | Purpose |
|---|---|
| `sudo` | Temporarily runs a command with elevated privileges |
| `useradd` | Creates a user |
| `usermod` | Modifies an existing user |
| `userdel` | Deletes a user |
| `chown` | Changes the ownership of a file or directory |

## Key Takeaways

- **Authentication** verifies a user's identity.
- **Authorization** determines what a user is allowed to access or modify.
- The **root user** has extensive administrative privileges and should be used carefully.
- **`sudo`** allows authorized users to temporarily perform commands with elevated privileges.
- `useradd` creates users and can assign primary and supplemental groups.
- `usermod` modifies existing users, including their groups, home directory, login name, and account status.
- `userdel` deletes user accounts, while `userdel -r` also removes the user's home directory and its files.
- `usermod -L` can lock an account without deleting it.
- `chown` changes the user or group ownership of files and directories.
- Elevated privileges should be granted only when necessary and used carefully to follow the principle of least privilege.