# Brute Force Attacks, Vulnerability Assessment, and Prevention

## Overview

A **brute force attack** is a trial-and-error process used by malicious actors to discover private information, such as login credentials.

Organizations can use **Operating System (OS) hardening**, virtual machines, sandboxes, and authentication controls to assess vulnerabilities and reduce the risk of brute force attacks.

## Usernames and Passwords

Usernames and passwords are among the most common security controls used to protect sensitive or private information.

They are commonly used on:

- Personal phones
- Computers
- Restricted organizational applications
- Systems that store or access sensitive information

However, login credentials can be:

- Stolen
- Guessed
- Targeted by malicious actors

Because of this, organizations should use additional security measures rather than relying only on usernames and passwords.

## Brute Force Attacks

**Brute Force Attack:** A trial-and-error process of discovering private information, such as passwords or login credentials.

Brute force attacks can be performed manually or with software tools.

### Types of Brute Force Attacks

#### Simple Brute Force Attack

A **simple brute force attack** occurs when an attacker attempts to guess a user's login credentials.

The attacker may try different combinations of:

- Usernames
- Passwords

The attacker continues trying combinations until the correct credentials are discovered.

#### Dictionary Attack

A **dictionary attack** uses a list of commonly used passwords or previously stolen credentials to attempt to access a system.

The term comes from the original use of lists of dictionary words to guess passwords.

Dictionary attacks became less effective as organizations introduced more complex password requirements, but they remain a type of brute force attack.

## Assessing Vulnerabilities

Organizations can perform security tests before a brute force attack or other cybersecurity incident occurs.

Security analysts can use:

- **Virtual machines (VMs)**
- **Sandbox environments**

These environments can be used to:

- Test suspicious files
- Identify vulnerabilities
- Investigate potentially infected systems
- Simulate cybersecurity incidents
- Test applications and security controls

## Virtual Machines (VMs)

**Virtual Machine (VM):** A software-based version of a physical computer that can run in an isolated environment.

VMs provide an additional layer of security because potentially malicious code can be executed separately from the main system.

### Uses of VMs

VMs can be used to:

- Run potentially malicious code in an isolated environment
- Investigate potentially infected machines
- Test applications
- Conduct vulnerability assessments
- Run malware in a constrained environment
- Switch between different testing environments
- Revert a system to a previous state
- Restore a VM to a clean or pristine image after testing

Using a VM can reduce the potential damage caused if security tools or malicious code are used improperly.

### VM Risks

VMs are not completely risk-free.

There is still a small possibility that malicious software could **escape virtualization** and gain access to the host machine.

> **Note:** VMs provide isolation, but they should not be treated as an absolute security boundary.

## Sandbox Environments

**Sandbox:** A testing environment that allows software or programs to be executed separately from a network or production environment.

Sandboxes are commonly used for:

- Testing software patches
- Identifying and addressing bugs
- Detecting cybersecurity vulnerabilities
- Evaluating suspicious software
- Analyzing files containing malicious code
- Simulating attack scenarios

### Types of Sandbox Environments

A sandbox can be:

- A standalone physical computer that is not connected to a network
- A software-based environment
- A cloud-based virtual environment

Software and cloud-based environments can be more time- and cost-effective than dedicated physical computers.

### Sandbox Limitations

Some malware authors design malware to detect whether it is running inside a VM or sandbox.

Malware can be programmed to behave differently in a testing environment, such as appearing harmless when it detects virtualization or sandboxing.

Therefore, sandbox results should be interpreted carefully.

## Prevention Measures

Organizations can use several security controls to help prevent brute force attacks.

### 1. Hashing and Salting

**Hashing** converts information into a value that can be used to help protect information and verify integrity. It is designed as a one-way function.

**Salting** adds random characters to passwords before or during the hashing process.

Salting helps make password hashes more difficult to attack by increasing their uniqueness and complexity.

> **Note:** Password hashing is intended to be one-way. The original password should not be recoverable directly from the stored hash.

### 2. Multi-Factor Authentication (MFA)

**Multi-Factor Authentication (MFA):** A security measure that requires a user to verify their identity using two or more authentication factors.

Examples of authentication factors include:

- Username and password
- Fingerprint
- Facial recognition
- One-time password (OTP) sent to a phone number or email

MFA provides an additional layer of protection if a password is compromised.

### 3. Two-Factor Authentication (2FA)

**Two-Factor Authentication (2FA)** is similar to MFA but specifically uses **two forms of verification**.

| Authentication Method | Number of Factors |
|---|---:|
| MFA | Two or more |
| 2FA | Exactly two |

### 4. CAPTCHA and reCAPTCHA

**CAPTCHA** stands for **Completely Automated Public Turing test to tell Computers and Humans Apart**.

A CAPTCHA asks users to complete a test designed to distinguish humans from automated software.

CAPTCHA can help prevent automated software from repeatedly attempting to brute force passwords.

**reCAPTCHA** is a CAPTCHA service from Google designed to help protect websites from bots and malicious software.

### 5. Password Policies

Organizations use **password policies** to standardize secure password practices.

Password policies can define:

- Password complexity requirements
- How often passwords must be updated
- Whether previously used passwords can be reused
- The maximum number of failed login attempts
- When an account should be suspended after repeated failed attempts

These controls can make automated password-guessing attacks more difficult.

## Security Controls at a Glance

| Security Control | Purpose |
|---|---|
| Hashing | Converts passwords or other information into a one-way value |
| Salting | Adds random data to make password hashes more difficult to attack |
| MFA | Requires two or more authentication factors |
| 2FA | Requires exactly two authentication factors |
| CAPTCHA | Helps distinguish humans from automated software |
| reCAPTCHA | Helps protect websites from bots and malicious software |
| Password policies | Establish rules for secure password creation and usage |
| VMs | Provide isolated environments for testing and investigation |
| Sandboxes | Allow suspicious software and attack scenarios to be tested separately |

## Key Takeaways

- A **brute force attack** uses trial and error to guess passwords or other private information.
- **Simple brute force attacks** attempt different combinations of usernames and passwords.
- **Dictionary attacks** use lists of commonly used passwords or stolen credentials.
- **Virtual machines** provide isolated environments for testing applications, suspicious files, malware, and vulnerabilities.
- **Sandbox environments** allow software and attack scenarios to be tested separately from production systems.
- VMs and sandboxes provide isolation but are not completely risk-free because sophisticated malware may detect or attempt to escape these environments.
- Common measures for preventing brute force attacks include:
  - **Hashing and salting**
  - **MFA**
  - **2FA**
  - **CAPTCHA and reCAPTCHA**
  - **Password policies**
- Combining multiple security controls provides stronger protection than relying only on usernames and passwords.