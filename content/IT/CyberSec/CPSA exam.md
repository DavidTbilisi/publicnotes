---
tags:
  - it/cybersecurity/CISSP
  - it/cybersecurity
  - academic
---
| Abbreviation   | Version (Example/Vulnerable)    | Full Name                             | Port Number(s)                       | Main Idea                                                                                      | Common Vulnerability                                                                                                                        | Mnemonic                                                                                       | **Russian Mnemonic**                                                                                                                               |
| :------------- | :------------------------------ | :------------------------------------ | :----------------------------------- | :--------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **DNS**        | N/A                             | Domain Name System                    | UDP/53, TCP/53                       | Translates domain names to IP addresses.                                                       | DNS zone transfers can expose sensitive information.                                                                                        | **D**omain **N**ames **S**olve **P**roblems on port **53**.                                    | **Пятьдесят три богатыря** (**53** warriors).                                                                                                      |
| **HTTP**       | N/A                             | HyperText Transfer Protocol           | TCP/80                               | Application-layer protocol for accessing the World Wide Web.                                   | Insecure protocol as data is transferred in clear-text.                                                                                     | **H**yper **T**ext **T**ravels on port **80**.                                                 | **Восемьдесят бабушек** (**80** grandmothers).                                                                                                     |
| **HTTPS**      | N/A                             | HyperText Transfer Protocol Secure    | TCP/443                              | Secure version of HTTP using SSL/TLS encryption.                                               | Insecure SSL certificate configurations (e.g., weak encryption protocols).                                                                  | **H**yper **T**ext **T**ravels **S**ecurely on port **443**.                                   | **Четыреста сорок три кошки** (**443** cats).                                                                                                      |
| **Telnet**     | Solaris 10/11 (Bypass)          | Telecommunication Network             | TCP/23                               | Lightweight, clear-text protocol for remote management of hosts/network devices.               | Insecure protocol due to clear-text authentication and data transmission. Can be brute-forced. Vulnerabilities in banners.                  | **Tel**l **Net**work details on port **23** are **clear**.                                     | **Двадцать три дровосека** (**23** lumberjacks).                                                                                                   |
| **TFTP**       | N/A                             | Trivial File Transfer Protocol        | UDP/69                               | Simple protocol for transferring files, but lacks many features like authentication.           | No built-in security mechanisms; doesn't support directory listing.                                                                         | **T**rivial **F**ile **T**ransfer on port **69** is **easy**.                                  | **Шестьдесят девять гусей** (**69** geese).                                                                                                        |
| **SSH**        | OpenSSH 3.3 (Overflow)          | Secure Shell                          | TCP/22                               | Secure protocol for remote administration, data transfer, and secure access.                   | Susceptible to brute-force attacks. Known vulnerabilities in different versions.                                                            | **S**ecure **SH**ell on port **22** is **secure**.                                             | **Двадцать две сороки** (**22** magpies).                                                                                                          |
| **NTP**        | 4.2.4p8 (Example)               | Network Time Protocol                 | UDP/123                              | Protocol to synchronize the clocks of devices within a network.                                | Disclosing NTP version and operating system information.                                                                                    | **N**etwork **T**ime on port **123** keeps time **precise**.                                   | **Сто двадцать три богатыря** (**123** warriors again, must be punctual!).                                                                         |
| **SNMP**       | v1, v2c (Clear-text)            | Simple Network Management Protocol    | UDP/161                              | Protocol to collect information from network devices for management.                           | SNMPv1 and v2c pass community strings in clear-text, acting like passwords.                                                                 | **S**imple **N**etwork **M**anagement on port **161** needs a **password** (community string). | **Сто шестьдесят один слон** (**161** elephants).                                                                                                  |
| **NetBIOS**    | N/A                             | Network Basic Input/Output System     | UDP/137, UDP/139, TCP/139            | Legacy protocol for communication between devices on a local network.                          | Can be used to gather role information within a domain.                                                                                     | **Net**work **BIOS** on ports **137/139** helps **find** devices.                              | **Сто тридцать семь лягушек и сто тридцать девять обезьян** (**137** frogs and **139** monkeys - a noisy network!).                                |
| **SMB**        | MS17-010 (EternalBlue)          | Server Message Block                  | TCP/445                              | Protocol for resource and file sharing in Microsoft Windows environments.                      | Vulnerable to various exploits like MS17-010 (EternalBlue). NULL share enumeration.                                                         | **S**erver **M**essage on port **445** allows **sharing**.                                     | **Четыреста сорок пять муравьев** (**445** ants - always sharing).                                                                                 |
| **FTP**        | N/A                             | File Transfer Protocol                | TCP/21 (Control)                     | Used to send and receive files across a network.                                               | Key risk is unauthorized data access.                                                                                                       | **F**ile **T**ransfer on port **21** helps **move** files.                                     | **Двадцать один гном** (**21** gnome - carrying files).                                                                                            |
| **rsh**        | N/A                             | Remote Shell                          | TCP/514                              | Allows executing commands on a remote Unix system.                                             | Uses .rshosts for authentication based on IP addresses and DNS hostnames, no password required, insecure.                                   | **R**emote **sh**ell on port **514** is **risky**.                                             | **Пятьсот четырнадцать разбойников** (**514** robbers - remotely controlling!).                                                                    |
| **rlogin**     | N/A                             | Remote Login                          | TCP/513                              | Allows logging into a remote Unix system.                                                      | Relies on .rhosts file for authentication, insecure, no encryption.                                                                         | **R**emote **login** on port **513** is **leaky**.                                             | **Пятьсот тринадцать шпионов** (**513** spies - logging in secretly).                                                                              |
| **rexec**      | N/A                             | Remote Execution                      | TCP/512                              | Allows executing a command on a target machine.                                                | Passwords used for authentication are transmitted in clear text.                                                                            | **R**emote **exec**ute on port **512** sends passwords in **plaintext**.                       | **Пятьсот двенадцать почтальонов** (**512** postmen - delivering clear messages).                                                                  |
| **SIP**        | N/A                             | Session Initiation Protocol           | UDP/5060 or TCP/5060                 | Signaling protocol used for Voice over IP (VoIP) to establish, modify, and terminate sessions. | Users can potentially be enumerated using the 'OPTIONS' SIP method.                                                                         | **S**IP on port **5060** **starts** phone calls.                                               | **Пять тысяч шестьдесят сов** (**5060** owls - making calls at night).                                                                             |
| **MySQL**      | N/A                             | MySQL                                 | TCP/3306                             | A common relational database management system.                                                | Vulnerabilities like SQL Injection if input is not properly validated.                                                                      | **My** **SQL** database on port **3306**.                                                      | **Три тысячи триста шесть мышей** (**3306** mice - storing lots of data).                                                                          |
| **OracleDB**   | N/A                             | Oracle Database                       | TCP/1521, TCP/1830                   | A widely used relational database management system.                                           | Vulnerabilities like SQL Injection. Exposure of TNS listener information. Default credentials risk.                                         | **O**racle **DB** on ports **1521/1830**.                                                      | **Одна тысяча пятьсот двадцать одна обезьяна и одна тысяча восемьсот тридцать змей** (**1521** monkeys and **1830** snakes - guarding the Oracle). |
| **PostgreSQL** | N/A                             | PostgreSQL                            | TCP/5432                             | An open-source relational database management system.                                          | Vulnerabilities like SQL Injection.                                                                                                         | **Postgre**s **SQL** on port **5432**.                                                         | **Пять тысяч четыреста тридцать две птицы** (**5432** birds).                                                                                      |
| **MSSQL**      | 2000, 2005, 2012 (Hash Formats) | Microsoft SQL Server                  | TCP/1433                             | A relational database management system developed by Microsoft.                                | Vulnerabilities like SQL Injection. Ability to execute OS commands via `xp_cmdshell` if credentials are known. Enumerating password hashes. | **M**icrosoft **SQL** on port **1433**.                                                        | **Одна тысяча четыреста тридцать три кота** (**1433** cats).                                                                                       |
| **LDAP**       | N/A                             | Lightweight Directory Access Protocol | TCP/389 (insecure), TCP/636 (secure) | Protocol for accessing and modifying directory services, like Active Directory.                | Vulnerable to LDAP Injection attacks if input is not sanitized.                                                                             | **L**ightweight **D**irectory on port **389/636** needs **protection**.                        | **Триста восемьдесят девять бобров и шестьсот тридцать шесть бегемотов** (**389** beavers and **636** hippos - managing the directory carefully).  |

