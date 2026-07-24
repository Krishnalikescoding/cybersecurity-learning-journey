# Network Protocols

## What is a Network Protocol?

A **network protocol** is a set of rules that defines how devices communicate, exchange, and process data over a network.

Protocols specify:

- How data is formatted
- How data is transmitted
- The order of communication
- Error handling
- Security measures

---

# Categories of Network Protocols

Network protocols are grouped into **three categories**:

1. Communication Protocols
2. Management Protocols
3. Security Protocols

---

# 1. Communication Protocols

These protocols control how data is exchanged between devices.

## Transmission Control Protocol (TCP)

### Purpose

Provides **reliable, connection-oriented** communication.

### Features

- Three-way handshake
- Error checking
- Packet retransmission
- Ordered delivery

### Three-Way Handshake

1. **SYN** → Client requests a connection.
2. **SYN-ACK** → Server acknowledges the request.
3. **ACK** → Client confirms, and the connection is established.

### TCP/IP Layer

**Transport Layer**

---

## User Datagram Protocol (UDP)

### Purpose

Provides **fast, connectionless** communication.

### Features

- No handshake
- No guaranteed delivery
- Lower overhead
- Faster than TCP

### Common Uses

- DNS requests
- Video streaming
- Voice over IP (VoIP)
- Online gaming

### TCP/IP Layer

**Transport Layer**

---

## Hypertext Transfer Protocol (HTTP)

### Purpose

Transfers web pages between browsers and web servers.

### Characteristics

- Unencrypted
- Uses **Port 80**
- Being replaced by HTTPS

### TCP/IP Layer

**Application Layer**

---

## Domain Name System (DNS)

### Purpose

Translates **domain names** into **IP addresses**.

### Example

```text
google.com → 142.250.x.x
```

### Characteristics

- Normally uses **UDP Port 53**
- Uses TCP for large responses

### TCP/IP Layer

**Application Layer**

---

# 2. Management Protocols

Management protocols monitor and manage network devices.

---

## Simple Network Management Protocol (SNMP)

### Purpose

Monitors and manages network devices.

### Functions

- Monitor bandwidth
- Change configurations
- Reset passwords
- Collect performance data

### TCP/IP Layer

**Application Layer**

---

## Internet Control Message Protocol (ICMP)

### Purpose

Reports network errors and diagnostics.

### Common Uses

- Ping command
- Connectivity testing
- Error reporting
- Latency troubleshooting

### TCP/IP Layer

**Internet Layer**

---

# 3. Security Protocols

Security protocols protect data while it is transmitted.

---

## Hypertext Transfer Protocol Secure (HTTPS)

### Purpose

Provides secure communication between browsers and web servers.

### Features

- Encrypts web traffic
- Uses **SSL/TLS**
- Protects sensitive information
- Uses **Port 443**

### TCP/IP Layer

**Application Layer**

---

## Secure File Transfer Protocol (SFTP)

### Purpose

Securely transfers files between devices.

### Features

- Uses **SSH**
- Typically uses **TCP Port 22**
- Encrypts file transfers using **AES** and other encryption methods

### Common Uses

- Cloud storage
- Secure file uploads/downloads
- Enterprise file sharing

### TCP/IP Layer

**Application Layer**

---

# Example: Visiting a Website

When you open a secure website, several protocols work together:

1. **DNS** translates the domain name into an IP address.
2. **TCP** establishes a reliable connection using a three-way handshake.
3. **ARP** finds the MAC address of the next device on the local network.
4. **HTTPS** securely transfers the webpage using SSL/TLS encryption.

---

# Common Ports

| Protocol | Port | Purpose |
|----------|-----:|---------|
| HTTP | **80** | Web communication (unencrypted) |
| HTTPS | **443** | Secure web communication |
| DNS | **53** | Domain name resolution |
| SFTP / SSH | **22** | Secure file transfer and remote access |

---

# Protocol Summary

| Protocol | Category | TCP/IP Layer | Purpose |
|----------|----------|--------------|---------|
| TCP | Communication | Transport | Reliable communication |
| UDP | Communication | Transport | Fast, connectionless communication |
| HTTP | Communication | Application | Web communication |
| DNS | Communication | Application | Domain name resolution |
| SNMP | Management | Application | Monitor and manage network devices |
| ICMP | Management | Internet | Error reporting and diagnostics |
| HTTPS | Security | Application | Secure web communication |
| SFTP | Security | Application | Secure file transfer |

---

# Security Considerations

- **HTTP** sends data without encryption and is vulnerable to interception.
- **HTTPS** protects data using **SSL/TLS** encryption.
- **DNS** can be abused by attackers to redirect users to malicious websites (DNS spoofing).
- **SFTP** securely transfers files using **SSH** encryption.
- Encryption protects the **contents** of communications but **does not hide the source or destination IP addresses**.

---

# Key Takeaways

- A **network protocol** defines the rules for communication between devices on a network.
- Protocols are grouped into:
  - **Communication Protocols**: TCP, UDP, HTTP, DNS.
  - **Management Protocols**: SNMP, ICMP.
  - **Security Protocols**: HTTPS, SFTP.
- **TCP** uses a **three-way handshake (SYN → SYN-ACK → ACK)** to establish reliable connections.
- **UDP** is faster but does not guarantee delivery.
- **HTTP (Port 80)** is unencrypted, while **HTTPS (Port 443)** secures web traffic using **SSL/TLS**.
- **DNS (Port 53)** converts domain names into IP addresses, and **SFTP (Port 22)** securely transfers files using **SSH**.
- Understanding these protocols helps cybersecurity analysts detect vulnerabilities, investigate network traffic, and strengthen network security.