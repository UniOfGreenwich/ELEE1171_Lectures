---
marp: true
---

<!--
# Metadata
title: Security Risks
author: Seb Blair (CompEng0001)
description: Lecture slides on Security Risks
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

# Security Risks

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

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/ELEE1171_Lectures/raw/main/content/SecurityRisks/SecurityRisks.pdf)" -->

---

<!-- header: "_Security Risks_" -->

<style scoped>
h1 { view-transition-name: header2; }
</style>


## Don't Forget

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

---

<div style="padding-top:200px">

# Give an example of a perfectly secure system/location…

<div style="padding-top:160px; font-size:20px">

I.e., A system/location without risks | If you cannot produce any, it means there is risk in everything | So what do you do?

---

## Remember this guy?

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

## Information Risk

<div style="font-size:28px">

**4 major steps involved in Risk Assessment**

- Prepare

- Perform

- Communicate

- Maintain

<br>

**Deming Cycle**

- Plan:
  - Identify opportunity for change

- Do: 
  - Implement change on a small scale {e.g., in a sandboxed environment | or experiment with a small group}

- Check: 
  - How does the change impact business?

- Act: 
  - Implement full change, if it goes well with business

</div>

---

## Information Assurance

<div style="padding-top:160px">

- The confidence that information systems will protect the information they carry and will function as they need to, when they need to, under control of legitimate users.

(UK Cabinet office, as cited in Information Security Mgt. Principles- 3rd edition)

</div>

<div style="padding-top:60px">

- Information Security: Preserving CIA | And supporting with the 5 A’s

---

## Risk Assessment

<div style="font-size:29px">

<br>

- Cost and Benefit are major considerations in Risk Assessment.

- If the Cost is more than the benefit, it is not worth it.

- If the Benefit is greater than the cost, then we do it

<br>

Cost could be in terms of:

- impact on business processes

- financial implication

- impact on lives | the Society

- impact on assets etc.

<br>

i.e., what price would we have to pay?

---

## Risk Assessment

<div class="columns-2" style="padding-top:150px">
<div style="">

 **Quantitative,**

- $E.F\ = \frac{\text{Value of asset lost}}{\text{Total value of asset}}$

- $SLE\ = AV\ \cdot\ E.F$

- $ARO\ = \frac{\text{No. of occurrences in a year}}{\text{Total time period}}$ 

- $ALE\ = SLE\ \cdot\ ARO$

</div>
<div>

**Qualitative,**

 - Risk matrix
 - A good standard to follow for this is the ISO27005

</div>
</div>

<br>
<br>

*Quantitative deals with numbers 

*Qualitative qualifies the risks using adjectival and/or adverbial phrases e.g., very likely


---

## Quantitative

<div class="columns-2" style="padding-top:10px">
<div style="">

- $AV$ = total value of the asset that could be affected by a particular risk

- $SLE$ = estimated financial loss resulting from a single occurrence of a specific risk or 
threat

- $ARO$ = quantifies how frequently a specific risk or threat is expected to occur within 
a year

- $E.F$ = expressed as a decimal or percentage, represents the proportion of the asset's value that would be lost in the event of a security incident

- $ALE$ = estimate the expected financial loss from specific risks over a year

</div>
<div style="padding-top:100px;font-size:30px">

<br>

- $SLE\ = AV\ \cdot\ E.F$

<br>
<br>
<br>

- $ARO\ = \frac{\text{No. of occurrences in a year}}{\text{Total time period}}$ 
<br>
<br>

- $E.F\ = \frac{\text{Value of asset lost}}{\text{Total value of asset}}$

<br>
<br>
<br>

- $ALE\ = SLE\ \cdot\ ARO$
 
</div>
</div>

---

## Quantitative

<div style="font-size:28px">

**Example 1**

You are managing a small business with an inventory system. The Asset Value ($AV$) of your inventory is £20,000, and the Exposure Factor ($E.F$) for the risk of inventory loss is 15%. The Annualised Rate of Occurrence ($ARO$) for this risk is 5, indicating that the threat occurs five times a year.

<br>

- $E.F\ = \frac{\text{Value of asset lost}}{\text{Total value of asset}}$

- $SLE\ = AV\ \cdot\ E.F$

- $ARO\ = \frac{\text{No. of occurrences in a year}}{\text{Total time period}}$

- $ALE\ = SLE\ \cdot\ ARO$

<br>

- **Take note,**
   - To get the ALE, we need the SLE and ARO
   - ARO is provided but we need to find SLE

---


## Quantitative

<div style="font-size:28px">

**Example 1 - Solution**

You are managing a small business with an inventory system. The Asset Value ($AV$) of your inventory is £20,000, and the Exposure Factor ($E.F$) for the risk of inventory loss is 15%. The Annualised Rate of Occurrence ($ARO$) for this risk is 5, indicating that the threat occurs five times a year.


- $E.F\ = \frac{\text{Value of asset lost}}{\text{Total value of asset}}$

  $\hspace{7em}£3000\ =\ £20000 \cdot 0.15$
<br>
- $SLE\ = AV\ \cdot\ E.F$

  $\hspace{7em}£3000\ =\ £20000 \cdot 0.15$
<br>
- $ARO\ = \frac{\text{No. of occurrences in a year}}{\text{Total time period}}$
  
  $\hspace{7em}5 = \frac{5}{1}$
<br>
- $ALE\ = SLE\ \cdot\ ARO$

  $\hspace{7em}£15000\ =\ £3000 \cdot 5$


--- 

## Quantitative

<div style="font-size:28px">

**Example 2**

You are an IT security manager for a company, and you are assessing the risk associated with phishing attacks targeting your employees. Your analysis shows that, on average, your company experiences 12 phishing incidents per year. Calculate the ARO for phishing attacks over a period of 5 years

<br>

- $ARO\ = \frac{\text{No. of occurrences in a year}}{\text{Total time period}}$

<br>

- **In this case,**
  - No. of occurrences in a year = 12 
  - Total time period = 5 years
  - ARO = 12 / 5 = 2.4

---

## Quantitative

<div style="font-size:28px">

**Organisations use ALE to:**

- **Prioritise Risks**:
  - ALE allows organisations to rank risks based on potential financial impact. High ALE 
values indicate risks that require immediate attention.

- **Allocate Resources**: 
  - ALE helps in allocating resources efficiently. Risks with higher ALE values may 
receive more budget for security measures.

- **Risk Mitigation**: 
  - ALE guides organisations in determining the most cost-effective security measures 
to mitigate risks with high ALE values.
 
- **Security Investments**: 
  - ALE supports decisions on investing in cybersecurity solutions and insurance 
based on the financial consequences of risks.

- **Compliance Requirements**:
  - ALE assists in understanding the financial implications of failing to meet 
compliance requirements, influencing decisions on compliance investments.

</div>

---

## Qualitative

<div style="padding-top:100px">

![drop-shadow](../../figures/risk_table_template.png "centered")

</div>

---

## Qualitative (Weighted)

<div style="padding-top:100px">

![drop-shadow](../../figures/weighted_risk_table_template.png "centered")

</div>

---

## Risk Management Strategies

<br>
<br>
<br>

**After risk is discovered/assessed, there is a need to apply a management strategy:**

- Risk Avoidance
<br>
- Risk Mitigation
<br>
- Risk Transference/sharing
<br>
- Risk Acceptance