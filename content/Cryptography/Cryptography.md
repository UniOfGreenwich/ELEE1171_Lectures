---
marp: true
---

<!--
# Metadata
title: Cryptography
author: Seb Blair (CompEng0001)
description: Lecture slides on Cryptography
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

# Cryptography

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

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/ELEE1171_Lectures/raw/main/content/Cryptography/Cryptography.pdf)" -->

---

<style scoped>
h1 { view-transition-name: header2; }
</style>

<!-- header: "_Cryptography_" -->

## Main Goals of Security: CIA

<div style="font-size:28px;padding-left:50px;padding-top:10px">

<br>

**CIA Triad (Information Security)**

<br>

**Confidentiality (C)**: Ensures that sensitive information is only accessible to authorized individuals, preventing unauthorized access or disclosure.

<br>

**Integrity (I)**: Maintains the accuracy and trustworthiness of data by preventing unauthorized modifications.

<br>

**Availability (A)**: Guarantees that information and systems are accessible to users when needed, ensuring reliable access.

</div>

![drop-shadow bg right:50% 80%](../../figures/CIA.jpg)

---

## Quick Definitions

<div style="font-size:28px">

- **Cryptography**: the art of secret writing!

<br>

- **Encryption**: converting information to a format **unreadable by unintended recipients**. Only intended recipients  with the correct key and algorithm can read it and get its true meaning.

<br>

- **Hashing**: converts data or message into an irreversible string of fixed length.

<br>

- Confidentiality can be achieved using **Encryption**

<br>

- Data Integrity can be verified using **Hashing**

</div>

---

##  Why Do We Need Cryptography?

<div style="padding-top:200px">

![drop-shadow w:1200](../../figures/why_do_we_need_crypt.png "centered")

</div>

---

<!-- _class: lead -->

# Steganography 

<style scoped>
h1 { view-transition-name: header2; }
</style>

---

<style scoped>
h1 { view-transition-name: header2; }
</style>

<!-- header: "_Cryptography_ > **Steganography**" -->

<div style="font-size:24px;padding-top:50px;">

**Definition:**  
Steganography is the practice of hiding a message **within another medium**, so that the very **existence** of the message is concealed.

</div>

<div class="columns-2">
<div style="font-size:20px">

<br>

|Factors | Steganography | Cryptography | 
|----|-----|-----|
|Explanation |It's a method to conceal the fact that communication is taking place |It's a method for making information unintelligible|
|Aim|Maintain communication security| Enable data protection|
|Key| Optional, but increases security when utilized| Necessary prerequisite|
|Data Visibility | No | Yes|
|Failure| Once hidden information is decoded, the data can be used by anyone |You can recover the original message from the ciphertext if you can access the decryption key|
|Data Structure|Does not modify the data's general structure|Modifies the overall data structure|

<br>

Using LSB steganography, encode with lossless PNG or BMP

</div>
<div>

![w:400](../../figures/iceland_waterfall.png) ![w:400](../../figures/iceland_waterfall_stego.png) 

</div>
</div>

---

<div>

## Techniques

</div>

- **Secure Cover Selection**
  - Involves finding the correct block image to carry malware. Then, hackers compare their chosen image medium with the malware blocks. If an image block matches the malware, the hackers fit it into the carrier image, creating an identical image infected with the malware. This image subsequently passes quickly through threat detection methods.

- **Least Significant Bit**
  - Grayscale image pixels are broken into eight bits, and the last bit, the eighth one, is called the Least Significant Bit. Hackers use this bit to embed malicious code because the overall pixel value will be reduced by only one, and the human eye can’t detect the difference in the image. So, no one is even aware that anything is amiss, and that the image is carrying something dangerous within.

- **Palette-Based Technique**
  - Hackers embed their message in palette-based images such as GIF files, making it difficult for cybersecurity threat hunters or ethical hackers to detect the attack.

---

<div style="padding-bottom:180px">

## Tools [to name a couple]

</div>

<div class="columns-2" style="padding-bottom:250px">
<div>

