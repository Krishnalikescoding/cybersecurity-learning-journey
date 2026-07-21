# Network Architecture and Devices

## What is Network Architecture?

**Network architecture** (or **network design**) is the structure and layout of a network, showing how devices are connected and communicate.

Understanding network architecture helps security analysts identify vulnerabilities, monitor traffic, and secure organizational networks.

---

# Network Devices

**Network devices** connect, manage, and control communication between devices on a network.

Devices communicate by sending **data packets**, which contain:

- Source address
- Destination address
- Data payload

### ![Network Devices](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/s-oBYPbLT42rx92K21cvxQ_611ef444b75147a5a6e61d82c34b0df1_9i07czTUt71fHdJt2WJV-5cS3YvI7Y1YQdOBF4c19c2wYkhrIu_6f5gYEgtzAKr8DArrVLx6QY6AQNHpMTmD410f6kyDVYNdP1x36o6lrmsv_CRG8iTBfcIZz4FA-g01ceMoYuXTJjCbvwf38YBSWVwB?expiry=1784713625589&hmac=HYt5Q7Ic3hfqhovPry87h_YRQoYNU0loW5vMyOyqYNU)

> **Note**: In this diagram, a router connects to the internet through a modem, which is provided by your internet service provider (ISP). The firewall is a security device that monitors incoming and outgoing traffic on your network. The router then directs traffic to the devices on your home network, which can include computers, laptops, smartphones, tablets, printers, and other devices. You can imagine here that the server is a file server. All devices on this network can access the files in this server. This diagram also includes a switch which is an optional device that can be used to connect more devices to your network by providing additional ports and Ethernet connections. Additionally, there are 2 routers connected to the switch here for load balancing purposes which will improve the performance of the network. 

---

# Common Network Devices

## 1. End Devices (Clients)

Examples:

- Desktop computers
- Laptops
- Smartphones
- Tablets
- IoT devices

### Characteristics

- Have a unique **MAC address**
- Have an **IP address**
- Use a **Network Interface Card (NIC)** to send and receive data
- Connect via Ethernet or Wi-Fi

---

## 2. Firewall

### Definition

A **firewall** is a network security device that monitors and filters incoming and outgoing network traffic based on security rules.

### Functions

- Allows trusted traffic
- Blocks unauthorized traffic
- Protects internal networks from external threats
- Acts as the first line of defense

### Location

Typically placed **between the internal network and the Internet**.

---

## 3. Server

### Definition

A **server** provides services, resources, or data to other devices (clients) on a network.

### Common Server Types

- File Server
- Web Server
- Mail Server
- DNS Server
- Database Server

### ![Server](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/yEzpFYBkSWChuqHQuw5-SA_47876296b9c140229777d37bc916bff1_DVEYhkRb2cM57vspz3iQIbbBaOfDTWTukQLteY2SDv_MAofv-SbuGazdECwDkbJneVXdDvAW6-CuMSMbYLZJVdkUm5b9k0YJd7m9NVDbEZzLgBhO7_0eq30pRJkkUl-QHu97fSitfr2Lva1bPsTd431k?expiry=1784713625589&hmac=PvTeJDd7PMebKlN89_kaqQ8DN75V4EOAhBpR3lJkiDk)

---

# Client-Server Model

### Definition

A networking model where:

- **Client** requests services or data.
- **Server** processes the request and responds.

### Examples

- Opening a website
- Downloading files
- Sending email
- Looking up a domain name

---

## 4. Hub

### Definition

A **hub** connects multiple devices and broadcasts every incoming packet to all connected devices.

### Characteristics

- No intelligence
- Broadcasts all traffic
- Low security
- Low efficiency

### Security Issue

Because all traffic is broadcast, hubs are vulnerable to **eavesdropping**.

---

## 5. Switch

### Definition

A **switch** forwards data only to the intended device using **MAC addresses**.

### Characteristics

- Intelligent device
- Maintains a **MAC address table**
- Improves performance
- Improves security

### Operates At

**Data Link Layer** (TCP/IP model)

---

## Hub vs Switch

| Feature | Hub | Switch |
|---------|-----|--------|
| Traffic | Broadcasts to all devices | Sends only to destination |
| Security | Lower | Higher |
| Performance | Lower | Higher |
| Intelligence | None | Uses MAC address table |

---

## 6. Router

### Definition

A **router** connects different networks and forwards packets using **IP addresses**.

### Functions

- Connect LANs and WANs
- Route traffic between networks
- Choose the best path for data
- Often includes firewall features

