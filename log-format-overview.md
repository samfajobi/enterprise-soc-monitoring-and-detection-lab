````md
# Overview of Log File Formats

Logs record events that happen on a system, application, or network. In cybersecurity, logs provide key details about activities across an organization, such as who signed into an application at a specific point in time, what actions were performed, and where those actions originated from.

As a security analyst, **log analysis** is the process of examining logs to identify events of interest, suspicious behavior, or malicious activity. Understanding how different log formats are structured is critical for uncovering key details during investigations and for effective SIEM analysis.

This document covers the following common log formats:
* JSON
* Syslog
* XML
* CSV
* CEF

---

## Purpose of Logs in Security

Logs help security teams to:
* Detect malicious activity
* Investigate security incidents
* Correlate events across systems
* Support compliance and auditing
* Perform root cause analysis

Logs are one of the most important data sources in a Security Operations Center (SOC).

---

## JavaScript Object Notation (JSON)

JavaScript Object Notation (JSON) is a file format used to store and transmit data. It is lightweight, easy to read, and easy to write. JSON is widely used in web technologies, APIs, and cloud environments.

JSON syntax is derived from JavaScript and commonly includes:
* Key-value pairs
* Commas
* Double quotes
* Curly brackets
* Square brackets

---

### Key-Value Pairs

A key-value pair represents two linked pieces of data: a key and its corresponding value. A key-value pair consists of a key, followed by a colon, and then a value.

Example:
```json
"Alert": "Malware"
````

For readability, it is recommended to include a space after the colon.

---

### Commas

Commas are used to separate multiple key-value pairs.

Example:

```json
"Alert": "Malware", "AlertCode": 1090, "Severity": 10
```

---









