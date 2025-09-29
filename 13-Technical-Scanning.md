# Technical Scanning

## Introduction
Technical scanning covers the tools and techniques attackers use to discover systems, services, and vulnerabilities on networks. During the **reconnaissance** phase of an attack, scanning reveals useful information (live hosts, open ports, service versions, network layout) that helps an attacker plan their next moves. Defenders use the same techniques to find and remediate weaknesses before attackers exploit them.

## Why it matters
- Scanning turns unknown networks into actionable maps.  
- It reduces attacker uncertainty and helps prioritize targets.  
- Defensive scanning (proactive discovery) is a core part of good security hygiene.

## Common scanning techniques (examples)
- **Host discovery / ping sweeps** — find which IPs are live.  
- **Port scanning** (e.g., TCP/UDP scans) — identify open services.  
- **Service/version detection / banner grabbing** — learn what software (and versions) are running.  
- **Vulnerability scanning** — check services/hosts for known CVEs and misconfigurations.  
- **Network mapping / traceroute** — reveal network topology and hops.

## Learning objectives
After completing this module, you should be able to:

- **Explain the purpose** of common technical scanning techniques and the types of information they provide.  
- **Perform basic network reconnaissance** using standard network scanning tools (e.g., tools for host discovery, port/service enumeration, and vulnerability checks).

---

# Why Technical Scanning?

Technical scanning is a core activity for both attackers **and** defenders. It reveals the technical makeup of devices and networks so that investigators can turn unknown systems into actionable information.

## Purpose
Technical scanning helps answer key questions about a target device or network, for example:
- **What operating system is in use?**  
- **What services are running?**  
- **Are any services vulnerable to known exploits?**

## Common Techniques (what they reveal)
- **Ping test** — verifies whether a host is reachable (alive).  
- **Traceroute** — maps the network path and intermediate hops between you and a host.  
- **Port scanning** — identifies open TCP/UDP ports and which services are listening.  
- **Vulnerability scanning** — scans services/hosts for known CVEs, misconfigurations, and weak settings.  
- **Search engines for the internet** — using web search (and advanced operators) to find exposed services, config files, or leaked data.  
- **Network scanning** — discovers devices on a network and enumerates hosts, subnets, and services.

## Why it matters
- **For attackers:** reduces uncertainty and helps choose the most effective attack vectors.  
- **For defenders:** enables proactive discovery and remediation of exposed services and vulnerabilities.  
- **Net effect:** scanning turns a blind network into a prioritized list of targets and mitigations.

## Quick reminder
- Scanning can be intrusive and may trigger alerts or violate policy/law — always have authorization before performing scans on networks you do not own or manage.

# Ping Test Overview

## How It Works
- A **ping test** measures the time it takes for a packet to travel between devices.
- It uses **ICMP (Internet Control Message Protocol)**:
  - **Echo request**: sent to the target IP.
  - **Echo reply**: confirms the device is active and reachable.
- Think of a packet like a **digital postcard**.

## What It Provides
- Confirms if a device is **responsive**.
- When repeated (sweep), it shows how many devices are on the network.
- Helps **debug networking issues**.
- Uses **Time to Live (TTL)** to show how many hops (routers) the packet traveled:
  - Each router decreases TTL by 1.

## Example
- Packet starts with TTL = 120.
- Reaches target with TTL = 108.
- Means the packet passed through **12 hops**.

## How to Run
- On Windows Command Prompt:
  ```bash
  ping target_name

# Traceroute Overview

## How It Works
- **Traceroute** is a network diagnostic tool that maps the path between a device and a destination.
- It works by sending packets with **increasing or decreasing TTL (Time to Live)** values.
- When a packet’s TTL reaches **zero**, the router/switch handling it sends back an **error message** to the scanning device.
- This allows the scanning device to identify each "hop" (network device) along the route.

## What It Provides
- A map of the network path between the scanner and the destination.
- Shows the **routers** (connect network to the internet) and **switches** (integrate devices on the network).
- Helps identify how many hops exist and where delays or issues occur.

## Example
- Target is **12 hops away**.
- A packet sent with **TTL = 11** will expire at hop 11.
- The error message reveals the IP of the device **11 hops away**.
- Repeating this with varying TTL values builds a **list of all network nodes** to the destination.

## How to Run
- On Windows Command Prompt:
  ```bash
  tracert target_name

# Port Scanning — Summary

