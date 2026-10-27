# Ongoing Monitoring of CI/CD: Automatically Finding Threats

## 1. CI/CD Monitoring
- **CI/CD:** Continuous Integration and Continuous Delivery/Deployment.
- CI/CD pipelines automate building, testing, and deploying software.
- If compromised, attackers may inject malicious code, steal secrets, or disrupt software.
- **CI/CD monitoring:** Continuously monitors pipeline activity to detect unusual behavior and potential security threats.
- Automation helps identify anomalies and Indicators of Compromise (IoCs) so security teams can respond quickly.

## 2. Common IoCs in CI/CD Pipelines

**1. Unauthorized Code Changes**
- Changes made by unauthorized users.
- Commits at unusual times or from unexpected locations.
- Suspicious code, confusing changes, or unusually large deletions.

**2. Suspicious Deployment Patterns**
- Deployments to unapproved systems.
- Unexpected or unusually frequent deployments.
- Production deployments initiated by unauthorized accounts or developer branches.

**3. Compromised Dependencies**
- Vulnerable dependencies containing known CVEs.
- Unexpected dependencies added to build configurations.
- Downloads from unofficial or untrusted sources.

**4. Unusual Pipeline Execution**
- Normally successful pipeline steps suddenly failing.
- Unexpectedly long execution times.
- Changes to the order or behavior of pipeline steps without approval.

**5. Secrets Exposure Attempts**
- Unauthorized attempts to access secrets.
- Hardcoded passwords, API keys, or other private credentials in code.

## 3. Benefits of Monitoring IoCs
- **Quick Incident Response:** Detects threats early so security teams can investigate and respond quickly.
- **Reduced Damage:** Limits the time attackers can remain inside the pipeline.
- **Improved Threat Knowledge:** Helps identify attack patterns and improve future threat hunting.
- **Better Security:** Protects source code, credentials, build systems, and deployed software.

## 4. Methods for Automated Monitoring

### A. Comprehensive Logging and Auditing
Logs provide the data needed to identify unusual activity and potential IoCs.

**Types of logs:**

1. **Pipeline Execution Logs**
   - Record pipeline steps, execution times, and success/failure rates.
   - Monitoring tools establish a baseline of normal behavior.
   - Unusual delays, errors, or changes in step order can indicate suspicious activity.

2. **Code Commit Logs**
   - Record code changes and who made them.
   - Unexpected authors, unusual commit times, and suspicious code changes may indicate compromise.

3. **Access Logs**
   - Record user logins and access to pipeline resources.
   - Unusual locations, repeated failed logins followed by successful ones, and unauthorized configuration changes are potential IoCs.

4. **Deployment Logs**
   - Record when, where, and how software is deployed.
   - Unexpected deployment times, destinations, or deployment patterns may indicate threats.

**Baseline:** A profile of normal pipeline behavior used to identify deviations and anomalies.

### B. SIEM Integration
- SIEM collects and analyzes CI/CD logs from multiple sources.
- Uses analytics and machine learning to identify unusual patterns.
- Applies detection rules to identify known threats.

**Examples of SIEM alerts:**
- Known malicious file hashes found in build results.
- CI/CD servers communicating with known malicious Command and Control (C2) servers.
- Unauthorized attempts to access or download secrets.

### C. Real-Time Alerting and Notifications
Automated alerts notify security teams immediately when suspicious activity is detected.

Important alerts include:
- Repeated or unusual build failures.
- Suspicious code changes.
- Attempts to access or expose secrets.
- Unusual outbound network traffic from CI/CD servers.

### D. Performance Monitoring
- Monitors pipeline speed and resource usage.
- Sudden slowdowns or unusually high resource consumption may indicate suspicious activity.
- These issues are potential Indicators of Attack (IoAs) that may require further investigation to identify IoCs.

### E. Continuous Vulnerability Scanning
- Regularly scans CI/CD infrastructure for security weaknesses.
- Identifies known CVEs in CI/CD tools, plugins, containers, and dependencies.
- Helps teams prioritize patches and reduce the risk of pipeline compromise.

**CVE (Common Vulnerabilities and Exposures):** A publicly documented identifier for a known cybersecurity vulnerability.

## 5. Important Terms

- **IoC (Indicator of Compromise):** Evidence suggesting that a system or pipeline may have been compromised.
- **IoA (Indicator of Attack):** Evidence of suspicious activity that may indicate an ongoing or attempted attack.
- **C2 (Command and Control):** Communication used by attackers to control compromised systems.
- **SIEM:** Collects and analyzes security logs to detect threats.
- **Baseline:** A representation of normal system or pipeline behavior.
- **CVE:** An identifier for a publicly documented vulnerability.
- **Continuous Vulnerability Scanning:** Repeatedly checking systems and software for known vulnerabilities.

## 6. Key Takeaways
- CI/CD monitoring protects the software supply chain against attacks.
- Common IoCs include unauthorized code changes, suspicious deployments, compromised dependencies, unusual pipeline execution, and secrets exposure.
- Logs provide the data needed for automated threat detection.
- SIEM integration helps identify anomalies and known threats at scale.
- Real-time alerts enable faster incident response.
- Performance monitoring can reveal suspicious behavior.
- Continuous vulnerability scanning helps identify weaknesses before attackers exploit them.

## 7. Resources for More Information

1. **Optimizing Logs for a More Effective CI/CD Pipeline: Best Practices**
   - https://coralogix.com/blog/optimizing-logs-for-a-more-effective-ci-cd-pipeline/

2. **Implementing AI in CI/CD Pipelines: A Practical Guide**
   - https://blog.axiomio.com/implementing-ai-in-ci-cd-pipelines-a-practical-guide-83466035e3c7

3. **What is CI/CD? - Continuous Integration, Delivery, and Deployment**
   - https://www.threatintelligence.com/blog/continuous-integration-continuous-delivery

4. **CI/CD & DevOps Pipelines: An Introduction**
   - https://www.splunk.com/en_us/blog/learn/ci-cd-devops-pipeline.html