## CPSA Cheat Sheet

This cheat sheet summarizes key concepts from the CPSA course materials.

### Law & Compliance

- **Computer Misuse Act (CMA) 1990**:
    - **Section 1**: **Unauthorised Access to Computer Material**. Examples include exploiting vulnerabilities, shoulder surfing for passwords, and bypassing security to access file shares.
    - **Section 2**: **Unauthorised access with intent to commit or facilitate the commission of further offences**. Examples include creating new accounts, installing RATs, and selling network access.
    - **Section 3**: **Unauthorised Acts with intent to impair, or with recklessness as to impairing the operation of a computer**. Examples include DDoS attacks, spam attacks, and ransomware installation.
    - **Amendments**: Made to more accurately define illegal activity.
    - **Section 3A (Police and Justice Act 2006)**: Illegal to create, supply, or obtain tools for committing CMA offences.
    - **Section 3ZA (Serious Crime Act 2015)**: Unauthorized acts causing or creating the risk of serious material damage illegal, especially if posing safety or national security risks.
- **Data Protection Act (DPA) 2018**: Updated law incorporating GDPR into UK law.
    - Governs data use and storage related to living individuals, on computers and paper.
    - **Personal Data Definition**: Includes name, address, DOB, contact details, job history.
    - **Key Principles**: Data must be obtained fairly and lawfully, held only for registered purposes, not disclosed incompatibly, relevant and not excessive, accurate and up-to-date, not kept longer than necessary, individuals have access/correction/removal rights, and must be protected against unauthorized access.
