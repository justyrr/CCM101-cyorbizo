# Automation Research

## Bash Script

A Bash script is a plain text file containing a series of Linux commands that the shell executes in order, allowing you to automate repetitive tasks instead of typing them one by one. The `#!/bin/bash` line at the top is called the **shebang** — it tells the operating system which interpreter to use (in this case, the Bash shell) so the file runs correctly when executed.

## Variables

Variables (like `$BACKUP_DIR`) let programmers store a value once and reuse it throughout the script by name, instead of typing the exact folder path every single time. This makes scripts easier to read, update, and maintain — if the path changes, you only edit it in one place instead of hunting down every occurrence.

## Cron Job

A cron job in Linux is a scheduled task that runs automatically at a specified time or interval, defined in a file called the crontab. It is essential for cloud operations because it eliminates the human element from routine tasks like backups, log rotation, and cleanup — ensuring critical processes run reliably at scale without anyone pressing a button.
