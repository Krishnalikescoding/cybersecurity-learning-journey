# Network Security Tools & Protocols (Summary)

## Network Protocols

A **network protocol** is a set of rules that defines how devices communicate and transfer data across a network.

### Categories of Network Protocols

| Category | Purpose | Examples |
|----------|---------|----------|
| **Communication Protocols** | Establish and manage data communication | TCP, UDP, HTTP, SMTP, DNS, ARP |
| **Management Protocols** | Monitor and troubleshoot networks | ICMP |
| **Security Protocols** | Protect data in transit through encryption | SSL/TLS, IPSec |

---

# Common Network Protocols

| Protocol | Purpose |
|----------|---------|
| **TCP** | Reliable, connection-oriented communication |
| **UDP** | Fast, connectionless communication |
| **HTTP** | Transfers web pages between browsers and web servers |
| **SMTP** | Sends outgoing email |
| **DNS** | Translates domain names into IP addresses |
| **ARP** | Maps IP addresses to MAC addresses on a local network |
| **ICMP** | Reports network errors and supports diagnostics (e.g., `ping`) |
| **SSL/TLS** | Encrypts data transmitted over the network |
| **IPSec** | Secures IP communications using encryption and authentication |

---

# Wi-Fi Security Protocols

Wi-Fi security has improved over time to provide stronger protection for wireless networks.

| Protocol | Status | Features |
|----------|--------|----------|
| **WEP** | Obsolete | Weak encryption, easily cracked |
| **WPA** | Legacy | Introduced TKIP and improved authentication |
| **WPA2** | Widely Used | Uses **AES** encryption and **CCMP** |
| **WPA3** | Most Secure | Uses **AES**, **SAE**, and stronger authentication |

### WPA2/WPA3 Modes

| Mode | Best For |
|------|----------|
| **Personal** | Home networks |
| **Enterprise** | Business and organizational networks |

---

# Firewalls

## What is a Firewall?

A **firewall** monitors and filters incoming and outgoing network traffic according to predefined security rules.

---

## Firewall Types

### Stateless Firewall
- Uses predefined filtering rules
- Does not track active connections
- Faster but less secure

### Stateful Firewall
- Tracks active network sessions
- Automatically allows return traffic
- More secure than stateless firewalls

### Next-Generation Firewall (NGFW)

An **NGFW** extends stateful firewall capabilities with advanced security features:

- Deep Packet Inspection (DPI)
- Intrusion Prevention System (IPS)
- Application-aware filtering
- Malware sandboxing
- Network antivirus
- URL filtering
- DNS filtering

Unlike traditional firewalls, NGFWs can filter traffic based on **applications**, not just **IP addresses and port numbers**.

---

# Proxy Servers

## What is a Proxy Server?

A **proxy server** acts as an intermediary between clients and external servers.

### Functions

- Uses **Network Address Translation (NAT)**
- Hides internal IP addresses
- Filters web traffic
- Blocks malicious websites
- Improves security

### Types

| Proxy | Purpose |
|--------|---------|
| **Forward Proxy** | Handles requests from internal users to the Internet |
| **Reverse Proxy** | Handles incoming requests from external users to internal servers |

---

# Virtual Private Network (VPN)

## What is a VPN?

A **Virtual Private Network (VPN)** encrypts data in transit and hides a user's public IP address.

### Features

- Encrypts network traffic
- Conceals user identity
- Protects communications over public networks
- Uses **encapsulation** to securely transmit data

### Benefits

- Improves privacy
- Secures remote access
- Protects sensitive information
- Masks physical location

---

# Software-Defined Wide Area Network (SD-WAN)

## Definition

A **Software-Defined Wide Area Network (SD-WAN)** is a virtual WAN service that securely connects users, branch offices, and applications across multiple geographic locations.

### Benefits

- Secure connectivity over long distances
- Centralized network management
- Better performance
- Often combined with VPNs for secure enterprise networking

---

# Security Tools Summary

| Tool | Purpose |
|------|---------|
| **Firewall** | Filters network traffic based on security rules |
| **NGFW** | Advanced firewall with DPI, IPS, application awareness, and threat protection |
| **Proxy Server** | Filters traffic and hides internal network addresses |
| **VPN** | Encrypts traffic and hides public IP addresses |
| **SD-WAN** | Securely connects multiple sites over wide geographic areas |

---

# Key Takeaways

- **Network protocols** fall into three categories: **Communication**, **Management**, and **Security**.
- Common protocols include **TCP, UDP, HTTP, SMTP, DNS, ARP, ICMP, SSL/TLS, and IPSec**.
- **WPA3** is the most secure Wi-Fi protocol, while **WPA2** remains widely deployed. **Enterprise mode** is preferred for business environments.
- **Firewalls** inspect and filter network traffic, with **NGFWs** adding features such as **Deep Packet Inspection (DPI)**, **Intrusion Prevention Systems (IPS)**, application awareness, malware sandboxing, and URL/DNS filtering.
- **Proxy servers** use **NAT** to hide internal IP addresses and filter web traffic. **Forward proxies** protect users, while **reverse proxies** protect servers.
- **VPNs** encrypt network traffic, hide public IP addresses, and use **encapsulation** to protect data across public networks.
- **SD-WAN** enables organizations to securely connect users and applications across multiple locations and is commonly used together with VPN technology.