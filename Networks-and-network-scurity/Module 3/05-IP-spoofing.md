# IP Spoofing: Concepts, Attacks, and Defenses

## Overview

**IP spoofing** is a network attack performed when an attacker alters the source IP address of a data packet to impersonate an authorized system and gain unauthorized access to a network.

In this type of attack, the hacker pretends to be a trusted entity to:
- Communicate over the network with the target computer.
- Bypass firewall rules that restrict external or untrusted traffic.

---

## Common IP Spoofing Attacks

### 1. On-Path Attack
An **on-path attack** (historically referred to as Man-in-the-Middle) occurs when a malicious actor places themselves in the middle of an authorized connection to intercept or alter data in transit.

- **How it works:**
  1. The attacker accesses the network and positions themselves between two communicating devices (e.g., a web browser and a web server).
  2. They sniff packet information to capture the IP and MAC addresses of the connected devices.
  3. Using this stolen information, the attacker impersonates either endpoint to hijack or tamper with the session.

---

### 2. Replay Attack
A **replay attack** is a network attack where a malicious actor intercepts a legitimate data packet in transit and delays or retransmits it at a later time.

- **Impact:**
  - **Delayed Packets:** Causes connection latency or desynchronization issues between target systems.
  - **Repeated Transmissions:** Re-sending an authorized user's authentic transmission at a later time allows the attacker to impersonate that user without knowing their credentials.

---

### 3. Smurf Attack
A **Smurf attack** is a hybrid threat that combines a Distributed Denial of Service (DDoS) attack with IP spoofing.

- **How it works:**
  1. The attacker sniffs an authorized user's target IP address.
  2. The attacker crafts broadcast ICMP (ping) requests with the source address spoofed as the victim's IP.
  3. The network nodes respond to the victim's IP, flooding it with traffic.
  4. This massive influx of packets overwhelms the target system, potentially bringing down a server or the entire network.

---

## How to Protect Against IP Spoofing

### 1. Implement Strong Encryption
Data transfers across the network should always be encrypted (e.g., via TLS/HTTPS, IPsec) so that intercepted payloads cannot be read, altered, or replayed by malicious actors.

### 2. Configure Firewalls (Ingress & Egress Filtering)
Firewalls can be configured to detect and block spoofed packets:

- **Concept:** IP spoofing attempts to make external packets look like internal traffic by copying the target network's private IP space.
- **Rule Configuration (Ingress Filtering):** Set up a firewall rule to **reject all incoming traffic from the internet** if its source IP address matches the private/local network address range. Since internal devices reside on the local subnet, any packet arriving from an external interface carrying a local IP address is spoofed and should be dropped immediately.

---

## Passive vs. Active Spoofing Context

| Attack Type | Primary Action | Objective | Primary Defense |
| :--- | :--- | :--- | :--- |
| **On-Path** | Intercepts & manipulates packets in transit | Session hijacking & eavesdropping | Encryption (TLS/IPsec), Mutual Auth |
| **Replay** | Captures and re-sends valid packets | Unauthorized access via replay | Timestamps, Nonces, Session Tokens |
| **Smurf** | Spoofs victim IP in broadcast requests | Denial of Service (DDoS) | Disabling IP Directed Broadcasts, Ingress Filtering |

---

## Key Takeaways

- **Core Concept:** IP spoofing involves altering a packet's source IP address to trick security controls and bypass access restrictions.
- **Attack Variations:** On-path attacks hijack connections, replay attacks reuse intercepted data, and smurf attacks cause amplification DDoS.
- **Defensive Measures:** Always enforce end-to-end encryption and configure firewall ingress filtering to drop packets from external interfaces bearing internal source IPs.
