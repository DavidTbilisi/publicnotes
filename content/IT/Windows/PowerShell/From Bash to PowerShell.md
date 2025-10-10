---
title: Bash → PowerShell Swap Sheet
tags: [it/linux/bash, it/powershell, cheatsheet, it/cli]
---

<h1>Bash → PowerShell Daily Swap Cheat-Sheet</h1>

<p>This is your translator between old Bash muscle memory and new PowerShell habits.</p>
<table>
  <thead>
    <tr>
      <th>Purpose</th>
      <th>Bash / Linux Command</th>
      <th>PowerShell Equivalent</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><b>List files</b></td><td><code>ls</code></td><td><code>Get-ChildItem</code> (alias: <code>ls</code>, <code>gci</code>)</td></tr>
    <tr><td><b>List recursively</b></td><td><code>ls -R</code></td><td><code>Get-ChildItem -Recurse</code></td></tr>
    <tr><td><b>Show hidden files</b></td><td><code>ls -a</code></td><td><code>Get-ChildItem -Force</code></td></tr>
    <tr><td><b>Print file contents</b></td><td><code>cat file.txt</code></td><td><code>Get-Content file.txt</code></td></tr>
    <tr><td><b>Write to file</b></td><td><code>echo "hi" &gt; file.txt</code></td><td><code>"hi" | Out-File file.txt</code></td></tr>
    <tr><td><b>Append to file</b></td><td><code>echo "hi" &gt;&gt; file.txt</code></td><td><code>"hi" | Add-Content file.txt</code></td></tr>
    <tr><td><b>Find files</b></td><td><code>find . -name "*.txt"</code></td><td><code>Get-ChildItem -Recurse -Filter *.txt</code></td></tr>
    <tr><td><b>Search inside files</b></td><td><code>grep "error" *.log</code></td><td><code>Select-String "error" *.log</code></td></tr>
    <tr><td><b>Count lines/words</b></td><td><code>wc -l file.txt</code></td><td><code>(Get-Content file.txt).Count</code></td></tr>
    <tr><td><b>Current directory</b></td><td><code>pwd</code></td><td><code>Get-Location</code></td></tr>
    <tr><td><b>Change directory</b></td><td><code>cd /path</code></td><td><code>Set-Location /path</code> (alias: <code>cd</code>)</td></tr>
    <tr><td><b>Copy file</b></td><td><code>cp file1 file2</code></td><td><code>Copy-Item file1 file2</code></td></tr>
    <tr><td><b>Move/Rename file</b></td><td><code>mv file1 file2</code></td><td><code>Move-Item file1 file2</code></td></tr>
    <tr><td><b>Delete file</b></td><td><code>rm file.txt</code></td><td><code>Remove-Item file.txt</code></td></tr>
    <tr><td><b>Process list</b></td><td><code>ps aux</code></td><td><code>Get-Process</code></td></tr>
    <tr><td><b>Kill process</b></td><td><code>kill 1234</code></td><td><code>Stop-Process -Id 1234</code></td></tr>
    <tr><td><b>Disk usage</b></td><td><code>du -sh</code></td><td><code>Get-ChildItem | Measure-Object -Property Length -Sum</code></td></tr>
    <tr><td><b>Free space</b></td><td><code>df -h</code></td><td><code>Get-PSDrive</code></td></tr>
    <tr><td><b>Environment vars</b></td><td><code>echo $PATH</code></td><td><code>$env:PATH</code></td></tr>
    <tr><td><b>Set env var</b></td><td><code>export VAR=foo</code></td><td><code>$env:VAR = "foo"</code></td></tr>

    <!-- Advanced Section -->
    <tr><td><b>Text processing (awk)</b></td><td><code>awk '{print $2}' file.txt</code></td><td><code>Get-Content file.txt | ForEach-Object { ($_ -split '\s+')[1] }</code></td></tr>
    <tr><td><b>Stream editing (sed)</b></td><td><code>sed 's/foo/bar/g' file.txt</code></td><td><code>(Get-Content file.txt) -replace 'foo','bar' | Set-Content file.txt</code></td></tr>
    <tr><td><b>HTTP requests (curl)</b></td><td><code>curl https://api.example.com</code></td><td><code>Invoke-RestMethod "https://api.example.com"</code></td></tr>
    <tr><td><b>Download file (wget)</b></td><td><code>wget https://file</code></td><td><code>Invoke-WebRequest "https://file" -OutFile file</code></td></tr>
    <tr><td><b>Cron job</b></td><td><code>crontab -e</code></td><td><code>Register-ScheduledTask</code> (Windows Task Scheduler)</td></tr>
  </tbody>
</table>
