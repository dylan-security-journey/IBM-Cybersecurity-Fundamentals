# Types of Cyberattacks

Attackers can exploit both **technical vulnerabilities** and **human weaknesses** to infiltrate systems.  
Some attacks directly target software and hardware flaws, while others manipulate the **flawed ways humans interact with technology**.

---

## Common Types of Cyberattacks

### 1. Denial-of-Service (DoS) Attack
- Overloads a system or network with traffic until it becomes **unavailable**.  
- Targets single systems or services.  

### 2. Distributed Denial-of-Service (DDoS) Attack
- Similar to DoS but launched from **multiple compromised systems (botnets)**.  
- More powerful and harder to block.  

### 3. Phishing
- **Mass emails or messages** designed to trick users into revealing sensitive data (passwords, credit card info).  
- Often impersonates trusted organizations.  

### 4. Spear Phishing
- A **targeted form of phishing** directed at specific individuals or organizations.  
- More convincing because it uses personal or organizational details.  

### 5. Malware
- Malicious software that disrupts, damages, or steals data.  
- Examples: viruses, worms, ransomware, spyware, trojans.  

### 6. Man-in-the-Middle (MitM) Attack
- An attacker secretly intercepts and possibly alters communication between two parties.  
- Common in unsecured Wi-Fi networks.  

### 7. Domain Name System (DNS) Attack
- Exploits vulnerabilities in DNS to redirect traffic or disrupt services.  
- Examples: DNS poisoning, DNS hijacking, or amplification attacks.  

---

## Learning Objectives

After completing this module, you should be able to:  
- **Describe common types of cyberattacks**.  
- **List ways AI can enhance attack sophistication** (e.g., automating phishing, polymorphic malware, adaptive evasion).  
- **Examine real-time cyberthreat maps** to visualize ongoing global attacks.  

# Denial-of-Service (DoS) Attack

A **Denial-of-Service (DoS) attack** is any attack that causes a **complete or partial system outage**.  
It prevents legitimate users from accessing services by overwhelming a system with traffic or consuming critical resources.

---

## Characteristics

- Works like a **traffic jam** — overwhelming a website or service with too many requests.  
- Can slow down or **completely shut down** systems.  
- Exploits **resource exhaustion**, forcing systems to crash or become unresponsive.  
- Common targets: websites, online services, application servers, or network infrastructure.  

---

## Example

- **Billion Laughs Attack (XML Bomb)**:  
  - Attacker submits a malicious XML file containing self-replicating code.  
  - The system processes the code, creating **exponential replications**.  
  - Result: **consumes all resources**, eventually crashing or severely slowing down the system.  

---

## Profile Summary

| **Who are they?** | **What is their objective?** |
|--------------------|------------------------------|
| Individuals or groups flooding systems with excessive traffic | Disrupt availability, prevent legitimate access |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Botnets, automated scripts, or crafted malicious inputs | Use traffic filtering, load balancing, intrusion detection, and resource monitoring |

# Distributed Denial-of-Service (DDoS) Attack

A **Distributed Denial-of-Service (DDoS) attack** is a denial-of-service attack launched **simultaneously from multiple sources** to cause a complete or partial outage.  
By leveraging many compromised devices, attackers generate massive traffic or resource requests that overwhelm the target.

---

## Characteristics

- Originates **from many sources at once** (unlike a single-source DoS).  
- Attackers control **botnets** — networks of malware-infected devices (bots/zombies) — to send coordinated traffic or requests.  
- A botnet can include **hundreds to thousands** of devices, each contributing traffic that, in aggregate, overwhelms servers or network devices.  
- Modern attackers may use **AI** to:  
  - Analyze traffic patterns and predict the optimal bot count and timing.  
  - Monitor bot performance in real time and adjust attack parameters for maximum impact.  
- Common targets: web servers, application servers, ticketing systems, APIs, and other internet-facing services.

---

## Example

- An attacker instructs a botnet to send a flood of page requests to a web server in a short window. The sudden surge exhausts server resources (CPU, memory, network), causing the service to slow dramatically or become unavailable to legitimate users.  
- Legitimate sudden spikes (e.g., ticket sales) can mimic DDoS symptoms and also overload systems if capacity planning is inadequate.

---

## Profile Summary

| **Who launches them?** | **What is their objective?** |
|------------------------|------------------------------|
| Organized attackers using botnets (criminal groups, hacktivists, or contractors) | Disrupt availability, cause downtime, or create collateral damage |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Botnets (compromised devices), orchestration tools, sometimes AI for optimization | Use scalable defenses: traffic filtering (WAF/rate limiting), CDN and DDoS mitigation services, load balancing, capacity planning, network-level scrubbing, and real-time monitoring/alerting |

