# IDS, IPS, and EDR

## 1. Why Detection Tools Are Needed
- Detection tools monitor networks and systems for suspicious activity.
- They generate alerts when potential threats are detected.
- They help security analysts investigate and respond to attacks.

## 2. Intrusion Detection System (IDS)
- **Definition:** An application that monitors system activity and alerts on possible intrusions.
- **Main function:** Detects and logs suspicious activity and generates alerts.
- **Limitation:** Does not prevent or stop attacks automatically.
- **Example:** Alerts when an unknown IP address attempts to log in.
- **Tools:** Snort, Suricata, Zeek, Sagan.

## 3. Intrusion Prevention System (IPS)
- **Definition:** An application that monitors system activity and takes action to stop intrusions.
- **Main functions:**
  - Detects malicious activity.
  - Generates alerts and logs events.
  - Blocks suspicious traffic to prevent attacks.
- **Example:** Blocks malicious traffic by modifying an access control list (ACL).
- **Tools:** Snort, Suricata, Sagan.
- **Note:** Some IDS tools can also operate as IPS.

## 4. Endpoint Detection and Response (EDR)
- **Definition:** An application that monitors endpoints for malicious activity.
- **Endpoint:** Any device connected to a network, such as a computer, phone, or tablet.
- **Main functions:**
  - Monitors, records, and analyzes endpoint activity.
  - Detects and alerts on suspicious behavior.
  - Uses behavioral analysis to identify unusual activity.
  - Can automatically block malicious processes.
- **Behavioral analysis:** Examines system behavior using AI and machine learning to identify suspicious patterns.
- **Example:** Automatically blocks an unusual or malicious process running on a computer.
- **Tools:** OpenEDR, Bitdefender EDR, FortiEDR.

## 5. Comparison of IDS, IPS, and EDR

| Capability | IDS | IPS | EDR |
|---|---|---|---|
| Detects malicious activity | Yes | Yes | Yes |
| Prevents intrusions | No | Yes | Yes |
| Logs activity | Yes | Yes | Yes |
| Generates alerts | Yes | Yes | Yes |
| Behavioral analysis | Not a core capability | Not a core capability | Yes |
| Monitoring focus | Network/system activity | Network/system activity | Endpoints |

## 6. IDS Detection Categories

1. **True Positive:** An attack exists, and the system correctly detects it.
2. **True Negative:** No attack exists, and no alert is generated.
3. **False Positive:** No actual attack exists, but the system incorrectly generates an alert.
4. **False Negative:** An attack exists, but the system fails to detect it.

**Remember:**
- False positives waste time investigating harmless activity.
- False negatives are dangerous because real attacks go undetected.

## 7. Key Differences
- **IDS:** Detects and alerts.
- **IPS:** Detects, alerts, and prevents.
- **EDR:** Monitors endpoints, analyzes behavior, and can automatically respond to threats.

## 8. Key Takeaways
- Detection tools improve security awareness by monitoring systems and networks.
- IDS mainly identifies threats, while IPS can actively block them.
- EDR focuses on endpoint activity and behavioral analysis.
- SIEM tools also provide detection capabilities.