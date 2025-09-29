# Threat Actor Groups

Cybersecurity professionals often use the term **threat actor** instead of **attacker**.  
- **Attacker / Cyberattacker**: Someone who actively tries to bypass system or network security without authorization.  
- **Threat Actor / Malicious Actor**: An entity (person, group, or organization) that poses a cybersecurity threat. They may not have attacked yet, but they intend to do so.  

While both terms are similar, **threat actor** emphasizes the *potential* threat.

---

## Five Main Threat Actor Groups

### 1. Script Kiddie
- Inexperienced individuals who use pre-made tools or scripts.  
- Motivation: Curiosity, mischief, or recognition.  
- Limited skills and resources.  

### 2. Hacktivist
- Individuals or groups driven by political, social, or ideological causes.  
- Motivation: Raise awareness, protest, or disrupt organizations.  
- Techniques often include website defacement or denial-of-service attacks.  

### 3. Criminal Gang
- Organized cybercriminal groups seeking financial gain.  
- Motivation: Profit through theft, fraud, ransomware, or data exfiltration.  
- Well-funded and often use sophisticated tools.  

### 4. Nation-State Hacker
- Sponsored by a government to target other nations or critical infrastructure.  
- Motivation: Espionage, disruption, or gaining a strategic advantage.  
- Highly skilled, well-resourced, and persistent.  

### 5. Malicious Insider
- Employees, contractors, or partners who abuse their access.  
- Motivation: Revenge, financial gain, or coercion.  
- Especially dangerous due to legitimate access to internal systems.  

---

## Learning Objective
After completing this module, you should be able to:  
- **Contrast the five main threat actor groups** based on their profiles and characteristics.

# Script Kiddie

Script kiddies are the **least advanced threat actor group**.  
They use pre-made tools and programs without understanding the underlying techniques. While they may have a basic grasp of networking or programming, they lack technical depth, patience, and strategic intent.

---

## Characteristics

- Mostly **teenagers or young adults**, self-taught through forums, videos, and experimentation.  
- Motivations: **reputation, status, entertainment, or settling grudges**.  
- Resources: Rely on **off-the-shelf tools**, publicly available exploits, and AI chatbots to generate malicious scripts.  
- Constraints: Generally **underfunded**, low expertise, and little tradecraft knowledge.  

---

## Defensive Considerations

- Maintain an **effective patching schedule**.  
- Harden basic defenses so that an organization appears as a **less attractive target**.  
- Even simple exploits will be used if they are available and unpatched.  

*Note*: Penetration testing simulates these kinds of attacks to find vulnerabilities before they can be exploited.

---

## Profile Summary

| **Who are they?** | **What is their objective?** |
|--------------------|------------------------------|
| Self-taught individuals, usually teenagers or young adults | Gain reputation, status, or hack for fun |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Little funding, minimal expertise, free tools made by others | Keep patching schedules effective, update perimeter defenses |

# Hacktivist

The term **hacktivist** combines *hacker* and *activist*.  
Hacktivists use hacking as a means to achieve **political, social, or economic change**, driven by ideology rather than personal profit.

---

## Characteristics

- **Driven by ideological causes** — political, social, environmental, or economic.  
- Groups include both **amateurs** (like script kiddies) and **experienced IT security members** who join when causes align.  
- Motivations vary widely, but usually support a **specific cause or movement** (e.g., political activities, regional conflicts, animal rights).  
- Tools: Use **basic but scalable techniques**, such as **denial-of-service (DoS) attacks**.  
- Collective power: One amateur poses little risk, but **hundreds working in unison** can be highly disruptive.  
- Example: The collective **Anonymous**, known for attacks on corporations and governments.  

---

## Defensive Considerations

- Organizations linked to **sensitive issues** (e.g., animal testing, political causes) may face **sustained campaigns**.  
- Strong defenses alone are not enough — **incident response planning** and strategies to **cope with extended attacks** are critical.  
- Preparedness, monitoring, and resilience planning reduce the impact of large-scale hacktivist campaigns.  

---

## Profile Summary

| **Who are they?** | **What is their objective?** |
|--------------------|------------------------------|
| Driven idealists forming loose coalitions | Bring about political, social, or economic change |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Varying tools, rely on collective size and scale | Ensure defenses can handle extended, disruptive campaigns |

# Criminal Gang

As long as there is easy money to make, **criminal gangs** will remain a problem.  
The internet enables criminals to prey on victims with unprecedented **scale, range, and ease**. Cybercriminals can launch attacks from anywhere in the world, hide behind cryptocurrencies, and evade conventional policing. Prosecution is difficult due to **international law challenges**, and most gangs exploit this advantage.

---

## Characteristics

- **Fastest-growing threat actor group**.  
- Activities include:  
  - **Ransomware attacks** (locking resources until payment).  
  - **Data theft** (customer information or intellectual property).  
- Cybercrime is often a **full-time, lucrative job**.  
- Gangs range from **small groups to multinational operations** with hundreds of members.  
- Well-organized, often with **specialists** in different roles (developers, distributors, money launderers).  
- They **trade tools, exploits, and stolen data on the dark web**.  
- Offer “**cybercrime-as-a-service**,” selling malware, ransomware kits, or stolen information.  
- Motivation: Always pursue the **quickest and easiest get-rich-quick scheme**.  

---

## Defensive Considerations

- Focus on **defenses around critical assets** — ransomware on a laptop is inconvenient, but ransomware on a production server can be devastating.  
- Ensure **backups, network segmentation, and incident response plans** are in place.  
- Monitor dark web activity where possible for early warnings.  
- Security awareness training can help employees spot phishing attempts (a common entry point).  