- **[Steghide](https://github.com/StegHigh/steghide)**:  is a free tool that uses steganography to conceal information in other files, such as media or text.

<br>

- **[silenteye](https://github.com/achorein/silenteye/)**: a cross-platform application design for an easy use of steganography, in this case hiding messages into pictures or sounds.

</div>
<div>

![alt="Steghide"](https://steghide.sourceforge.net/images/logo.png "centered")

<br>
<br>

![w:600](https://github.com/achorein/silenteye/blob/0.4/website/static/images/header.jpg?raw=true "centered")

</div>

---

<div style="padding-bottom:150px">

## Theory

</div>

<div class="columns-2" style="padding-bottom:200px">
<div >

![](../../figures/matirx.png) 

<br>

<br>

![](../../figures/diff.png)

</div>
<div>

![](../../figures/encode.png)

</div>
</div>

Least signifcant bit, means the least signifcant impact on the original image

---

<!-- header: "_Cryptography_" -->

## Encryption - Substitution Cipher

<div style="padding-bottom:40px">

![drop-shadow](../../figures/transposition_one.png "centered")

</div>

*Also known as Ceaser Cipher

---



## Ceaser Cipher



<div style="padding-top:150px">

Example: Backward shift of 6

Assumption: ?

- ROTAD

</div>

---


## Hashing

<div class="columns-2" style="font-size:28px;padding-bottom:150px">
<div style="padding-top:150px">

 **Windows**
 
 ```cmd
 certutil–hashfile <filename>    <md5, sha1, sha256, sha512>    [ENTER]
 ```
 
 **Linux/macOS**

 ```sh
 sha256sum   <filename>    [ENTER]
 ```
</div>
<div style="padding-top:200px">

![drop-shadow center w:700](../../figures/hashing.png)

</div>
</div>

The major difference between Hashing and Encryption is that: 
- No keys are used in hashing but only algorithms e.g., MD5

---

## Types of Encryption

![drop-shadow w:1200](../../figures/asym_sym.png "centered")

----

## Symmetric

<div class="columns-2" style="padding-top:100px">
<div>

![drop-shadow w:800](../../figures/sym.png)

</div>
<div style="font-size:28px">

 - Same key for encryption
 - Key sharing is a problem
 - Low overhead
 - Fast
 - Sutiable for transmitting bluk data

</div>
</div>

---

## Asymmetric

<div class="columns-2" style="padding-top:100px">
<div style="padding-top:60px">

![drop-shadow w:800](../../figures/asym.png)

</div>
<div style="font-size:28px">

- Uses Public Key Infrastructure (PKI)
- Both parties have their key pair
- One key for encryption, another for decryption
- Solves the problem of key sharing
- High overhead
- No need to/and never share your private key

</div>

---

## Example Asymetric

<div class="columns-2">
<div style="padding-top:200px">

**Generate Key**

```sh
$ ssh-keygen -t ed25519 -C "ELEE1171"
```

</div>
<div style="padding-top:100px">

**Public key**

```sh
cat ~/.ssh/id_ed25519.pub
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJqFxk/iuYfO2GeOx4BTK4Gy0Mhe1g7SQYmQRYnqu3zP ELEE1171
```

**Private Key**

```sh
cat ~/.ssh/id_ed25519
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACCahcZP4rmHzthnjseAUyuBstDIXtYO0kGJkEWJ6rt8zwAAAJDGb9KYxm/S
mAAAAAtzc2gtZWQyNTUxOQAAACCahcZP4rmHzthnjseAUyuBstDIXtYO0kGJkEWJ6rt8zw
AAAED0Oks/Py0THM2cX0k+QqhjzGx4CZ6xXU3UL3vejLTHRJqFxk/iuYfO2GeOx4BTK4Gy
0Mhe1g7SQYmQRYnqu3zPAAAACEVMRUUxMTcxAQIDBAU=
-----END OPENSSH PRIVATE KEY-----
```

</div>
</div>

----

## Encryption Algorithms

<div style="font-size:22px">

|Algorithm|	Key Type|	Key Length (bits)|	Strengths	|Common Uses|
|---|----|---|---|---|
|AES|	Symmetric	|128, 192, 256|	Fast, secure, widely used|	File encryption, TLS, VPNs|
|DES|	Symmetric	|56|	Weak, outdated|	Legacy encryption|
|3DES|	Symmetric	|112, 168|	More secure than DES but slower|	Banking, legacy systems|
|ChaCha20	|Symmetric	|256	|Fast, efficient for mobile/IoT|	Secure messaging, mobile encryption|
|Blowfish	|Symmetric|	32-448|	Flexible key sizes, strong security	|File encryption, password hashing|
|RSA|	Asymmetric|	1024, 2048, 4096|	Strong security, widely used|	SSL/TLS, email encryption|
|ECDSA|	Asymmetric|	256, 384, 521|	Efficient for digital signatures|	Digital signatures, SSL/TLS|
|Ed25519|	Asymmetric	|256|	Highly efficient, secure, resistant to quantum attacks|	SSH, Git, digital signatures|
|DSA|	Asymmetric|	1024, 2048, 3072|	Secure, used in government applications|	Government applications, digital signatures|
|Diffie-Hellman|	Asymmetric	|Varies|	Used for secure key exchange|	Key exchange, secure communication|

</div>

---

## Digital Signature

<div style="font-size:28px; padding-top:220px">

-  Digital Signature: 
   -  Encrypt message hash with private key, and recipient decrypts hash using sender’s public key. 
   -  This verifies **authenticity**

</div>

![drop-shadow bg right:50% 90% ](../../figures/digital_sig_one.png)

---

## Combining Digital Signature With PKI

<div style="font-size:28px; padding-top:220px">

-  Digital Signature: Encrypt message hash with private key, and recipient decrypts hash using sender’s public key. This verifies **authenticity**

</div>

![drop-shadow bg right:50% 90% ](../../figures/digital_sig_two.png)

---

## Digital Certifcates

<div style="font-size:24px; padding-top:180px">

- Digital Certificate: A file that contains your public key and other necessary information to verify the validity and authenticity of your public key.

- Issued by the Certificate Authority (CA)

- A digital certificate is issued after verification of the website or Organisation.

- This is the mechanism your browser uses to detect secure websites

</div>

![drop-shadow bg right:50% 90% ](../../figures/Dig_sig_CA.png)

---

## Asymmetric vs Symmetric: Which Should I Use?

<div style="padding-top:150px">

![drop-shadow w:800](../../figures/SecOpTriad.png "centered")

---

## Asymmetric vs Symmetric: Which Should I Use?

![drop-shadow w:800](../../figures/SecOpTriad.png "centered")

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
