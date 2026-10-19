# Checkpoint 2: The Language of Automation

## 1. Bash Script

A Bash script is a text file containing Linux shell commands that can be executed together to automate tasks. The `#!/bin/bash` line, also called a shebang, tells the operating system to use the Bash interpreter to execute the commands in the file.

## 2. Variables

Variables store values, such as directory paths, filenames, or timestamps, so they can be reused throughout a script. For example, using `$BACKUP_DIR` makes it easier to change the backup location in one place instead of editing every command that uses the same directory.

## 3. Cron Job

A cron job is a scheduled task in Linux that automatically runs a command or script at a specified time or interval. It is useful in cloud operations because it can automate repetitive tasks, such as backups and maintenance, without requiring someone to run them manually each time.
