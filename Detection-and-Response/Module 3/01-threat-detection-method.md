# Methods of Threat Detection

## 1. Detection and Analysis Phase
- **Detection:** Prompt discovery of security events.
- **Analysis:** Investigating and validating alerts to confirm whether an incident has occurred.
- IDS and SIEM tools help detect suspicious activity and analyze security data.
- Detection tools may miss threats if they are not properly configured, so organizations need additional detection methods.

## 2. Threat Hunting
- **Definition:** The proactive search for threats on a network that may have gone undetected by security tools.
- Combines human analysis with technology to discover hidden threats.
- Helps identify threats before they cause damage.
- Used to investigate suspicious activity and analyze existing detections.

**Example:** Detecting fileless malware that hides in memory instead of using files, allowing it to evade traditional detection methods such as signature analysis.

**Threat Hunters:**
- Research emerging threats and attack techniques.
- Assess an organization's vulnerability to potential attacks.
- Use threat intelligence, indicators of compromise (IoCs), indicators of attack (IoAs), and machine learning.

## 3. Threat Intelligence
- **Definition:** Evidence-based information that provides context about existing or emerging threats.
- Helps organizations understand attackers, their techniques, and potential risks.

### Sources of Threat Intelligence
1. **Industry Reports:** Provide information about attackers' tactics, techniques, and procedures (TTPs).
2. **Government Advisories:** Share information about threats, attack methods, and recommended defenses.
3. **Threat Data Feeds:** Provide streams of threat-related information, such as malicious IP addresses, domains, and file hashes.

**Advanced Persistent Threat (APT):**
- A threat in which an attacker maintains unauthorized access to a system for an extended period.

### Threat Intelligence Platform (TIP)
- **Definition:** An application that collects, centralizes, and analyzes threat intelligence from multiple sources.
- Helps security teams identify relevant threats and prioritize risks.
- Threat intelligence feeds should be evaluated before use and should support detection rather than determine detections entirely.

## 4. Cyber Deception
- **Definition:** Techniques that deliberately deceive attackers to improve threat detection and defensive strategies.

### Honeypots
- **Definition:** Decoy systems or resources designed to attract potential attackers.
- Help security teams observe suspicious activity and generate alerts when attackers interact with them.

**Example:** Creating a fake file named `Client Credit Card Information - 2022`. If an attacker attempts to access it, security teams are alerted.

## 5. Key Takeaways
- **Threat Hunting:** Proactively searches for hidden threats.
- **Threat Intelligence:** Provides evidence-based information about threats and attackers.
- **TIP:** Collects and analyzes threat intelligence from multiple sources.
- **Cyber Deception:** Misleads attackers to improve detection.
- **Honeypot:** A decoy resource used to attract and detect attackers.
- Organizations should combine automated tools with human-driven detection methods to improve security coverage and accuracy.

## 6. Resources for more information
- If you would like to explore more on threat hunting and threat intelligence, here are some resources:
    - An [informational repository about threat hunting from](https://www.threathunting.net/) The ThreatHunting Project 
    - Research on [state-sponsored hackers](https://blog.google/threat-analysis-group/) from Threat Analysis Group (TAG) 