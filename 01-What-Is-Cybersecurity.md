# Module 1: What is Cybersecurity?

## Introduction
- **Cost of breaches**: Global average total cost of a data breach = **USD 4.35M** (IBM Security, 2023).  
- **Cybercrime scale**: Expected to cost **USD 8T in 2023**, making it the **3rd largest economy** if ranked as a country (Cybersecurity Ventures).  
- **Digital integration**: IoT and digital technologies are embedded in banking, shopping, communication, and work.  
- **Challenge**: Expanding **digital footprints** increase vulnerability of personal and professional data.  
- **Solution**: Cybersecurity safeguards data, systems, and infrastructure.  

> *“The art of war teaches us to rely not on the likelihood of the enemy’s not coming, but on our own readiness to receive him...”* – **Sun Tzu**

---

## Learning Objectives
After completing this module, you will be able to:
1. **Define cybersecurity**
2. **Describe the three components**:
   - **Digital security**
   - **Human security**
   - **Physical security**
3. **Identify CIA triad objectives** and their relevance:
   - **Confidentiality**
   - **Integrity**
   - **Availability**
4. **List security controls** for each CIA objective.

# Cybersecurity

## Definition
Cybersecurity is the practice of **protecting and recovering data, networks, devices, and programs** from threats.  
- Threats may have **digital, human, or physical components**.  
- Effective cybersecurity must address **all three areas**.

---

## Key Examples of Cybersecurity Concerns
- **Fraudulent email (phishing):** A fraudster impersonates a bank and requests a PIN.  
- **Social engineering call:** An investigator tricks an employee into printing and leaving confidential files.  

Both illustrate that cybersecurity extends **beyond just technology**.

---

## Components of Cybersecurity

### 1. Digital Security
- **Focus**: Protecting data and systems from digital threats.  
- **Threats**: Malware (viruses, ransomware), hacking attempts, data theft.  
- **Controls**: Firewalls, encryption software, intrusion detection/prevention systems.  

### 2. Human Security
- **Focus**: Mitigating risks caused by human behavior (intentional or accidental).  
- **Threats**:  
  - Unintentional: Employee opens malicious attachment.  
  - Intentional: Insider leaks confidential data.  
- **Controls**: Security awareness training, phishing simulations, strong password policies.  

### 3. Physical Security
- **Focus**: Protecting tangible assets supporting digital infrastructure.  
- **Assets**: Workstations, server rooms, data centers.  
- **Threats**: Theft, tampering, fire, flooding, natural disasters.  
- **Controls**: Surveillance systems, access control measures (badges, biometrics), disaster recovery/business continuity plans.  

---

# CIA Triad

## Overview
- Cybersecurity aims to achieve **three core objectives**:  
  - **Confidentiality**  
  - **Integrity**  
  - **Availability**  
- Together, these form the **CIA Triad** – a cornerstone of cybersecurity frameworks and policies.  
- Organizations may prioritize one objective over the others depending on industry, operations, or risk profile.  

---

## 1. Confidentiality
- **Definition**: Ensuring that data is kept secret and only accessible to authorized users.  
- **Examples**:  
  - Software companies restrict access to **source code** for competitive advantage.  
  - Healthcare providers protect **patient records** (diagnoses, prescriptions) under privacy laws.  
- **Controls**: Access management, authentication, encryption, and data classification.  
- **Industry Context**:  
  - Most critical for **government intelligence agencies** where leaks may compromise national security or put lives at risk.  

---

## 2. Integrity
- **Definition**: Ensuring that data remains **accurate, consistent, and trustworthy**; preventing unauthorized modifications or destruction.  
- **Examples**:  
  - A $10 pizza transaction altered to $10,000 shows a breach of integrity.  
  - Errors may be **technical (system glitches)** or **human (data entry mistakes)**.  
- **Controls**: Hashing, checksums, audit trails, digital signatures, and role-based permissions.  
- **Industry Context**:  
  - Most critical for **banks**, where accurate financial data is essential to avoid losses or legal issues.  

---

## 3. Availability
- **Definition**: Ensuring **timely and reliable access** to data and systems when needed.  
- **Examples**:  
  - Customers expect **24/7 online banking** or retailer website access.  
  - School transcripts may take days but are still considered available within a **reasonable timeframe**.  
- **Controls**: Redundancy, backups, disaster recovery, DDoS protection, fault-tolerant infrastructure.  
- **Industry Context**:  
  - Most critical for **online retailers** where downtime can lead to lost business and reduced trust.  

---

# Controls for the CIA Triad

## Overview
- **Controls** = Safeguards or countermeasures used to **avoid, detect, counteract, or minimize** cybersecurity risks.  
- They apply to **digital, human, and physical assets** to ensure confidentiality, integrity, and availability.  

---

## 1. Controls for Confidentiality
- **Encryption**: Converts data into unreadable form unless decrypted with the correct key.  
- **Access Controls**: Restrict who can view, modify, or share data.  
  - Examples: Passwords, biometrics (fingerprints, retinal scans).  
- **Patch Management**: Regular software updates to close vulnerabilities that attackers could exploit.  

---

## 2. Controls for Integrity
- **Checksums**: Mathematical values that change if the underlying data changes → detect tampering.  
- **Access Controls & User Permissions**: Limit who can alter data and what changes they can make.  
- **Data Backups**: Restore data to a correct state if unauthorized modifications occur.  
- **Audit Trails**: Record who made changes, when, and what was altered → provide accountability.  

---

## 3. Controls for Availability
- **Redundant Systems & Backups**: Multiple servers or data stored in different locations to prevent loss.  
- **Antimalware & Firewalls**: Protect against attacks (e.g., malware, DDoS) that disrupt services.  
- **Disaster Recovery & Business Continuity Plans**: Predefined steps to restore services quickly and reduce downtime.  

---

# Evaluating Assets with the CIA Triad

## Overview
- In cybersecurity, an **asset** is something valuable to its owner.  
- Assets can be:  
  - **Digital**: Programs, code, databases, photo libraries.  
  - **Physical**: Servers, mobile phones, laptops.  
  - **Information assets**: Research reports, healthcare records, personal data.  

The CIA triad (Confidentiality, Integrity, Availability) can be applied to **personal or organizational assets** to evaluate their importance.

---

## Personal Examples of Assets
1. **Bank account**  
2. **Photo library**  
3. **Social media account**  
4. **Mobile phone**

---

## Rating Scale
Use the **1–5 scale** to assess the impact of losing CIA triad objectives for each asset:  
- **1 = Low consequence**: No noticeable impact.  
- **3 = Medium consequence**: Minor impact; a couple of hours of lost time.  
- **5 = High consequence**: Life-changing impact lasting months or years.  

---

## Example (Online Debate Submission)
- **Confidentiality**: If anonymity is lost → rating **2** (annoying, minor impact).  
- **Integrity**: If someone edits the post → rating **3** (argument, wasted time).  
- **Availability**: If the comment disappears → rating **4** (disruption in debate flow).  

---

## Key Takeaways
- Different assets have different values depending on your priorities.  
- **Highest-rated assets** should receive the strongest protections.  
- Example:  
  - Password manager → very strong password, never shared.  
  - Home Wi-Fi → may occasionally be shared with friends/family.  

Organizations use the same process: **prioritize protections around the most critical assets**.