- **General Data Protection Regulation (GDPR) 2018**:
    - **Key Roles**: **Controller** (determines purposes and means of processing), **Processor** (processes data on behalf of controller).
    - **Key Differences with DPA**: Age of consent (GDPR: 16, DPA: 13), Automated decision making (DPA allows with safeguards, GDPR prohibits), Scope clarification for areas excluded from GDPR (DPA), Regulatory Body (DPA details ICO role).
- **Human Rights Act 1998**: Enforces European Convention on Human Rights into UK law.
    - **Article 8**: Right to privacy. Personal life should not be included in assessments.
- **Legal Measures for Penetration Testers**:
    - **Obtain explicit, written consent**.
    - **Stay within agreed-upon scope**.
    - **Avoid breaching GDPR**.
    - **Ensure authorized and documented tools**.
    - **Be aware of international implications**.

### Engagement Lifecycle

- **Benefits of Penetration Testing**: Identify risks, assess IR effectiveness, ensure business continuity, meet compliance, justify security budgets.
- **Activities**: **Pre-Engagement**, **Information Gathering and Enumeration**, **Vulnerability Identification**, **Exploitation**, **Post Exploitation**, **Reporting**.
- **Pre-Engagement**: Key to a successful test.
    - **Scoping**: Defines what is tested and how. Client provides explicit details of in-scope and out-of-scope systems. Testers assess only in-scope systems. A **Scoping Questionnaire** helps understand client requirements (e.g., internal/external, web application). Information forms a **Scoping Document**. Key information includes number of hosts, IP ranges, web applications, and need to bypass controls. Assists in resource allocation, timeline, and cost.
    - **Pre-requisites**: Testers define further access and detail requirements after scoping. Actioned before testing to prevent delays.
    - **Contracts/NDAs/Authorisation forms**: Legal agreements confirming permission and commercial details.
    - **Tester Awareness**: Identify mission-critical systems, access restrictions, environment type (Production, etc.), backup status, technical points of contact.
- **Enumeration**: Identify live systems, running services, software versions, operating systems. Prioritize systems for deeper probing.
- **Vulnerability Identification**: Identify potential methods of compromise after enumeration.
- **Exploitation**: Demonstrating issues, may not always involve full exploitation due to scope. **Explicit client permission** is essential for disruptive exploits. Includes trivial (e.g., phishing) and advanced techniques. Document ease of exploitation.
- **Post Exploitation**: Actions after initial foothold. Data from one machine can compromise the entire network. Provides evidence of attack repercussions (e.g., gathering credentials, identifying other networks).
- **Reporting**: Provides accurate, detailed, and actionable information. The report is the main evidence. Should be understandable for various audiences.
    - **Executive Summary**: High-level overview for non-technical stakeholders, business impacts, risk summary, strategic recommendations.
    - **Technical Summary**: Detailed explanation of each issue for technical teams, including proof of concepts and recommendations.
- **Record Keeping**: Maintain accurate records of findings with **high-resolution screenshots/code snippets** and detailed notes.
- **Interim Reporting**: Inform client of **critical severity findings** immediately, as well as system outages or evidence of compromise.
- **Project Closure / Debrief**: Remove all testing artifacts (exploit code, uploaded files, temporary accounts). Aim to leave systems in their original state. Highlight any inability to remove artifacts. Debrief may summarize findings, business risk, testing impacts, and retest needs.
- **Types of Engagement**: White Box, Grey Box, Black Box Testing.

### Introduction to Networking

- **TCP VS UDP**:
    - **TCP (TCP/21, 22, 23, 53, 80, 443, 445, 512, 513, 514, 1521, 1830, 3306, 5060, 636, 1433, 389)**: Connection-oriented, reliable data delivery with error checking and guaranteed delivery. Uses a **three-way handshake** (SYN, SYN-ACK, ACK) to establish a full-duplex connection. Suitable for images, data files, web pages.
    - **UDP (UDP/53, 69, 123, 137, 139, 161, 500, 1985, 5060)**: Connectionless, faster but unreliable, no guaranteed delivery or error checking.