### Operates At

**Network Layer** (TCP/IP model)

---

## 7. Modem

### Definition

A **modem (Modulator-Demodulator)** connects a local network to an **Internet Service Provider (ISP)**.

### Functions

- Converts ISP signals into a usable digital format
- Provides Internet connectivity
- Usually connects directly to a router

### ![Modem](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6gFK3i1wRCyopAF5k1j0HQ_c8d352d18c8e4474941916da8fed74f1_GGmNcX8TiMojwILA_9er2cddFq573EvzkLIBJWj8Bpx5asAiGYLNe-aPI6ZluB_5ub9YgBHeHF5xMvQ52k5VknA8RtTVa033ZN5juPaHECodnA1W0ZhlbBJmWbgXrpomHeRypDrDT36bR8LFLRUN4Kxd?expiry=1784713625589&hmac=EHluwSDzlPabSKinRyNNrmKsW7Sh-6pDK5HUmaCBPk0)

> **Note:** Large enterprise networks often use high-speed broadband technologies instead of traditional modems.

---

## 8. Wireless Access Point (WAP)

### Definition

A **Wireless Access Point (WAP)** creates a wireless network by transmitting and receiving data over radio waves.

### Functions

- Provides Wi-Fi access
- Connects wireless devices
- Sends wireless traffic to routers and switches

### Uses

- Wi-Fi standards (IEEE 802.11)

### ![WAP](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/8vl7L2RlSvGkk3LvXaMeKg_6a15bfb726f541d38671388c13b052f1_XU9XxDWBAwQu9gCYs4ZbRB4Do3xxXScibznS8UvafzSyYJoW9JpmUjL8VNbhYvmNmvmgP9x6AwGltYH7SnkcuyJjEGQNsFLvyeyun2-GdCqjHnXbExJgx67JoFd9KMohmA2xv462hh3O2xkvqhl1kX-z?expiry=1784713625589&hmac=nOX8ZNzSmvkjrR03ol3X52f8bYK6MA8IP4WUQ2Hw2R8)
---

# Data Flow Example

When visiting a website:

1. Client device sends a request.
2. Request reaches the switch (or WAP if wireless).
3. Switch forwards it to the router.
4. Router sends it through the modem/ISP to the Internet.
5. The web server responds.
6. Data returns through the router and switch to the client.

---

# Network Diagram

### Definition

A **network diagram** is a visual map showing:

- Network devices
- Connections
- Data paths
- Overall network architecture

### Why Security Analysts Use Network Diagrams

- Understand network layout
- Identify critical assets
- Locate potential vulnerabilities
- Plan security controls
- Troubleshoot connectivity issues
- Improve incident response

### ![Netwoork Structure](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/v540rACBSUepbsQcE4s3PQ_3b799a13034d42938c980d7c473725f1_2SOA6jNuKUowAynp64ms-agTTUcxt1xas4SFTTAcKU-JfqJHyG2vzmM7qgqMh4J_Euwmri_t3G_CUXydGZRlmV4EZABYDusKE7pBnNWi5gZ_fUbiAetmRiQWL3cMO2iRWDtjtAPMazNxnmT-i5pWmPAe?expiry=1784713625589&hmac=IsCLQ2lN2UAr0JZiR2qF-dmvASDfiUU4Jkk98cO1nmU)
---

# Summary of Network Devices

| Device | Primary Function |
|---------|------------------|
| Client | Requests data and services |
| Server | Provides data and services |
| Firewall | Filters network traffic |
| Hub | Broadcasts data to all devices |
| Switch | Forwards data using MAC addresses |
| Router | Connects networks using IP addresses |
| Modem | Connects the network to an ISP |
| Wireless Access Point | Provides Wi-Fi connectivity |

---

# Key Takeaways

- **Network architecture** describes how network devices are connected and communicate.
- Devices exchange information using **data packets** that contain source and destination information.
- **Clients** request services, while **servers** provide them in the **client-server model**.
- A **firewall** monitors and filters traffic to protect internal networks.
- A **hub** broadcasts traffic to all devices, whereas a **switch** forwards traffic only to the intended destination using a **MAC address table**.
- A **router** connects different networks and routes packets based on **IP addresses**.
- A **modem** connects a network to an **Internet Service Provider (ISP)**, while a **Wireless Access Point (WAP)** enables devices to connect via **Wi-Fi**.
- **Network diagrams** help security analysts visualize network architecture, identify vulnerabilities, and design effective security strategies.