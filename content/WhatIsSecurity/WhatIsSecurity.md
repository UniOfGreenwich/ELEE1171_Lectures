---
marp: true
---

<!--
# Metadata
title: What Is Security
author: Seb Blair (CompEng0001)
description: Lecture slides on What Is Security
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

# What Is Security

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

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/ELEE1171_Lectures/raw/main/content/WhatIsSecurity/WhatIsSecurity.pdf)" -->

---

<!-- header: "_What is Security_" -->

<style scoped>
h1 { view-transition-name: header2; }
</style>

## Some Terms to Note

<div>

- 2FA – Two-factor Authentication
<br>
- ACL – Access control list
<br>
- BIA – Business Impact Analysis
<br>
- 5G – Fifth generation cellular network telephony
<br>
- BCP – Business Continuity Plan
<br>
- CC – Common Criteria
<br>
- CCTV – Close Circuit Television
<br>
- CERT – Computer Emergency Response Team

</div>

----


## Content

- What is security

- CIA

- Threats | Risks | Vulnerabilities

- Encryption

- Privacy

- GDPR

- BCP | IRP | CP

- What is management?

- Do I need to be technical for Cybersecurity?

----

## What is Security?

**Introduction**

<div class="columns-2">
<div style="padding-top:100px;font-size:28px">

Two main objectives of Security:

- Making sure authorised personnel have access to the resources they need

- Making sure unauthorised personnel do not have access to the resources

- Authentication is the procedure of confirming the identity of the user trying  to access certain data

- It is a mandatory element of security model

</div>
<div style="padding-top:120px">

![drop-shadow w:800](../../figures/padlock_security.png)

</div>
</div>

---

## What are we protecting?

<div class="columns-2">
<div style="padding-top:100px;font-size:28px">

Assets: Anything __of value__ to your Organisation

- Hardware

- Software

- Staff

- Data

- Network
 
<br>

Lives: 
- This is because Cyber Security involves protecting beyond your Organisation. E.g. Citizens of a Country, customers, children etc.

</div>

<div style="padding-top:50px">

![drop-shadow w:500 ](../../figures/protecting_assets.png)

</div>
</div>

---

<div style="padding-bottom:150px">

## What are we protecting?

</div>

**Asset types**

 - Physical Assets: know any?
<br>
 - Pure information/Data
<br>
 - Software: for managing or processing information

---

## What are we protecting from?

<div>

- **Threats**: 
  - Something that can cause harm to assets
<br>
- **Vulnerability**: 
  - a weakness or loophole that can be exploited by a  threat
<br>
- **Risk**: 
  - Chances that something will happen OR effect of  uncertainty. E.g:
    - Walking into a crowd during the pandemic without a face covering increases your chances (or Risk) of catching the virus.
    - Wearing a mask also does not totally eradicate it but mitigates the chances.
<br>
- **Impact**: 
  - How much it affects our **business** | **operations** | **assets**

</div>

---

## Bringing all together;

<div class="columns-2">
<div style="padding-top:150px">

- A threat needs a vulnerability
<br>
- A vulnerability is a loophole that a threat can take advantage of
<br>
- A threat would usually need a vulnerability to be successful
<br>
- It is risky to your business if you have vulnerabilities that threats can exploit

</div>
<div style="padding-top:170px">

![drop-shadow w:800](../../figures/brokenumbrella.png)

</div>
</div>

---

## Main Goals of Security

<div style="padding-top:50px;font-size:26px">

**Confidentiality**: 
- Only authorised subjects can view or access information. If you are not authorised, no access. If you do not have clearance, no access.

<br>

**Integrity**: 
- Information is not modified illegally or by an unauthorised subject.  Can also mean a system is working as it is supposed to. E.g. patient monitor at hospitals. {Accuracy and completeness}.

<br>

**Availability**: 
- System is available when needed or queried. That is, it responds  when it is expected to. Availability can affect both data and system. E.g. Ransomware
<br>

**Strategic alignment**: 
- All the above need to work together towards achieving the Company’s goals