- **ICMP**: Used for network diagnostics and error reporting. Includes a **Code** field to specify the message type and a **Checksum** for integrity.
- **OSI Model (7 Layers)**: Application, Presentation, Session, Transport, Network, Data Link, Physical. Logical and conceptual model for network communication.
- **TCP/IP Model (4 Layers)**: Application, Transport, Internet, Network Access. Open, vendor-neutral networking model.
- **IP Addressing**: **Public** and **Private** IP Addresses. **IPV4 Address Classes** exist. **Binary to Decimal Conversion** is fundamental.
- **Subnet Masks**: Used to divide networks into smaller subnetworks.

### Network Architectures

- **Network Media**: Connects nodes/hosts.
    - **Cabling (Ethernet)**: Physical cables with categories (CAT) defining speed and protection.
    - **Shielded Twisted Pair (STP)**: Foil wrapping for individual pairs and overall, reduces EMI/RFI. Braided (90%), Spiral (98%), Metal-coated Mylar/foil (100%) shielding.
    - **Unshielded Twisted Pair (UTP)**: Twisted pairs without wrapping, less expensive.
    - **Fiber Optics**: High-speed transmission using light. Core holds light, cladding limits it. Tighter cladding and smaller core = faster speed and further distance.
- **Security Concerns with Switches**:
    - **Physical access**: Attackers plugging in can gain network access.
    - **DHCP vs Static IP**: DHCP is easier but exploitable. Static IP is harder to leverage without config knowledge.
    - **Mitigation**: Configure switch ports to prevent unauthorized trunk port negotiation (prevents VLAN hopping).

### Network Mapping

- **Nmap (Network Mapper)**: Powerful tool for mapping network hosts and services. Used for network discovery and security auditing. Helps understand running devices and services.
- **Banner Grabbing**: Connect to open ports to retrieve service banners containing software version and identifying information, aiding in vulnerability identification.
- **DNS Zone Transfer (AXFR)**: Used to obtain a copy of DNS records from a DNS server. Use `dig axfr @<DNS_IP> <DOMAIN>`.

### Google Hacking (Dorking)

- Uses advanced search operators to find information not easily accessible through regular queries. Often uncovers exposed sensitive information or misconfigured web servers.
- **Shodan**: Search engine for internet-connected devices, indexes open ports, services, and device banners.

### Information Disclosure From Mail

- **NNTP Newsgroup (TCP/119)**: Allows connection to news servers.
- **Document Metadata Collection**: Using tools like **FOCA** and **Metagoofil**. Google Dorks can identify open documents (e.g., `site:tesla.com filetype:pdf`). Metadata can reveal author and software used, aiding targeted social engineering.
- **Email Headers**: Contain information about the sender, recipient, path, and other details of an email.

### Network and Management Protocols

- **Address Resolution Protocol (ARP)**: Maps IP addresses to MAC addresses within the same network. Devices use ARP requests to find MAC addresses and ARP replies to respond. Maintains an **ARP cache** to speed up communication.
- **Telnet (TCP/23)**: Insecure clear-text protocol for remote access. Telnet banners can reveal OS and have common vulnerabilities. **Cisco Reverse Telnet** allows connecting to console ports of other devices via a router.
- **Trivial File Transfer Protocol (TFTP) (UDP/69)**: Simple protocol for file transfer, commonly used for boot images and reading/writing files to remote servers. No directory listing, requires knowing filenames. Enumeration can be done with Nmap scripts or Metasploit modules.
- **Secure Shell (SSH) (TCP/22)**: Secure encrypted protocol for remote access. Configuration in `/etc/ssh/ssh_config`. Supports password and key-based authentication. **SSH1** is less secure than **SSH2**. **X11 forwarding** (`ssh -X`) allows secure GUI application forwarding.
- **Network Time Protocol (NTP) (UDP/123)**: Synchronizes clocks of network devices, crucial for logging and authentication. Can be enumerated using `ntpq -c v -d` to disclose version and OS information.
- **Simple Network Management Protocol (SNMP) (UDP/161)**: Collects information from network devices for management. Uses **Management Information Base (MIB)** and **Object Identifiers (OIDs)**. **SNMPv1** uses clear-text community names for security. **SNMPv2c** improved error handling but still no encryption. **SNMPv3** offers enhanced security with authentication and encryption. Enumeration requires valid community names, tools include `onesixtyone`, `snmpwalk`, `snmpcheck`, Metasploit. Common community names: `public`, `private`, `cisco`, `manager`. `snmpwalk -v <version> -c <community> <IP>`.
- **Server Message Block (SMB) / CIFS (TCP/445)**: Facilitates file and resource sharing (Windows and others). **NULL shares/sessions** allow access without credentials. Key shares: `C$`, `ADMIN$`, `IPC$`, `SYSVOL`, `NETLOGON`, `PRINT$`, `FAX$`. Enumeration tools: `net use`, `rpcclient`, `smbmap`. Vulnerabilities like **MS17-010 (EternalBlue)** can lead to remote code execution.
- **Cisco Discovery Protocol (CDP)**: Cisco proprietary protocol to share information about directly connected Cisco equipment (OS version, IP address). Sends announcements to multicast `01-00-0c-cc-cc-cc` every 60 seconds. Information stored in a neighbors table (`show cdp`). Vulnerabilities: Information disclosure by sniffing, spoofing CDP packets, flooding neighbors table (DoS).
- **Hot Standby Router Protocol (HSRP) (UDP/1985)**: Cisco redundancy protocol for fault-tolerant default gateway. Sends hello messages to `224.0.0.2`. Vulnerabilities: DoS (flooding), MITM (becoming active router), clear-text authentication in older versions (newer uses MD5).
- **VLAN Trunking Protocol (VTP)**: Cisco proprietary Layer 2 protocol for managing VLANs network-wide. Vulnerabilities: Information disclosure (VLAN IDs), VLAN modification (misconfiguration), DoS (Catalyst crash).
- **Spanning Tree Protocol (STP)**: Prevents loops in bridged LAN topologies. Uses Bridge Protocol Data Units (BPDU). No authentication, allowing malicious BPDUs. Vulnerabilities: Configuration changes via raw BPDUs, claiming root role for MITM.
- **Terminal Access Controller Access-Control System Plus (TACACS+) (TCP/49)**: Remote authentication protocol (commonly UNIX). Encrypts the entire payload (including credentials), unlike RADIUS. Security concern: Packet headers are not encrypted.