## How it works
- **Ports** are numeric connection points on an IP address that allow specific services (HTTP, RDP, SMTP, etc.) to send and receive data.  
  - **Analogy:** IP address = building, port = floor.
- A **port scan** systematically probes a host's ports to determine whether each port:
  - **Accepts** the connection → **Open** (service likely present)
  - **Rejects** the connection → **Closed**
  - **Gives no response** → **Filtered** (often blocked by a firewall or packet filter)
- Scanners send protocol-specific packets (TCP, UDP, or other) and infer service presence from responses or lack thereof.

## What it provides
- Maps likely **services** running on a host by identifying open ports.
- Reveals the host’s **attack surface** so defenders can close unnecessary ports or apply controls.
- Helps investigators understand a machine’s role on the network by checking well-known ports.

## Port ranges & notable ports
- TCP/UDP ports range from **0–65,535**.
- **Well-known ports:** 0–1,023 (common, standardized services).
- Examples:
  - **TCP 80** — HTTP (web servers)
  - **TCP 445** — SMB / Windows file sharing (historically targeted by malware like WannaCry)
  - **TCP 3389** — Microsoft RDP (remote desktop; high-risk if exposed)

## Example use
- If **port 80** is open → likely a web service is running.
- If **port 445** is open → Windows file-sharing services exist; patching and access controls should be checked.
- If **port 3389** is open → remote desktop may be exposed; consider VPN, MFA, or blocking from the internet.

## Common techniques / tools (brief)
- **SYN scan, TCP connect, UDP scan, banner grabbing** — different tradeoffs in speed, stealth, and accuracy.
- Popular tool: **nmap**
  ```bash
  # basic TCP scan of common ports
  nmap -sT target_ip_or_hostname

  # scan all TCP ports
  nmap -p- target_ip_or_hostname

  # service/version detection
  nmap -sV target_ip_or_hostname

# Vulnerability Scanning — Summary

## How it works
- **Vulnerability scanning** is an automated process that inspects devices and applications to find known security weaknesses.
- Scanners use multiple techniques, including:
  - **Dynamic scanning (active testing):** simulates attack techniques (e.g., SQL injection, XSS) to discover exploitable flaws.
  - **Version detection:** identifies software and service version numbers (e.g., Apache 2.4.29).
  - **OS detection:** determines the operating system (e.g., Windows Server 2019, macOS).
  - **Configuration checks:** verifies insecure settings or default credentials.
- Many scanners combine passive discovery (collecting banners, configs) with active probes that attempt benign exploitation to confirm vulnerabilities.

## What it provides
- A prioritized list of **vulnerabilities** (usually with severity ratings) that need remediation.
- Actionable details: affected host, vulnerable component/version, proof-of-concept or evidence, and remediation suggestions.
- Ongoing visibility into an organization’s **attack surface** and opportunities to patch, reconfigure, or mitigate risks before attackers exploit them.

## Example
- A scanner connects to a web server, detects it runs an **outdated application version** with a known CVE, attempts a controlled exploit to confirm the issue, and reports the finding with remediation guidance.

## Common techniques & outputs
- **Credentialed vs. uncredentialed scans:** credentialed scans log in (deeper visibility); uncredentialed scans probe externally.
- **False positives/negatives:** scanners can misidentify or miss issues — human validation is recommended.
- **Outputs:** vulnerability ID, CVE references, CVSS severity score, affected asset list, remediation steps, and evidence (request/response snippets).

## Common tools (examples)
- Commercial & open-source scanners: **Nessus**, **Qualys**, **OpenVAS/Greenbone**, **Rapid7 Nexpose**, **Burp Suite** (web-app scanning).
- CI/CD integration: many scanners offer APIs or automation for build pipelines.

## Security & legal note
- **Only scan targets you own or have explicit, written permission to test.**  
- Active/dynamic scans can be intrusive, may crash services, or be illegal in some jurisdictions. Treat vulnerability scanning as an authorized security activity and coordinate with asset owners.

# Shodan — Search Engine for Internet-Connected Devices

## What it is
- **Shodan** is a specialized search engine that indexes internet-connected devices and the services they expose (sometimes described as “the world’s first search engine for internet-connected devices”).
- Instead of crawling web pages like Google, Shodan **scans the Internet** and stores service banners, open ports, device types, software versions, and other metadata.

## How it works (high-level)
- Shodan performs large-scale scans of IP ranges and records responses from devices (service banners, headers, TLS certs, etc.).
- It indexes those responses so users can search by:
  - IP address or range
  - Service or port (e.g., `port:22` for SSH)
  - Product or banner string (e.g., `product:Apache`)
  - Location, organization, or other metadata

## What it provides
- A searchable catalog of **internet-exposed services and devices** (cameras, routers, industrial control systems, web servers, databases, etc.).
- Quick visibility into **where particular software or hardware is deployed** globally and whether known services/ports are exposed.
- Useful for large-scale research, asset discovery, and threat intelligence.

## Use cases / examples
- Security researchers: find instances of a vulnerable product/version across the globe to prioritize disclosure or mitigation.
- Network defenders: discover exposed assets belonging to an organization (by ASN, IP range, or domain).
- Attackers: can similarly locate misconfigured, outdated, or exposed devices to target — which is why access must be handled responsibly.

## Example query ideas
- `port:3389 country:"US"` — list RDP endpoints in the United States.
- `product:"Apache" version:"2.4.29"` — find servers running a specific Apache version.
- `org:"ExampleCorp"` — find services exposed by a specific organization.

## Legal & ethical note
- Data from Shodan is powerful and sensitive. **Do not use Shodan to scan, access, or attack systems you do not own or have explicit authorization to test.**
- Use Shodan for defense, research, or responsible disclosure. Misuse can be illegal and unethical.

## Common tools & access
- Shodan website & web interface
- Shodan API (programmatic searches and integration)
- Shodan CLI and community tools that consume its API

## Want a one-line summary for a slide?
- Shodan = **search engine for internet-connected devices** — indexes service banners and exposed ports to help defenders and researchers locate exposed assets at scale.

# Network Scanning — Summary

## What it is
- **Network scanning** collects information about networks by probing hosts and services to assess status, connectivity, and security.
- Administrators use network scans for asset discovery, inventory, troubleshooting, and vulnerability assessment — the same tools can be used by attackers for reconnaissance.

## Common tool: Nmap
- **Nmap (Network Mapper)** is the most well-known open-source network scanner (Windows, macOS, Linux).
- Core feature: **port scanning**, but Nmap also supports many other capabilities used for network investigation.

## Key Nmap capabilities (flip-card style)
- **Network path discovery / Traceroute:** reveals the path from scanner to host and intermediate devices (hops).  
- **Version & OS detection:** identifies software versions and operating systems running on hosts.  
- **Firewall detection:** can infer the presence and sometimes type of firewall or packet-filtering behavior.

## Usability
- Nmap is primarily a **command-line tool** (powerful, scriptable, flexible).
- **Zenmap** is the official GUI for Nmap — helpful for beginners:
  - Lets you build scans via a friendly interface.
  - Shows the equivalent Nmap command-line invocation for learning and reproducibility.

## Typical use cases
- Asset discovery and inventory (what devices and services exist).
- Incident response and forensics (where is traffic going; which hosts are reachable).
- Pre-assessment before vulnerability scans or penetration tests.
- Network troubleshooting (latency, unreachable hosts, routing issues).

## Example (basic Nmap commands)
```bash
# quick scan of common ports
nmap target_ip_or_hostname

