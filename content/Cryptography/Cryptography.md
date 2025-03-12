---
title: Intro to Cryptography
description: Intro to Cryptography Slides
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
      font-size: 16.5px;
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

<!-- _footer: "[Download as a PDF](https://github.com/UniOfGreenwich/ELEE1171_Lectures/raw/gh-pages/content//c/Users/dev/Git/UoG/ELEE1171/Lectures/content/Cryptography/Cryptography.pdf)" -->

# Intro to Cryptography

    Module Code: ELEE1171

    Module Name: Securing Technologies

    Lecturer: Seb Blair BEng(H) PGCAP MIET MIHEEM FHEA

---


## Main Goals of Security: CIA

- Confidentiality

- Integrity
  
- Availability

![bg right:50% 80%](../../figures/CIA.jpg)

---

## Quick Definitions

<div style="font-size:24px">

- **Cryptography**: the art of secret writing!

- **Encryption**: converting information to a format **unreadable by unintended recipients**. Only intended recipients  with the correct key and algorithm can read it and get its true meaning.

- **Hashing**: converts data or message into an irreversible string of fixed length.
- Confidentiality can be achieved using **Encryption**
- Data Integrity can be verified using **Hashing**

</div>

---

##  Why Do We Need Cryptography?

<div style="padding-top:100px">

![](../../figures/why_do_we_need_crypt.png)

</div>

---

## Encryption - Substitution Cipher

<div style="padding-bottom:40px">

![center](../../figures/transposition_one.png)

</div>

---

## Hashing


![center w:700](../../figures/hashing.png)

<div style="font-size:22px">

 **Windows**
 
 ```cmd
 certutil–hashfile <filename>    <md5, sha1, sha256, sha512>    [ENTER]
 ```
 
 **Linux/macOS**

 ```sh
 sha256sum   <filename>    [ENTER]
 ```

 The major difference between Hashing and Encryption is that:
 No keys are used in hashing but only algorithms e.g., MD5

 </div>

---

## Types of Encryption

![center w:700](../../figures/asym_sym.png)

----

## Symmetric

![center w:750](../../figures/sym.png)

<div style="font-size:22px">

 - Same key for encryption
 - Key sharing is a problem
 - Low overhead
 - Fast
 - Sutiable for transmitting bluk data

</div>

---

## Asymmetric

![center w:750](../../figures/asym.png)

<div style="font-size:22px">

- Uses Public Key Infrastructure (PKI)
- Both parties have their key pair
- One key for encryption, another for decryption
- Solves the problem of key sharing
- High overhead
- No need to/and never share your private key

</div>

---

## Example Asymetric

<div style="font-size:21px">

**Generate Key**

```sh
$ ssh-keygen -t ed25519 -C "ELEE1171"
```

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

---

## Digital Signature

<div style="font-size:24px; padding-bottom:20px">

-  Digital Signature: Encrypt message hash with private key, and recipient decrypts hash using sender’s public key. This verifies **authenticity**

</div>

![center w:1000](../../figures/digital_sig_one.png)

---

## Combining Digital Signature With PKI

<div style="font-size:24px; padding-bottom:20px">

-  Digital Signature: Encrypt message hash with private key, and recipient decrypts hash using sender’s public key. This verifies **authenticity**

</div>

![center w:1000](../../figures/digital_sig_two.png)

---

## Digital Certifcates

<div style="font-size:24px;">

- Digital Certificate: A file that contains your public key and other necessary information to verify the validity and authenticity of your public key.

- Issued by the Certificate Authority (CA)

- A digital certificate is issued after verification of the website or Organisation.

- This is the mechanism your browser uses to detect secure websites

</div>

![bg right:50% 90%](../../figures/Dig_sig_CA.png)

----

## Encryption Algorithms


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

---

## Asymmetric vs Symmetric: Which Should I Use?

![](../../figures/SecOpTriad.png)