### Cisco Configuration Analysis

- Process of assessing the configuration of network devices. CREST recommends learning Cisco configuration.
- **Web Server Configuration**: Cisco devices can run a web server (disabled by default except on some models). Default is insecure HTTP. Enable HTTPS with `ip http secure-server`.
- **Auxiliary Configuration**: Older routers/firewalls have an AUX port.
- **NTP Configuration**: Ensures accurate timestamps for security incidents. Check for at least one NTP server using "ntp server". Recommend configuring two for failover.
- **Logging Configuration**: Crucial for investigating Indicators of Compromise (IoC). By default, no timestamps. Enable with `Service timestamps log datetime localtime show-timezone msc`.
- **SNMP Configuration**: Check for strong community strings (upper/lowercase, numbers, special chars, avoid company names). Use SNMPv3 for enhanced security with authentication and encryption.
- **Cisco Password Security**: Password hashes stored in the configuration file. Use strong hash types.
    - **Type 0**: Clear text (insecure).
    - **Type 4**: Unsalted SHA-256 (crackable).
    - **Type 5**: MD5 (crackable with tools).
    - **Type 7**: Vigenère Cipher (easily decodable).
    - **Type 8**: PBKDF2-SHA-256 (harder to crack).
    - **Type 9**: Scrypt (most secure).

### Windows Security Assessments

- Process of enumerating a corporate network (typically Active Directory) to obtain valuable information for attacks. Goals: uncover file shares, discover compromised accounts, gather role information.
- **Active Directory (AD)**: Centralized management of users, computers, and resources. Key components: domains, domain controllers, forests, OUs, objects. Handles authentication and authorization using Group Policy Objects (GPOs). Uses LDAP for directory access.
- **AD Services**:
    - **DNS (TCP/53, UDP/53)**: Used for DNS zone transfers (AXFR).
    - **Global Catalog**: Partial replica of all objects for faster forest-wide searching.
    - **Master Browser**: Maintains list of available devices for workgroups/domains not solely relying on DNS/AD.
- **FSMO Roles**: PDC Emulator (time), RID Master (RIDs), Infrastructure Master (cross-domain references), Schema Master (schema modifications), Domain Naming Master (domain/forest naming).
- **Group Policy Objects (GPOs)**: Enforce security settings and configurations. **Group Policy Preference (GPP) Attack Vector**: Passwords and other sensitive info stored in GPOs are readable by any domain user and can be decrypted with freely available tools or Metasploit module `post/windows/gather/credentials/gpp`.
- **Gathering Role Information**:
    - **Nbtscan-unixwiz**: Can retrieve NetBIOS hostname, domain/workgroup, current user, MAC address, system role (DC, File Server). Command: `Nbtscan-unixwiz –f <<IP or IP range>>`.
    - **Compromised Windows System**: `nltest.exe /dclist:<domain>`, `netdom.exe QUERY /Domain:<domain> DC/WORKSTATION/SERVER`.
    - **Meterpreter Modules**: `post/windows/gather/enum_domains`, `enum_computers`, `enum_ad_computers`, `enum_domain`.
