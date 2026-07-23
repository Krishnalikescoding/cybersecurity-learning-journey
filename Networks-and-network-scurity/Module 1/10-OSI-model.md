# OSI Model

## What is the OSI Model?

The **OSI (Open Systems Interconnection) Model** is a **7-layer conceptual framework** that explains how data is transmitted between devices over a network.

It helps network engineers and security analysts:

- Understand network communication
- Troubleshoot network problems
- Identify security threats
- Describe where issues occur

![OSI model](../../src/image.png)

---

# TCP/IP vs OSI Model

| TCP/IP Model | OSI Model |
|--------------|-----------|
| 4 Layers | 7 Layers |
| Simpler, practical model | More detailed reference model |
| Used for Internet communication | Used for learning and troubleshooting |

### Layer Mapping

| TCP/IP | OSI Equivalent |
|---------|----------------|
| Application | Application + Presentation + Session |
| Transport | Transport |
| Internet | Network |
| Network Access | Data Link + Physical |

---

# Layer 7: Application Layer

## Purpose

Provides network services directly to end-user applications.

### Responsibilities

- User interaction
- Access to network services
- Sending application requests

### Common Protocols

- HTTP
- HTTPS
- SMTP
- DNS
- FTP

### Examples

- Browsing websites
- Sending emails
- Looking up domain names

---

# Layer 6: Presentation Layer

## Purpose

Formats data so both devices can understand it.

### Responsibilities

- Data translation
- Encryption
- Decryption
- Compression
- Character encoding

### Example

- **SSL/TLS** encrypts web traffic for HTTPS.

---

# Layer 5: Session Layer

## Purpose

Establishes, manages, and terminates communication sessions between devices.

### Responsibilities

- Session establishment
- Authentication
- Reconnection
- Session checkpoints
- Session termination

### Benefit

If communication is interrupted, checkpoints allow the transfer to resume from the last saved point.

---

# Layer 4: Transport Layer

## Purpose

Ensures reliable data delivery between devices.

### Responsibilities

- End-to-end communication
- Segmentation of data
- Flow control
- Error checking
- Reassembly of data

### Protocols

- TCP
- UDP

---

# Layer 3: Network Layer

## Purpose

Routes data packets between different networks.

### Responsibilities

- Logical addressing
- Packet routing
- Path selection
- Packet forwarding

### Main Protocol

- Internet Protocol (**IP**)

### Device

- Router

---

# Layer 2: Data Link Layer

## Purpose

Transfers data within the same local network.

### Responsibilities

- Frame transmission
- MAC addressing
- Error detection
- Local network communication

### Devices

- Switches
- Network Interface Cards (NICs)

### Common Protocols

- NCP
- HDLC
- SDLC

---

# Layer 1: Physical Layer

## Purpose

Transmits raw bits across the physical network.

### Responsibilities

- Electrical and optical signaling
- Physical connections
- Bit transmission

### Devices

- Cables
- Hubs
- Modems
- Connectors

Data is transmitted as streams of **0s and 1s** across the physical medium.

---

# OSI Layer Summary

| Layer | Name | Main Function | Examples |
|------|---------|----------------|----------|
| 7 | Application | User-facing network services | HTTP, HTTPS, SMTP, DNS |
| 6 | Presentation | Translation, encryption, compression | SSL/TLS |
| 5 | Session | Manages communication sessions | Authentication, checkpoints |
| 4 | Transport | Reliable delivery and segmentation | TCP, UDP |
| 3 | Network | Routing and logical addressing | IP, Routers |
| 2 | Data Link | Local communication using MAC addresses | Switches, NICs |
| 1 | Physical | Physical transmission of bits | Cables, Hubs, Modems |

---

# Data Flow Through the OSI Model

### Sending Data

7 → Application  
6 → Presentation  
5 → Session  
4 → Transport  
3 → Network  
2 → Data Link  
1 → Physical

### Receiving Data

1 → Physical  
2 → Data Link  
3 → Network  
4 → Transport  
5 → Session  
6 → Presentation  
7 → Application

---

# Importance for Security Analysts

Understanding the OSI model helps analysts:

- Identify where attacks occur
- Troubleshoot connectivity issues
- Analyze network traffic
- Apply security controls at the correct layer
- Communicate technical issues effectively

---

# Key Takeaways

- The **OSI model** is a **7-layer framework** used to explain how data moves across a network.
- The layers are:
  1. **Application** – User-facing network services (HTTP, HTTPS, SMTP, DNS).
  2. **Presentation** – Data translation, encryption, decryption, and compression.
  3. **Session** – Establishes, manages, and terminates communication sessions.
  4. **Transport** – Provides reliable data delivery using **TCP** or fast, connectionless communication using **UDP**.
  5. **Network** – Routes packets between networks using **IP** addresses.
  6. **Data Link** – Handles communication within a local network using **MAC addresses** and switches.
  7. **Physical** – Transmits raw bits over physical media such as cables and hubs.
- The **TCP/IP model** is a simplified **4-layer model** used in real-world networking, while the **OSI model** provides a more detailed conceptual view for learning, troubleshooting, and security analysis.