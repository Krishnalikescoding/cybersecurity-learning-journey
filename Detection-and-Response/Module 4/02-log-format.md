# Log Formats

**Log analysis** = examining logs to identify events of interest. Knowing how to read different formats lets you extract key details (who, what, when) and spot unusual or malicious activity. There is **no standard logging format**, so you'll encounter many.

---

## 1. JSON (JavaScript Object Notation)
- Lightweight, easy to read/write; common in web technologies and cloud environments.
- Syntax derived from JavaScript.
- **Key-value pair:** `"Alert": "Malware"` (key, colon, value)
- **Commas:** separate data, e.g. `"Alert": "Malware", "Alert code": 1090`
- **Double quotes:** enclose text (strings). Numbers are not quoted, e.g. `"Alert code": 1090`
- **Curly brackets `{}`:** enclose an **object** (comma-separated key-value pairs). JSON log entries start and end with a curly bracket.
  ```
  "User": { "id": "1234", "name": "user", "role": "engineer" }
  ```
- **Square brackets `[]`:** enclose an **array** (ordered list), e.g. `["Administrators", "Users", "Engineering"]`

---

## 2. Syslog
Syslog refers to three capabilities:
- **Protocol:** transports logs to a centralized log server. Port **514** (plaintext), port **6514** (encrypted).
- **Service:** consolidates logs from multiple sources into one location and forwards them to a remote server.
- **Log format:** native logging format in Unix systems. Three components:

| Component | Contains |
|---|---|
| **Header** | Timestamp, hostname, application name, message ID |
| **Structured-data** | Extra info in `[ ]` as key-value pairs |
| **Message** | Detailed description of the event |

**Example:**
```
<236>1 2022-03-21T01:11:11.003Z virtual.machine.com evntslog - ID01 [user@32473 iut="1" eventSource="Application" eventID="9999"] This is a log entry!
```

- **Timestamp:** `2022-03-21T01:11:11.003Z`
  - `2022-03-21` = date (YYYY-MM-DD)
  - `T` = separates date and time
  - `01:11:11.003` = 24-hour time with milliseconds
  - `Z` = UTC
- **Hostname:** `virtual.machine.com`
- **Application:** `evntslog`
- **Message ID:** `ID01`
- **Priority (PRI):** `<236>`, in angle brackets; indicates urgency. Generally, **lower number = more urgent**.

> Syslog headers can be combined with JSON and XML formats. Custom log formats also exist.

---

## 3. XML (eXtensible Markup Language)
- Language/format for storing and transmitting data; native file format in **Windows** systems.
- **Tags:** come in pairs, a start tag `<tag>` and an end tag `</tag>`.
- **Elements:** the tags plus the data inside them. Every XML entry needs at least one **root element**, which contains **child elements**.
  ```xml
  <Event>
      <EventID>4688</EventID>
      <Version>5</Version>
  </Event>
  ```
  `<Event>` = root; `<EventID>` and `<Version>` = child elements.
- **Attributes:** extra info about an element, placed inside the tag and always quoted (single or double quotes).
  ```xml
  <Data Name='SubjectUserName'>JSMITH</Data>
  ```
  Tag = `<Data>`, attribute = `Name='SubjectUserName'`, data = `JSMITH`.

---

## 4. CSV (Comma Separated Value)
- Commas separate data values.
- Position of the data corresponds to its field name, but **field names may not be included** in the log.
- You must know which fields the source device (IPS, firewall, scanner, etc.) includes.

**Example:**
```
2009-11-24T21:27:09.534255,ALERT,192.168.2.7, 1041,x.x.250.50,80,TCP,ALLOWED,1:2001999:9,"ET MALWARE BTGrab.com Spyware Downloading Ads",1
```

---

## 5. CEF (Common Event Format)
- Uses key-value pairs to structure data and identify fields.
- **Syntax:**
  ```
  CEF:Version|Device Vendor|Device Product|Device Version|Signature ID|Name|Severity|Extension
  ```
- Fields are separated by the pipe `|`. The **Extension** must be key-value format.
- Syslog is a common transport for CEF; when used, a **timestamp and hostname are prepended**.
- Extension and syslog prefix are **optional**.

**Example:**
```
Sep 29 08:26:10 host CEF:1|Security|threatmanager|1.0|100|worm successfully stopped|10|src=10.0.0.2 dst=2.1.2.2 spt=1232
```

| Field | Value |
|---|---|
| Syslog Timestamp | Sep 29 08:26:10 |
| Syslog Hostname | host |
| Version | CEF:1 |
| Device Vendor | Security |
| Device Product | threatmanager |
| Device Version | 1.0 |
| Signature ID | 100 |
| Name | worm successfully stopped |
| Severity | 10 (high) |
| Extension | src=10.0.0.2, dst=2.1.2.2, spt=1232 |

**Meaning:** The threatmanager security application stopped a worm spreading from internal host 10.0.0.2 to external 2.1.2.2 via port 1232, with high severity (10).

---

## Key Takeaways
- No single standard log format exists; logs come from many different sources.
- Being able to interpret each format helps you find key information to support investigations.

## Resources

- [The Syslog Protocol (RFC 5424)](https://www.rfc-editor.org/rfc/rfc5424)
- [Open-source Test Data Generator](https://generatedata.com/)
- [Date and Time on the Internet: Timestamps (RFC 3339)](https://www.rfc-editor.org/rfc/rfc3339)