---
tags:
  - it/cli
  - it/linux
  - search
  - progress
  - enabler
created: 2025-09-14
modified: 2025-09-14T10:27:00
---
# Linux `find` Command

## Why `find` is Unique
The `find` command is one of the most powerful and versatile tools in Linux. Unlike simple `ls` or `grep`, `find`:
- Traverses directories recursively.
- Matches files by **name, type, size, permissions, ownership, time, or content**.
- Can **execute commands** on the results (`-exec`, `-delete`, etc.).
- Works efficiently even in huge filesystems.

It’s like having a search engine for your filesystem that also acts as a Swiss Army knife for file operations.

---

## Basic Syntax
```bash
find [path] [options] [expression]
````

* **path** → where to start searching (e.g., `.` for current dir, `/` for root).
* **options** → how to search (case sensitivity, depth, etc.).
* **expression** → what to look for (name, size, etc.).

---

## Examples

### 1. Find by filename

```bash
find . -name "*.txt"
```

Finds all `.txt` files in the current directory and subdirectories.

### 2. Case-insensitive match

```bash
find . -iname "*.jpg"
```

### 3. Find by size

```bash
find . -size +100M
```

Finds files larger than 100 MB.

### 4. Find by type

```bash
find /var/log -type f -name "*.log"
```

### 5. Find by modification time

```bash
find . -mtime -7
```

Files modified in the last 7 days.

### 6. Execute command on matches

```bash
find . -name "*.tmp" -exec rm {} \;
```

Deletes all `.tmp` files.

### 7. Search for content inside files (with `grep`)

```bash
find . -type f -name "*.conf" -exec grep "Listen" {} \;
```

---

## Why People Love `find`

* Replaces manual file-hunting in nested directories.
* Saves time by combining **search + action**.
* Essential for **system administration, forensics, and automation**.

Think of it as **Google + batch processing** for your Linux filesystem.



