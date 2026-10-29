# Security Alert Triage

## 1. What is Triage?
- **Triage:** The process of prioritizing incidents according to their importance or urgency.
- Helps security teams evaluate alerts, allocate resources, and address critical threats first.
- Ensures incidents are handled quickly to reduce potential damage.

## 2. Triage Process

The triage process consists of three steps:

1. Receive and assess.
2. Assign priority.
3. Collect and analyze.

### Step 1: Receive and Assess
- Receive an alert from a detection tool such as an IDS.
- Review the alert to verify its validity and understand the suspicious activity.
- Gather information about the activity, affected systems, and assets.

**Questions to consider:**
- Is the alert a false positive?
- Has this alert occurred before, and how was it resolved?
- Is the alert related to a known vulnerability?
- How severe is the alert?

### Step 2: Assign Priority
- Determine the urgency of the incident based on its potential impact.
- Prioritization helps security teams use time and resources effectively.

**Factors affecting priority:**

1. **Functional Impact**
   - Determines how the incident affects the services provided by a system.
   - Example: Ransomware may encrypt or delete data, making systems unavailable.

2. **Information Impact**
   - Determines how the incident affects the confidentiality, integrity, and availability (CIA) of information.
   - Example: Data exfiltration can expose sensitive customer or organizational information.

3. **Recoverability**
   - Determines whether the organization can recover from the incident and the resources required.
   - Example: Stolen proprietary data published publicly may be impossible to fully recover.

**Note:** Alerts may already have an assigned severity or priority level.

### Step 3: Collect and Analyze
- Perform a detailed investigation of the incident.
- Collect evidence from different sources.
- Conduct external research when necessary.
- Document investigative steps and findings.
- Escalate serious or complex incidents to a Level 2 analyst or manager when required.
- Use the collected evidence to make informed response decisions.

## 3. Benefits of Triage

### A. Resource Management
- Directs resources toward urgent and high-impact threats.
- Prevents unnecessary effort on lower-priority alerts.
- Helps reduce incident response time.

### B. Standardized Approach
- Provides a consistent process for handling alerts.
- Uses documentation and playbooks to guide investigations.
- Ensures alerts are assessed and validated before further escalation.

## 4. Key Takeaways
- **Triage:** Prioritizes incidents according to urgency and importance.
- **Receive and Assess:** Verify the alert and gather initial information.
- **Assign Priority:** Evaluate functional impact, information impact, and recoverability.
- **Collect and Analyze:** Gather evidence, investigate, document findings, and escalate when necessary.
- **False Positive:** An alert that incorrectly identifies harmless activity as a threat.
- Triage improves resource management, standardizes incident handling, and helps organizations respond to threats efficiently.