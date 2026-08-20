# Kali Linux

## Overview

**Kali Linux™** is a trademark of **Offensive Security** and is a **Debian-derived, open-source Linux distribution** designed specifically for:

- Penetration testing
- Digital forensics

Kali Linux includes many security tools pre-installed, making it a widely used distribution among cybersecurity professionals.

> **Note:** Kali Linux should be used on a **virtual machine (VM)** when possible. This helps prevent accidental damage to the host system if security tools are used improperly. A virtual machine also allows users to revert to a previous state when needed.

## Kali Linux for Penetration Testing

**Penetration testing:** A simulated attack that helps identify vulnerabilities in:

- Systems
- Networks
- Websites
- Applications
- Processes

Security professionals who specialize in penetration testing commonly use Kali Linux because it provides numerous tools designed for security testing.

### Common Penetration Testing Tools

| Tool | Purpose |
|---|---|
| **Metasploit** | Used to identify and exploit vulnerabilities on machines |
| **Burp Suite** | Used to test web applications for security weaknesses |
| **John the Ripper** | Used to guess passwords |

## Kali Linux for Digital Forensics

**Digital forensics:** The process of collecting and analyzing data to determine what happened after a security attack.

Security professionals may use digital forensics to investigate information such as:

- Network activity
- System activity
- Stored data
- Evidence related to security incidents

Kali Linux includes many tools that support digital forensic investigations.

### Common Digital Forensics Tools

#### tcpdump

**`tcpdump`** is a command-line packet analyzer used to capture network traffic.

It can be used by security professionals to investigate network activity and examine captured traffic.

#### Wireshark

**Wireshark** is a network protocol analyzer with a **Graphical User Interface (GUI)**.

It can be used to:

- Analyze live network traffic
- Analyze captured network traffic
- Investigate network activity

#### Autopsy

**Autopsy** is a digital forensics tool used to analyze:

- Hard drives
- Smartphones

It can assist investigators in examining digital evidence after a security event.

## Using Kali Linux in a Virtual Machine

Kali Linux should be used in a **virtual machine** when performing security testing, particularly when experimenting with potentially disruptive tools.

Using a VM provides two important benefits:

1. **Isolation:** Helps protect the host system from accidental damage caused by improperly used tools.
2. **Revert capability:** Allows the user to return the virtual machine to a previous state.

This makes a virtual machine a useful environment for learning, testing, and security experimentation.

## Kali Linux Tool Categories

Kali Linux provides many tools for different cybersecurity activities.

```text
Kali Linux
├── Penetration Testing
│   ├── Metasploit
│   ├── Burp Suite
│   └── John the Ripper
│
└── Digital Forensics
    ├── tcpdump
    ├── Wireshark
    └── Autopsy
```

## Key Takeaways

- **Kali Linux™** is a trademark of **Offensive Security**.
- Kali Linux is an **open-source, Debian-derived distribution** designed for penetration testing and digital forensics.
- Kali Linux comes with many **pre-installed cybersecurity tools**.
- Using Kali Linux in a **virtual machine** helps protect the host system and allows users to revert to previous VM states.
- **Metasploit** can be used to identify and exploit vulnerabilities.
- **Burp Suite** is used to test web applications for security weaknesses.
- **John the Ripper** is used to guess passwords.
- **`tcpdump`** is a command-line packet analyzer used to capture network traffic.
- **Wireshark** provides a GUI for analyzing live and captured network traffic.
- **Autopsy** is a forensic tool used to analyze hard drives and smartphones.
- Kali Linux is widely used in security, but it is only one of several Linux distributions used by cybersecurity professionals.