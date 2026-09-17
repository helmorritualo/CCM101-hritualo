# Checkpoint 7 – Mission Reflection

## 1. How does the boot time and setup process of a Docker container compare to installing an operating system on a Virtual Machine?

Installing an operating system on a virtual machine means creating a full guest OS with its own kernel, drivers, and packages. That setup can take minutes because the guest OS has to boot before the application can start. A Docker container does not install a separate operating system. It shares the host kernel and starts as an isolated process, which is why the Nginx container in KillerCoda was serving pages in seconds after `docker pull nginx` and `docker run -d -p 8080:80 nginx`.

## 2. Why is port mapping (-p 8080:80) necessary when running a web server inside a container?

Nginx listens on port 80 inside the container's isolated network. Without publishing a port, that service is not reachable on the host as `localhost:8080`. The `-p 8080:80` flag maps host port 8080 to container port 80, which is why `curl http://localhost:8080` returned the Welcome to nginx! page. Docker documentation describes this flag as mapping a host port to a TCP port inside the container.

## 3. What happens to the data inside a container when you use the docker rm command?

`docker rm` deletes the container and its writable layer, so files created or changed inside that container are removed. The image remains on the host, which is why Nginx could be started again from `nginx:latest`, but the stopped container `df39493b17c3` no longer existed after removal. Data in a named Docker volume would persist, but this laboratory did not mount a volume, so the running container's filesystem did not survive `docker rm`.

## 4. How do you think containerization changes the way software developers and IT operations teams work together (DevOps)?

Containers package the application with its libraries, so developers and operations can run the same image instead of installing a full guest OS in each environment. That reduces "it works on my machine" problems and lets operations start, stop, and replace services with Docker commands instead of rebuilding virtual machines. The shared unit of work becomes the container image, which supports faster testing, deployment, and recovery.

## 5. How is your GitHub portfolio evolving?

The portfolio now includes a fourth laboratory with a VM-versus-container report, Docker command evidence, lifecycle documentation, and this reflection. Checkpoint commits and screenshots show how each step was completed. The repository has moved from Linux basics and multi-cloud research to documenting a live containerized web server that can be replicated from the recorded commands.
