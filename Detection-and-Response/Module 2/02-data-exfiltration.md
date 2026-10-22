# Data Exfiltration and Network Monitoring

## 1. Data Exfiltration
- **Data Exfiltration:** Unauthorized transfer of sensitive data outside an organization's network.

## 2. Stages of a Data Exfiltration Attack

1. **Initial Access:** Attackers gain access through methods like phishing emails containing malicious links or attachments.
2. **Lateral Movement (Pivoting):** Attackers explore the network to access other systems.
3. **Identify Valuable Assets:** Attackers search for sensitive data in file shares, intranet sites, and code repositories.
4. **Data Collection and Preparation:** Attackers collect, package, and compress data to hide it or bypass security controls.
5. **Data Exfiltration:** Attackers transfer stolen data outside the network, for example, by emailing it to themselves.

## 3. How Organizations Defend Against Data Exfiltration

### A. Prevent Access
- Protect against phishing attacks.
- Use **Multi-Factor Authentication (MFA)** to add an extra layer of security.

### B. Monitor Network Activity
- Monitor unusual network behavior to detect possible compromises.
- Investigate multiple logins from IP addresses outside the organization's network.

### C. Protect Assets
- Maintain an **asset inventory** containing all organizational assets.
- Apply appropriate security controls to prevent unauthorized access.

### D. Detect Data Exfiltration
Monitor for these suspicious activities:
- Large internal file transfers.
- Large external uploads.
- Unexpected file writes.

**SIEM (Security Information and Event Management):** Tools that collect and analyze security data to detect suspicious activities and generate alerts.

### E. Respond to the Attack
- Investigate security alerts.
- Block attacker-associated IP addresses using firewall rules.
- Stop the suspicious activity and prevent further data theft.

## Key Takeaways
- Data exfiltration involves unauthorized transfer of sensitive information.
- Attackers commonly use phishing, lateral movement, and data collection before stealing data.
- MFA, asset inventories, and security controls help protect networks.
- Network monitoring and SIEM tools help detect suspicious data transfers.
- Firewalls can block malicious IP addresses to stop ongoing attacks.