- **Enumerating Users and User Groups**:
    - **Local Users**: `net users`, `net user <USERNAME>`, `net localgroup Administrators`.
    - **Domain Users**: `net user <USERNAME> /domain`.
- **RID and SID**: Relative ID (RID) is unique within a domain. Security Identifier (SID) is unique across all domains.
- **RID Cycling**: Reverse lookup on RID to get username. Requires NULL session and tools like `user2sid.exe` and `sid2user.exe`.
- **LDAP Enumeration**: Tools like `ldapsearch` can be used to enumerate computers and usernames. Example commands provided.
- **Obtaining Domain Admin**: Major goal. May require multiple compromises. Post-exploit activities: `hashdump`, `net users`, `systeminfo`, `wmic qfe get`, `ipconfig /all`.
- **Dumping Hashes on a DC**: Domain account hashes in Active Directory within `ntds.dit` file. Local account hashes in SAM database.
    - **Metasploit**: `hashdump`.
    - **Manual Dump**: `ntdsutil.exe` to create a full copy.
- **Formatting and Cracking Hashes**: Use tools like `impacket-secretsdump`, `john`, `hashcat`.
- **Hash Storage**: LANMAN and NTLM.

### Windows Security

- **LANMAN (LAN Manager) Authentication**: Older, major weaknesses include 14-character limit (case-insensitive, split into two 7-char blocks), no salt, DES encryption.
- **NTLM (New Technology LAN Manager)**: Challenge-response mechanism, supports variable length hashing, but no server-side validation, vulnerable to MITM and NTLM relay attacks (hashes stored in memory).
- **Password Cracking**: Offline process. Techniques: dictionary/wordlist attack, brute force, rainbow tables.
- **Password Brute Forcing**: Trial-and-error. Dictionary brute force uses wordlists.
- **Password Policies Best Practices**: Unique passwords, use symbols, passphrases, minimum 12 characters, periodic reassessment, MFA, audit against breaches, password managers, avoid personal details.
- **Patch Management**: Crucial to address vulnerabilities. Tools: Windows Update, WSUS, SCCM, MBSA.
- **Privilege Escalation**: Exploiting vulnerabilities to gain higher-level permissions. Common vulnerabilities: unpatched systems (e.g., EternalBlue), misconfigured services.
- **Common Post-Exploitation Activities**:
    - Obtaining Password Hashes from SAM (using Mimikatz).
    - Obtaining Cached Credentials (using Mimikatz, crack with Hashcat).
    - Obtaining locally-stored cleartext passwords (using Mimikatz).
    - Checking Patch levels (WMIC `qfe`).
- **Common Windows Privilege Escalation Vulnerabilities**: Examples listed.
- **Microsoft Exchange Vulnerabilities**: ProxyLogon (CVEs listed), CVE-2022-41082, CVE-2022-41040.

### Desktop Lockdown

- Process of "hardening" an OS to limit user functionality and prevent breaches. Achieved by configuring user/network permissions, software/internet access.
- **Breakout Assessment**: Aims to assess how a malicious user can escape a hardened environment (e.g., Citrix/AVD).
- **Common Breakout Techniques**:
    - **Environmental**: Right-click Save (pointing to executables like `cmd.exe`, `powershell.exe`).
    - **Shortcuts**: Leveraging unrestricted keyboard shortcuts (examples provided).
    - **Software**: Using accessible software to launch command prompt (e.g., saving `.bat` in Notepad, file paths in web browsers, Paint exploit).

### Unix Security Assessments

- Key to understand the Unix version using `/etc/os-release` or `uname -a`.
- **File Permissions**: Essential for privilege escalation. Owner, Group, and World permissions (read, write, execute). Represented in triplets (e.g., `rwxr-xr--`).
- **File Enumeration**: Find sensitive information in files (usernames, hostnames, clear-text passwords) using `find` command with `-iname` and looking in home directories for history files (`.*_hist*`). Check common files for passwords (e.g., Apache configs, Anaconda config, MySQL user file). Knowing sensitive areas is fundamental.

### FTP

- **File Transfer Protocol (TCP/21)**: Used to send and receive files. Has two modes (not detailed).

### Berkeley R Services

- Used before widespread SSH adoption, insecure with limited security and no encryption.
    - **rsh (remote shell) (TCP/514)**
    - **rlogin (remote login) (TCP/513)**
    - **rexec (remote execution) (TCP/512)**
- Configuration in `/etc/hosts.equiv` and `.rhosts` can allow connections without passwords (e.g., `++` allows any host/user). Should no longer be used.

### IPsec

