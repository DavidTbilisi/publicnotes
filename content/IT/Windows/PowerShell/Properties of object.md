---
tags:
  - it/cli
  - it/powershell
created: 2025-09-14
modified: 2025-09-14T11:20:00
---
### Step 1. Inspect Objects with `Get-Member`

Example with processes:

```powershell
Get-Process | Get-Member
```

This shows you the properties and methods of process objects (`CPU`, `Id`, `ProcessName`, `StartTime`, etc.).

Now you know what `$_` carries inside the `Where-Object` filter.

---

### Step 2. Look at One Object

If you want to see just one object’s details:

```powershell
Get-Process | Select-Object -First 1 | Format-List *
```

* `Select-Object -First 1` → take only one result
* `Format-List *` → show all properties in a readable way

Do the same for files:

```powershell
Get-ChildItem | Select-Object -First 1 | Format-List *
```

You’ll see properties like `Name`, `Extension`, `Length`, `LastWriteTime`.

---

### Step 3. Use in `Where-Object`

Once you know the property names, you can filter.
Example:

```powershell
Get-ChildItem -Recurse | Where-Object { $_.Length -gt 1MB }
```

---

### Why This Matters

Unlike Bash (where you grep blind through text), PowerShell lets you *inspect the structure first* and then filter precisely. It’s like looking at a map’s legend before you start plotting a route.

---

Want me to prepare a **ready-to-use Obsidian “Where-Object Recipes” sheet** that lists common commands (files, processes, registry, services) with their useful properties and example filters? That way you won’t need to rediscover them each time.
