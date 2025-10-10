---
tags:
  - it/cli
published: 2025-08-07
---
# Sync Drive Mobile & Notebook via Drive Google

`rclone config`


download
`rclone sync -P "gd:obsidian/David" ${local folder path}`


upload
`rclone sync -P ${local folder path} "gd:obsidian/David" `