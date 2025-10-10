
# Manual Privilege Escalation (Privesc) TODO List

---
## Top directories to check 

| Directory         | Why Check It?                                | What to Look For                       |
| ----------------- | -------------------------------------------- | -------------------------------------- |
| `/var/log`        | System & application logs                    | Auth logs, syslog, daemon logs, errors |
| `/etc`            | Config files, sometimes with creds           | Password files, service configs        |
| `/home`           | User data and personal configs               | Hidden files (`.ssh`, `.bash_history`) |
| `/root`           | Root’s home directory (if accessible)        | Root creds, scripts                    |
| `/tmp`            | Temporary files, sometimes leftover scripts  | Scripts, injected files                |
| `/opt`            | Optional software, sometimes manual installs | Custom software logs/configs           |
| `/usr/local/bin`  | Locally installed executables                | Custom binaries or scripts             |
| `/var/spool/cron` | User cron jobs                               | Scheduled task scripts                 |
| `/var/www`        | Web server root, often writable by www-data  | Web shells, upload logs                |
| `/dev/shm`        | Shared memory filesystem                     | Sometimes used for temporary payloads  |

## 1. **Enumerate System Information**

- OS version, kernel version
    
    ```bash
    uname -a
    cat /etc/os-release
    systeminfo (Windows)
    ```
    
- Installed patches & updates status
    
- Architecture (x86, x64)
    
- User and group info
    
    ```bash
    id
    whoami
    net user (Windows)
    ```
    

---

## 2. **Check User Privileges**

- Are you running as a normal user or admin/root?
- List current user groups
- Check sudo privileges without password
    ```bash
    sudo -l
    ```
---

## 3. **Search for Sensitive Files & Configs**
- Look for readable `/etc/shadow`, `/etc/passwd`, or credential files
- Check home directories for private keys, config files with creds
- Windows: Search for `.rdp`, `.ini`, `.xml` files containing passwords

---
## 4. **Check for SUID/SGID Executables (Linux)**

- Find binaries with elevated permissions
    ```bash
    find / -perm -4000 -type f 2>/dev/null
    find / -perm -2000 -type f 2>/dev/null
    ```
- Identify any vulnerable versions or misconfigured SUID binaries

---

## 5. **Check for Writable Files and Directories**
- Look for writable files owned by root/admin or binaries in PATH
    ```bash
    find / -writable -type f 2>/dev/null
    ```
- Writable scripts, config files used by services
- Windows: Search for writable folders in Program Files or service directories

---

## 6. **Look for Passwords or Tokens**

- Environment variables
    ```bash
    env
    ```
- Check bash history, PowerShell history
- Windows Credentials Manager or saved passwords
- Look for API keys or tokens in configs or logs

---

## 7. **Analyze Scheduled Tasks / Cron Jobs**

- Linux:
    ```bash
    crontab -l
    cat /etc/crontab
    ls -la /etc/cron.*
    ```
- Windows:
    ```powershell
    schtasks /query /fo LIST /v
    ```
- Look for scripts or programs running with elevated privileges you can hijack

---

## 8. **Check Network and Services**
- List open ports and services
    ```bash
    ss -tuln
    netstat -ano (Windows)
    ```
- Look for vulnerable services or misconfigurations
- Check service executable paths for writable locations

---
## 9. **Kernel Exploits / Vulnerabilities**
- Check kernel version vs known exploit databases (e.g., [exploit-db](https://www.exploit-db.com/))
- Look for unpatched kernel vulnerabilities

---

## 10. **Check Installed Software Versions**
- Identify outdated software with known exploits
- Focus on web servers, database servers, interpreters (Python, Ruby, Node)

---

## 11. **Manual Exploitation Techniques**
- Exploit writable SUID binaries or scripts
- Exploit weak sudo rules (`sudo -l` output)
- Hijack PATH environment or binaries
- Abuse file write permissions to escalate
- Use cron or scheduled task hijacking
- Abuse misconfigured services or daemons
- Dump password hashes from SAM (Windows) or /etc/shadow (Linux)

---

## 12. **Post-Privesc: Verify and Clean Up**

- Confirm you have root/admin privileges
- Cover tracks: clear logs if needed (only ethical when in pentest scope)
- Secure any backdoor access (for your own testing lab)

---

# Quick Commands Cheat Sheet (Linux)

```bash
# Check SUID files
find / -perm -4000 -type f 2>/dev/null

# Check sudo privileges
sudo -l

# Find writable files owned by root
find / -user root -writable -type f 2>/dev/null

# List cron jobs
crontab -l
cat /etc/crontab

# Check network ports
ss -tuln

# Check OS/kernel info
uname -a
cat /etc/os-release
```

---

# Quick Commands Cheat Sheet (Windows PowerShell)

```powershell
# User info
whoami
net user

# List scheduled tasks
schtasks /query /fo LIST /v

# List services
Get-Service

# List open ports
netstat -ano

# Check environment variables
gci env:
```

---

# Final Thought

Manual privesc is all about **smart enumeration + looking for weaknesses in file permissions, scheduled jobs, sudo rights, and service configs**. Automating is fine but knowing this checklist gives you a **killer edge** when tools fail or are blocked.


#privesc #it/cybersecurity #it/hacking/pentesting #it/linux #windows #checklist



Here’s a short, punchy hacker story to lock in your privesc steps — no fluff, all grit:

---

# Short Story: **“Root in Reach”**

David sat at his terminal, eyes sharp. First, he scanned the **System** — kernel, users, versions. Next, he checked his **User** powers — sudo? groups? Nothing locked down.

His gaze caught the glow of strange **SUID** files lurking in hidden folders. Then, writable files whispered secrets he could change. Passwords and tokens? Scattered like breadcrumbs.

The **Cron** jobs ticked away, running tasks with admin rights. He hijacked one, gaining more control. Networks and services lay open, waiting. Kernel flaws cracked the final wall.

Old software gave him the key. Exploit done, he wiped his tracks. Root was his.

---
