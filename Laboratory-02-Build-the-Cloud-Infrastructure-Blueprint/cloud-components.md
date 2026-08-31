# Cloud Infrastructure Components

## Checkpoint 3: Identify Cloud Infrastructure Components

## Objective

The objective of this checkpoint is to identify the main cloud infrastructure components present in the KillerCoda Linux environment. For each component, this report:

1. Identifies an example found in the environment.
2. Describes its purpose.
3. Explains its importance in cloud computing.
4. Relates it to the command output collected from the KillerCoda server.

The four required components are **compute resources**, **storage resources**, **networking resources**, and the **operating system**.

## Environment Summary

| Component            | Observed example in KillerCoda                                |
| -------------------- | ------------------------------------------------------------- |
| Compute resources    | One Intel Xeon E312xx virtual CPU and 1.9 GiB of RAM          |
| Storage resources    | A 20 GB virtual disk named `/dev/vda`                         |
| Networking resources | Hostname `ubuntu`; IP addresses `172.30.1.2` and `172.17.0.1` |
| Operating system     | Ubuntu 24.04.4 LTS (Noble Numbat), kernel `6.8.0-138-generic` |

## 1. Compute Resources

### Example identified

The KillerCoda environment provides a virtual processor and system memory. The `lscpu` output shows **one CPU** with the model name **Intel Xeon E312xx (Sandy Bridge, IBRS update)**. It has one socket, one core per socket, and one thread per core. The architecture is `x86_64`, and the hypervisor vendor is **KVM** with a virtualization type of **full**.

The `free -h` output shows **1.9 GiB of total RAM**. At the time of inspection, 422 MiB was used, 860 MiB was free, 788 MiB was used for buffer/cache, and 1.4 GiB was available. The server also had 1.0 GiB of swap space, with none in use.

### Purpose

Compute resources execute operating-system instructions, commands, processes, and applications. The CPU performs calculations and processes instructions, while RAM temporarily holds data and instructions that are actively needed. Swap space supplements physical memory by providing disk-based virtual memory.

### Importance in cloud computing

Compute capacity determines how much processing work a cloud server can perform. The number of virtual CPUs and the amount of memory affect how many applications or services can run and how well they perform. Virtualization allows a cloud provider to allocate part of a physical host's processing capacity to an isolated virtual server.

### Relationship to the KillerCoda environment

The reported **KVM hypervisor** and **full virtualization** show that the KillerCoda Linux system is operating as a virtualized environment. Its one virtual CPU and 1.9 GiB of RAM provide the compute capacity used to run Linux commands and processes during this activity.

### Commands used

```bash
lscpu
free -h
```

## 2. Storage Resources

### Example identified

The `lsblk` output shows a **20 GB virtual disk** named `/dev/vda`. It is divided into the following partitions:

| Partition    |   Size | Mount point                         |
| ------------ | -----: | ----------------------------------- |
| `/dev/vda1`  |  19 GB | `/`                                 |
| `/dev/vda14` |   4 MB | Not mounted in the displayed output |
| `/dev/vda15` | 106 MB | `/boot/efi`                         |
| `/dev/vda16` | 913 MB | `/boot`                             |

The `df -h` output shows that the 19 GB root file system on `/dev/vda1` had 5.4 GB used and 13 GB available, for 30% usage. The `findmnt` output identifies `/dev/vda1` as an `ext4` file system mounted at `/`. It also shows `/dev/vda16` as `ext4` mounted at `/boot` and `/dev/vda15` as `vfat` mounted at `/boot/efi`.

### Purpose

Storage resources retain the operating system, applications, configuration files, user files, logs, and other data. Unlike RAM, disk storage is intended to preserve data when a process finishes or the system is restarted. Mounted file systems make storage devices and partitions accessible through the Linux directory structure.

### Importance in cloud computing

Cloud workloads require storage for persistent data and system files. Storage capacity, organization, availability, and file-system type affect how data is saved and accessed. Separating the root, boot, and EFI file systems also supports the system's startup process and organizes critical files.

### Relationship to the KillerCoda environment

