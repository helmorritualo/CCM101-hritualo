# Laboratory 01 – Welcome to the Cloud

## Mission Overview

Laboratory Activity 1, "Mission 1: Welcome to the Cloud," is an introductory cloud computing activity designed to familiarize me with a cloud-based Linux environment. The laboratory used the KillerCoda Playground to provide an Ubuntu environment where I could practice basic Linux system administration and documentation tasks.

The activity also introduced the organization of a professional Cloud Computing portfolio using GitHub and Markdown.

## Objectives

The objectives of this laboratory activity were to:

- Access and use a cloud-based Linux environment using KillerCoda.
- Explore and navigate the Linux operating system.
- Gather basic system information.
- Create and manage users in Linux.
- Organize files and directories using Linux commands.
- Create and maintain a GitHub repository.
- Document technical work using Markdown.
- Practice professional documentation practices used by cloud engineers.

## Activities Performed

The following activities were completed during the laboratory:

1. Launched an Ubuntu Linux environment using KillerCoda.
2. Created a new Linux user named `hritualo`.
3. Configured the user with:
    - Bash as the login shell
    - A home directory
    - `sudo` privileges
4. Set a password for the new user.
5. Logged in using the newly created user account.
6. Checked the current username, working directory, and hostname.
7. Collected information about the Linux distribution, kernel, CPU, memory, and disk space.
8. Created the required workspace directories inside the user's home directory.
9. Created the `about-me.md` file inside the `NOTES` directory.
10. Captured screenshots as evidence of the completed laboratory tasks.

## Linux Commands Used

| Command                                    | Purpose                                                                                   |
| ------------------------------------------ | ----------------------------------------------------------------------------------------- |
| `whoami`                                   | Displays the current username.                                                            |
| `pwd`                                      | Displays the current working directory.                                                   |
| `hostname`                                 | Displays the system hostname.                                                             |
| `useradd -m -s /bin/bash -G sudo hritualo` | Creates the `hritualo` user with a home directory, Bash shell, and sudo group membership. |
| `passwd hritualo`                          | Sets or changes the user's password.                                                      |
| `id hritualo`                              | Displays the user's UID, GID, and group memberships.                                      |
| `ls -ld /home/hritualo`                    | Verifies the user's home directory.                                                       |
| `su - hritualo`                            | Logs in as the `hritualo` user.                                                           |
| `cat /etc/os-release`                      | Displays Linux distribution information.                                                  |
| `uname -r`                                 | Displays the kernel version.                                                              |
| `lscpu`                                    | Displays CPU information.                                                                 |
| `free -h`                                  | Displays memory usage and available memory.                                               |
| `df -h`                                    | Displays disk space information.                                                          |
| `mkdir`                                    | Creates directories.                                                                      |
| `cd`                                       | Changes the current working directory.                                                    |
| `touch`                                    | Creates an empty file.                                                                    |
| `ls`                                       | Lists files and directories.                                                              |

## Skills Learned

Through this laboratory activity, I practiced basic Linux system administration tasks in a cloud-based environment. I learned how to create and configure a user account, navigate the Linux file system, collect system information, and organize directories and files using terminal commands.

I also gained experience in documenting technical activities using Markdown and organizing laboratory outputs for a GitHub-based portfolio.

These skills provide a foundation for later cloud computing activities involving Linux administration, containers, Kubernetes, cloud infrastructure, and other enterprise technologies.