# Phishing

**Phishing** is the practice of sending **fraudulent messages** that appear to come from a **trusted source**, with the intent to trick users into taking a harmful action.  
It blends **social engineering** with **technical deception** to exploit human trust.

---

## Characteristics

- Delivered via **email, text messages (smishing), or phone calls (vishing)**.  
- Messages are crafted to look **legitimate and urgent**, often imitating banks, companies, or colleagues.  
- Attacks aim to **deceive users** into:  
  - Installing malware  
  - Enabling remote access  
  - Divulging sensitive credentials or financial information  
- Common red flags: spelling errors, generic greetings, suspicious links, or unexpected attachments.  

---

## Example

- An attacker sends an email with a **malicious attachment** or a link to a **spoofed website**.  
- When the user clicks or opens it, they may:  
  - **Install malware** unknowingly  
  - Be redirected to a **fake login page** designed to steal usernames and passwords  

---

## Profile Summary

| **Who launches them?** | **What is their objective?** |
|------------------------|------------------------------|
| Cybercriminals, scammers, or organized groups | Steal sensitive data, gain unauthorized access, or deliver malware |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Email accounts, spoofing tools, social engineering techniques | Train users to recognize phishing, use spam filters, multi-factor authentication (MFA), and URL/email verification tools |

# Spear Phishing

**Spear phishing** is a targeted form of phishing that aims at a **specific person, group, or organization**.  
Attackers invest time in research to craft personalized, highly convincing messages that increase the likelihood the target will take the desired action.

---

## Characteristics

- **Targeted** — uses personal or organizational details to increase credibility.  
- Attackers **research targets** via social media, corporate sites, public records, and data leaks.  
- Messages are **personalized and relevant** (job role, recent events, contacts), making them harder to spot than mass phishing.  
- **AI/automation** is increasingly used to generate realistic, tailored emails and to scale personalization while retaining high quality.  
- Typical goals: credential theft, fraudulent fund transfers, privilege escalation, or initial access for deeper compromise.

---

## Example

- An attacker gathers details about a target from LinkedIn and company pages, then **calls pretending to be a bank representative** claiming the account is compromised.  
- Because the attacker references legitimate personal or account details, the victim is convinced and **transfers money** to an attacker-controlled account or reveals MFA/passcodes.

---

## Defensive Considerations

- **User training** focused on targeted scams (how to verify requests that reference personal details).  
- **Multi-Factor Authentication (MFA)** to reduce impact of credential theft.  
- **Email authentication and filtering**: SPF, DKIM, DMARC, advanced spam/phishing filters.  
- **Verification procedures** for high-risk requests (out-of-band confirmation for wire transfers or sensitive actions).  
- **Least privilege & segmentation** to limit what a compromised account can access.  
- **Monitor for account takeover signals** (unusual logins, geo-anomalies, password resets) and alert for suspicious behavior.  

---

## Profile Summary

| **Who launches them?** | **What is their objective?** |
|------------------------|------------------------------|
| Skilled cybercriminals and targeted threat actors (criminal gangs, nation-state, or opportunistic attackers) | Steal credentials, commit fraud, gain foothold for deeper intrusion |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Personal reconnaissance, social engineering expertise, spoofing tools, increasingly AI for personalization | Train users on targeted scams, enforce MFA, implement SPF/DKIM/DMARC and advanced email filtering, require out-of-band verification for sensitive requests |

# Malware

**Malware** is a broad term for **malicious software** designed to harm systems, data, or users **without their informed consent**.  
It can disrupt operations, steal information, or render systems inoperable.

---

## Characteristics

- Installed often through **unintentional user actions** (e.g., downloading a file, opening an attachment, or running a program).  
- Once active, malware may:  
  - **Block access** to files or systems  
  - **Steal information** (credentials, financial data, intellectual property)  
  - **Cause operational damage** (slowing, crashing, or disabling systems)  
- Comes in many forms: viruses, worms, trojans, spyware, adware, ransomware, rootkits, and keyloggers.  
- **AI-enhanced malware**: Uses adaptive techniques to **evade detection** by antivirus or monitoring tools, making it harder to contain.  

---

## Example

- **Keyloggers** capture keystrokes to steal sensitive data like usernames, passwords, or banking info.  
- **Ransomware** encrypts files and demands a ransom for decryption, often paid in cryptocurrency.  
- Other malware may create backdoors, allowing attackers remote control of the system.  

---

## Defensive Considerations

- Use **endpoint protection** (antivirus, EDR solutions).  
- Apply **regular software patching** to close known vulnerabilities.  
- Train users to avoid **suspicious downloads, links, and attachments**.  
- Maintain **regular backups** to recover from ransomware without paying attackers.  
- Employ **network segmentation and monitoring** to prevent lateral movement.  
- Use **AI-driven security tools** that adapt alongside evolving threats.  

