---
tags:
  - it/OpenSSL
  - it/Cryptography
  - it/TLS
  - SSL
  - it/cli
  - it/cybersecurity/CISSP
aliases:
  - openssl guide
  - openssl tutorial
---

# 🛡️ OpenSSL Complete Guide: From Basics to Advanced

Welcome to the **Obsidian Vault** documentation for mastering **OpenSSL** — from the basics of key generation to advanced certificate manipulation and encryption.

---

## 📘 Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Basic Commands](#basic-commands)
4. [Key Management](#key-management)
5. [Certificate Management](#certificate-management)
6. [CSRs (Certificate Signing Requests)](#csrs-certificate-signing-requests)
7. [Encrypting and Decrypting Files](#encrypting-and-decrypting-files)
8. [Debugging & Inspecting Certificates](#debugging--inspecting-certificates)
9. [Advanced Usage](#advanced-usage)
10. [OpenSSL in Real-World Use Cases](#openssl-in-real-world-use-cases)

---

## 🧾 Introduction

**OpenSSL** is an open-source command-line toolkit that implements the SSL and TLS protocols. It also provides cryptographic operations such as hashing, symmetric/asymmetric encryption, and certificate management.

---

## 💻 Installation

### Ubuntu/Debian:
```bash
sudo apt update
sudo apt install openssl
```

### macOS:
```bash
brew install openssl
```

### Windows:
Use [https://slproweb.com/products/Win32OpenSSL.html](https://slproweb.com/products/Win32OpenSSL.html)

---

## 🧰 Basic Commands

### Check OpenSSL Version:
```bash
openssl version
```

### List Available Ciphers:
```bash
openssl ciphers -v
```

---

## 🔑 Key Management

### Generate RSA Private Key:
```bash
openssl genrsa -out private.key 2048
```

### Extract Public Key:
```bash
openssl rsa -in private.key -pubout -out public.key
```

### Convert to PKCS #8:
```bash
openssl pkcs8 -topk8 -inform PEM -in private.key -outform PEM -nocrypt
```

---

## 📜 Certificate Management

### Generate Self-Signed Certificate:
```bash
openssl req -x509 -new -nodes -key private.key -sha256 -days 365 -out cert.crt
```

### View Certificate Content:
```bash
openssl x509 -in cert.crt -text -noout
```

### Convert PEM to DER:
```bash
openssl x509 -outform der -in cert.crt -out cert.der
```

---

## 📩 CSRs (Certificate Signing Requests)

### Generate CSR:
```bash
openssl req -new -key private.key -out request.csr
```

### View CSR Details:
```bash
openssl req -in request.csr -text -noout
```

---

## 🔐 Encrypting and Decrypting Files

### Encrypt with AES-256:
```bash
openssl enc -aes-256-cbc -salt -in file.txt -out file.txt.enc
```

### Decrypt the File:
```bash
openssl enc -aes-256-cbc -d -in file.txt.enc -out file_decrypted.txt
```

---

## 🕵️‍♂️ Debugging & Inspecting Certificates

### Verify Private Key:
```bash
openssl rsa -in private.key -check
```

### Check Certificate and Key Match:
```bash
openssl x509 -noout -modulus -in cert.crt | openssl md5
openssl rsa -noout -modulus -in private.key | openssl md5
```

---

## 🧠 Advanced Usage

### Create a PFX File (PKCS#12):
```bash
openssl pkcs12 -export -out cert.pfx -inkey private.key -in cert.crt
```

### Extract from PFX:
```bash
openssl pkcs12 -in cert.pfx -out extracted_cert.pem -nodes
```

### Create Certificate Chain:
```bash
cat intermediate.crt root.crt > chain.crt
```

---

## 🌐 OpenSSL in Real-World Use Cases

- 📶 HTTPS Server Setup with Apache/Nginx
- 🧾 Secure Email with S/MIME
- 🔒 Encrypt backups and sensitive archives
- ✅ TLS Mutual Authentication
- 🔁 VPN Certificates (e.g., OpenVPN)

---

## 🧠 Mnemonics for Memory:
**CRISP CERTS**
- **C**reate Keys
- **R**equest CSRs
- **I**nspect Certificates
- **S**ign or Self-Sign
- **P**arse Key Details
- **C**onvert Formats
- **E**ncrypt Files
- **R**eview Validity
- **T**est TLS Connectivity
- **S**ecure with Protocols

---
