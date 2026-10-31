# SIEM: Log Ingestion

## SIEM Process Overview

**SIEM (Security Information and Event Management):** Tools that collect and analyze log data to monitor an organization's security activities.

The SIEM process consists of three main steps:

1. **Collect and Aggregate Data:** Collects event data from different sources such as servers, computers, and network devices.
2. **Normalize Data:** Converts collected data into a standard format so it is consistent, readable, and easier to search.
3. **Analyze Data:** Organizes and indexes data so it can be searched, correlated, and analyzed to identify suspicious activities.

## 1. Log Ingestion

**Log Ingestion:** The process of collecting and importing data from different log sources into a SIEM tool.

- SIEM tools collect logs from sources such as servers, computers, applications, and network devices.
- The SIEM creates a copy of the received event data and stores it.
- Original source logs remain unchanged.
- Centralized data allows security analysts to investigate incidents more efficiently.

**Examples of collected data:**
- Authentication attempts.
- Network activity.
- System events.
- Application events.

**Purpose:** Provides a centralized location for monitoring, investigating, and analyzing security events.

## 2. Log Forwarders

**Log Forwarders:** Software that automatically collects and sends log data from different devices and systems to a SIEM tool.

### Why Use Log Forwarders?
- Manually uploading logs is time-consuming and inefficient.
- Organizations may have thousands of devices generating logs.
- Log forwarders automate the collection and transmission process.

### How Log Forwarders Work

1. Install a log forwarder on a device.
2. Configure which logs need to be collected.
3. Specify the destination, such as a SIEM tool.
4. The forwarder collects and sends the logs.
5. The SIEM processes and normalizes the received data.
6. Security analysts can search, correlate, and analyze the data.

### Types of Log Forwarders

- **Native Log Forwarders:** Built into certain operating systems.
- **Third-Party Log Forwarders:** Additional software installed when native forwarding is unavailable or insufficient.
- **Proprietary Log Forwarders:** Developed specifically for particular SIEM tools.
- **Open-Source Log Forwarders:** Freely available forwarding software that can integrate with SIEM tools.

### Factors for Choosing a Log Forwarder

- Organizational requirements.
- Compatibility with existing infrastructure.
- System requirements.
- Integration with the SIEM tool.

## Log Ingestion Process

**Flow:**

Log Sources → Log Forwarder → SIEM → Data Normalization → Search, Correlation and Analysis

## Key Takeaways

- SIEM tools require log data to detect and investigate security incidents.
- Log ingestion collects and imports data into SIEM tools.
- SIEM stores copies of received logs without modifying the original source logs.
- Log forwarders automate log collection and transmission.
- Log normalization makes data consistent and easier to analyze.
- Understanding log sources helps analysts identify where security incidents originate.

## Resources

- [Splunk: Guide on Getting Data into Splunk](https://docs.splunk.com/Documentation/SplunkCloud/9.0.2303/Data/Howdoyouwanttoadddata)
- [Google Security Operations: Data Ingestion Guide](https://cloud.google.com/chronicle/docs/data-ingestion-flow)