![drop-shadow bg right:20% 70%](../../figures/security_stamps.png)

---

## Information Security Principles

**DAD Acronym {Opposite of the CIA}**

 - Disclosure:
   - Unauthorised disclosure of sensitive information can lead to severe privacy breaches and compromise the security of an organisation
<br>
 - Alteration:
   - Data alteration by malicious actors can corrupt critical information, making it unreliable and potentially harmful.
<br>
 - Destruction/Denial:
   - Destruction or denial of access to essential data can disrupt operations and cause significant losses for businesses

![bg right:20% 70%](../../figures/security_stamps.png)

---

## Why is confidentiality important?

<div style="padding-top:120px">

![drop-shadow w:1200](../../figures/confidentialityImportance.png "centered")

</div>

---

## Subject vs Object

<div class="columns-2">
<div style="padding-top:150px">

-  Subject: makes request to access/use an object

<br>
<br>
<br>
<br>
<br>

-  Objects: the resource a subject needs access to

</div>
<div style="padding-top:175px">

`curl -S https://path/to/url --data $(cat)`
<br>
<br>
```json
{
  "id": 1001,
  "title": "Who invented JSON?",
  "author": {
  "name": "Douglas Crockford"
  },
  "tags": ["api", "json", "programming"],
  "published": false,
  "publishedTimestamp": null
}
```
</div>
</div>

---

## Importance of Integrity

<div class="columns-2">
<div style="padding-top:150px">

- Helps ensure information is unchanged between source and destination

<br>
<br>
<br>
<br>

- Hashing can be used to easily compare files and spot those that have been altered (by comparing their hashes)

</div>
<div style="padding-top:150px">

```sh
Your Hash: 2f2bae6733b6449f88b7c372108c1eb7
Your String: "This MD5 generator is useful for encoding passwords,"
```

<br>
<br>
<br>
<br>

```sh
Your Hash: 441ab12d5386b0eb6755df60bccb5b08
Your String: "This MD5 generator is useful for encoding passwords"
```

</div>
</div>

----

## Practical- How to check for file Integrity

<br>
<br>


**Windows**

```sh
certutil   –hashfile    <filename>    <md5, sha1, sha256, sha512>    [ENTER]
```

<br>
<br>

**Linux/Mac**

```sh
<md5sum, sha1sum, sha256sum. sha512sum>   <filename>  [ENTER]
```

<div style="padding-top:200px;font-size:28px">

\* The major difference between Hashing and Encryption is that: No keys are used in hashing but only algorithms e.g., MD5

</div>

---

## Why is availability important?

<br><br>
- Using an e-commerce site for example
<br>
- Customers should always be able to buy. If the site is not reachable, no sales,  and if no sales, no profit.Continuous lack of profit = loss of business
<br>
- Not being reachable could also affect the business’s reputation and furthermore push customers to competitors.


<div style="font-size:26px; padding-top:100px">

| \*Information that is not available when and as required is not information  at all but irrelevant data |

</div>

----

## The Security and Operational Triad

<div class="columns-2">
<div style="font-size:24px">

**CIA Triad (Information Security)**
**Confidentiality (C)**: Ensures that sensitive information is only accessible to authorized individuals, preventing unauthorized access or disclosure.

**Integrity (I)**: Maintains the accuracy and trustworthiness of data by preventing unauthorized modifications.

**Availability (A)**: Guarantees that information and systems are accessible to users when needed, ensuring reliable access.

</div>
<div style="font-size:24px">

**FSP Triangle (Design Trade-offs)**
**Functionality (F)**: Refers to the features and capabilities a system provides to meet user and business requirements.

**Security (S)**: Involves protecting systems and data from threats, often requiring compromises with functionality or performance.

**Performance (P)**: Measures how efficiently a system runs, including speed and responsiveness, which can sometimes conflict with security measures.

</div>
</div>

![drop-shadow w:800](../../figures/SecOpTriad.png "centered")

----

## Information Security Principles


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