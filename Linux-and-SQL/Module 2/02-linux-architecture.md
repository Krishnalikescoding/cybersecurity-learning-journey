# Linux Architecture

## Overview

Understanding **Linux architecture** is important for security analysts because it helps explain how the different components of a Linux system interact.

A request to perform a task generally flows through the following components:

```text
User
  ↓
Applications
  ↓
Shell
  ↓
Filesystem Hierarchy Standard (FHS)
  ↓
Kernel
  ↓
Hardware
```

Each component has a specific role in the operation of the Linux system.

## User

The **user** is the person interacting with the computer.

Users:

- Initiate computer tasks
- Manage tasks
- Interact with applications and the operating system

Linux is a **multi-user system**, meaning multiple users can use the same system resources at the same time.

## Applications

**Application:** A program that performs a specific task.

Examples include:

- Calculators
- Calendars
- Web browsers
- Email clients

Some applications are pre-installed, while others need to be installed separately.

### Package Manager

A **package manager** is a tool used to:

- Install applications
- Manage applications
- Remove applications

A **package** is a piece of software that can be combined with other packages to form an application.

Linux commonly uses package managers to install and manage software.

## Shell

The **shell** is a **command-line interpreter** that allows users to communicate with the operating system using text-based commands.

The shell:

- Accepts commands entered by the user
- Translates commands
- Communicates requests to the kernel
- Receives responses from the kernel

The shell can be thought of as a translator between the user and the computer.

```text
User
  ↓
Shell
  ↓
Kernel
  ↓
Hardware
```

## Filesystem Hierarchy Standard (FHS)

**Filesystem Hierarchy Standard (FHS):** A standard that defines how data and directories are organized within a Linux operating system.

The FHS specifies where different types of data are stored, allowing the operating system and users to locate files consistently.

### Directories

A **directory** is a file system location used to organize other files and directories.

Directories are commonly referred to as **folders** and can contain:

- Files
- Other directories

The FHS defines how directories and their contents are organized within the Linux filesystem.

## Kernel

The **kernel** is a core component of the Linux operating system that manages processes and memory and communicates with applications.

The kernel:

- Routes commands from applications
- Manages system resources
- Allocates resources
- Manages processes and memory
- Controls major hardware functions

The Linux kernel is a critical component of Linux and helps applications interact with the underlying hardware.

## Hardware

**Hardware:** The physical components of a computer.

Hardware can be divided into:

- **Peripheral devices**
- **Internal hardware**

### Peripheral Devices

**Peripheral devices:** Hardware components attached to and controlled by a computer system that are not core components required to operate the computer.

Peripheral devices can generally be added or removed from a computer.

Examples include:

- Monitor
- Printer
- Keyboard
- Mouse

### Internal Hardware

**Internal hardware:** Components required for the computer to operate.

Internal hardware is connected to the computer's main circuit board, called the **motherboard**.

Important internal hardware components include:

- Central Processing Unit (CPU)
- Random Access Memory (RAM)
- Hard drive

#### Central Processing Unit (CPU)

**Central Processing Unit (CPU):** The main processor of a computer that performs general computing tasks.

The CPU:

- Executes instructions provided by programs
- Processes data
- Enables programs to run

#### Random Access Memory (RAM)

**Random Access Memory (RAM):** A hardware component used for short-term memory.

RAM temporarily stores data needed while programs and tasks are running.

For example, when writing a report, data required by the application is temporarily stored in RAM.

Important characteristics of RAM include:

- It provides temporary storage.
- The CPU uses data stored in RAM when running programs.
- Data in RAM is lost when the computer is powered off.

#### Hard Drive

A **hard drive** is a hardware component used for long-term storage.

It stores:

- Programs
- Files
- Other data

Unlike RAM, data stored on a hard drive remains available after the computer is powered off and restarted.

A computer can have multiple hard drives.

## Linux Architecture at a Glance

| Component | Main Function |
|---|---|
| **User** | Initiates and manages computer tasks |
| **Applications** | Perform specific tasks |
| **Shell** | Interprets text-based commands and communicates with the kernel |
| **FHS** | Organizes the Linux filesystem and data |
| **Kernel** | Manages processes, memory, resources, and hardware |
| **Hardware** | Performs physical processing and stores data |

## Key Takeaways

- Linux architecture consists of the **user, applications, shell, FHS, kernel, and hardware**.
- Linux is a **multi-user operating system**.
- A **package manager** is used to install, manage, and remove software packages.
- The **shell** interprets text-based commands and communicates with the kernel.
- The **FHS** organizes files and directories within Linux.
- The **kernel** manages processes, memory, system resources, and hardware.
- **Peripheral devices** are attached hardware components that are not essential to the core operation of the computer.
- **CPU**, **RAM**, and **hard drives** are important internal hardware components.
- Understanding how these components interact helps security analysts understand how Linux systems function and how they can be secured.