# Backup Script Guide

## 1. Writing the Backup Script

A Bash script can simplify the process of backing up files by combining multiple commands into a single executable file. For this activity, I created a script that compresses the `app-data` folder into a `.tar.gz` archive. Each backup uses a timestamp in its filename to distinguish it from previous backups.

### Script Code

```bash
#!/bin/bash

# Define the source and backup locations
SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Starting file backup..."

# Create the backup directory if it does not exist
mkdir -p "$BACKUP_DIR"

# Archive and compress the source directory
tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully!"
```

The script identifies the folder to back up, creates the destination directory when necessary, and generates a compressed archive with the current date and time in its filename.

## 2. Setting Script Permissions

Before executing the script, I used `chmod` to grant it permission to run.

```bash
chmod +x backup.sh
```

After setting the permission, I executed the script with:

```bash
./backup.sh
```

This runs the backup process and creates an archive inside the `backups` directory.

## 3. Automating Backups with Cron

Cron is a Linux utility that executes scheduled tasks automatically. I can use it to run the backup script every day at 2:00 AM.

```cron
0 2 * * * /root/backup.sh
```

The path `/root/backup.sh` is only an example. It must be replaced with the actual absolute path of the script.

### Understanding the Cron Schedule

| Field | Value | Meaning |
|---|---|---|
| Minute | `0` | At the start of the hour |
| Hour | `2` | At 2:00 AM |
| Day of Month | `*` | Every day |
| Month | `*` | Every month |
| Day of Week | `*` | Every day of the week |

To edit the scheduled tasks, use:

```bash
env EDITOR=nano crontab -e
```

To display the current schedule, use:

```bash
crontab -l
```

## 4. Checking the Backup Files

After running the script, I checked the `backups` directory to confirm that the archive was generated.

```bash
ls -lh backups/
```

To inspect the files stored inside an archive without extracting them, I can use:

```bash
tar -tzf backups/backup_FILENAME.tar.gz
```

Replace `backup_FILENAME.tar.gz` with the actual archive filename. This command lists the archived contents so I can check whether the expected files were included.

## Conclusion

Creating a Bash backup script helped me learn how to automate file compression and organize backup versions using timestamps. I also learned how to make scripts executable and configure Cron for recurring tasks. These techniques can help simplify routine maintenance and make file backup procedures more consistent in a Linux environment.

