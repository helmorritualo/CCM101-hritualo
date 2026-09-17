# Checkpoint 2 – Research: Virtual Machines vs. Containers

CloudNova Technologies has a client whose traditional virtual machines take too long to boot and consume more RAM than their web applications need. The client has heard of Docker and containers but does not yet understand how they differ from virtual machines. This report compares the two technologies using official Docker, IBM, and Microsoft documentation so the client can decide whether containerizing the web applications is a better approach.

## Comparison

| Category | Virtual Machines (VMs) | Containers |
| --- | --- | --- |
| Architecture | A hypervisor virtualizes physical hardware and each VM runs a complete **guest operating system**, including its own kernel, drivers, and applications. | Containers virtualize the operating system instead of the hardware. They share the **host operating system kernel** and package only the application plus its libraries as isolated processes in user space. |
| Boot Time | Startup is slow, often measured in **minutes**, because the guest operating system, kernel, and drivers must boot before the application can start. | Startup is fast, often measured in **seconds**, because the container starts as a process on an already running host kernel and does not boot a separate operating system. |
| Resource Efficiency | **Heavy / high RAM.** Each VM includes a full operating-system copy, commonly tens of gigabytes, plus the application. Fewer workloads can run on the same server, and unused guest-OS memory is wasted. | **Lightweight / low RAM.** Container images are commonly tens of megabytes because they do not include a guest OS for every application. More web servers can share the same host with less memory overhead. |
| Isolation Level | **Hardware-level isolation.** The hypervisor separates each VM from the host and from other VMs, which provides a strong security boundary. | **Process-level isolation.** Linux namespaces and control groups separate what each container can see and use, but the shared kernel is a lighter boundary than a VM. |

## Recommendation for the Client

The client's web applications should move from one virtual machine per application to containers because each VM boots a complete guest operating system, which is why startup takes minutes and RAM usage stays high. A container shares the host operating system kernel and runs the application as an isolated process, so it can start in seconds and use much less memory. Docker packages the web server with its required libraries, which lets the same application run consistently on the client's servers without installing a new guest OS for every instance. Process-level isolation is enough for these web workloads and allows several containers to share one host instead of wasting a full virtual machine on each application.

## Sources

- Docker. (n.d.). *What is a container?* Docker Documentation. https://docs.docker.com/get-started/docker-concepts/the-basics/what-is-a-container/
- Docker. (n.d.). *What is a container?* Docker. https://www.docker.com/resources/what-container/
- IBM. (n.d.). *Containers versus virtual machines (VMs): What's the difference?* IBM Think. https://www.ibm.com/think/topics/containers-vs-vms
- Microsoft. (n.d.). *Containers vs. virtual machines.* Microsoft Learn. https://learn.microsoft.com/en-us/virtualization/windowscontainers/about/containers-vs-vm
