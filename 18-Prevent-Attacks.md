# Goal of Attack Prevention Strategies — Summary

## Core idea
- No **perfect, unbeatable security strategy** exists — attackers continually evolve tactics.  
- The realistic goal: make attacks **too costly, time-consuming, or complex** for most adversaries.  
  - Example: If an attack costs **$100,000** but yields only **$80,000 value**, the attacker will likely walk away.  

## Effective approach
- Focus on **raising the cost and effort of attacks** to deter all but the most determined adversaries.  
- Practical strategies include:  
  - **Layered defenses** (multiple protective barriers).  
  - **Regular updates and patching** to close vulnerabilities.  
  - **Threat intelligence** to anticipate emerging threats.  

## Ultimate goal
- Reduce **operational risk** to an **acceptable level** through a balanced mix of:  
  - **Education** (training users to spot and prevent threats).  
  - **Processes** (policies, incident response, governance).  
  - **Technologies** (tools and security solutions).  

## Common prevention strategies
- **Reduce the attack surface** — limit exposure by minimizing unnecessary services, apps, or access points.  
- **Create a Demilitarized Zone (DMZ)** — separate internal systems from external-facing services.  
- **Principle of Least Privilege** — grant users only the access they need, nothing more.  
- **Manage software vulnerabilities** — patch and update consistently to reduce known risks.  
- **Defense in depth** — use multiple layers of defense so if one fails, others remain effective.  

# Reduce the Attack Surface — Summary

## Definition
- The **attack surface** is all the points in a system where an attacker could attempt to:  
  - Enter the system  
  - Impact operations  
  - Access or steal data  
- Includes **interfaces, protocols, services**, and any other potential vulnerability points.  

## Key concept
- **Larger attack surface = greater risk of infiltration.**  
- A core goal of any security strategy is to **minimize the attack surface**, making systems less attractive and harder to breach.  

## Example
- An organization restricts access to its **payment record system** so employees can only use it from specific office locations.  
- This eliminates external internet access points, forcing attackers to compromise a **trusted internal device first**.  
- Result: attackers face **added complexity and difficulty**, lowering the likelihood of a successful breach.  

## Modern challenge
- Organizations are expanding access options (e.g., **remote work**, **personal devices**, **BYOD policies**).  
- These features improve **flexibility and services** but also **expand the attack surface**.  
- Maintaining a **secure perimeter** has become more complex, requiring proactive **monitoring and defense**.  

# Create a Demilitarized Zone (DMZ) — Summary

## Definition
- A **Demilitarized Zone (DMZ)** is a **network segment** positioned between an organization’s **internal private network** and the **internet**.  
- Acts as a **buffer zone**, adding an extra layer of safety.  
- Even if attackers breach the DMZ, the **internal network remains protected**.  

## Purpose
- DMZs host servers that need to be **accessible from the internet** but still require protection.  
- Common servers in a DMZ:  
  - Web servers  
  - Email servers  
  - File Transfer Protocol (FTP) servers  
  - DNS servers  
- These servers typically contain **public data**, not sensitive internal information.  

## How it works
- The **internet connects to the DMZ**, which is placed between **external and internal firewalls**.  
- **External users** can access applications or services in the DMZ (e.g., email, order systems).  
- Sensitive systems (e.g., **employee records, customer financial data**) remain protected behind the **internal firewall**.  

## Example
- A customer may access a company’s digital payment system hosted in the DMZ.  
- However, they **cannot access sensitive servers** in the internal network, such as HR databases or confidential client records.  

## Key takeaway
- A DMZ provides **controlled, limited access** to necessary services without exposing critical internal systems, strengthening **overall network security**.  

# Follow the Principle of Least Privilege — Summary

## Definition
- The **principle of least privilege (PoLP)** means granting a **user or application only the minimum permissions** necessary to perform their role or function.  
- Reduces unnecessary access rights, limiting potential damage from misuse or compromise.  

## Example
- An organization configures its **HR database** so managers have **read-only access** to job role data they oversee.  
- If an attacker steals a manager’s credentials:  
  - They can view only those records (limited confidentiality impact).  
  - They **cannot modify data** (read-only restriction).  
  - They **cannot access other applications** or departments.  
- This containment reduces the **risk value** and limits the **blast radius** (the scope of impact from an attack).  

## Key takeaway
- Applying PoLP ensures that even if credentials are compromised, the attacker’s **ability to cause harm is minimized**.  
- By reducing permissions, organizations **reduce consequences and overall risk exposure**.  

# Software Vulnerability Management

## Overview
- **Software vulnerability management**: Monitoring and mitigating vulnerabilities in software systems.
- **Patch management**: Applying patches and updating systems as fixes become available.

## Vendor Support
- Vendors may stop supporting older versions (e.g., Microsoft ending support for Windows 7).
- Unsupported software no longer receives patches → increases risk of attack.
- Organizations should:
  - Use supported versions whenever possible.
  - Apply **compensating controls** (e.g., disable features, strengthen network security, increase monitoring) if using unsupported software.

## Updates and Risks
- Updating to the latest versions reduces attack risk.
- New versions may also introduce new vulnerabilities.
- Organizations must:
  - Check with vendors for patch release timelines.
  - Apply temporary compensating controls if no fix is available.

## Vulnerability Scanners
- **Purpose**: Identify flaws before attackers exploit them.
- Types:
  - **Network-based scanners**: Actively test for vulnerabilities (e.g., outdated software, missing patches, misconfigurations, weak passwords).
  - **Source code scanners**: Analyze static code for errors.
- Both provide valuable insight into system weaknesses.

# Defense in Depth

## Overview
- **Definition**: A layered security strategy that uses multiple controls to protect assets.
- **Origin**: Borrowed from the military concept—rather than relying on a single defense, use multiple layers.

## Layers of Security
- **Network defenses**: Firewalls
- **Device defenses**: Malware scanners
- **Data defenses**: Encryption

## Key Point
- For an attack to succeed, it must compromise or bypass **all layers of defense**, making successful attacks significantly more difficult.





































