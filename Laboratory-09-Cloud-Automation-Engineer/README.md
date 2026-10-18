# Laboratory 09: The Cloud Automation Engineer

## Mission Overview

In this laboratory, I explored how to automate file backup tasks in a Linux environment using Bash scripting and Cron. I created a directory containing sample data, wrote a script to generate backup files, and tested the backup process. I also explored how Cron can be used to schedule tasks automatically.

## Objectives

- Learn the basics of Bash scripting.
- Create and manage files and directories in Linux.
- Set executable permissions for scripts.
- Create compressed backup archives using `tar`.
- Understand how Cron schedules automated tasks.
- Document the commands and results of the activity.

## Commands Executed

| Command | Description |
|---|---|
| `mkdir app-data` | Creates a directory for storing sample files. |
| `echo "This is critical client data." > app-data/data.txt` | Writes sample information into a text file. |
| `cat app-data/data.txt` | Displays the saved data. |
| `nano backup.sh` | Opens the text editor to create or modify the backup script. |
| `chmod +x backup.sh` | Gives the script permission to execute. |
| `./backup.sh` | Starts the backup script. |
| `ls -l backups/` | Lists the generated backup files. |
| `crontab -l` | Shows the user's existing scheduled Cron jobs. |
| `env EDITOR=nano crontab -e` | Opens the Cron schedule for editing in Nano. |

## Skills Learned

- Creating and executing Bash scripts.
- Managing files and directories using Linux commands.
- Generating compressed `.tar.gz` backup archives.
- Setting file permissions with `chmod`.
- Checking backup outputs and verifying generated files.
- Exploring task scheduling with Cron.
- Writing organized documentation using Markdown.

## Reflection

This laboratory helped me understand how automation can reduce repetitive work in system administration. By creating a Bash backup script, I learned how several commands can be combined into one process to make file backups easier to perform.

I also learned the purpose of Cron in scheduling tasks to run at specified times. This can be useful for regular backups and other maintenance activities without requiring someone to execute the commands manually every time.

Overall, the activity improved my understanding of Linux scripting and basic automation. These skills can be useful when managing servers, protecting important files, and performing routine tasks in a cloud environment.

