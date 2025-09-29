# Structure of a Cyberattack

As computing environments evolve, adversaries adapt their techniques. A piece of malware that worked yesterday may fail today after vendors ship a patch — yet the *overall structure* of many cyberattacks remains useful to study. Two industry frameworks commonly used to model and analyze attacks are the **Lockheed Martin Cyber Kill Chain®** and the **MITRE ATT&CK®** matrix.

---

## Learning objectives
- **Explain** the overall stages of a typical cyberattack using the Cyber Kill Chain.  
- **Apply** the Cyber Kill Chain to a realistic scenario to identify likely attacker goals and controls.  
- **Identify** attacker tactics and techniques using the MITRE ATT&CK matrix to support detection and response.

---

## 1) Lockheed Martin — Cyber Kill Chain (high level)

The Cyber Kill Chain models an attack as a sequence of phases from initial reconnaissance through mission completion. Common stage names (simplified):

1. **Reconnaissance** — Attacker collects information about targets (public profiles, IP ranges, employee names).  
2. **Weaponization** — Build or assemble the attack payload (malicious documents, exploit kits).  
3. **Delivery** — Send the payload to the target (phishing email, USB drop, drive-by download).  
4. **Exploitation** — Trigger the vulnerability (open document, exploit web app).  
5. **Installation** — Establish persistence (drop malware, install backdoor).  
6. **Command & Control (C2)** — Create a channel to remotely control compromised hosts.  
7. **Actions on Objectives** — Execute the attacker’s primary goals (data exfiltration, ransomware, destruction, lateral movement).

**Uses / benefits**
- Breaks an attack into actionable stages so defenders can place controls at each phase.  
- Encourages detection/prevention earlier in the chain (e.g., disrupt reconnaissance or delivery to stop later stages).  
- Easy to teach and apply to tabletop exercises and IR playbooks.

**Limitations**
- Linear model — real-world attacks may be iterative, non-linear, or skip stages.  
- Less granular about specific attacker techniques than ATT&CK.

---

## 2) MITRE ATT&CK (high level)

MITRE ATT&CK is a **knowledge base** of real-world adversary tactics, techniques, and procedures (TTPs).  
- **Tactics** = the *why* (high-level adversary goals like Persistence, Privilege Escalation, Lateral Movement).  
- **Techniques** = the *how* (concrete methods used to achieve those goals, often with sub-techniques).  
- Mapped to telemetry sources (processes, command lines, network activity, Windows event logs) to support detection engineering.

**Uses / benefits**
- Provides a **detailed, searchable catalogue** of attacker behavior tied to observed incidents.  
- Helps defenders: threat hunting, SIEM/EDR rule creation, detection gaps analysis, purple-team exercises, and cyber threat intelligence mapping.  
- Supports sharing and comparing incidents in a consistent language.

**Limitations**
- Large and detailed — can be overwhelming without prioritization.  
- Requires telemetry and tooling to operationalize effectively.

---

## How the two frameworks complement each other

- **Kill Chain = macro timeline** of an intrusion (good for strategy, playbooks, and early-stage prevention).  
- **ATT&CK = micro catalogue** of specific tactics & techniques that appear across kill-chain stages (good for detection rules, hunting, and IR).  
- Example mapping: *Delivery* and *Exploitation* (Kill Chain) → techniques like **Spearphishing Attachment** or **Exploit Public-Facing Application** (ATT&CK).  
- Use both: model the attack flow with Kill Chain, then drill into ATT&CK to identify exact telemetry and detections.

---

## Practical example (brief)
**Scenario**: Spear-phishing email leads to data exfiltration.

- **Kill Chain view**: Recon → Weaponize (malicious doc) → Deliver (spear-phish) → Exploit (macro) → Install (backdoor) → C2 → Actions on Objectives (steal data).  
- **ATT&CK view**:  
  - Recon: *Search Open Websites/Domains* (reconnaissance techniques)  
  - Delivery/Exploit: *Spearphishing Attachment (T1566.001)*, *Exploitation for Client Execution (T1203)*  
  - Persistence/C2: *Create or Modify System Process*, *Standard Application Layer Protocol (C2 channels)*  
  - Exfiltration: *Exfiltration Over C2 Channel (T1041)* or *Exfiltration Over Web Service (T1567)*

