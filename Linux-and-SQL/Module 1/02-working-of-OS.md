# How Operating Systems Work

## Overview

An **Operating System (OS)** is a critical component of a computer that connects applications with hardware and allows users to perform tasks.

The OS operates largely in the background, interpreting requests from applications and directing them to the appropriate hardware components.

## Booting the Computer

When a computer is turned on, either a **BIOS** or **UEFI** microchip is activated.

### BIOS

**Basic Input/Output System (BIOS):** A microchip containing loading instructions that help start a computer.

BIOS was prevalent in older computer systems and was the standard until around 2007.

### UEFI

**Unified Extensible Firmware Interface (UEFI):** A microchip containing loading instructions for starting a computer and the modern replacement for BIOS.

Most newer computers use UEFI, which also provides enhanced security features.

### Boot Process

BIOS or UEFI contains instructions that the computer follows during startup. One example is checking the health of the computer's hardware.

The final instruction from BIOS or UEFI activates the **bootloader**.

**Bootloader:** A software program that starts the operating system.

The basic boot process is:

1. The computer is powered on.
2. BIOS or UEFI is activated.
3. BIOS or UEFI follows its loading instructions.
4. The computer's hardware is checked.
5. BIOS or UEFI activates the bootloader.
6. The bootloader starts the operating system.
7. The operating system finishes loading and the computer becomes ready for use.

## Completing a Task

Once the computer has booted, completing a task involves four main components:

1. **User**
2. **Application**
3. **Operating System**
4. **Hardware**

![inside-OS](../../src/OS-working.png)

### 1. User

The **user** initiates the process by deciding what they want to accomplish.

Examples:

- Calculate a number
- Write a report
- Print a document
- Download a file

### 2. Application

The **application** is the software that the user interacts with to complete a task.

Examples:

- Calculator application for calculations
- Word processor for writing reports
- Internet browser for downloading files

The application communicates the user's request to the operating system.

### 3. Operating System

The **operating system** receives the request from the application.

Its role is to:

- Interpret the request
- Direct the request
- Send the request to the appropriate hardware components

The OS acts as the connection between applications and hardware.

### 4. Hardware

The **hardware** performs the processing required to complete the task.

Examples:

- The **CPU** performs calculations.
- A **hard drive** stores files.

After the hardware completes the requested operation, the output is sent back through the operating system to the application. The application then displays the result to the user.

The operating system coordinates communication between the application and hardware without requiring the user to directly manage the underlying hardware operations.

## OS at Work Behind the Scenes

Much of the work performed by an operating system is not directly visible to the user.

A useful analogy is a **restaurant**:

| Computer | Restaurant |
|---|---|
| User | Customer |
| Application | Placing an order |
| Operating System | Kitchen |
| Hardware | Cooking and preparing the food |
| Output | Completed meal |

When a customer places an order, they do not see everything happening in the kitchen. However, the kitchen is responsible for interpreting the request and ensuring the correct food is prepared.

Similarly, when a user makes a request through an application, the OS works behind the scenes to interpret the request and coordinate the appropriate hardware.

## Example: Downloading a File

Consider a user downloading a file through an internet browser.

1. **User:** The user finds a file online and clicks the download button.
2. **Application:** The internet browser communicates the user's action to the OS.
3. **Operating System:** The OS processes the request and sends it to the appropriate hardware for processing.
4. **Hardware:** The hardware performs the operations required to download and store the file.
5. **Operating System:** The OS communicates the download status back to the browser.
6. **Application:** The browser informs the user that the file has been downloaded.


## Key Takeaways

- **BIOS** and **UEFI** provide startup instructions for a computer.
- **UEFI** is the modern replacement for BIOS and provides enhanced security features.
- The **bootloader** starts the operating system during the boot process.
- The OS connects **applications** and **hardware**.
- A typical task flows from the **user → application → OS → hardware**, with the result returning through the OS and application to the user.
- Much of the OS's work happens in the background and is not directly visible to the user.
- Understanding how the OS coordinates applications and hardware is important for understanding computer and operating system security.