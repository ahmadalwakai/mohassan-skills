---
name: سكربتات Bash و PowerShell
description: أتمتة الطرفية بالسكربتات: سكربت Bash، سكربت PowerShell، أوامر الطرفية، إعادة تسمية الملفات، المهام المجدولة، cron، Task Scheduler، الحلقات. bash shell zsh powershell ps1 terminal command commands cli cron crontab scheduled automation rename loop cmd linux الطرفية سطر الأوامر أوامر أتمتة اتمتة باور شل
version: 1.0.0
category: coding
---
Use this for Bash or PowerShell scripts and command-line automation.
1. State the shell and operating system; commands differ between Bash (Linux, macOS, Git Bash) and PowerShell (Windows).
2. Bash header: `#!/usr/bin/env bash` and `set -euo pipefail`; quote every variable ("$file"); pass arguments with "$@"; prefer `$(...)` to backticks; check required tools with `command -v`.
3. PowerShell: full cmdlet names in scripts (Get-ChildItem, Rename-Item), `-ErrorAction Stop` with try/catch, `Join-Path` for paths, `-WhatIf` to preview destructive commands.
4. Anything that renames, moves or deletes: run a dry run first (print the planned action or use -WhatIf), handle names with spaces and Arabic characters, refuse to overwrite existing files, and log each change.
5. File loops: Bash `find . -type f -print0 | while IFS= read -r -d '' f; do ...; done`; PowerShell `Get-ChildItem -File | ForEach-Object { ... }`.
6. Scheduling: cron on Linux (`crontab -e`, five time fields, absolute paths, output redirected to a log file); Task Scheduler on Windows (Register-ScheduledTask or the GUI) with the working directory set.
7. Exit codes: 0 is success; check them, and exit non-zero on failure so schedulers notice.
8. Never run a script fetched from the internet without reading it first.
Answer shape: the complete script with comments on risky lines, how to run it, and how to test it safely.
