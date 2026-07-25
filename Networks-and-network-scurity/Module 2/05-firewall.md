# Firewalls

## What is a Firewall?

A **firewall** is a network security device that **monitors incoming and outgoing network traffic** and **allows or blocks traffic** based on predefined security rules.

### Functions
- Monitors network traffic
- Allows legitimate traffic
- Blocks unauthorized or malicious traffic
- Enforces an organization's security policy

---

# Port Filtering

Firewalls can use **port filtering** to control which services are allowed on a network.

### Example

| Port | Service |
|------|---------|
| **443** | HTTPS |
| **25** | SMTP (Email) |

Any traffic on ports that are not explicitly allowed can be blocked.

---

# Types of Firewalls

## 1. Hardware Firewall

### Overview
- Physical network device
- Inspects packets before they enter the network
- Protects the entire network

### Advantages
- Strong network-wide protection
- Dedicated hardware
- Does not consume computer resources

### Disadvantages
- Higher cost
- Requires separate hardware

---

## 2. Software Firewall

### Overview
- Software installed on a computer or server
- Monitors traffic to and from the host device

### Advantages
- Lower cost
- Easy to install and update
- No additional hardware required

### Disadvantages
- Uses system resources
- Protects only the device (or server) where it is installed

---

## 3. Cloud-Based Firewall (Firewall as a Service - FaaS)

### Overview
- Firewall hosted by a **Cloud Service Provider (CSP)**
- Managed through a cloud interface

### Advantages
- Protects cloud and on-premises resources
- Easy to manage remotely
- Automatically scalable
- No physical hardware required

---

# Firewall Types by Operation

## Stateless Firewall

### Characteristics
- Uses predefined rules only
- Does **not** remember previous connections
- Examines each packet independently

### Advantages
- Fast
- Simple
- Low resource usage

### Disadvantages
- Cannot detect suspicious traffic patterns
- Less secure than stateful firewalls

---

## Stateful Firewall

### Characteristics
- Tracks active network connections
- Remembers previous packets in a session
- Analyzes traffic behavior

### Advantages
- Better threat detection
- More accurate filtering
- Higher security

### Disadvantages
- Uses more memory and processing power

---

## Next-Generation Firewall (NGFW)

### Overview
An **NGFW** combines stateful inspection with advanced security features.

### Features
- Stateful packet inspection
- Deep Packet Inspection (DPI)
- Intrusion Prevention System (IPS)
- Application awareness
- Threat intelligence integration
- Protection against emerging cyber threats

---

# Stateful vs Stateless Firewall

| Stateful Firewall | Stateless Firewall |
|-------------------|--------------------|
| Tracks active sessions | Examines each packet independently |
| Detects suspicious behavior | Uses only predefined rules |
| More secure | Less secure |
| Higher resource usage | Lower resource usage |

---

# Hardware vs Software Firewall

| Hardware Firewall | Software Firewall |
|-------------------|-------------------|
| Physical device | Software application |
| Protects the entire network | Protects a single device or server |
| Uses dedicated hardware | Uses system resources |
| Higher cost | Lower cost |

---

# Firewall Summary

| Firewall Type | Purpose |
|--------------|---------|
| **Hardware Firewall** | Protects the entire network using dedicated hardware |
| **Software Firewall** | Protects individual computers or servers |
| **Cloud Firewall (FaaS)** | Protects cloud and on-premises environments |
| **Stateless Firewall** | Filters packets using predefined rules only |
| **Stateful Firewall** | Tracks connections and filters based on session state |
| **Next-Generation Firewall (NGFW)** | Provides advanced protection with DPI, IPS, and threat intelligence |

---

# Importance for Security Analysts

Security analysts use firewalls to:

- Monitor network traffic
- Block unauthorized access
- Enforce security policies
- Reduce attack surfaces
- Detect and prevent network-based threats

---

# Key Takeaways

- A **firewall** monitors and controls network traffic based on predefined security rules.
- **Port filtering** allows or blocks traffic based on port numbers, such as **HTTPS (443)** and **SMTP (25)**.
- **Hardware firewalls** protect entire networks, while **software firewalls** protect individual devices or servers.
- **Cloud-based firewalls (FaaS)** secure cloud and on-premises environments through cloud-hosted services.
- **Stateless firewalls** filter packets using predefined rules, whereas **stateful firewalls** track active connections and provide stronger security.
- **Next-Generation Firewalls (NGFWs)** add advanced features such as **Deep Packet Inspection (DPI)**, **Intrusion Prevention Systems (IPS)**, and **threat intelligence integration** for enhanced protection.