---
tags:
  - it/cli
  - windows
  - it/powershell
  - search
created: 2025-09-14
modified: 2025-09-14T10:30:00
---
## Pre
[[Where-object]]

# PowerShell Alternative to Linux `find`

## Why It’s Unique
PowerShell doesn’t have a single `find` command, but its **object-oriented pipeline** gives you the same power:
- `Get-ChildItem` (alias `gci` or `ls`) handles recursive traversal.
- `Where-Object` allows fine-grained filtering (by name, size, date, etc.).
- `Select-String` works like `grep` for content searches.
- `ForEach-Object` executes actions on results.

This combination makes it just as powerful as `find`—but with structured objects instead of raw text.

---

## Basic Syntax
```powershell
Get-ChildItem [path] -Recurse [options] | Where-Object { condition }
````

* **path** → where to start searching.
* **-Recurse** → search subdirectories.
* **Where-Object** → filter conditions.

---

```powershell
Get-Alias

#CommandType     Name    Version    Source
#-----------     ----    -------    ------
#Alias           ls -> Get-ChildItem
#Alias           cat -> Get-Content
#Alias           cp -> Copy-Item
```



## Examples

### 1. Find by filename

```powershell
Get-ChildItem -Recurse -Filter *.txt
```

### 2. Case-insensitive match

```powershell
Get-ChildItem -Recurse | Where-Object { $_.Name -match "\.jpg$" }
```

### 3. Find by size

```powershell
Get-ChildItem -Recurse | Where-Object { $_.Length -gt 100MB }
```

### 4. Find by type

```powershell
Get-ChildItem C:\Logs -Recurse -File -Filter *.log
```

### 5. Find by modification time

```powershell
Get-ChildItem -Recurse | Where-Object { $_.LastWriteTime -gt (Get-Date).AddDays(-7) }
```

### 6. Execute command on matches

```powershell
Get-ChildItem -Recurse -Filter *.tmp | ForEach-Object { Remove-Item $_.FullName }
```

### 7. Search for content inside files

```powershell
Get-ChildItem -Recurse -Filter *.conf | Select-String "Listen"
```

---

## Why People Love the PowerShell Way

* Integrates **search + action** in one pipeline.
* Works with structured objects, not plain text → more precise.
* Perfect for **Windows admins, automation, and scripts**.

Think of it as **find + grep + batch + JSON**—all rolled into one.



---

# Linux `find` vs PowerShell Alternative

This table maps common `find` usages in Linux to their PowerShell equivalents.

| Purpose | Linux `find` | PowerShell Equivalent |
|---------|--------------|------------------------|
| **List all files recursively** | `find .` | `Get-ChildItem -Recurse` |
| **Find by name** | `find . -name "*.txt"` | `Get-ChildItem -Recurse -Filter *.txt` |
| **Case-insensitive name match** | `find . -iname "*.jpg"` | `Get-ChildItem -Recurse &#124; Where-Object { $_.Name -match "\.jpg$" }` |
| **Find by size** | `find . -size +100M` | `Get-ChildItem -Recurse &#124; Where-Object { $_.Length -gt 100MB }` |
| **Find by file type** | `find /var/log -type f -name "*.log"` | `Get-ChildItem C:\Logs -Recurse -File -Filter *.log` |
| **Find by modification time** | `find . -mtime -7` | `Get-ChildItem -Recurse &#124; Where-Object { $_.LastWriteTime -gt (Get-Date).AddDays(-7) }` |
| **Delete matching files** | `find . -name "*.tmp" -delete` | `Get-ChildItem -Recurse -Filter *.tmp &#124; Remove-Item` |
| **Run a command on matches** | `find . -name "*.sh" -exec chmod +x {} \;` | `Get-ChildItem -Recurse -Filter *.sh &#124; ForEach-Object { $_ &#124; Set-ItemProperty -Name IsReadOnly -Value $false }` *(example)* |
| **Search for text inside files** | `find . -type f -name "*.conf" -exec grep "Listen" {} \;` | `Get-ChildItem -Recurse -Filter *.conf &#124; Select-String "Listen"` |

---

> [!note]
> - **Linux `find`** outputs *plain text paths* → needs `grep` or `xargs` for extra work.  
> - **PowerShell** outputs *objects* → filter directly by properties (`Length`, `LastWriteTime`, `Extension`).  
> - Both become unstoppable when combined with their ecosystems (`find + grep` vs PowerShell pipelines).  

Think of Linux `find` as **surgical precision with scalpels**, while PowerShell is **Lego blocks with magnets** - snap them together for workflows.

---

## Notes

- Linux `find` outputs **plain text paths** → needs `grep` or `xargs` for extra work.  
- PowerShell outputs **objects**, so you can filter by properties (`Length`, `LastWriteTime`, `Extension`, etc.) directly.  
- Both are insanely powerful when combined with other tools in their ecosystem (`find + grep`, or PowerShell pipelines).  

Think of Linux `find` as **surgical precision with scalpels**, while PowerShell is **Lego blocks with magnets** - snap things together for complex workflows.

---

## Notes

- Linux `find` outputs plain text paths → needs `grep` or `xargs` for extra work.  
- PowerShell outputs **objects**, so you can filter by properties (`Length`, `LastWriteTime`, `Extension`, etc.) directly.  
- Both are insanely powerful when combined with other tools in their ecosystem (`find + grep`, or PowerShell pipelines).  

---

Think of Linux `find` as **surgical precision with scalpels**, while PowerShell is **Lego blocks with magnets**—snap things together for complex workflows.
