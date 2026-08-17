# System Information

This document contains the basic system information collected from the Ubuntu Linux environment provided by the KillerCoda Playground during Laboratory Activity 1.

## 1. Linux Distribution

The Linux distribution running in the KillerCoda environment is **Ubuntu 24.04.4 LTS**.

### Details

- **Distribution:** Ubuntu
- **Version:** Ubuntu 24.04.4 LTS
- **Codename:** noble
- **Version ID:** `24.04`
- **ID:** `ubuntu`
- **ID Like:** `debian`

### Command Used

```bash
cat /etc/os-release
```

### Result

```text
PRETTY_NAME="Ubuntu 24.04.4 LTS"
NAME="Ubuntu"
VERSION="24.04.4 LTS (Noble Numbat)"
VERSION_ID="24.04"
ID=ubuntu
ID_LIKE=debian
```

---

## 2. Kernel Version

The Linux kernel version running in the environment is:

**`6.8.0-136-generic`**

### Command Used

```bash
uname -r
```

### Result

```text
6.8.0-136-generic
```

---

## 3. CPU Information

The KillerCoda environment provides a virtualized CPU through KVM.

### CPU Details

- **Architecture:** `x86_64`
- **CPU(s):** `1`
- **Online CPU(s):** `0`
- **Vendor:** `GenuineIntel`
- **Model Name:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
- **CPU Family:** `6`
- **Model:** `42`
- **Stepping:** `1`
- **Sockets:** `1`
- **Cores per Socket:** `1`
- **Threads per Core:** `1`
- **Virtualization:** `KVM`
- **Virtualization Type:** `full`

### Command Used

```bash
lscpu
```

### Relevant Result

```text
Architecture:        x86_64
CPU(s):              1
On-line CPU(s) list: 0
Vendor ID:           GenuineIntel
Model name:          Intel Xeon E312xx (Sandy Bridge, IBRS update)
CPU family:          6
Model:               42
Thread(s) per core:  1
Core(s) per socket:  1
Socket(s):            1
Stepping:             1
Virtualization:       KVM
Virtualization type:  full
```

---

## 4. Memory Information

The memory information was collected using the `free -h` command.

### Memory Details

| Memory Category  |  Amount |
| ---------------- | ------: |
| Total Memory     | 1.9 GiB |
| Used Memory      | 421 MiB |
| Free Memory      | 829 MiB |
| Shared Memory    | 1.1 MiB |
| Buff/Cache       | 821 MiB |
| Available Memory | 1.4 GiB |
| Swap Total       | 1.0 GiB |
| Swap Used        |     0 B |
| Swap Free        | 1.0 GiB |

### Command Used

```bash
free -h
```

### Result

```text
              total       used       free     shared    buff/cache   available
Mem:          1.9Gi       421Mi      829Mi     1.1Mi       821Mi       1.4Gi
Swap:         1.0Gi         0B       1.0Gi
```

---

## 5. Disk Space

The available disk space was checked using the `df -h` command.

The main root filesystem is `/dev/vda1`.

### Root Filesystem Details

| Disk Category   |      Amount |
| --------------- | ----------: |
| Filesystem      | `/dev/vda1` |
| Total Size      |         19G |
| Used Space      |        5.4G |
| Available Space |         13G |
| Usage           |         30% |
| Mount Point     |         `/` |

### Command Used

```bash
df -h
```

### Relevant Result

```text
/dev/vda1       19G    5.4G    13G    30%    /
```

---

## 6. System Information Summary

| Category             | Information                                   |
| -------------------- | --------------------------------------------- |
| Operating System     | Ubuntu 24.04.4 LTS                            |
| Codename             | Noble Numbat                                  |
| Version ID           | `24.04`                                       |
| Kernel Version       | `6.8.0-36-generic`                            |
| Architecture         | `x86_64`                                      |
| CPU                  | Intel Xeon E312xx (Sandy Bridge, IBRS update) |
| CPU(s)               | 1                                             |
| Cores per Socket     | 1                                             |
| Threads per Core     | 1                                             |
| Virtualization       | KVM                                           |
| Total Memory         | 1.9 GiB                                       |
| Available Memory     | 1.4 GiB                                       |
| Root Disk            | `/dev/vda1`                                   |
| Total Disk Space     | 19G                                           |
| Available Disk Space | 13G                                           |
| Disk Usage           | 30%                                           |

## 7. Conclusion

The KillerCoda Playground provided an Ubuntu 24.04.4 LTS cloud-based Linux environment running on a virtualized KVM system. The environment includes a single virtual CPU, approximately 1.9 GiB of memory, and a 19 GB root filesystem with approximately 13 GB of available space.

These system details were gathered using standard Linux commands such as `cat`, `uname`, `lscpu`, `free`, and `df`. The information provides a basic overview of the computing environment used during this laboratory activity.
