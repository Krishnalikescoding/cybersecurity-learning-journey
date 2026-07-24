# Common Network Protocols

## Network Address Translation (NAT)

### Definition
**Network Address Translation (NAT)** allows multiple devices with **private IP addresses** to share a single **public IP address** when accessing the Internet.

### How NAT Works
1. A device sends data using its **private IP address**.
2. The router replaces the private IP with its **public IP**.
3. Responses from the Internet return to the router.
4. The router translates the public IP back to the correct private IP.

### Benefits
- Conserves public IP addresses
- Hides internal network addresses
- Improves security by masking private devices

---

## Private vs Public IP Addresses

| Feature | Private IP | Public IP |
|---------|------------|-----------|
| Assigned By | Router | ISP / IANA |
| Visibility | Local network only | Internet-wide |
| Cost | Free | Usually leased from ISP |
| Purpose | Internal communication | Internet communication |

### Private IP Address Ranges

- **10.0.0.0 – 10.255.255.255**
- **172.16.0.0 – 172.31.255.255**
- **192.168.0.0 – 192.168.255.255**

---

## Dynamic Host Configuration Protocol (DHCP)

### Purpose
Automatically assigns network settings to devices.

### Functions
- Assigns IP addresses
- Assigns DNS server addresses
- Assigns default gateway

### Ports

| Server | UDP 67 |
|--------|--------|
| Client | UDP 68 |

---

## Address Resolution Protocol (ARP)

### Purpose
Maps an **IP address** to a **MAC address** on a local network.

### Features
- Works within a LAN
- Stores mappings in an **ARP cache**
- No port number (Network Access Layer protocol)

---

## Telnet

### Purpose
Provides remote access to another computer.

### Characteristics
- Command-line interface
- Sends data in **plain text**
- Not secure
- Largely replaced by SSH

**Port:** TCP **23**

---

## Secure Shell (SSH)

### Purpose
Secure remote login and administration.

### Features
- Encrypted communication
- Secure authentication
- Replacement for Telnet

**Port:** TCP **22**

---

## Post Office Protocol (POP3)

### Purpose
Retrieves incoming email from a mail server.

### Characteristics
- Downloads emails to the local device
- Emails may be removed from the server
- Limited synchronization across multiple devices

**Ports**

- TCP/UDP **110** (Unencrypted)
- TCP/UDP **995** (SSL/TLS Encrypted)

---

## Internet Message Access Protocol (IMAP)

### Purpose
Accesses incoming email while keeping messages on the mail server.

### Features
- Synchronizes email across multiple devices
- Allows reading emails before full download

**Ports**

- TCP **143** (Unencrypted)
- TCP **993** (TLS Encrypted)

---

## Simple Mail Transfer Protocol (SMTP)

### Purpose
Sends and routes outgoing email.

### Features
- Delivers email between mail servers
- Uses DNS to locate recipient servers
- Helps regulate email transmission and reduce spam

**Ports**

- TCP/UDP **25** (Unencrypted)
- TCP/UDP **587** (TLS Encrypted / SMTPS)

---

# Protocol Summary

| Protocol | Layer | Port | Purpose |
|----------|-------|------|---------|
| **NAT** | Internet / Transport | - | Translates private IPs to a public IP |
| **DHCP** | Application | UDP 67 (Server), UDP 68 (Client) | Automatically assigns IP configuration |
| **ARP** | Network Access | - | Resolves IP addresses to MAC addresses |
| **Telnet** | Application | TCP 23 | Remote access (unencrypted) |
| **SSH** | Application | TCP 22 | Secure remote access |
| **POP3** | Application | 110 / 995 | Downloads incoming email |
| **IMAP** | Application | 143 / 993 | Synchronizes incoming email |
| **SMTP** | Application | 25 / 587 | Sends outgoing email |

---

# POP3 vs IMAP

| POP3 | IMAP |
|------|------|
| Downloads email to the device | Keeps email on the server |
| Limited multi-device support | Full synchronization across devices |
| Better for single-device access | Better for multiple-device access |

---

# Telnet vs SSH

| Telnet | SSH |
|--------|-----|
| Unencrypted | Encrypted |
| TCP Port 23 | TCP Port 22 |
| Insecure | Secure replacement for Telnet |

---

# Why Port Numbers Matter

Port numbers tell devices which application or service should receive incoming data.

Security analysts use port numbers to:
- Monitor network traffic
- Configure firewall rules
- Detect unauthorized services
- Identify suspicious activity during investigations

---

# Key Takeaways

- **NAT** enables multiple devices with private IP addresses to share a single public IP address.
- **DHCP** automatically assigns IP addresses, DNS servers, and default gateways using **UDP Ports 67 and 68**.
- **ARP** translates IP addresses into MAC addresses on a local network and stores mappings in an ARP cache.
- **Telnet (TCP 23)** provides remote access but is insecure because it transmits data in plain text, while **SSH (TCP 22)** provides encrypted and secure remote access.
- **POP3 (Ports 110/995)** downloads emails to a device, whereas **IMAP (Ports 143/993)** keeps emails on the server for synchronization across multiple devices.
- **SMTP (Ports 25/587)** is responsible for sending outgoing emails.
- Understanding common protocols and their port numbers is essential for configuring firewalls, analyzing network traffic, and investigating security incidents.