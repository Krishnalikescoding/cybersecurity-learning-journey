# Packet Sniffing: Security, Threats, and Defense

## Overview

Packets contain information about network communication. A packet generally includes:

- **Header:** Contains metadata such as the sender's and receiver's IP addresses, ports, protocol type, and sequence numbers.
- **Body (Payload):** Contains the actual data being transmitted, which may include usernames, passwords, names, dates of birth, personal messages, financial information, and credit card numbers.

**Packet sniffing** is the practice of using software or hardware tools to capture and inspect data packets as they move across a network.

Security analysts can use packet sniffing to:
- Investigate security incidents
- Analyze network traffic
- Troubleshoot network issues
- Identify suspicious activity
- Monitor network communications

However, malicious actors can also use packet sniffing to capture information that was not intended for them.

---

## Malicious Packet Sniffing

A malicious actor may insert themselves into an authorized connection between two devices and inspect the packets traveling between them.

The attacker's goal is often to extract valuable information inside the packets for unauthorized or malicious purposes.

### Tools Used by Attackers
- **Software Applications:** Protocol analyzers, custom scripts, and promiscuous mode capture tools (e.g., Wireshark, tcpdump).
- **Hardware Devices:** Physical network taps, inline drop boxes, or compromised network infrastructure.
- **Packet-Sniffing Frameworks:** Automated tools designed for credential harvesting or session hijacking.

### Sensitive Data Targeted
- Usernames and passwords
- Personal Identifiable Information (PII)
- Financial and banking details
- Credit card numbers
- Private messages and emails

Attackers can also modify packets while they are in transit. For example, an attacker could intercept an online banking transaction and modify the recipient's bank account number to an account controlled by the attacker.

---

## Types of Packet Sniffing

Packet sniffing is broadly categorized into two types:

1. **Passive Packet Sniffing**
2. **Active Packet Sniffing**

### Passive Packet Sniffing

**Passive packet sniffing** is an attack where data packets are observed and read while traveling across a network, without altering the packets in any way.

- The attacker does not modify the packets or inject new data.
- Passive sniffing is particularly effective on unswitched networks using **hubs**, as hubs broadcast network traffic to all connected network interfaces.
- On modern switched networks, passive sniffing can still occur via NIC promiscuous mode, network taps, or port mirroring (SPAN ports).

#### Example
Imagine a postal worker responsible for delivering someone's mail who secretly opens and reads letters before delivering them intact. The postal worker accesses the mail because of their physical access/position, but has no authorization to read its contents. Similarly, a passive packet sniffer observes network traffic without authorization.

---

### Active Packet Sniffing

**Active packet sniffing** is an attack where data packets are actively intercepted and manipulated while traveling across the network.

An active attacker may:
- Modify the contents of packets in transit
- Inject malicious network traffic or protocol responses
- Redirect packets (e.g., via ARP spoofing, DNS poisoning, or MAC flooding)
- Reroute traffic to unintended ports or malicious endpoints
- Alter sensitive values contained within data payloads

#### Example
Imagine an attacker intercepting a letter during delivery, changing its monetary amount or recipient address, and then forwarding it to the recipient. Unlike passive sniffing, the attacker actively tampers with the communication channel.

---

## Passive vs Active Packet Sniffing

| Feature | Passive Packet Sniffing | Active Packet Sniffing |
| :--- | :--- | :--- |
| **Primary Action** | Captures and reads packets in transit | Captures, injects, and manipulates packets |
| **Packet Modification** | No | Yes |
| **Detection Difficulty** | High (stealthy, no added traffic) | Lower (often generates network anomalies) |
| **Common Techniques** | Promiscuous mode, Hub listening, SPAN mirroring | ARP Spoofing, DNS Poisoning, MAC Flooding, MitM |

---

## How to Protect Against Packet Sniffing

### 1. Use a Virtual Private Network (VPN)
A **Virtual Private Network (VPN)** encrypts data before it travels across local networks and the internet, masking payload contents from eavesdroppers.

```text
+--------+      Encrypted Traffic      +------------+      Internet      +-------------+
| Device | --------------------------> | VPN Server | -----------------> | Destination |
+--------+                             +------------+                    +-------------+
```

- If an attacker intercepts encrypted VPN traffic, they only see ciphertext and cannot read the underlying payload without the cryptographic keys.
- VPNs are critical when connecting through untrusted or public network environments.

### 2. Enforce HTTPS and Transport Layer Security (TLS)
Web applications should always enforce HTTPS instead of unencrypted HTTP.

- **HTTP:** Sent in cleartext (unencrypted communication) — fully readable by sniffers.
- **HTTPS:** Uses SSL/TLS encryption to protect communication between browser and server.

When entering credentials, personal information, or financial data on a website, HTTPS protects the transmission against inline network interception.

### 3. Avoid Unprotected Wi-Fi Networks
Unprotected Wi-Fi networks do not enforce encryption for wireless traffic. Risky environments include public Wi-Fi networks at:
- Coffee shops
- Restaurants
- Airports
- Hotels
- Other open public venues

*Note:* Using an encrypted VPN on public Wi-Fi provides an essential security barrier against rogue access points and local packet sniffers.

---

## Packet Sniffing and Security Analysts

Packet sniffing is not inherently malicious; it is a foundational skill and tool in network defense. Security professionals legitimately use packet analyzers (e.g., Wireshark, tcpdump, TShark) to:

- Investigate suspected security incidents and breaches
- Identify anomalous or suspicious network traffic patterns
- Troubleshoot network connectivity and latency issues
- Analyze network protocol behavior and performance
- Identify unauthorized or out-of-policy network communications
- Determine whether sensitive data is being transmitted unencrypted (in cleartext)

---

## Packet Sniffing Overview Architecture

```text
                            Packet Sniffing
                                   |
                   +---------------+---------------+
                   |                               |
             Legitimate Use                  Malicious Use
                   |                               |
           +-------+-------+               +-------+-------+
           |       |       |               |               |
        Incident Traffic Network        Passive         Active
        Analysis Analysis Troubleshooting Sniffing        Sniffing
                                           |               |
                                       Read Only        Read & Modify
```

---

## Key Takeaways

1. **Definition:** Packet sniffing involves capturing and inspecting data packets traveling across a network.
2. **Packet Structure:** Packets consist of headers (routing metadata) and payloads (transmitted data).
3. **Dual Use:** Packet sniffing can be used legitimately for network troubleshooting and defense, or maliciously for data theft and interception.
4. **Passive vs Active:** Passive sniffing observes traffic without alteration; active sniffing manipulates, redirects, or alters packets in transit.
5. **Vulnerabilities:** Legacy hubs and unencrypted networks (HTTP, plain Wi-Fi) make packet sniffing significantly easier.
6. **Defensive Controls:** Implement strong encryption protocols including VPNs, HTTPS/TLS, and avoid unencrypted public wireless networks.
