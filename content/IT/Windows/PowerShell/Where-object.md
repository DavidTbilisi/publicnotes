---
tags:
  - it/cli
  - it/powershell
created: 2025-09-14
modified: 2025-09-14T11:10:00
---
Think of **`Where-Object`** in PowerShell as the **gatekeeper of the pipeline**. Every object flows through, and only the ones that match your condition are let past.

---
## Pre
[[Select-Object]]
[[Format-List]]
### The Basics

Syntax:

```powershell
command | Where-Object { <condition> }
```

* The **`command`** (e.g., `Get-Process`) produces objects.
* `Where-Object` takes those objects one by one and applies your condition inside `{ }`.
* If the condition is true → the object passes through.
* If false → it gets dropped.

---

### The Magic Variable: `$_`

Inside `Where-Object`, PowerShell hands you each object in the pipeline as `$_`.
Think: “current object.”

Example:

```powershell
Get-Process | Where-Object { $_.CPU -gt 100 }
```

* `Get-Process` outputs a list of process objects.
* `$_` is one process at a time.
* `.CPU` is its CPU usage property.
* Only processes with CPU > 100 are kept.

---

### Classic Use-Cases

1. **Filter files by size**

```powershell
Get-ChildItem -Recurse | Where-Object { $_.Length -gt 1MB }
```

2. **Filter by file extension**

```powershell
Get-ChildItem | Where-Object { $_.Extension -eq ".log" }
```

3. **Find processes by name**

```powershell
Get-Process | Where-Object { $_.ProcessName -like "chrome*" }
```

---

### Operators You’ll Use

* `-eq` → equal
* `-ne` → not equal
* `-gt` → greater than
* `-lt` → less than
* `-like` → wildcard match (`*stuff*`)
* `-match` → regex

Example:

```powershell
Get-ChildItem | Where-Object { $_.Name -match "^data\d+\.csv$" }
```

---

### Shorthand (PowerShell 3+)

You don’t always need `{ $_.Property -eq something }`. You can write:

```powershell
Get-Process | Where-Object CPU -gt 100
```

It’s cleaner but does the same thing.

---

### Why It’s Powerful

In Bash, you’d grep or awk raw text. In PowerShell, `Where-Object` filters **objects**. That means you don’t parse strings — you grab exact properties.

It’s like shopping with a barcode scanner instead of squinting at shelf labels.

---

Do you want me to build you a **cheat sheet of `Where-Object` recipes** (files, processes, registry, services, etc.) so you can drop it in Obsidian and use it like a pattern book?
