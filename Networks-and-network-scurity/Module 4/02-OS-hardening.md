# Operating System (OS) Hardening

## Overview

The **Operating System (OS)** acts as an interface between the user and computer hardware. It is the first program loaded when a computer starts and acts as an intermediary between software applications and hardware.

Securing the OS is important because a single insecure OS can potentially lead to the compromise of an entire network.

Different operating systems share many similar **OS hardening** practices.

## OS Hardening

**OS hardening** is a set of procedures used to maintain and improve the security of an operating system.

Hardening tasks can be performed:

- **Regularly:** Updates, backups, device inventories, and authorized-user reviews.
- **Initially:** One-time security configurations, such as configuring a device to use a secure encryption standard.

## Regular OS Hardening Tasks

### 1. Patch Updates

**Patch update:** A software or OS update that addresses security vulnerabilities within a program or product.

Organizations should upgrade operating systems to the latest available software version and install security patches as soon as possible.

When an OS vendor releases a patch for a vulnerability, malicious actors may learn where the vulnerability exists in systems running outdated software. Prompt patching helps reduce the risk of exploitation.

> **Example:** An organization may need to perform an emergency patch when a vulnerability is discovered in a commonly used programming library. If the library is widely used, many servers and applications may need to be patched quickly.

## 2. Baseline Configuration

A newly updated OS should be added to the organization's **baseline configuration**, also called a **baseline image**.

**Baseline Configuration:** A documented set of specifications within a system that serves as a basis for future builds, releases, and updates.

A baseline can include security settings such as:

- Firewall rules
- Allowed network ports
- Disallowed network ports
- Other approved system configurations

If unusual activity is detected, security teams can compare the current OS configuration against the baseline to determine whether changes have occurred.

## 3. Hardware and Software Disposal

Organizations should properly dispose of old hardware and remove unused software.

### Hardware Disposal

Old hardware should be properly **wiped** before disposal to help prevent unauthorized access to stored information.

### Software Removal

Unused software applications should be removed because software can contain known vulnerabilities.

Removing unnecessary software:

- Reduces the attack surface
- Removes unnecessary vulnerabilities
- Reduces the number of programs that need to be secured and monitored

## 4. Strong Password Policy

A **password policy** defines rules that users must follow when creating and using passwords.

A policy may require:

- A minimum number of characters
- At least one capital letter
- At least one number
- At least one symbol

Password policies may also limit repeated failed login attempts. For example, a user may lose access to the network after entering an incorrect password a certain number of times consecutively.

## 5. Multi-Factor Authentication (MFA)

**Multi-Factor Authentication (MFA):** A security measure that requires a user to verify their identity using two or more methods before accessing a system or network.

Authentication methods can include:

| Factor | Example |
|---|---|
| Something you know | Password |
| Something you have | ID card |
| Something unique about you | Fingerprint |

Using multiple authentication factors makes unauthorized access more difficult.

## OS Hardening Summary

OS hardening involves maintaining and improving the security of operating systems through regular security practices and appropriate configurations.

Important OS hardening practices include:

1. Installing **patch updates** promptly.
2. Maintaining an up-to-date **baseline configuration**.
3. Properly wiping and disposing of old hardware.
4. Removing unused software applications.
5. Enforcing strong **password policies**.
6. Using **Multi-Factor Authentication (MFA)** where required.
7. Regularly reviewing security measures such as access privileges and password policies.

## Key Takeaways

- The **OS** acts as an intermediary between users, applications, and computer hardware.
- An insecure OS can contribute to the compromise of an entire network.
- **OS hardening** maintains and improves operating system security.
- **Patch updates** address security vulnerabilities and should be applied promptly.
- A **baseline configuration** provides an approved reference configuration for systems.
- Removing unused software and properly disposing of old hardware helps reduce security risks.
- Strong password policies and **MFA** help prevent unauthorized access.
- Security measures such as access privileges and password policies should be reviewed regularly.