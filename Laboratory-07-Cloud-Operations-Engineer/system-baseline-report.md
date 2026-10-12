# System Baseline Report

## 1. Host System Resources

The baseline health check was performed in the KillerCoda Linux environment before deploying the Nginx web server container.

### Memory (RAM)

The `free -h` command reported the following memory statistics:

| Metric            | Observed Value |
| ----------------- | -------------: |
| Total RAM         |        1.9 GiB |
| Used RAM          |        414 MiB |
| Free RAM          |        1.2 GiB |
| Buffers and Cache |        458 MiB |
| Available RAM     |        1.5 GiB |
| Total Swap        |        1.0 GiB |
| Used Swap         |            0 B |

The server had approximately 1.5 GiB of available memory and was not using swap space at the time of inspection. This indicates that memory resources were available for the upcoming container deployment.

### Disk Storage

The `df -h /` command reported the following root filesystem statistics:

| Metric           | Observed Value |
| ---------------- | -------------: |
| Root Filesystem  |    `/dev/vda1` |
| Total Capacity   |          19 GB |
| Used Space       |         5.5 GB |
| Available Space  |          13 GB |
| Disk Utilization |            30% |
| Mount Point      |            `/` |

The root filesystem had 13 GB of available space, with 30% of its total capacity in use. This provided available storage for the upcoming laboratory tasks, including downloading the Nginx image and generating application logs.

## 2. CPU Activity and Running Processes

The `top` command was used to inspect CPU utilization, system load, memory usage, and running processes.

The observed results were:

- CPU idle time: 100.0%
- User CPU utilization: 0.0%
- System CPU utilization: 0.0%
- Load average: 0.00, 0.00, 0.02
- Total tasks: 129
- Running tasks: 1
- Sleeping tasks: 128
- Zombie processes: 0
- Available memory: 1,489.1 MiB
- Swap usage: 0 MiB

The server showed minimal CPU activity and low system load during the inspection. The Docker daemon (`dockerd`) was running and reported 0.3% CPU utilization. These observations establish the server's baseline condition before deploying and testing the Nginx container.

## 3. Why Disk Space Matters

Checking disk space before a massive traffic surge is important because insufficient storage can prevent applications from writing logs, temporary files, and other required data, potentially causing errors or service interruptions even when CPU and memory resources remain available.

## 4. Baseline Summary

The initial inspection showed that the KillerCoda server had 1.9 GiB of RAM, a 19 GB root filesystem, 13 GB of available disk space, low CPU load, and no swap usage. These measurements serve as a reference for evaluating container resource consumption during the subsequent laboratory checkpoints.