Defender actions: block the phishing domain (prevent delivery), enable macro-blocking and EDR for exploit detection (stop exploitation/installation), monitor outbound C2-like patterns and unusual data transfers (detect C2/exfiltration).

---

## How to apply these frameworks in an org
1. **Map common attack scenarios** to the Kill Chain to identify where current controls live and where gaps exist.  
2. **Select ATT&CK techniques** that are most relevant to your environment (industry, assets, threat intel).  
3. **Instrument telemetry** (process, network, auth logs, EDR) for those techniques and develop detections/hunts.  
4. **Run purple-team exercises**: simulate techniques from ATT&CK, observe detections, tune controls.  
5. **Update incident playbooks** using Kill Chain stages and ATT&CK technique IDs for clear triage and escalation steps.  

---

## Quick reference (one-line)
- **Kill Chain** = timeline of an intrusion (recon → weaponize → deliver → exploit → install → C2 → actions).  
- **MITRE ATT&CK** = detailed library of adversary tactics & techniques you can map to telemetry to detect and hunt threats.

---

# Lockheed Martin — Cyber Kill Chain® Framework

The **Cyber Kill Chain®** (Lockheed Martin) models a typical intrusion as a sequence of seven ordered stages.  
Treating an attack as a process (not a single event) helps defenders place controls and detection at each stage to **interrupt** the chain as early as possible.

> **Note:** “Kill Chain” is a Lockheed Martin term; the model is widely used for teaching and IR tabletop exercises.

---

## The Seven Steps

### 1. Reconnaissance  
**What:** Attacker gathers intelligence about the target (public profiles, IP ranges, software versions, employees, news, open ports).  
**Goal:** Find weaknesses and plan the attack.  
**Defender actions:** threat intel, external attack surface management, reduce public exposure, monitor unusual scanning.

---

### 2. Weaponization  
**What:** Attacker builds or acquires a payload to exploit an identified weakness (malicious document, exploit kit, malware).  
**Goal:** Produce a deliverable exploit tailored to the target.  
**Defender actions:** track exploit kits/zero-days, apply threat intelligence, harden dev/test environments, sandbox suspicious artifacts.

---

### 3. Delivery  
**What:** Attacker transmits the weapon to the target (phishing email, malicious link, drive-by download, removable media).  
**Goal:** Get the victim to execute or accept the payload.  
**Defender actions:** email filtering, URL protection, content sandboxing, user training, blocking risky file types, device control policies.

---

### 4. Exploitation  
**What:** The delivered payload runs and exploits a vulnerability (opening a malicious attachment, browser exploit, macro execution).  
**Goal:** Execute code on the target system.  
**Defender actions:** patch management, exploit mitigation (DEP/ASLR), endpoint protection (EDR), application whitelisting, macro restrictions.

---

### 5. Installation  
**What:** Malware establishes persistence (backdoors, new accounts, scheduled tasks, services).  
**Goal:** Maintain long-term access despite reboots/patching.  
**Defender actions:** EDR blocking/remediation, integrity checks, least-privilege accounts, monitoring for new services/accounts, configuration baselining.

---

### 6. Command & Control (C2)  
**What:** Attacker creates a channel to communicate with compromised hosts (HTTP/S, DNS, social platforms, custom protocols).  
**Goal:** Send instructions, exfiltrate data, update tools.  
**Defender actions:** egress filtering, DNS monitoring, proxy/SSL inspection, anomaly detection for beaconing, block known C2 IPs/domains, network segmentation.

---

### 7. Actions on Objectives  
**What:** Attacker completes mission goals (data exfiltration, lateral movement, privilege escalation, disruption, ransomware).  
**Goal:** Achieve the strategic outcome (steal, modify, destroy, extort).  
**Defender actions:** data loss prevention (DLP), monitoring for unusual data flows, rapid containment/quarantine, backups, incident response playbooks, legal/forensic readiness.