---

## Profile Summary

| **Who launches them?** | **What is their objective?** |
|------------------------|------------------------------|
| Cybercriminals, nation-state actors, or malicious insiders | Steal data, extort victims, disrupt operations, or gain unauthorized access |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Malware kits, exploit frameworks, AI-enhanced evasion tools | Deploy endpoint protection, patch systems, train staff, back up data, segment networks, and monitor for anomalies |

# Man-in-the-Middle (MitM) Attack

A **Man-in-the-Middle (MitM) attack** occurs when an attacker **inserts themselves into communications** between a client and a server.  
The attacker can **intercept, read, alter, or redirect** messages exchanged between the two parties without their knowledge.

---

## Characteristics

- Attacker positions themselves **between two communicating parties** (client ↔ server) to eavesdrop or manipulate traffic.  
- Can be performed on **unsecured Wi-Fi networks, compromised routers, or via ARP/DNS spoofing**.  
- Goals include **credential theft, session hijacking, data interception, or injecting malicious content**.  
- May be passive (just listening) or active (modifying traffic, redirecting to fake pages).  
- Modern MitM attacks can leverage SSL/TLS weaknesses or man-in-the-browser techniques (e.g., compromised browser extensions).

---

## Example

- An attacker configures a **free Wi-Fi hotspot** in a busy location.  
- Victims connect and their traffic passes through the attacker’s system, allowing the attacker to **inspect communications**, capture credentials, redirect users to **fake login pages**, or inject malicious content into web pages.

---

## Defensive Considerations

- **Use HTTPS/TLS everywhere**; enforce HSTS to prevent downgrade attacks.  
- **Verify certificates** and use certificate pinning where appropriate.  
- Avoid unsecured public Wi-Fi or use a **trusted VPN** when on untrusted networks.  
- Implement **network segmentation** and secure router configurations (disable default creds, apply firmware updates).  
- Use **MFA** to reduce impact of credential interception.  
- Deploy **intrusion detection/prevention** (IDS/IPS) and monitor for ARP/DNS anomalies and unusual session behavior.

---

## Profile Summary

| **Who launches them?** | **What is their objective?** |
|------------------------|------------------------------|
| Opportunistic attackers, cybercriminals, or advanced actors exploiting network weaknesses | Intercept, steal, or manipulate data in transit; hijack sessions; capture credentials |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Network access (rogue APs, compromised routers), spoofing tools, SSL/TLS downgrade exploits | Enforce TLS/HTTPS, HSTS, VPN usage on public Wi-Fi, certificate verification/pinning, MFA, network monitoring and IDS/IPS |

# Domain Name System (DNS) Attack

The **Domain Name System (DNS)** translates human-friendly domain names (e.g., `bmw.com`) into IP addresses that computers use.  
A **DNS attack** manipulates or disrupts that resolution process to **redirect users**, **deny access**, or otherwise tamper with internet traffic.

---

## Characteristics

- Targets the **DNS infrastructure** (resolvers, caches, registrar records, or routers).  
- Common tactics: **DNS cache poisoning**, **DNS hijacking**, **domain takeover**, and **DNS amplification**.  
- Effects range from **user redirection to malicious sites**, to **service disruption** and loss of trust in legitimate domains.  
- Attackers may compromise routers, registrars, or DNS servers to change resolution behavior.  
- DNS-based attacks can be stealthy (users think they’re visiting a legitimate site) or noisy (large-scale outages).

---

## Example

- Attackers compromise home or small office **wireless routers** so that normal domain lookups are redirected to malicious sites.  
- Victims who visit what looks like a valid website are instead sent to a page that **delivers malware**. That malware can turn the device into a bot, which is then used to propagate further compromises or join a botnet.

---

## Defensive Considerations

- Use **DNSSEC** (DNS Security Extensions) to validate DNS responses and reduce cache-poisoning risks.  
- Harden and update **DNS servers and resolvers**; restrict zone transfers and use strong registrar account protections (2FA, access controls).  
- Monitor DNS traffic for anomalies (unexpected IPs, sudden TTL changes, unusual query patterns).  
- Secure customer/employee routers and edge devices (change default credentials, apply firmware updates).  
- Employ **DNS filtering/response policies** and reputable recursive DNS services with anti-abuse features.  
- Maintain incident response playbooks for domain hijacking or registrar compromise scenarios.

---

## Profile Summary

