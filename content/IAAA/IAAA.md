---
marp: true
---

<!--
# Metadata
title: Identification | Authentication | Authorisation | Accounting
author: Seb Blair (CompEng0001)
description: Lecture slides on Identification | Authentication | Authorisation | Accounting
keywords: module handbook
lang: en

# Slide styling
theme: uog-theme
_class: lead title
paginate: true
_paginate: false
transition: fade 250ms

style: |
  header em { font-style: normal; view-transition-name: header; }
  header strong { font-weight: inherit; view-transition-name: header2; }
  header:not:has(em) { view-transition-name: header; }
-->

<style scoped>
h1 {
  view-transition-name: header;
  display: flex;
  align-items: center;
  margin: 0 auto;
}
</style>

# Identification | Authentication | Authorisation | Accounting

<div align=center style="font-size:76px; padding-left:300px;padding-right:300px;" >

```py
module = Module(
    code="ELEE1171",
    name="Securing Technologies",
    credits=15,
    module_leader="Seb Blair BEng(H) PGCAP MIET MIHEEM FHEA"
)
```

</div>

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/ELEE1171_Lectures/raw/main/content/IAAA/IAAA.pdf)" -->

---

<style scoped>
h1 { view-transition-name: header2; }
</style>

<!-- header: "_IAAA_" -->

## Quick Recap

<div style="padding-top:100px">

![drop-shadow w:1000](../../figures/SecOpTriad.png "centered")

</div>

---

## Quick Recap

<style scoped>ul { list-style: square; padding: 100; }</style>

5 Supporting A’s
<br>
- **Authentication**: verifying credentials or identity
<br>
- **Accountability**: Ability to trace actions back to the source
<br>
- **Auditing**: Checking for controls and compliance
<br>
- **Assurance**: Confidence that systems are working as intended
<br>
- **Accounting**: Property of recording every action taken by subjects on objects (logging)

![drop-shadow bg right:20% 70%](../../figures/security_stamps.png)

---

## What’s the difference

<div style="font-size:28px">

- **Identity** is declaring who you are:

  - Username
  - Email address
  - Unambiguous or unique (especially within a domain).
  - Useful for creating audit trails. There is no accountability without identity

- **Authentication** is confirming who you say you are:
 
  - i.e. is this claim authentic?
  - OR is it genuine?

- **Authorisation** talks about what you can or cannot do:

  - After gaining access
  - Privilege
  - Permissions

</div>

![drop-shadow bg right:40% 90% ](../../figures/audit_image.png)

---

## Biometrics – Access Ctrl

<br>

- The Crossover Error Rate (CER), alternatively  referred to as the Equal Error Rate (EER), signifies the juncture at which the False Reject Rate (FRR) aligns with the False Accept Rate (FAR).

<br>

- This metric serves as an indicator of the  comprehensive accuracy of a biometric system.

![drop-shadow bg right:50% 90% ](../../figures/CER_ERR_FRR_FAR.png)

---

## Additional Resources

<br>

