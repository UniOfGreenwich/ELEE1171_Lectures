---
title: Threats & Threat Actors
description: Threats & Threat Actors Slides
class: gaia
_class:
  - lead
  - invert
style: |
    #img-right{
      float: right;
    }
    img[alt~="center"] {
      display: block;
      margin: 0 auto;
    }
    table {
      border-collapse: collapse;
      font-size: 22px;
    }
    table, th,tr, td {
      border: none!important;
      vertical-align: middle;
    }
    section::after {
      content: attr(data-marpit-pagination) '/' attr(data-marpit-pagination-total);
    }
footer: "ELEE1171 | Securing Technologies"
size: 16:9
paginate: true
_paginate: false
marp: true
math: true
---

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/ELEE1171_Lectures/raw/gh-pages/content//c/Users/dev/Git/UoG/ELEE1171/Lectures/content/CommonThreatActors/CommonThreatActors.pdf)" -->

# Threats & Threat Actors

    Module Code: ELEE1171

    Module Name: Securing Technologies

    Lecturer: Seb Blair BEng(H) PGCAP MIET MIHEEM FHEA

---


## Remember?

- Threats: Something that can cause harm to assets

- Vulnerability: a weakness or loophole that can be exploited by a threat

- Risk: Chances that something will happen OR effect of uncertainty. E.g., Walking into a crowd during the pandemic without a face covering increases your chances (or Risk) of catching the virus. Wearing a mask also does not totally eradicate it but **mitigates** the chances.

- Impact: How much it affects our business | operations | assets

---

## What are Threats?

**Threat**
- Potential harmful events, actions, or occurrences that can exploit system vulnerabilities (computer systems, networks, applications).

- Can lead to security breaches, data loss, or damage to an organisation's assets.

- Basically, anything that has potential to cause harm to our assets.
 
**Threat Actor**

- Also known as malicious actors or adversaries, are individuals, groups, or entities that initiate, execute, or orchestrate the threats.

- They are responsible for activities aimed at causing harm, damage, or unauthorised access.

---

# Common Threats & Threat Actors

---


## Threats

- **Malware**: Malware simply means malicious software, designed to disrupt, damage,  or gain unauthorised access to information systems and assets. Common types include viruses, worms, Trojans, ransomware, and spyware.

- **Example**: A user unknowingly downloads a malicious email attachment, infecting their computer with ransomware that encrypts valuable files until a ransom is paid.

- **Actors**: 

- **Control**: ?


---

## Threats

- **Phishing Attacks**: Phishing attacks use deceptive emails, messages, or websites to trick users into revealing sensitive information, such as login credentials or financial data.

- **Example**: An attacker sends an email disguised as a legitimate bank, asking users to  update their account information by clicking a link that leads to a fake website capturing their login details.

- **Actors**: 

- **Control**: ?

---

## Threats

- **Denial-of-Service (DoS) Attacks**: DoS attacks aim to overwhelm or disable a target  system or network, making it inaccessible to legitimate users by flooding it with excessive traffic or resource requests.

- **Example**: An attacker launches a DoS attack against a company's web server, causing  it to crash, and rendering the website unavailable to customers.

- **Actors**: 
- **Control**: ?

---

## DDOS

![center w:800](../../figures/ddos.png)

---

##  Threats

- **Insider Threats**: Insider threats come from within an organization and can be 
accidental or malicious. Employees or contractors may leak sensitive data or misuse 
their access privileges.

- **Example**: An employee with access to sensitive customer data leaks the information 
to a competitor for personal gain.

- **Actors**: 

- **Control**: ?


---

## Threats

- **Social Engineering**: Social engineering involves manipulating people into revealing confidential information or performing certain actions. Attackers use psychological tactics to gain trust or deceive individuals.

- **Example**: An attacker impersonates an IT technician over the phone, convincing an employee to share their login credentials, claiming it's for a system upgrade.

- **Actors**: 

- **Control**: ?

---

## Threats

<div style="font-size:22px">

- **Man-in-the-middle Attack**: attacker intercepts and potentially alters the communication between two parties who believe they are communicating directly with each other. In this type of attack, the attacker secretly positions themselves between the two parties, acting as an unauthorised intermediary. The primary goal of a man-in-the-middle attacker is to eavesdrop on the communication, manipulate it, or both, without the knowledge or consent of the legitimate parties involved.

- Example: Attackers manipulate DNS requests, redirecting users to 
malicious websites that impersonate legitimate ones.

- Actors: 

- Control: ?

</div>

![bg right:40% 100%](../../figures/mitm.png)

---

## Threats

- **Zero-Day Exploits**: Zero-day exploits target software vulnerabilities that vendors are unaware of or haven't yet released a patch for. Attackers use these vulnerabilities to gain unauthorised access.

- Example: A hacker discovers a previouslyunknown vulnerability in a widely used software application and exploits it before the vendor can develop a patch.

- Actors: 

- Control: ?

---

## Threats
 
- **Insider Data Theft**: This threat involves authorised individuals stealing sensitive  information for personal gain or to sell to external parties.
 
- **Example**: A disgruntled employee copies customer data, including credit card details, to sell it to a competitor.

- **Actors**: 

- **Control**: ?

---

## Threats

- **Advanced Persistent Threats (APTs)**: APTs are sophisticated, long-term cyber-attacks launched by skilled attackers who aim to infiltrate and remain undetected within a target organization to extract valuable information.

- **Example**: A nation-state-sponsored group infiltrates a government agency's network, gathering classified data over an extended period without being detected.