| **Who launches them?** | **What is their objective?** |
|------------------------|------------------------------|
| Cybercriminals, organized gangs, or advanced actors targeting DNS infrastructure | Redirect users to malicious sites, distribute malware, disrupt access, or hijack domains |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Compromised routers/servers, access to registrar accounts, or botnets for amplification | Deploy DNSSEC, harden DNS/registrar accounts, monitor DNS telemetry, secure edge devices, use DNS filtering and reputable recursive DNS services |

# SQL Injection (Structured Query Language Injection)

**SQL (Structured Query Language)** is used to access, manage, and query relational databases.  
**SQL injection** occurs when an attacker inserts malicious SQL code into input fields or parameters that are then executed by the database, allowing the attacker to read, modify, or delete data.

---

## Characteristics

- Exploits **unsanitized user input** in web applications (forms, URL parameters, headers, cookies).  
- Can allow attackers to **bypass authentication**, **exfiltrate data**, **modify or delete records**, or even **drop entire databases**.  
- One of the **most common web application attacks** (OWASP Top Ten historically).  
- Attackers may use **automation and AI** to discover vulnerable endpoints and craft payloads at scale.  
- Vulnerabilities often stem from **improper input validation**, dynamic SQL construction, or excessive database privileges.

---

## Example

- Attackers submit SQL fragments in a web form (e.g., ` ' OR '1'='1` ) that alter the intended query logic, causing the application to return all user records or bypass login checks.  
- Real-world case: Attackers used SQL injection against a company website to steal large volumes of customer data (e.g., high-profile breaches like TalkTalk in 2015).

---

## Defensive Considerations

- **Use parameterized queries / prepared statements** instead of concatenating SQL strings.  
- Implement **input validation and sanitization**; enforce allow-lists for expected values.  
- Apply the **principle of least privilege** to database accounts (only grant required permissions).  
- Employ **stored procedures** cautiously (they are useful but not a silver bullet).  
- Use **web application firewalls (WAFs)** to block common injection patterns and automated scanning.  
- Conduct **regular code reviews and security testing** (SAST/DAST), and include SQLi tests in pentests.  
- Monitor database queries and alerts for anomalous activity (unexpected SELECTs, large dumps, or DROP statements).

---

## Profile Summary

| **Who exploits it?** | **What is their objective?** |
|----------------------|------------------------------|
| Cybercriminals, opportunistic attackers, and advanced threat actors | Steal, alter, or destroy data; escalate access; bypass authentication |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Automated scanners, SQL payload libraries, and AI-driven discovery tools | Use parameterized queries, validate/sanitize input, enforce least privilege, deploy WAFs, run SAST/DAST and pentests |

# Artificial Intelligence (AI) in Cyberattacks

Attackers are increasingly using **AI** to improve the **speed, scale, and sophistication** of cyberattacks.  
Machine learning and deep learning enable adversaries to adapt faster than traditional defenses, making AI a powerful tool in offensive cyber operations.

---

## Key Applications of AI in Cyberattacks

### 1. Task Automation
- **AI automates repetitive tasks**, allowing attackers to operate at massive scale.  
- Example: AI-generated and mass-distributed **phishing emails** tailored for higher success rates.  

### 2. Detection Evasion
- AI-powered malware can **adapt and morph** to avoid detection.  
- Uses **machine learning algorithms** to learn from failed detection attempts and alter code accordingly.  
- Results in polymorphic malware that traditional antivirus solutions struggle to stop.  

### 3. Target Identification
- Sophisticated AI algorithms analyze **large datasets** to find:  
  - Vulnerable systems  
  - High-value assets or organizations  
- Makes attacks **more efficient and effective** by focusing resources on the weakest or most profitable targets.  

### 4. Social Engineering
- AI enhances deception through **deep learning**.  
- Attackers create **deepfakes** (fake video, audio, or images) to impersonate trusted individuals.  
- Example: An attacker uses an **audio deepfake** of a CEO to trick employees into transferring funds or sharing sensitive information.  

---

## Defensive Considerations

- Incorporate **AI-driven defense systems** (threat intelligence, anomaly detection, automated response).  
- Train employees to detect **AI-enhanced phishing and deepfakes**.  
- Use **multi-factor authentication (MFA)** and out-of-band verification to counter AI-driven impersonation attempts.  
- Continuously update and retrain security models to counter evolving AI tactics.  

---

## Profile Summary

| **How attackers use AI** | **Impact** |
|---------------------------|------------|
| Task automation | Enables mass phishing, faster scanning, and large-scale exploitation |
| Detection evasion | Produces adaptive malware that bypasses traditional defenses |
| Target identification | Identifies weakest/vulnerable systems or high-value victims |
| Social engineering | Creates convincing deepfakes and impersonations to trick humans |

**Note**: AI has introduced a new challenge for defenders — cybersecurity strategies must now evolve to **incorporate AI** in order to effectively **counter AI-enhanced threats**.

