# Antimalware Software

## Overview
- **Definition**: Specialized software that detects, quarantines, and destroys malware on computers or networks.
- **Examples**: Malwarebytes, McAfee Antivirus, Windows Defender.
- **Deployment**: Can be installed locally on a single device or managed centrally on a server.

## How It Works
- **Detection**: Scans files for malware signatures.
- **Malware signature**: A pattern of attributes that corresponds to known malware.
- **Response actions**:
  - Delete the infected file
  - Quarantine the file
  - Alert the user of potential infection

# Logging

One of the most essential methods for attack detection is logging. Logging is the process where actions are accurately recorded in a secure location. Log records should be tamper-proof and act as a permanent record of what has occurred within a network. You can perform logging on individual machines or applications.

The types of actions logged depend on the organization’s systems and security needs. Commonly logged actions include:

- User logins and logouts  
- Failed login attempts  
- System configuration changes  
- Packet traffic  
- Process or service initiation  
- Alterations to files or databases  

Though a single log entry might not be highly valuable in isolation, a larger collection helps track activities of legitimate users and malicious actors. These logs provide an audit trail invaluable for diagnosing issues and identifying malicious activity or security breaches.

# Network Monitoring

In addition to recording events happening on servers, organizations can monitor communications across their network. This approach, known as **traffic analysis**, can identify network activity, even encrypted activity. Traffic analysis involves tracking different metrics related to the network.  

Some examples of these metrics include:  
- Source and destination of traffic  
- Network protocols used  
- Bandwidth usage  
- Packet size  

Advanced traffic analysis can also identify:  
- Specific applications or services in use  
- Presence of malicious code  
- Unusual behavior or anomalies that might indicate a cyberattack  

Some types of malware pivot from device to device in ways that good network monitoring tools can easily identify.

---

## Example

Imagine a network monitoring tool is in use:  

- If someone uses a network device to **stream video**, the tool will show **high bandwidth consumption** from the device over an extended period.  
- If someone uses a network device to **download a large file**, the tool will show a **sharp peak in bandwidth usage** followed by little or no demand after the download completes.

# Security Information and Event Management (SIEM) Tools

The **IBM Security QRadar** interface shows various information about a network, including network traffic data. This SIEM service (Security Information and Event Management) provides network security intelligence and analytics software that monitors for threats and insider attacks.

Making sense of all the data collected through network monitoring can be challenging. For help, many cybersecurity professionals turn to SIEM tools.  

A **SIEM tool**:  
- Collects data throughout an organization’s technology infrastructure  
- Aggregates it into a central location  
- Helps the cybersecurity team identify and analyze events and patterns of potential attacks  

---

## Example

Imagine that a cybersecurity team suspects an attacker is trying to compromise a user’s account using **brute force attacks**.  

- They configure the SIEM tool to **trigger an alert** if **five or more failed logins occur within one minute** for the account.  
- If an attacker attempts millions of username or password combinations, the failed login attempts will exceed the threshold.  
- The SIEM tool detects this, triggers an alert, and notifies the team of the potential attack.

# Security Operations Center (SOC)

The group responsible for looking after an organization’s security is often part of the **security operations center (SOC)**. A SOC is a dedicated team of cybersecurity professionals that uses specialized software to actively monitor, detect, investigate, and respond to potential security threats and incidents in real time.  

One of the SOC’s key objectives is to detect attacks in progress using SIEM and other monitoring tools.  

---

## Responsibilities of a SOC

Security analysts in a SOC are responsible for:  
- Assessing an organization’s security posture  
- Detecting attacks or potential attacks  
- Deciding how to respond to threats based on organizational procedures  

---

## False Alarms

One challenge in SOCs is determining the best thresholds for alerts. Their goal is to reduce **false positives** (legitimate events incorrectly recorded as malicious).  

- Confirming whether an alert is a false positive is the responsibility of a security analyst.  
- If a specific legitimate event repeatedly triggers false positives, the analyst may adjust thresholds to reduce noise.  

---

## Example

Consider an employee who returns to work after a long holiday and forgets her password.  

- She attempts to log in multiple times with incorrect guesses.  
- These repeated failed attempts might exceed the SOC’s alert threshold.  
- The SOC would receive an alert, which an analyst would need to review and confirm as a false positive.  

# Artificial Intelligence (AI)

Artificial intelligence (AI) is enhancing organizations’ attack detection and defense. Let’s explore how AI impacts key areas of attack detection.

---

## Logging

AI automates the process of logging and analyzing large volumes of data from various sources.  
- This task would take humans an enormous amount of time.  
- AI can perform it quickly, enabling **real-time threat detection and prevention**.  

---

## Network Monitoring

AI can analyze traffic patterns and identify anomalies that might indicate an attack.  
- Example: A sudden surge in network traffic may indicate a **Distributed Denial-of-Service (DDoS) attack**.  
- With AI, organizations can detect anomalies instantly and initiate **countermeasures**.  

---

## SIEM Tools

SIEM tools use AI to collate and analyze data across an organization’s network.  
- They identify patterns and correlations to detect potential security threats.  
- Example: **IBM QRadar SIEM** can set alert thresholds for abnormal activities, such as multiple failed login attempts.  

---

## Security Operations Centers (SOCs)

In a SOC, AI helps analysts work more efficiently.  
- Instead of manually sifting through massive amounts of data, analysts focus on **responding to AI-generated alerts**.  
- AI saves time and helps **mitigate threats more swiftly**.  

---

## Machine Learning (ML)

Organizations can train AI systems to distinguish between **normal** and **unusual** behavior using historical data.  

- AI learns from examples of legitimate threats and false positives.  
- Over time, the system improves at **reducing false positives** and fine-tuning thresholds.  
- It can even automate parts of the verification process, reducing the time spent investigating false alerts.  

**Example:**  
A system might recognize that multiple failed logins from a trusted internal IP during working hours are likely just a forgotten password. It learns not to trigger an unnecessary alert, improving efficiency and accuracy.  








