# DoS & DDoS Attacks

## Denial-of-Service (DoS) Attack

A **Denial-of-Service (DoS)** attack is a cyberattack that floods a network, server, or service with excessive traffic or requests, making it unavailable to legitimate users.

### Objective

- Disrupt normal business operations
- Consume system resources
- Prevent legitimate users from accessing services
- Cause downtime

### Effects

- Slow network performance
- Server crashes
- Service unavailability
- Financial losses
- Increased vulnerability to additional attacks

---

# Distributed Denial-of-Service (DDoS) Attack

A **Distributed Denial-of-Service (DDoS)** attack is a type of DoS attack that uses **multiple compromised devices or servers** from different locations to overwhelm a target.

### Characteristics

- Multiple attacking systems
- Much larger attack volume
- More difficult to detect and block
- Greater impact than a standard DoS attack

---

# DoS vs DDoS

| DoS | DDoS |
|------|-------|
| Single attacking device | Multiple attacking devices |
| Easier to detect | Harder to detect |
| Smaller attack volume | Massive attack volume |
| Less powerful | More powerful and scalable |

---

# Common DoS Attacks

## 1. SYN Flood Attack

A **SYN Flood** exploits the **TCP three-way handshake** by sending a large number of SYN requests without completing the connection.

### Normal TCP Handshake

1. Client → **SYN**
2. Server → **SYN/ACK**
3. Client → **ACK**
4. Connection established

### During a SYN Flood

1. Attacker sends thousands of **SYN** packets.
2. Server responds with **SYN/ACK**.
3. Attacker never sends the final **ACK**.
4. Server keeps many ports open waiting for responses.
5. Available ports become exhausted.
6. Legitimate users cannot establish new connections.

### Impact

- Consumes server resources
- Exhausts available ports
- Prevents legitimate connections

---

## 2. ICMP Flood Attack

An **ICMP Flood** repeatedly sends ICMP packets (such as ping requests) to a target server.

### How it Works

- Attacker floods the server with ICMP Echo Requests.
- Server attempts to respond to every request.
- Network bandwidth becomes saturated.
- Server performance degrades or crashes.

### Impact

- High bandwidth consumption
- Network congestion
- Service interruption

---

## 3. Ping of Death (PoD)

A **Ping of Death** attack sends an **oversized ICMP packet** that exceeds the maximum valid packet size.

### Details

- Normal ICMP packet size: **Up to 64 KB**
- Attack packet: **Greater than 64 KB**

Older or vulnerable systems may fail when processing these malformed packets.

### Impact

- System crash
- Buffer overflow (historically)
- Service disruption

> **Note:** Modern operating systems are generally protected against classic Ping of Death attacks.

---

# ICMP (Internet Control Message Protocol)

ICMP is a management protocol used for:

- Reporting network errors
- Network diagnostics
- Connectivity testing (e.g., `ping`)
- Status messages between devices

Attackers can abuse ICMP to perform flood-based DoS attacks.

---

# Attack Comparison

| Attack | Exploits | Method | Result |
|---------|-----------|--------|--------|
| **SYN Flood** | TCP Handshake | Floods SYN requests without completing connections | Exhausts server resources |
| **ICMP Flood** | ICMP | Sends massive numbers of ping requests | Consumes bandwidth |
| **Ping of Death** | ICMP | Sends oversized malformed packets | Crashes vulnerable systems |

---

# Importance for Security Analysts

Security analysts monitor for:

- Unusually high network traffic
- Excessive SYN requests
- Large volumes of ICMP packets
- Bandwidth spikes
- Sudden service outages
- Repeated connection failures

Early detection helps minimize downtime and protect network availability.

---

# Key Takeaways

- A **Denial-of-Service (DoS)** attack overwhelms a server or network with traffic or requests, making services unavailable to legitimate users.
- A **Distributed Denial-of-Service (DDoS)** attack uses **multiple compromised devices** to generate a much larger and more difficult-to-stop attack.
- A **SYN Flood** abuses the TCP three-way handshake by sending many SYN requests without completing the connection, exhausting server resources.
- An **ICMP Flood** overwhelms a target with excessive ICMP (ping) requests, consuming bandwidth and degrading performance.
- A **Ping of Death** sends oversized ICMP packets that can crash vulnerable systems, although modern systems are generally protected against this attack.
- Monitoring abnormal traffic patterns, bandwidth usage, and protocol-specific activity is essential for detecting and mitigating DoS attacks.