- **Internet Protocol Security**: Collection of protocols for secure connections (VPNs) by encrypting IP packets and authenticating source/destination.
- **Modes**: **Tunnel Mode** (encrypts header and payload), **Transport Mode** (encrypts payload only).
- **Components**: **Authentication Header (AH)** (integrity, authenticity, replay protection), **Encapsulating Security Payload (ESP)** (confidentiality). **Security Association (SA)** (defines protocol, algorithms, keys, lifetime) established via **Internet Key Exchange (IKE)**.
- **Internet Key Exchange (IKE) (UDP/500)**: Securely exchanges keys for AH/ESP. Should update keys periodically.
    - **Phase 1**: Authenticates hosts, establishes secure channel. **Main Mode** (6 messages, more secure), **Aggressive Mode** (3 messages, faster but less secure).
    - **Phase 2**: Negotiates IPsec SAs over the secure channel from Phase 1.
- **Enumerating IPsec**: If IKE Aggressive Mode is used, `ikecrack` can brute-force authentication messages offline. `ikeprobe` enumerates encryption configurations.

### VoIP

- **Voice over Internet Protocol (UDP/5060 or TCP/5060)**: Protocol for voice communication over IP networks.
- **SIP Methods**: INVITE, ACK, BYE, CANCEL, OPTIONS, REGISTER, PRACK, SUBSCRIBE, NOTIFY, PUBLISH, INFO, REFER, MESSAGE, UPDATE (descriptions provided).
- **Enumerating VoIP**: Use SIP `OPTIONS` method to probe for information and test connectivity. Tools: `svmap.py --fingerprint`, Metasploit `auxiliary/scanner/sip/options`.
- **Spoofing Caller ID**: Metasploit module `auxiliary/voip/sip_invite_spoof`.

### Wireless

- Allows hosts/devices to connect without ethernet cables.
- **WPA/WPA2**: Uses **PSK (Pre-Shared Key)**. Attacker needs to sniff traffic during authentication (4-way handshake) to capture the PSK for offline cracking.
- **PEAP (Protected Extensible Authentication Protocol)**: Enhances wireless security by encapsulating EAP within an encrypted tunnel.

### Encryption

- **Types**: **Symmetric** (same key for encryption/decryption), **Asymmetric** (different keys).
- **Functions**: Confidentiality, Authentication, Integrity.
- **Symmetric Ciphers**:
    - **Block Ciphers**: Encrypt fixed-length blocks (ECB, CBC).
    - **Stream Ciphers**: Work bit-by-bit.
    - **Common**: **AES** (128/192/256 bit blocks/keys), **RC4** (used in Kerberos), **DES** (deprecated, 56-bit key), **3DES** (DES applied thrice, 168-bit key).
- **Asymmetric Ciphers**: Public key encryption.
    - **Common**: **RSA** (key generation, encryption, decryption), **DSA** (digital signatures), **PGP** (uses both symmetric and asymmetric).
- **Weaknesses**: SSL/TLS vulnerabilities due to supporting older/weak algorithms.
    - **Heartbleed (2014)**: OpenSSL buffer over-read (up to 64KB memory).
    - **POODLE**: Downgrading attack from TLS to SSLv3, exploits CBC.
    - **BEAST**: MITM attack against SSL/TLSv1.0, leverages CBC.
- **Best Practice**: Disable deprecated protocols/weak algorithms/CBC ciphers, implement HSTS, enable secure cookie flag.
- **Encoding**: Reversible transformation, not for confidentiality.
- **Password Hashes**: One-way functions. Common examples: **SHA-1** (broken), **MD5** (broken).
- **MAC (Message Authentication Code)**: Authenticates a message. **HMAC (Hash-based MAC)** uses a secret key and hash function.
- **Threat Modelling and Attack Vectors**: Identify potential threats (malware, breaches, DoS), assess likelihood and exposure to prioritize risk reduction.

### Website Analysis

- Reviewing a website to understand the company and key assets for identifying sensitive information.
- **Identify**:
    - **Content**: Configuration disclosure, HTML structure (titles, forms, images).
    - **HTML Source Code**: Reveals hostnames, emails, usernames, passwords (viewable via "View Page Source"). Can contain credentials, hashes, sensitive data in comments, hidden links/directories, user information, web/database server details.
    - **Hidden Content**: Source files, hidden directories (e.g., `robots.txt`).

### Web Application Architectures

- **Web Server**: Processes requests from web clients to serve content.
- **HTTP (TCP/80)**: Lightweight, stateless protocol. Uses headers and an optional message body.
- **HTTPS (TCP/443)**: HTTP over SSL/TLS for confidentiality and secure data transfer.
- **Web Services**:
    - **SOAP (Simple Object Access Protocol)**: XML-based, platform/language-independent, supports stateful/stateless.
    - **REST (Representational State Transfer)**: Language/platform-independent, faster than SOAP, treats data as resources, uses JSON/XML.