# aggressive scan (OS, version, script scanning)
nmap -A target_ip_or_hostname

# scan a range or subnet
nmap 192.168.1.0/24

# AI in Technical Scanning — Summary

## How it works
- **Artificial Intelligence (AI)** and **Machine Learning (ML)** enhance network scanning by going beyond basic detection to deliver deeper analysis.
- Capabilities include:
  - Automatically **analyzing and categorizing vulnerabilities**.
  - **Prioritizing vulnerabilities** based on severity and business impact.
  - **Learning from past scans** to detect patterns, trends, and anticipate emerging threats.

## What it provides
- **Faster scanning:** streamlines analysis of large, complex networks.
- **Improved accuracy:** reduces human error and false positives.
- **Proactive defense:** identifies trends to predict and mitigate future risks.
- **Efficiency:** frees analysts to focus on confirmed threats instead of chasing noise.

## Example — IBM QRadar® Advisor with Watson™
- Uses **AI + ML** to analyze massive volumes of security data.  
- Functions include:
  - Investigating offenses to determine if they are real threats.
  - Reducing **false positives** by filtering out benign events.
  - Delivering **actionable insights** for security teams.  
- Result: analysts spend more time addressing **confirmed threats** and less time triaging irrelevant alerts.

## Key takeaway
AI-driven scanners make network security **smarter, faster, and more predictive** by combining automation with intelligent analysis.



