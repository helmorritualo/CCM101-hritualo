# Backup Script Guide

## 1. Overview

The backup script automates the process of creating a compressed backup of the application's data directory. It creates a backup directory if one does not already exist and generates a timestamped `.tar.gz` archive containing the source files.

## 2. Full Bash Script

The following is the complete `backup.sh` script used in this laboratory activity.

```bash
#!/bin/bash
# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

# Create the backup directory if it does not exist
mkdir -p $BACKUP_DIR

# Compress the source directory into a tarball (.tar.gz)
tar -czf $BACKUP_DIR/backup_$TIMESTAMP.tar.gz $SOURCE_DIR

echo "Backup completed successfully at $TIMESTAMP!"
```

## 3. File Permissions: `chmod +x`

The command `chmod +x backup.sh` adds executable permission to the Bash script. This allows the script to be executed directly using `./backup.sh` instead of only being treated as a regular text file.

## 4. Cron Job Configuration

The following cron expression schedules the backup script to run every day at 2:00 AM.

```cron
0 2 * * * /root/backup.sh
```

### Breakdown of the Cron Expression

| Field        | Value | Explanation                     |
| ------------ | ----- | ------------------------------- |
| Minute       | `0`   | Runs at minute zero.            |
| Hour         | `2`   | Runs at 2:00 AM.                |
| Day of Month | `*`   | Runs on every day of the month. |
| Month        | `*`   | Runs during every month.        |
| Day of Week  | `*`   | Runs on every day of the week.  |

The command `/root/backup.sh` specifies the absolute path of the script that cron executes. The schedule follows the server's configured timezone.

## 5. Important Commands

| Command                                                    | Purpose                                              |
| ---------------------------------------------------------- | ---------------------------------------------------- |
| `mkdir app-data`                                           | Creates the application data directory.              |
| `echo "This is critical client data." > app-data/data.txt` | Creates a sample file containing test data.          |
| `nano backup.sh`                                           | Opens Nano to create or edit the Bash script.        |
| `chmod +x backup.sh`                                       | Adds executable permission to the script.            |
| `./backup.sh`                                              | Executes the backup script.                          |
| `ls -l backups/`                                           | Lists the generated backup archives.                 |
| `crontab -l`                                               | Displays the current user's installed cron schedule. |

## 6. Conclusion

This laboratory demonstrates how Bash scripting, file permissions, compression, and cron scheduling can work together to automate a recurring backup task. The configuration reduces the need for manual execution, while verification and monitoring remain important to ensure backups are created successfully.
