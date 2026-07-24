# IP Addresses and MAC Addresses

## What is an IP Address?

An **Internet Protocol (IP) address** is a unique logical address assigned to a device on a network.

It identifies the location of a device so data can be sent to the correct destination.

Think of an IP address like a **mailing address** for a device on the Internet.

---

# Types of IP Addresses

There are **two versions** of IP addresses:

- **IPv4 (Internet Protocol Version 4)**
- **IPv6 (Internet Protocol Version 6)**

---

# IPv4

## Definition

**IPv4** is the original and most widely used IP addressing system.

### Format

- Four decimal numbers
- Each number ranges from **0–255**
- Numbers are separated by periods (`.`)

### Example

```text
192.168.1.10
```

### Characteristics

- 32-bit address
- Approximately **4.3 billion** unique addresses
- Limited address space

---

# IPv6

## Definition

**IPv6** is the newer version of IP designed to overcome the address limitations of IPv4.

### Format

- Eight groups of hexadecimal characters
- Groups are separated by colons (`:`)

### Example

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

### Characteristics

- 128-bit address
- Vastly larger address space
- Supports many more Internet-connected devices
- Designed for the future growth of the Internet

---

# IPv4 vs IPv6

| Feature | IPv4 | IPv6 |
|---------|------|-------|
| Address Size | 32-bit | 128-bit |
| Format | Decimal | Hexadecimal |
| Example | 192.168.1.10 | 2001:db8::1 |
| Address Capacity | ~4.3 Billion | Extremely large (3.4 × 10³⁸) |

---

# Public IP Address

## Definition

A **public IP address** is assigned by an **Internet Service Provider (ISP)** and is visible on the Internet.

### Characteristics

- Unique on the Internet
- Identifies your network externally
- Shared by devices on the same local network through the router

---

# Private IP Address

## Definition

A **private IP address** is assigned within a local network and is **not visible on the public Internet**.

### Characteristics

- Used for communication inside a LAN
- Assigned by the router
- Unique only within the local network

### Example

Devices in a home network communicate using private IP addresses, while sharing a single public IP address to access the Internet.

---

# Public vs Private IP

| Public IP | Private IP |
|------------|------------|
| Assigned by ISP | Assigned within the local network |
| Visible on the Internet | Visible only inside the LAN |
| Used for external communication | Used for internal communication |

---

# MAC Address

## Definition

A **Media Access Control (MAC) address** is a unique hardware identifier assigned to a network interface.

Unlike an IP address, a MAC address is tied to the physical network device.

### Characteristics

- Unique for each network interface
- Used within local networks
- Operates at the **Data Link Layer**
- Assigned by the manufacturer

---

# MAC Address Table

A **switch** maintains a **MAC address table** that maps:

- **MAC Address → Switch Port**

### Purpose

- Learns where devices are connected
- Sends packets only to the correct destination port
- Improves network performance and security

Think of the MAC address table as an **address book** that helps the switch deliver data efficiently.

---

# IP Address vs MAC Address

| IP Address | MAC Address |
|------------|-------------|
| Logical address | Physical hardware address |
| Used between networks | Used within a local network |
| Can change | Usually permanent |
| Assigned by ISP/router | Assigned by manufacturer |

---

# Importance for Security Analysts

Understanding IP and MAC addresses helps analysts:

- Identify devices on a network
- Trace network traffic
- Investigate security incidents
- Detect unauthorized devices
- Analyze packet captures and logs

---

# Key Takeaways

- An **IP address** is a unique logical identifier used to locate devices on a network.
- **IPv4** uses **32-bit** decimal addresses, while **IPv6** uses **128-bit** hexadecimal addresses to support a much larger number of devices.
- A **public IP address** is assigned by an **ISP** and is visible on the Internet, whereas a **private IP address** is used only within a local network.
- A **MAC address** is a unique hardware identifier assigned to a network interface and is used for communication within a local network.
- **Switches** use a **MAC address table** to map MAC addresses to ports, ensuring data packets are forwarded to the correct device.
- Security analysts rely on **IP addresses** and **MAC addresses** to identify devices, monitor network activity, and investigate security events.