- ISO 27000 Series:
  - [https://www.iso.org/standard/iso-iec-27000-family](https://www.iso.org/standard/iso-iec-27000-family)

<br>

- Information Security Management Principles:
  - [https://www.oreilly.com/library/view/information-security-management/9781780175201/](https://www.oreilly.com/library/view/information-security-management/9781780175201/)

<br>

- NIST SP-800:
    - [https://www.nist.gov/itl/publications-0/nist-special-publication-800-series-general-information](https://www.nist.gov/itl/publications-0/nist-special-publication-800-series-general-information)

---

<!-- class: lead -->

# Accountability | Audit | Compliance

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<!-- header: "_IAAA_ > **Accountability | Audit | Compliance** " -->

<div style="padding-bottom:50px">

## What’s they are...

</div>

<style scoped>ul { list-style: square; padding: 100; }</style>

<div style="font-size:28px">

- **Accountability**
  - You can trace actions back to source
  - Actions can be uniquely traced to the identity:
    - (username ! ID ! SSN ! NI ! Drivers license number)
  - To ensure the power given is not being abused to carry out malicious activities
<br>
- **Audit**
  - It’s a process of reviewing:
    - Capacity to meet initial  approval agreements as a service provider
    - Capacity to meet on-going approval agreements as a service provider
    - Checking of system records to ensure what is expected to happen has happened
    - Also used to check if nothing unusual has happened (e.g. system logs)
<br>
- **Compliance**
  - Meeting or exceeding expected operating procedure {Guideline | Standards | Policies }

</div>

----

<div>

## Policies | Standards | Guidelines | Baselines

</div>

<div class="columns-2" style="padding-top:100px">
<div style="font-size:28px">

- **Policy**
  - High level governance document that needs to be understood by directors etc
- **Standards**
  - Vendor specific
- **Baseline**
  - Minimum Configuration
- **Guidelines**
  - Recommended best practices; not mandatory
- **Procedures**
  - Step-by-step guide

</div>
<div style="padding-top:100px">

![drop-shadow](../../figures/P_S_G_B.png)

</div>
</div>

---

<div>

## Key components of Strategic Alignment

</div>

<div style="font-size:28px; padding-top:50px">

*Business enabler

- **Risk Management**: 
  - Understand the risks, make decisions about them whether to accept, mitigate or change the activity

<div style="padding-top:40px;padding-bottom:15px;">

- **Value delivery**: 
  - ensure security delivers value
<br>
- **Resource management**: 
  - ensure resources are used wisely
<br>
- **Performance**: 
  - ensure Organisation performance is enhanced and not hindered
</div>

*When IT Security is strategically aligned, security becomes a business enabler that adds value
*Major goal is the protection of the entity from harm and contributing to Organisation success.

</div>

---

<div>

## Cyber security Policy

</div>

<div style="font-size:24px">

To provide clarity about what is expected of employees and 3rd parties when it comes to data security and use of systems and applications. That is, how they can maintain security of both data and applications.

</div>

<div style="font-size:24px">

Some important policies {could be renamed or added to as business requires}
- Acceptable Use Policy (AUP)
<br>
- Change Management Policy
<br>
- Information Security Policy
<br>
- Business Continuity Plan (BCP)
<br>
- Disaster Recovery Policy
<br>
- Incident Response Policy (or IR Policy)
<br>
- Remote Access Policy
<br>
- Email Policy

<div style="font-size:21px">

<br>

Implementing Cyber Security Policies “provide assurance that information is being managed securely and in a consistent and corporate way” 

---

<div>

## 3 main types of Policy

</div>


<div style="font-size:26px">

1. **Regulatory**: Seeing the organisation follows standards put up by specific industry regulations

<br>

2. **Advisory**: Strongly advises employees of what behaviours and activities are allowed or prohibited according to Organisation Standard and serious consequences could follow disobedience of such.

<br>

3. **Informative**: The primary purpose of an informative policy is to educate and inform the  readers or stakeholders about a particular subject matter, procedure, or set of expectations. These policies are typically designed to be clear, concise, and easily understood by the intended audience. E.g., Privacy policy, health & safety policy, employee handbooks etc:

    <br>
    
    - Health and Safety Policies: These policies detail procedures and guidelines for maintaining a safe and healthy workplace. They cover topics like emergency procedures, safety equipment usage, and accident reporting.
    
    <br>
    
    - Privacy Policies: Privacy policies inform individuals about how an organisation collects, uses, stores, and protects their personal information. These policies are common on websites and apps that collect user data.
      
    </div>

---

<!-- header: "IAAA > Accountability | Audit | Compliance" -->

<div>

## Applying Security Governance Principles

</div>

<br>

<div>

- **Governance**: sets strategic direction and provide leadership

<br>

- **Due Care**: A standard of care

<br>

- **Due Diligence**: Continued effort

<br>

- **Strategic Alignment**: Supporting business objectives

<br>

- **Corporate Culture**: Shared attitude, vision and goals

</div>

---

## Info Security Management Systems {ISMS}

![drop-shadow center w:1000](../../figures/iso_ISMS.png)

--- 

<!-- class: lead -->

#  National and International Standards


<style scoped>
h1 { view-transition-name: header2; }
</style>


---

<!-- header: "_IAAA > Accountability | Audit | Compliance_ > **National and International Standards**" -->


---
<div style="padding-bottom:100px">

## How important are standards?

</div>

<div>

- As professionals, we need to be aware of them
<br>
- We need to understand them and know which ones apply to their Organisation, Environment, etc.
<br>
- **They inform us on best practices**
<br>
- **It is important to know best practices and general principles that apply to info security**

</div>

---

<div>

## Some Important Standards to Note

</div>

<div style="font-size:24px">

- **GDPR (General Data Protection Regulation)**: GDPR is a European Union regulation that applies to the protection of personal data. It imposes strict  requirements on how organizations handle and protect personal data of EU residents
<br>
- **GLBA (Gramm-Leach-Bliley Act)**: GLBA is a U.S. law that requires financial institutions to establish safeguards to protect customer information. It  addresses the security and privacy of financial data.
<br>
- **FISMA (Federal Information Security Management Act)**: FISMA is a U.S. federal law that mandates cybersecurity practices for federal agencies and  their contractors. It requires the development and maintenance of information security programs and compliance with NIST (National Institute of Standards and Technology) cybersecurity standards.
<br>
- **SOX (Sarbanes-Oxley Act)**: SOX is a U.S. federal law that primarily focuses on financial reporting and disclosure. It includes provisions related to internal controls and data protection, which have implications for cybersecurity.
<br>
- **HIPAA (Health Insurance Portability and Accountability Act)**: HIPAA is a U.S. law that governs the security and privacy of healthcare information. It  imposes stringent requirements on the protection of electronic health records (EHRs) and patient data.

</div>

<div style="font-size:20px">

<br>

**Key**: GLBA and Sox: Financial | FISMA: Federal agencies | GDPR & DPA: Data protection | HIPAA: Health | PCIDSS: Credit & Debit cards

</div>

---

<div>

## Some Important Standards to Note

</div>

<div style="font-size:24px">

-  **DPA (Data Protection Act)**: The DPA is the UK's implementation of data protection laws post-Brexit, aligning with GDPR principles. It regulates the processing of personal data within the UK.
<br>
- **ISO Standards (ISO 27001 and ISO 27002)**: ISO 27001 is an international standard for information security management systems (ISMS), while ISO 27002 provides guidelines for implementing security controls. These standards are globally recognized and widely used for cybersecurity best practices.
<br>
- **NIST Cybersecurity Framework**: Developed by NIST, this framework provides a risk-based approach to managing  cybersecurity risk. It offers guidelines for improving cybersecurity posture and aligning with other standards.
 <br>
- **PCI DSS (Payment Card Industry Data Security Standard)**: PCI DSS is a set of security standards for organizations that handle credit card transactions. It specifies requirements for securing cardholder data

</div>

<div style="font-size:20px">

<br>

Take note of the difference between ISO27001 and 27002 | Remember how they work together

</div>

---

<div style="padding-bottom:20px">

## NIST 800-14

</div>

<div style="font-size:27px">

\* Based on OECD Guidelines for Security of Info systems

1. Info/computer security supports the mission of the Organisation
<br>
2. Computer security is an integral element of sound management
<br>
3. Computer security should be cost-effective
<br>
4. System owners have security responsibilities outside their organisation
<br>
5. Computer security responsibilities and accountability should be made explicit
<br>
6. computer security requires a comprehensive and integrated approach
<br>
7. computer security should be periodically reassessed
<br>
8. Computer security is constrained by societal factors

*Hint: You need to know and understand this

</div>

---

<div style="padding-top:200px">

# Give an example of a perfectly secure system/location…

<div style="padding-top:180px; font-size:22px">

…to be continued | Think of the above ahead of the next class |  There might be a reward for the best answer