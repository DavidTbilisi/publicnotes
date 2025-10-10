---
tags:
  - it/ProgrammingLanguages
  - it/powershell
---
https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/schtasks


```powershell
# Run the task every minute
schtasks /create /sc minute /mo 1 /f /tn "Schtasks Test" /tr dir /ru System
```

```powershell
# Run the task once at HH:MM
schtasks /create /sc once /st 14:29 /f /tn "Schtasks Test" /tr dir /ru System
```

```powershell
# Query task by name
schtasks /query /v /tn "Schtasks Test" /fo list
```


```powershell
# Delete task by name
schtasks /delete /f /tn "Schtasks Test"
```


Specifies the schedule type
```powershell
schtasks /<action> [options]
```




## 🛠 `/Create` – Create a Scheduled Task
	
|Option|Description|Example|
|---|---|---|
|`/SC`|**Schedule type** (`DAILY`, `WEEKLY`, `MINUTE`, etc)|`/SC DAILY`|
|`/MO`|**Modifier** (e.g., every 5 minutes)|`/SC MINUTE /MO 5`|
|`/TN`|**Task name**|`/TN "MonicaBackup"`|
|`/TR`|**Task run command**|`/TR "C:\Scripts\backup.ps1"`|
|`/ST`|**Start time (HH:MM)**|`/ST 03:00`|
|`/SD`|**Start date (MM/DD/YYYY)**|`/SD 07/06/2025`|
|`/RU`|**Run as user (or SYSTEM)**|`/RU SYSTEM` or `/RU "David"`|
|`/RP`|**Password** (required if not SYSTEM)|`/RP yourpassword`|
|`/RL`|**Run level: LIMITED or HIGHEST (admin)**|`/RL HIGHEST`|
|`/D`|**Days (for WEEKLY)**|`/D MON,WED,FRI`|

## 📄 `/Query` – View Scheduled Tasks

| Option | Description                               | Example              |
| ------ | ----------------------------------------- | -------------------- |
| `/FO`  | Format output (`TABLE`, `LIST`, `CSV`)    | `/FO LIST`           |
| `/V`   | Verbose output (shows triggers and paths) | `/V`                 |
| `/TN`  | Filter by task name                       | `/TN "MonicaBackup"` |


## ❌ `/Delete` – Delete a Task

| Option | Description             | Example              |
| ------ | ----------------------- | -------------------- |
| `/TN`  | Task name to delete     | `/TN "MonicaBackup"` |
| `/F`   | Force (no confirmation) | `/F`                 |


## 🔄 `/Change` – Modify an Existing Task

| Option     | Description               | Example              |
| ---------- | ------------------------- | -------------------- |
| `/TN`      | Task name                 | `/TN "MonicaBackup"` |
| `/ENABLE`  | Re-enable a disabled task | `/ENABLE`            |
| `/DISABLE` | Disable the task          | `/DISABLE`           |