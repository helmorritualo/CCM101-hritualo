# Cloud Infrastructure Report

## Overview

This report documents the cloud server environment investigated through the KillerCoda Linux terminal. The findings below are based on the command outputs captured during Checkpoint 2.

## Infrastructure Summary

| Item                | Finding                                       |
| ------------------- | --------------------------------------------- |
| Operating System    | Ubuntu 24.04.4 LTS (Noble Numbat)             |
| Kernel Version      | 6.8.0-138-generic                             |
| CPU Model           | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| CPU Cores           | 1                                             |
| Total RAM           | 1.9 GiB                                       |
| Swap Space          | 1.0 GiB                                       |
| Disk Capacity       | 20 GB                                         |
| Root Partition      | `/dev/vda1` — 19 GB, mounted on `/`           |
| Hostname            | `ubuntu`                                      |
| IP Addresses        | `172.30.1.2` and `172.17.0.1`                 |
| Architecture        | `x86_64`                                      |
| Hypervisor          | KVM                                           |
| Virtualization Type | Full virtualization                           |

## Operating System

The server is running **Ubuntu 24.04.4 LTS**, with the codename **Noble Numbat**. The operating-system information was collected with:

```bash
cat /etc/os-release
```

The relevant results were:

- `PRETTY_NAME="Ubuntu 24.04.4 LTS"`
- `VERSION_ID="24.04"`
- `VERSION="24.04.4 LTS (Noble Numbat)"`
- `VERSION_CODENAME=noble`
- `ID=ubuntu`

## Kernel and CPU

The kernel and processor details were collected with:

```bash
uname -r
lscpu
```

The server uses Linux kernel **6.8.0-138-generic** and has the following CPU configuration:

| CPU Detail          | Value                                         |
| ------------------- | --------------------------------------------- |
| Architecture        | `x86_64`                                      |
| CPU operating modes | 32-bit and 64-bit                             |
| Byte order          | Little Endian                                 |
| CPU count           | 1                                             |
| Online CPU list     | `0`                                           |
| Vendor ID           | GenuineIntel                                  |
| BIOS vendor ID      | Red Hat                                       |
| Model name          | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| BIOS model name     | RHEL-9.6.0 PC (Q35 + ICH9, 2009) CPU @ 2.0GHz |
| CPU family          | 6                                             |
| Model               | 42                                            |
| Threads per core    | 1                                             |
| Cores per socket    | 1                                             |
| Sockets             | 1                                             |
| BogoMIPS            | 7008.00                                       |
| Hypervisor vendor   | KVM                                           |
| Virtualization type | Full                                          |
| NUMA nodes          | 1                                             |

## Memory

Memory information was collected with:

```bash
free -h
```

The observed memory status was:

| Resource |   Total |    Used |    Free |  Shared | Buff/Cache | Available |
| -------- | ------: | ------: | ------: | ------: | ---------: | --------: |
| RAM      | 1.9 GiB | 422 MiB | 860 MiB | 1.1 MiB |    788 MiB |   1.4 GiB |
| Swap     | 1.0 GiB |     0 B | 1.0 GiB |       — |          — |         — |

## Storage

Storage information was collected with:

```bash
lsblk
df -h
```

### Block Devices

| Device       |   Size | Type      | Mount Point |
| ------------ | -----: | --------- | ----------- |
| `/dev/vda`   |  20 GB | Disk      | —           |
| `/dev/vda1`  |  19 GB | Partition | `/`         |
| `/dev/vda14` |   4 MB | Partition | —           |
| `/dev/vda15` | 106 MB | Partition | `/boot/efi` |
| `/dev/vda16` | 913 MB | Partition | `/boot`     |

### Disk Usage

| File System  |   Size |   Used | Available | Use | Mounted On  |
| ------------ | -----: | -----: | --------: | --: | ----------- |
| `/dev/vda1`  |  19 GB | 5.4 GB |     13 GB | 30% | `/`         |
| `tmpfs`      | 952 MB |  84 KB |    952 MB |  1% | `/dev/shm`  |
| `tmpfs`      | 5.0 MB |    0 B |    5.0 MB |  0% | `/run/lock` |
| `/dev/vda16` | 881 MB | 117 MB |    703 MB | 15% | `/boot`     |
| `/dev/vda15` | 105 MB | 6.2 MB |     99 MB |  6% | `/boot/efi` |

## Mounted File Systems

Mounted file systems were inspected with:

```bash
findmnt
```

The main mounted file systems shown in the output were:

| Target      | Source       | File-System Type |
| ----------- | ------------ | ---------------- |
| `/`         | `/dev/vda1`  | `ext4`           |
| `/sys`      | `sysfs`      | `sysfs`          |
| `/proc`     | `proc`       | `proc`           |
| `/dev`      | `udev`       | `devtmpfs`       |
| `/dev/pts`  | `devpts`     | `devpts`         |
| `/dev/shm`  | `tmpfs`      | `tmpfs`          |
| `/run`      | `tmpfs`      | `tmpfs`          |
| `/run/lock` | `tmpfs`      | `tmpfs`          |
| `/boot`     | `/dev/vda16` | `ext4`           |
| `/boot/efi` | `/dev/vda15` | `vfat`           |

## Hostname and IP Addresses

Network identity information was collected with:

```bash
hostname
hostname -I
```

The server hostname is **`ubuntu`**. The reported IP addresses are:

- `172.30.1.2`
- `172.17.0.1`

## Commands Used

```bash
cat /etc/os-release
uname -r
lscpu
free -h
lsblk
df -h
findmnt
hostname
hostname -I
```

## Conclusion

The investigated environment is an Ubuntu 24.04.4 LTS virtual server running Linux kernel 6.8.0-138-generic on KVM. It has one Intel Xeon virtual CPU core, 1.9 GiB of RAM, 1.0 GiB of swap space, and a 20 GB virtual disk. Its hostname is `ubuntu`, and the terminal reported the IP addresses `172.30.1.2` and `172.17.0.1`.
