---
tags:
  - it/cli
  - enabler
  - progress
---
Global Regular Expression Print

|Tool|Use Case|
|---|---|
|`egrep`|Same as `grep -E` for extended regex|
|`fgrep`|Same as `grep -F` for fixed strings|
|`ripgrep (rg)`|Super-fast grep replacement|
|`ack`, `ag`|Developer-friendly `grep` alternatives|


```bash
grep [options] 'pattern' [file...]
# find what where
```

```bash
grep "error" logfile.txt
```

```bash
grep -r "TODO" ./src # recursive
```

```bash
grep -i "warning" logfile.txt # Ignore case
```

```bash
grep -n "main" main.c # Show line numbers
```

```bash
grep -c "fail" logfile.txt # count matches
```

```bash
grep --color=auto "pattern" file.txt # colorful life
```

```bash
grep --color=auto "pattern" file.txt --include="*.php"# only that file extention 
```