- **HTTP Methods**: GET, POST, HEAD, PUT, DELETE, TRACE, OPTIONS.
- **HTTP Status Codes**: Server responses to requests (e.g., 200 OK, 404 Not Found).
- **Web Application Security Headers**: `X-Content-Type-Options`, `Content-Security-Policy (CSP)`, `X-Content-Security-Policy`, `Content-Security-Policy-Report-Only`.
- **Web Markup Languages**: **HTML** (structure).
- **Server-Side Technologies**:
    - **PHP**: Common vulnerabilities listed.
    - **JSP (JavaServer Pages)**: Dynamic pages for Java web apps, common vulnerabilities listed.
    - **ASP.NET**: Interactive UIs using C#, common vulnerabilities listed.
    - **CGI (Common Gateway Interface)**: Standards for info exchange between web server and scripts (Perl), vulnerabilities listed (Shellshock).
    - **JavaScript (JS)**: Client/server-side for interactivity, common vulnerabilities include XSS.
    - **Adobe ColdFusion**: Verbose errors disclosing info, default management interfaces (/CFIDE/), common vulnerabilities.

### Web Architecture Sub-Components

- **File Analysis**: Seeking sensitive info in local files, registry, memory (usernames/passwords, connection strings, API keys).
- **DLL Hijacking**: Exploits Windows search/load algorithm to inject malicious code.
- **Binary Analysis**: Reviewing source code for sensitive info (hardcoded credentials, API keys/endpoints, comments, hidden functions). .NET applications can be decompiled.

### Information Disclosure

- Common sources include **error messages**.
- **Common Disclosed Information Through Errors**: OS version, usernames/passwords, file paths/configuration files.
- **Enumerating Error-Based Disclosure**: Access non-existent URLs and assess the error response.

### Authentication and Authorisation Mechanisms

- **Authentication**: Confirms user identity (e.g., passwords, OTP).
- **Enumerating Authorization Mechanisms**: Look for **unprotected parameters** in URLs or requests that may allow unauthorized access by manipulation (e.g., `isAdmin`, `User`, `User_id`).

### SQL Injection

- Attackers modify SQL statements in web applications to manipulate databases. Common on login pages and application parameters.
- **Prevention**: Prepared Statements, Stored Procedures, Allow-list Input Validation.
- **Enumerating SQLi**: Trial and error to construct effective SQL statements. Look for arithmetic operations, alphabetic values, semicolon, comments, double quotes, union operations in parameters.
- **Enumerating SQLi Authentication Bypass**: Common to target user credential references.

### LDAP Injection

- Attackers modify LDAP statements to manipulate or access directory services. LDAP stores info about users, hosts, network resources. Server-side attack.
- **LDAP Distinguished Names (DNs)**: Unique identifiers for entities (cn, ou, dc - examples provided).

### Cross-Site Scripting (XSS)

- Client-side attack executed within the end user's browser. Target common input fields like search bars.
- **Common Payloads**: `<script>alert('1')</script>` (PoC), `<script>alert(document.cookie)</script>` (cookie theft).
- **Types**:
    - **Reflected XSS**: Payload in the request is reflected in the immediate response.
    - **Stored XSS**: Payload is stored server-side (e.g., forums) and executed later.
    - **DOM-based XSS**: Vulnerability in client-side JavaScript code manipulates the DOM.
- **Advanced XSS**: Can be used to steal sessions by exfiltrating cookies.

### Parameter Manipulation

- Modifying web application parameters to change behavior/outcome (e.g., price/quantity in e-commerce, privilege levels).
- **GET Method**: Data in the URL. Example URL provided.
- **POST Method**: Data in the request body (below headers).

### Databases

- Collection of organized data in a computer system (tables and records).
- **MSSQL 2012 Hash Formatting**: Fixed value, Salt, SHA-1 Hash Value (format described). Need formatting before cracking.
- **Enumerating Oracle RDBMS**:
    - **TNS Listener (TCP/1521, 1830)**: Acts as a proxy, `tnscmd10g -h`, Metasploit `auxiliary/scanner/oracle/tnslnr_version`. `SECURITY = OFF` indicates no authentication.
    - **SID Brute-Forcing**: Site-Identifier, Metasploit `auxiliary/scanner/oracle/sid_brute`.
    - **SID from SNMP**: Query OID `1.3.6.1.2.1.25.4.2.1.2`.
    - **User Enumeration**: Metasploit `auxiliary/admin/oracle/oraenum`, brute-force `auxiliary/scanner/oracle/oracle_login`.
    - **Version Enumeration**: Metasploit `auxiliary/scanner/oracle/tnslsnr_version`, `tnscmd.pl status -h`.
    - **Default User Credentials**: Many default credentials are not removed (examples provided).

### Session Management

- Sessions map a user to their activity after authentication using a session cookie.
- **Source Code Review for Session Security**: Ensure proper timeouts and secure cookie handling.