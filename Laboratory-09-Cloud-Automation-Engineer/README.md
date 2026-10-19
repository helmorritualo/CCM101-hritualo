# Laboratory 09: The Cloud Automation Engineer

## Mission Overview

This laboratory focuses on automating routine cloud administration tasks using Bash scripting and Linux cron scheduling. The main task is to create a script that compresses sample application data into a timestamped backup archive and configure a cron job to run the script every day at 2:00 AM.

## Objectives

- Understand the basic syntax of Bash scripts, including variables and the shebang.
- Create a sample application directory and test file.
- Write and execute a Bash script that generates compressed backups.
- Manage file execution permissions using `chmod`.
- Configure a cron job to schedule a recurring task.
- Document the script, commands, and scheduling configuration in Markdown.

## Commands Executed

### Create the Application Data

```bash
mkdir app-data
echo "This is critical client data." > app-data/data.txt
```

### Create and Run the Backup Script

```bash
nano backup.sh
chmod +x backup.sh
./backup.sh
```

### Verify the Backup

```bash
ls -l backups/
```

### Configure and Verify the Cron Job

```bash
crontab -l
env EDITOR=nano crontab -e
crontab -l
```

Configured cron expression:

```cron
0 2 * * * /root/backup.sh
```

## Skills Learned

- Bash scripting and the use of variables.
- Creating directories and files using Linux commands.
- Compressing directory contents into `.tar.gz` archives.
- Modifying file permissions with `chmod`.
- Scheduling recurring tasks with Linux cron.
- Verifying backup archives and documenting technical procedures in Markdown.
