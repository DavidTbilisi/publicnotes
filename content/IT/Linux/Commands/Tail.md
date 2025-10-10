---
tags:
  - it/linux/bash
---
;
Reads the last 200 MB of the file and creates new temp.log
```bash
tail -c 200M log_file.log > temp.log
```

Safer alternative
```bash
split -n 2 file.txt
mv xab file.txt  # Keeps the second half
rm xaa           # Removes the first half
```

```bash
split -n 8 -d --additional-suffix=.log error.log error
```