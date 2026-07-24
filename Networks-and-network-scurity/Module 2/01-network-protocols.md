# Network Protocols

## What is a Network Protocol?

A **network protocol** is a set of rules that defines how devices communicate and exchange data over a network.

Protocols specify:
- How data is formatted
- How data is transmitted
- The order of communication
- Error handling
- Security measures

---

# Categories of Network Protocols

## 1. Communication Protocols
Protocols that control how data is transmitted between devices.

### Transmission Control Protocol (TCP)
- Reliable, connection-oriented protocol
- Uses a **three-way handshake**:
  1. SYN
  2. SYN-ACK
  3. ACK
- Ensures ordered delivery
- Retransmits lost packets

### User Datagram Protocol (UDP)
- Fast, connectionless protocol
- No handshake
- No guaranteed delivery
- Low overhead
- Commonly used for DNS, streaming, VoIP, and online gaming

### Hypertext Transfer Protocol (HTTP)
- Transfers web pages between browsers and web servers
- Unencrypted communication
- Uses **Port 80**
- Mostly replaced by HTTPS

### Domain Name System (DNS)
- Converts domain names into IP addresses
- Example:
  ```text
  google.com → 142.250.x.x
  ```
- Usually uses **UDP Port 53**
- Switches to TCP for large responses

---

## 2. Management Protocols

### Simple Network Management Protocol (SNMP)
- Monitors and manages network devices
- Tracks bandwidth usage
- Changes configurations
- Resets passwords
- Collects device statistics

### Internet Control Message Protocol (ICMP)
- Reports network errors
- Used for diagnostics
- Powers the **ping** command
- Helps troubleshoot connectivity and latency

---

## 3. Security Protocols

### Hypertext Transfer Protocol Secure (HTTPS)
- Secure version of HTTP
- Encrypts web traffic using **SSL/TLS**
- Protects sensitive information
- Uses **Port 443**

### Secure File Transfer Protocol (SFTP)
- Securely transfers files between devices
- Uses **SSH**
- Typically uses **TCP Port 22**
- Encrypts data using **AES** and other encryption methods
- Commonly used with cloud storage

---

# Website Communication Example

When you visit a secure website:

1. **DNS** translates the domain name into an IP address.
2. **TCP** establishes a reliable connection using a three-way handshake.
3. **ARP** finds the MAC address of the next device on the local network.
4. **HTTPS** securely transfers the webpage using SSL/TLS encryption.

---

# Common Protocols Summary

| Protocol | Category | Layer | Port | Purpose |
|----------|----------|-------|------|---------|
| **TCP** | Communication | Transport | - | Reliable communication |
| **UDP** | Communication | Transport | - | Fast, connectionless communication |
| **HTTP** | Communication | Application | 80 | Web communication |
| **HTTPS** | Security | Application | 443 | Secure web communication |
| **DNS** | Communication | Application | 53 | Domain name resolution |
| **SNMP** | Management | Application | 161/162 | Network monitoring and management |
| **ICMP** | Management | Internet | - | Error reporting and diagnostics |
| **SFTP** | Security | Application | 22 | Secure file transfer |
| **ARP** | Communication | Network Access | - | Maps IP addresses to MAC addresses |

---

# Security Considerations

- **HTTP** is unencrypted and vulnerable to interception.
- **HTTPS** protects data using **SSL/TLS** encryption.
- **DNS** can be exploited through attacks like **DNS spoofing** to redirect users to malicious websites.
- **SFTP** securely transfers files using **SSH** encryption.
- Encryption protects the **contents** of network traffic but **does not hide the source or destination IP addresses**.

---

# Key Takeaways

- A **network protocol** defines the rules for communication between devices.
- Protocols are divided into **Communication**, **Management**, and **Security** categories.
- **TCP** provides reliable communication through a **three-way handshake**, while **UDP** prioritizes speed over reliability.
- **HTTP (Port 80)** is unencrypted, whereas **HTTPS (Port 443)** secures web traffic using **SSL/TLS**.
- **DNS (Port 53)** resolves domain names into IP addresses, and **SFTP (Port 22)** securely transfers files using **SSH**.
- Security analysts use protocol knowledge to analyze network traffic, identify vulnerabilities, and investigate security incidents.