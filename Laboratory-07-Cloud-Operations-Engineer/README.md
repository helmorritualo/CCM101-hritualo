# Mission 7: The Cloud Operations Engineer

## Mission Overview

This laboratory activity focused on monitoring a Linux host and observing the performance of a containerized web server using KillerCoda and Docker. The mission involved establishing a system resource baseline, deploying an Nginx web server, generating HTTP requests, inspecting application logs, and monitoring container resource consumption.

The activity demonstrated how system monitoring and application logs help cloud operations engineers assess service health and investigate potential problems.

## Objectives

The objectives of this laboratory activity were to:

- Monitor host RAM, disk capacity, CPU activity, and running processes using Linux command-line tools.
- Deploy an Nginx web server container named `client-website` and expose it through host port `8080`.
- Generate successful HTTP requests and intentionally trigger an HTTP 404 response.
- Inspect Nginx application logs and identify the failed request.
- Monitor container CPU, memory, network I/O, and block I/O using Docker.
- Document monitoring results and maintain a structured GitHub Cloud Computing portfolio.

## Monitoring Commands Executed

| Command                                                | Purpose                                                                                   |
| ------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| `free -h`                                              | Check system memory usage and available RAM.                                              |
| `df -h /`                                              | Inspect the root filesystem's total capacity, used space, and available disk space.       |
| `top`                                                  | Observe CPU activity, system load, memory usage, and running processes.                   |
| `docker run -d --name client-website -p 8080:80 nginx` | Deploy the Nginx container in the background and map host port 8080 to container port 80. |
| `docker ps --filter name=client-website`               | Verify the container's running status.                                                    |
| `curl` requests to `http://localhost:8080/`            | Generate HTTP requests to test the website homepage.                                      |
| `curl -i http://localhost:8080/hidden-admin-page`      | Request a nonexistent page and inspect the HTTP 404 response.                             |
| `docker logs client-website`                           | Retrieve the container's application logs and inspect HTTP request results.               |
| `docker stats`                                         | Monitor the container's CPU, memory, network, block I/O, and process count in real time.  |

## Skills Learned

- **Linux system monitoring:** Learned how to inspect RAM, disk capacity, CPU utilization, system load, and running processes.
- **Docker container management:** Practiced deploying and verifying a containerized Nginx web server.
- **HTTP testing:** Used `curl` to send web requests and examine HTTP status codes, including successful responses and a 404 error.
- **Log analysis:** Used Docker logs to investigate web requests and identify failed resource access.
- **Container observability:** Used `docker stats` to inspect real-time resource consumption and interpret CPU, memory, and I/O measurements.
- **Technical documentation:** Practiced recording system measurements, analyzing observations, and organizing Markdown documentation and screenshots in GitHub.

## Related Reports and Evidence

- [System Baseline Report](system-baseline-report.md) — Host memory, disk capacity, and CPU observations.
- [Container Observability Report](container-observability.md) — Application logs, HTTP error analysis, and container resource metrics.
- [Mission Reflection](reflection.md) — Reflection on the laboratory's learning objectives and troubleshooting experience.
- [Screenshots](screenshots/) — Terminal evidence collected during the laboratory checkpoints.
