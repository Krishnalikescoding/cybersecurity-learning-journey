# Network Attacks: Packet Sniffing, IP Spoofing, and DoS

## 1. Packet Sniffing

**Packet sniffing** is the practice of capturing and inspecting data packets across a network.

* **Standard Network Operations:** 
  * A **Network Interface Card (NIC)** connects a device to a network.
  * In normal mode, the NIC reads data transmissions and accepts a packet only if it contains the device’s matching **MAC address**.
* **Promiscuous Mode:** 
  * A NIC can be set to **promiscuous mode**, allowing it to accept *all* network traffic—even packets not addressed to that specific device.
* **Malicious Use:** 
  * Attackers use software like **Wireshark** to capture and store network data.
  * Stolen personal information, IP addresses, and MAC addresses can be exploited directly or used to perform **IP spoofing**.

---

## 2. IP Spoofing Overview

After sniffing packets, malicious actors can impersonate the IP and MAC addresses of authorized devices to launch an **IP spoofing attack**.

* **Core Concept:** Attackers send IP packets containing fake/spoofed IP addresses.
* **Primary Defense:** Firewalls configured to refuse unauthorized IP packets and suspicious traffic.

---

## 3. Common IP Spoofing & Network Attacks

### A. On-Path Attack (Meddler-in-the-Middle)
Occurs when an attacker intercepts communication between two devices or servers that share a trusted relationship.

* **Vectors & Risks:**
  * **Credential Harvesting:** Intercepts sensitive data in transit, such as usernames and passwords.
  * **DNS Spoofing:** Intercepts a DNS lookup and spoofs the server's response, redirecting a domain name to a malicious IP address containing threats.
* **Primary Defense:** Encrypt data in transit using protocols like **TLS**.

---

### B. Smurf Attack
A hybrid attack that combines **IP spoofing** with a **Denial of Service (DoS)** technique to flood a network with unwanted traffic.

* **How It Works:**
  1. The attacker sniffs an authorized user's IP address and spoofs it.
  2. The attacker sends spoofed ICMP ping packets to the network's **broadcast address**.
  3. The packet is broadcast to all devices and servers on the network.
  4. Devices reply to the victim's spoofed IP with ICMP echo responses, overwhelming the target system and causing a denial of service.
* **Primary Defense:** Use advanced/Next-Generation Firewalls (**NGFW**) that monitor network anomalies and detect oversized broadcasts before they disrupt operations.

---

### C. Denial of Service (DoS) Attack
A class of attacks where an attacker prevents a compromised system from responding to legitimate traffic or executing normal operations.

* **Key Differences from Standard IP Spoofing:**
  * The attacker does **not** receive a response from the targeted host.
  * In a standard authorized request, packet details are legitimate, whereas IP spoofing continuously floods the target with fake source IP headers until the server crashes.

---

## 4. Key Security Takeaways

* **Defense-in-Depth:** No single strategy stops every attack vector. Security must be implemented in layers.
* **Layered Strategies:** Combine Next-Generation Firewalls (NGFW), proper NIC monitoring controls, and industry-standard encryption (e.g., TLS) to defend against IP spoofing and DoS attacks across multiple levels.