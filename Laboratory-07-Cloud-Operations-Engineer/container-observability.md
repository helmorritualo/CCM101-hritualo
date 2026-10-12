## Application Logs

The application logs were retrieved using the `docker logs client-website` command.

### HTTP 404 Log Entry

172.17.0.1 - - [12/Oct/2026:04:31:55 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
2026/10/12 04:31:55 [error] 29#29: *4 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"

### Why Application Logs Matter

Application logs help troubleshoot problems by recording HTTP requests, response status codes, and other useful event details. By examining these records, an administrator can identify failed requests, investigate possible causes, and determine whether an issue comes from the application or the requested resource.

## Real-Time Container Metrics

The `docker stats` command was used to monitor the resource consumption of the `client-website` container in real time.

### Observed Metrics

| Metric                        |    Observed Value |
| ----------------------------- | ----------------: |
| Container Name                |  `client-website` |
| Container ID                  |    `8c0365786681` |
| CPU Usage                     |             0.00% |
| Memory Usage                  |         2.723 MiB |
| Memory Limit                  |         1.859 GiB |
| Memory Utilization            |             0.14% |
| Network I/O (Received / Sent) | 3.84 kB / 5.29 kB |
| Block I/O (Read / Written)    |     0 B / 12.3 kB |
| Process Count (PIDs)          |                 2 |

### Analysis

The Docker metrics showed that the `client-website` container was consuming 0.00% CPU and approximately 2.723 MiB of memory, equivalent to 0.14% of its displayed memory limit. Its network I/O was 3.84 kB received and 5.29 kB sent, while its block I/O showed 0 B read and 12.3 kB written.

These measurements indicate low resource consumption at the time of observation. However, the results represent a snapshot of the container's resource usage and do not, by themselves, prove that the server can handle thousands of simultaneous users.
