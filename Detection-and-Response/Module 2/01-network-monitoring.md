# Network Monitoring

## 1. Basic Terms

- **Network Traffic:** Amount and type of data moving across a network.
- **Network Data:** Data transmitted between devices on a network.
- **Network Monitoring:** Collecting and analyzing network traffic to detect suspicious activities.
- **Baseline:** A reference point representing normal network behavior. It helps identify unusual activities.

## 2. Importance of Network Monitoring

- Detects suspicious network activities.
- Helps identify security threats and intrusions.
- Identifies unusual data transfers.
- Helps protect network devices and sensitive information.

## 3. What to Monitor

### A. Flow Analysis
- **Flow:** Movement of network communications, including packets, protocols, and ports.
- **Packets:** Units of data transmitted across a network.
- **Ports:** Communication endpoints used by applications and services.
- **Protocols:** Rules that govern network communication.
- Example: HTTPS commonly uses port 443.

**Command and Control (C2):** Communication between an attacker's system and a compromised device.

- Attackers may use unusual ports to hide their communications.
- Analysts monitor mismatches between protocols and ports.

### B. Packet Payload Information
- **Payload:** The actual data carried inside a network packet.
- Payloads may be encrypted and require decryption to be read.
- Monitoring payloads helps identify suspicious data transfers.

**Data Exfiltration:** Unauthorized transfer of sensitive data outside an organization's network.

### C. Temporal Patterns
- Refers to patterns of network activity over time.
- Analysts compare activity with normal working hours and traffic levels.
- Unusual traffic outside expected hours may indicate malicious activity.

**Off-baseline Activity:** Network behavior that differs from the established baseline.

## 4. SOC vs NOC

| SOC | NOC |
|---|---|
| Security Operations Center | Network Operations Center |
| Focuses on security threats | Focuses on network performance |
| Detects and responds to attacks | Handles outages and disruptions |
| Protects systems and data | Maintains availability and uptime |

## 5. Indicators of Compromise (IoCs)

- **IoCs:** Signs that a system or network may have been compromised.
- Security analysts monitor network activity to identify IoCs and investigate potential security incidents.

## 6. Network Monitoring Tools

### A. Intrusion Detection System (IDS)
- Monitors system or network activity.
- Detects suspicious behavior and generates alerts.
- Can identify patterns associated with malware and phishing attempts.

### B. Network Protocol Analyzers
Also called **packet sniffers**.

- Capture and analyze network traffic.
- Help analysts examine network communications in detail.
- Packet captures can be investigated for malicious activity.

**Examples:**
- **Wireshark:** Provides a graphical interface for packet analysis.
- **tcpdump:** Captures and analyzes packets through the command line.

## Key Takeaways

- Network monitoring helps detect suspicious activities and intrusions.
- Baselines help identify abnormal network behavior.
- Flow analysis examines packets, protocols, and ports.
- Packet payload analysis examines the actual transmitted data.
- Temporal analysis identifies unusual activity based on time.
- SOC focuses on security, while NOC focuses on network performance.
- IDS detects and alerts on suspicious activity.
- Wireshark and tcpdump capture and analyze network packets.

## Resources

- If you would like to learn more about network components organizations can monitor, check out [network traffic - MITRE ATT&CK®](https://attack.mitre.org/datasources/DS0029/)
- Attackers can leverage different techniques to exfiltrate data, should you like to learn more, check out [data exfiltration techniques - MITRE ATT&CK®](https://attack.mitre.org/tactics/TA0010/)