- **Actors**: 

- **Control**: ?

----

## Threats

- **Physical Security Breaches**: Physical security breaches occur when unauthorised individuals gain physical access to information assets, such as servers or data centres.
  
- **Example**: An intruder gains access to a company's data centre and steals 
backup tapes containing sensitive customer information.

- **Actors**: 

- **Control**: ?

---

## Threats

- **Supply Chain Attacks**: Supply chain attacks target vulnerabilities in the supply chain process, aiming to compromise hardware, software, or firmware before reaching end-users.

- **Example**: Attackers inject malicious code into a software update, which is then distributed to customers, infecting their systems when installed.

- **Actors**: 

- **Control**: ?

---

## Recall...

A threat needs a vulnerability

A vulnerability is a loophole that a threat can take advantage of

A threat would usually need a vulnerability to be successful

It is risky to your business if you have vulnerabilities that threats can exploit!

![bg right:50% 100%](../../figures/brokenumbrella.png)

---

# Attacker’s Point of View

---

## Hacking Process

<div style="padding-top:100px">

![](../../figures/hacking_flow.png)


<div style="padding-top:100px">

Before this, remember ethics in relation to approval and authorisation.

---

## Cyber Kill Chain

[https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html)

![bg left:50% 70%](../../figures/cyber_kill_chain.png)

---

## MITRE ATT&CK Framework


![w:900 center](../../figures/mitre_attck.png)

<div style="font-size:21px">

Visit here to explore further: [https://attack.mitre.org/](https://attack.mitre.org/)

</div>

---

# So How Do We Detect/Prevent?

---

## Threats

- **Anomaly-based**: establishes a baseline of normal network or system behaviour. It then identifies deviations from this baseline, flagging activities that are unusual or potentially malicious.

  - **User and Entity Behaviour Analytics (UEBA) solutions** such as Exabeam and Splunk detect anomalies in user and entity behaviour by analysing historical data to identify deviations from normal patterns.

  - **Credit Card Fraud Detection** Financial institutions use anomaly-based detection to identify unusual transactions, such as large purchases in different geographic locations, as potential credit card fraud

---

## Threat/Intrusion Detection

- **Heuristic-Based Detection**: relies on rules and algorithms to  identify potentially suspicious activities. The rules here are based on general knowledge of attack techniques rather than specific signatures.
 
  - **Email filtering systems**, like those used by Gmail and Microsoft Outlook, employ heuristics to analyse incoming emails for suspicious content, attachments, or links that may indicate phishing attempts.

  - **Web Application Firewalls (WAFs)** like ModSecurity use heuristic analysis to detect and block web application attacks based on known attack patterns

---

## Threat/Intrusion Detection

- **Behaviour-Based Detection**: Behaviour-based detection focuses on the behaviour of software or users. It monitors patterns of activities and flags deviations that indicate malicious behaviour.

  - **Endpoint Detection and Response (EDR)** solutions like CrowdStrike and Carbon Black monitor the behaviour of endpoints (e.g., computers) and alert administrators to unusual activities, such as file modifications or unauthorised access attempts.
  
  - Also used in **user authentication systems** to flag suspicious login attempts, such as multiple failed logins or login attempts from unusual locations.


---

# Security Measures

![bg right:40% 100%](../../figures/padlock.png)

✓ Hardware

✓ Software

✓ Processes and Procedures

✓ Best Practices

<div style="padding-top:100px" align=center>

Must Know!

</div>

---

## Best Practices

- Principle of least privilege!

- Principle of need-to-know

- Defence-in-depth/Layered security

- System Hardening

- SETA Programs

- Network Segmentation

- Keeping Systems Up-to-date

- Clean Desk Policy

![bg left:40% 100%](../../figures/datra_dots.png)

---

## Processes/Procedures


- Backups

- Patch and Change Management

- Vulnerability & Penetration Tests

- Continuous Monitoring

- Asset Inventory

- Secure Coding

- Input validation

- Background check/Security Clearance

- Access Control

![bg right:40% 100%](../../figures/cloud_storage.png)

---

## Hardware/Software


- Firewalls

- DMZ

- Intrusion Detection (Prevention) Systems {IDS/IDPS}

- Proxy/VPN Servers

- Secure Web Gateways {SWG}

- Security Information and Event Mgt {SIEM}

- Security Orchestration, Automation and Response {SOAR}

- Antivirus Program

- Data Loss Prevention Systems {DLP}

---

## Categorising Security Controls

**Categorising By Purpose,**

- Preventative: aim to stop disasters or security incidents

- Detective: uses IoCs or sensors to identify likely attacks or attempts

- Recovery: after an incident has taken place (i.e., after a successful breach or attack)


**Categorising By Mechanism & Action,**

- Technical: achieved using technology

- Administrative: processes for managing/maintaining the security of technology

- Physical: physical restrictions or measures put in place to protect either technology or human assets

----

## System Hardening

![](../../figures/SystemHardening.png)

---

## Access Control Types

- Mandatory Access Control (MAC)

- Discretionary Access Control (DAC)

- Role-based Access Control (RBAC)

- Rule-based Access Control (RuBAC)

![bg right:40% 180%](../../figures/Access-Control-Systems-scaled-1.jpeg)

---

## Conclusion

- You cannot protect against what you don’t know!

- Understanding these different types of security threats is essential for protecting information assets effectively.

- It starts with knowing what assets there are.

- By recognising potential vulnerabilities and implementing appropriate security measures, organisations can mitigate risks and safeguard their valuable data and systems