---

## Profile Summary

| **Who are they?** | **What is their objective?** |
|--------------------|------------------------------|
| Groups of people in national or international teams | Make money through cybercrime |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Broad range of tools, exploits, and equipment traded on the dark web | Protect critical assets, maintain strong backups, train workforce, prepare incident response |

# Nation-State Hacker

Nation-state attackers receive the **most media attention** of all threat actor groups.  
Many governments now treat cyberspace as a **fifth domain of warfare** (alongside sea, land, air, and space).  
These groups project power across borders, with wide-ranging consequences.

---

## Characteristics

- Purpose: Provide a **strategic advantage** to their country.  
  - Activities range from **espionage and reconnaissance** (signals intelligence, spying) to **subversion and manipulation**.  
- Members are **highly trained, educated specialists**, often working full-time at the cutting edge of their fields.  
- Motivations align with **political or strategic objectives**.  
  - Example: Russian activity during the **2016 U.S. presidential election**, aiming to interfere and create discord.  
- Resources:  
  - Access to **advanced research**, **dedicated infrastructure teams**, and **political backing**.  
  - Use of **AI/ML tools** to automate attacks and evade detection.  
  - Exploitation of new vectors like the **Internet of Things (IoT)**.  

---

## Defensive Considerations

- Protection against nation-state hackers is **extremely challenging**.  
- Requires **coordinated, enterprise-wide security defenses** across every aspect of the organization.  
- Focus areas: threat intelligence sharing, multi-layer defenses, incident response planning, and advanced detection systems.  

---

## Profile Summary

| **Who are they?** | **What is their objective?** |
|--------------------|------------------------------|
| Highly trained and educated specialists | Execute long-term strategic, political, and military objectives |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Huge budgets, advanced tools, cutting-edge research, and political support | Incredibly difficult — requires fully coordinated defenses across all organizational layers |

# Malicious Insider

Malicious insiders are arguably the **most concerning threat actor group**.  
An insider is someone **authorized to access organizational resources** (systems, data, or accounts) but uses that access with the intent to cause harm.

---

## Characteristics

- Can be **resentful from the start** or become hostile over time.  
- Motivations vary:  
  - **Financial gain**  
  - **Revenge/bitterness**  
  - **Fame or notoriety**  
- Rarely rely on advanced technical skills:  
  - Some use **social engineering** to trick others into revealing information.  
  - Most simply exploit their **legitimate access and permissions**.  
- Examples:  
  - **Extortion** of employees to provide access.  
  - **Disgruntled staff stealing secrets** before termination.  
  - Famous case: **Edward Snowden**, who leaked NSA files.  

---

## Defensive Considerations

- Strongest defenses come from **employee vetting, effective management, and healthy culture**.  
- Technical controls (e.g., monitoring access logs) help but may fail since insiders already know how systems work.  
- Watch for **warning signs**:  
  - Isolation or working alone  
  - Expressions of resentment  
  - Declining work quality  
  - Suspicious or unexplained activities  
- Early identification of warning signs can prevent insider incidents.  

---

## Profile Summary

| **Who are they?** | **What is their objective?** |
|--------------------|------------------------------|
| Employees or contractors working against an organization’s interests | Seek revenge, financial gain, or notoriety |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Require no special budget — they use their **granted access** | Monitor staff behavior, foster a healthy culture, and apply targeted controls |

# Offensive Security Researcher

Not all hackers hack for malicious purposes.  
**Offensive security researchers** (often called **ethical hackers**) use their skills to **test, assess, and strengthen systems**.  
They adopt the same mindset and methods as attackers but apply them for **defensive and constructive purposes** — helping clients and consumers prepare for real incidents.

---

## Characteristics

- Use hacker techniques but with **legal and ethical intent**.  
- Motivation: **Improve security, protect organizations, and monetize skills through legitimate means**.  
- Common roles:  
  - **Penetration testers** (simulate attacks to find vulnerabilities).  
  - **Bug bounty hunters** (find and responsibly disclose flaws for rewards).  
  - **Security researchers** (study exploits and publish findings).  
- Highly valued by organizations — often paid generously for **expert knowledge and insights**.  
- Examples of methods: vulnerability scanning, red teaming, exploit development, and adversarial simulation.  

---

## Notable Experts

### Brian Krebs
- A celebrated **journalist who investigates cybercrime**.  
- Former Washington Post reporter (1995–2009), wrote the *Security Fix* blog.  
- Currently runs the widely-read **Krebs on Security** blog.  
- Named **2019 “Cybersecurity Person of the Year” by CISO MAG**.  
- *Fun fact*: His interest in security started after a **Chinese hacking group hijacked his home network**.  

### Georgia Wiedman
- **Entrepreneur, penetration tester, and researcher**.  
- Founder & CTO of **Shevirah**, specializing in mobile device security.  
- Known for work in **smartphone exploitation and mobile security**.  
- Author, trainer, and frequent speaker at global events (NSA, West Point, Black Hat).  
- *Fun fact*: She has trained and spoken to **audiences worldwide** on cybersecurity.  

---

## Profile Summary

| **Who are they?** | **What is their objective?** |
|--------------------|------------------------------|
| Ethical hackers, penetration testers, and security researchers | Test and fortify systems to protect clients and consumers |

| **What resources do they have?** | **How do you protect against them?** |
|----------------------------------|--------------------------------------|
| Advanced technical expertise, legal frameworks, and security tools | Partner with them — they strengthen defenses and help prevent real attacks |

