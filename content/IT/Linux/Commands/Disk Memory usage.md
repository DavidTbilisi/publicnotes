---
tags:
  - it/linux/bash
---

Overview
```bash
df -h
```

Top 20
```bash
sudo du -ahx / | sort -rh | head -20
```

## du 
Summarize disk usage of each FILE, recursively for directories.



## Phone
Find files larger than 100MB
```shell
find /storage/emulated/0 -type f -size +100M 2>/dev/null -exec ls -lh {} \;
```
