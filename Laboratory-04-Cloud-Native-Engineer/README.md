# Laboratory 04: Cloud-Native Engineer

## Mission Overview

Laboratory Activity 4, "Mission 4: The Cloud-Native Engineer," examined the shift from traditional virtual machines to containers. The activity first compared virtualization with containerization for a CloudNova Technologies client whose virtual machines boot slowly and consume more RAM than their web applications need. A KillerCoda Docker environment was then used to verify Docker, pull and run an Nginx web server, confirm it with `curl`, and manage the container lifecycle.

This laboratory continues the CCM101 Cloud Computing portfolio by adding container research, command evidence, and a mission reflection.

## Objectives

The objectives of this laboratory were to:

- Differentiate between traditional virtual machines (VMs) and containers.
- Access a Docker-enabled cloud environment using KillerCoda.
- Execute fundamental Docker CLI commands.
- Pull, run, manage, and terminate a containerized Nginx application.
- Create professional technical documentation of container operations using Markdown.
- Continue developing a well-organized GitHub Cloud Computing portfolio.

## Docker Commands Executed

The following commands were executed in Checkpoints 3, 4, and 5.

### Checkpoint 3 – Enter the Docker Playground

| Command | Purpose |
| --- | --- |
| `docker version` | Displayed the Docker client and server versions and confirmed that the Docker daemon was installed and running. |
| `docker info` | Displayed the current Docker environment, including container counts, storage driver, operating system, CPU, and memory. |

### Checkpoint 4 – Deploy Your First Container

| Command | Purpose |
| --- | --- |
| `docker pull nginx` | Downloaded the official Nginx image from Docker Hub. |
| `docker run -d -p 8080:80 nginx` | Started the Nginx container in detached mode and mapped host port 8080 to container port 80. |
| `curl http://localhost:8080` | Sent a local HTTP request and returned the HTML for the Welcome to nginx! page. |

### Checkpoint 5 – The Container Lifecycle

| Command | Purpose |
| --- | --- |
| `docker ps` | Listed running containers and showed Nginx container `df39493b17c3` with port mapping `8080->80`. |
| `docker stop df39493b17c3` | Stopped the running Nginx container. |
| `docker ps -a` | Listed all containers, including stopped ones, and confirmed that Nginx had status `Exited (0)`. |
| `docker rm df39493b17c3` | Removed the stopped Nginx container completely. |

## Skills Learned

The laboratory helped develop the following skills:

- Comparing virtual machine and container architecture, boot time, resource use, and isolation using official documentation.
- Verifying that Docker is installed and that the daemon is running with `docker version` and `docker info`.
- Pulling an official image from Docker Hub and running it as a detached container.
- Publishing a container port with `-p 8080:80` and testing the web server with `curl`.
- Managing the container lifecycle by listing, stopping, verifying, and removing a container.
- Distinguishing `docker ps` from `docker ps -a` when checking whether a container is running or only stopped.
- Documenting Docker procedures in Markdown and linking screenshot evidence with relative paths.
- Using checkpoint commits to record progress in the GitHub portfolio.

## Challenges Encountered

### Verifying Docker Client and Server Status

`docker version` was required instead of `docker --version` because only the full command shows both the client and the server. If the daemon had not been running, the Server section would have failed. `docker info` then produced a long environment report that did not fit in one screenshot, so additional captures were saved as `docker-version-info.png` and `docker-version-info2.png`.

### Understanding Port Mapping

It was initially unclear why Nginx could listen on port 80 inside the container while the test used `http://localhost:8080`. The `-p 8080:80` flag maps the host port to the container port. Without that mapping, `curl` on the host would not reach the isolated web server.

### Confirming That a Container Had Stopped

`docker ps` lists only running containers, so an empty list after `docker stop` could mean either that the container stopped or that it was never there. `docker ps -a` was needed to show the same container ID with status `Exited (0)` before `docker rm` deleted it.

### Keeping Commands Consistent with Screenshot Evidence

The README and `docker-deployment.md` had to use the same commands, container ID, and port mapping that appear in the KillerCoda screenshots. The container ID `df39493b17c3` was copied from `docker ps` so the lifecycle documentation would match the evidence.

## Repository Contents

```text
Laboratory-04-Cloud-Native-Engineer/
├── README.md
├── virtualization-vs-containers.md
├── docker-deployment.md
├── reflection.md
└── screenshots/
    ├── docker-version.png
    ├── docker-version-info.png
    ├── docker-version-info2.png
    ├── nginx-running.png
    └── container-lifecycle.png
```