The `/dev/vda` device is the environment's virtual disk. Its main partition, `/dev/vda1`, contains the root file system where the Ubuntu installation and most files are stored. The `/boot` partition stores boot-related files, while `/boot/efi` supports the EFI startup process. Temporary file systems such as `tmpfs` are also mounted for runtime and shared-memory data.

### Commands used

```bash
lsblk
df -h
findmnt
```

## 3. Networking Resources

### Example identified

The `hostname` command reports the server hostname as **`ubuntu`**. The `hostname -I` command reports two IP addresses:

- `172.30.1.2`
- `172.17.0.1`

### Purpose

Networking resources allow a cloud server to identify itself and communicate with other systems. A hostname provides a human-readable system identity. An IP address identifies a network interface or network endpoint so that data can be sent to and from the server.

### Importance in cloud computing

Networking connects cloud servers to users, other servers, application services, storage services, and management systems. IP addressing is necessary for routing traffic, while hostnames help administrators and applications distinguish systems. Without networking resources, cloud services could not exchange data or be accessed remotely.

### Relationship to the KillerCoda environment

The hostname `ubuntu` identifies the Linux server. The two addresses displayed by `hostname -I` are the IP addresses assigned within the environment. They demonstrate that the server has network connectivity and can participate in one or more internal networks. The command output alone does not identify the exact interface or role associated with each address, so no additional interface assignment is assumed in this report.

### Commands used

```bash
hostname
hostname -I
```

## 4. Operating System

### Example identified

The `/etc/os-release` file identifies the operating system as **Ubuntu 24.04.4 LTS**, with the codename **Noble Numbat**. The distribution ID is `ubuntu`, and the version ID is `24.04`. The `uname -r` command reports Linux kernel version **6.8.0-138-generic**.

### Purpose

The operating system manages the server's hardware and virtual resources. It provides the environment in which commands, processes, applications, users, file systems, and network services operate. The Linux kernel is the core part of the operating system that manages CPU time, memory, devices, storage, and communication with hardware or virtual hardware.

### Importance in cloud computing

A cloud server requires an operating system to make allocated compute, storage, and networking resources usable. The operating system provides security controls, process management, software installation, file management, and networking capabilities. An LTS release is intended to provide a stable software base with long-term support.

### Relationship to the KillerCoda environment

Ubuntu provides the command-line environment used for this activity. Commands such as `lscpu`, `free`, `lsblk`, `df`, `findmnt`, and `hostname` are executed within this Linux operating system to inspect the virtual infrastructure. Kernel `6.8.0-138-generic` manages the environment's virtual CPU, memory, storage devices, and networking resources.

### Commands used

```bash
cat /etc/os-release
uname -r
```

## How the Components Work Together

The four components form one working cloud server:

1. **Compute resources** execute Ubuntu and its applications.
2. **Storage resources** hold Ubuntu, boot files, applications, and data.
3. **Networking resources** identify the server and enable communication.
4. **The operating system** manages the compute, storage, and networking resources and provides the interface used by administrators and applications.

In the KillerCoda environment, Ubuntu runs on a KVM virtual machine with one virtual CPU, 1.9 GiB of RAM, a 20 GB virtual disk, and two reported IP addresses. Together, these resources provide the functional Linux cloud environment investigated in this checkpoint.

## Screenshot Evidence

### Operating-System Evidence

This screenshot shows the output of `cat /etc/os-release`.

![Ubuntu operating-system information](screenshots/server-information.png)

### Compute Evidence

This screenshot shows the kernel version and `lscpu` output.

![Kernel and CPU information](screenshots/cpu-information.png)

### Memory, Storage, and Networking Evidence

This screenshot shows the output of `free -h`, `lsblk`, `df -h`, `findmnt`, `hostname`, and `hostname -I`.

![Memory, storage, and networking information](screenshots/storage-network-information.png)

## Conclusion

The KillerCoda environment contains all four required cloud infrastructure components. Compute is supplied by one virtual Intel Xeon CPU and 1.9 GiB of RAM. Storage is supplied by a 20 GB virtual disk and its mounted partitions. Networking is represented by the hostname `ubuntu` and the IP addresses `172.30.1.2` and `172.17.0.1`. Ubuntu 24.04.4 LTS and Linux kernel 6.8.0-138-generic manage these resources and provide the working server environment.
