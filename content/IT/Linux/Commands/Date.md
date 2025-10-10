---
tags:
  - it/linux/bash
---

Set custom time to deduce the day of the week. Is this day Sabbath for example or not? 
```bash
date -j -f "%d %b %Y" "12 Apr 2025" "+%A"
```

```powershell
Get-Date -Date "12 Apr 2025" -Format "dddd"
```