---

## How to Use the Kill Chain Practically

- **Map controls to stages:** Identify which existing controls detect/prevent activity at each step and where gaps exist.  
- **Prioritize early disruption:** Stopping an attacker at Recon/Delivery is cheaper and less disruptive than remediation after Installation or C2.  
- **Integrate with ATT&CK:** Use Kill Chain for high-level flow and MITRE ATT&CK to enumerate specific tactics/techniques for detection engineering.  
- **Exercise & measure:** Run tabletop/purple-team tests that simulate steps of the chain and measure detection/response times at each stage.  
- **Automate containment:** Where possible, automate isolation and blocking to prevent progression (e.g., auto-quarantine on suspicious EDR indicators).

---

## One-line summary
**Kill Chain = 7-stage intrusion timeline (Recon → Weaponize → Deliver → Exploit → Install → C2 → Actions).**  
Place layered defenses and detections at each stage to break the chain as early as possible.

# MITRE ATT&CK® Matrix

The **MITRE ATT&CK®** matrix is an open, community-driven knowledge base of **Adversarial Tactics, Techniques, and Common Knowledge** — pronounced “attack.”  
It catalogs real-world attacker **tactics** (the *why*) and **techniques** (the *how*), making it easier to map adversary behavior to telemetry and to build detections, hunts, and mitigations.

---

## How to read the ATT&CK matrix

- **Columns = Tactics** — high-level adversary objectives (e.g., Initial Access, Persistence, Privilege Escalation, Exfiltration).  
- **Cells under each column = Techniques** — specific methods used to achieve that tactic (each technique often has sub-techniques).  
- Each technique entry links to detailed guidance: detection data sources, examples, mitigation suggestions, and known actors who used it.  
- The matrix is **non-linear**: attackers pick techniques across tactics and iterate, adapt, or skip steps.

---

## Key uses & benefits

- **Detection engineering:** Map techniques to required telemetry (process, command-line, network, PowerShell logs, Windows events, etc.).  
- **Threat hunting:** Build hypotheses based on ATT&CK techniques and design hunts to find them in your environment.  
- **Gap analysis:** Compare existing detections/controls against ATT&CK to find blind spots.  
- **Purple teaming / red teaming:** Use ATT&CK techniques to plan realistic adversary emulations and validate defenses.  
- **Threat intelligence:** Describe adversary behavior in a consistent language for sharing and reporting.

---

## Example (reading + application)

**Scenario:** An attacker wants **credentialed access** (tactic).  
- ATT&CK technique: **Brute Force** (a technique listed under Credential Access).  
- Attack flow: The attacker runs automated attempts against login endpoints until credentials succeed.  
- Defender mapping: Instrument authentication logs, alert on high-volume failed logins, enforce rate-limits, enable account lockout & MFA.  
- If brute force fails, the attacker may switch to other techniques (e.g., credential stuffing, phishing, or taking advantage of exposed password databases).

---

## How to operationalize ATT&CK in your org

1. **Prioritize tactics/techniques** relevant to your industry, tech stack, and threat actors.  
2. **Map telemetry**: identify which logs/sensors show evidence for each technique (EDR, network flow, proxy, auth logs, DNS, cloud logs).  
3. **Develop detections & hunts** for high-risk techniques; document detection logic and false-positive handling.  
4. **Run tabletop & purple-team exercises** using ATT&CK techniques to test detection efficacy and response playbooks.  
5. **Track coverage**: maintain an ATT&CK matrix mapping showing which techniques are detectable, prevented, or not covered.  
6. **Feed findings into risk assessments** and prioritize engineering/remediation work based on technique prevalence and impact.

---

## Quick reference (one-line)
- **MITRE ATT&CK = a granular, searchable library of attacker tactics & techniques** you can map to telemetry to detect, hunt, and measure defensive coverage.

