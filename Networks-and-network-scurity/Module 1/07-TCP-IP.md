# TCP/IP Model Basics

## What is the TCP/IP Model?

**TCP/IP (Transmission Control Protocol/Internet Protocol)** is the standard suite of communication protocols used for transmitting data across networks, including the Internet.

It defines **how devices communicate, organize, send, route, and receive data packets**.

---

# TCP (Transmission Control Protocol)

## Definition

**Transmission Control Protocol (TCP)** establishes a reliable connection between two devices and ensures data is delivered accurately and in the correct order.

### Functions

- Establishes a connection between devices
- Breaks data into packets
- Ensures packets arrive correctly
- Reorders packets if necessary
- Retransmits lost packets
- Provides reliable communication

### Purpose

TCP guarantees that data reaches its intended destination without loss or corruption.

---

# IP (Internet Protocol)

## Definition

**Internet Protocol (IP)** is responsible for addressing and routing data packets across networks.

### Functions

- Assigns source and destination IP addresses
- Routes packets between networks
- Determines the best path for packet delivery

### IP Address

An **IP address** is a unique logical address assigned to a device on a network.

It identifies where data should be sent.

---

# TCP vs IP

| TCP | IP |
|-----|----|
| Establishes reliable communication | Routes data between networks |
| Ensures delivery and correct order | Provides addressing |
| Retransmits lost packets | Determines packet path |

---

# Network Ports

## Definition

A **port** is a software-based communication endpoint within an operating system.

Ports allow multiple network services to run simultaneously on the same device.

Think of an IP address as a building address and a **port number** as the apartment number that tells data exactly which service or application should receive it.

---

# Purpose of Ports

Ports help computers:

- Organize network traffic
- Identify applications
- Prioritize communication
- Send data to the correct service

---

# Common Port Numbers

| Port | Protocol / Service | Purpose |
|------|--------------------|---------|
| **20** | FTP (Data) | Large file transfers |
| **25** | SMTP | Sending email |
| **443** | HTTPS | Secure web communication |

> **Note:** HTTPS uses encryption (TLS/SSL) to protect data transmitted over the web.

---

# How TCP/IP Works

1. An application creates data.
2. **TCP** divides the data into packets and establishes a reliable connection.
3. Each packet receives **IP addressing information**.
4. Packets are assigned the appropriate **port number** based on the service.
5. Routers forward the packets across the network.
6. The receiving device uses the **IP address** to identify the destination and the **port number** to deliver the data to the correct application.
7. **TCP** reassembles the packets into the original data.

---

# Components of Network Communication

| Component | Function |
|-----------|----------|
| TCP | Reliable data transmission |
| IP | Addressing and routing |
| IP Address | Identifies a device on the network |
| Port | Identifies the specific application or service |
| Data Packet | Unit of data transmitted across the network |

---

# Key Takeaways

- **TCP/IP** is the standard communication model used for data transmission across networks and the Internet.
- **TCP (Transmission Control Protocol)** establishes reliable connections, divides data into packets, ensures packets arrive correctly, and retransmits lost packets if necessary.
- **IP (Internet Protocol)** provides logical addressing and routes packets between networks using **IP addresses**.
- A **port** is a software-based communication endpoint that directs incoming data to the correct application or service.
- Common ports include:
  - **20** – FTP data transfer
  - **25** – SMTP (email)
  - **443** – HTTPS (secure web traffic)
- Together, **TCP**, **IP**, and **port numbers** ensure that data reaches the correct device and the correct application reliably and efficiently.