# Mission Reflection

This laboratory activity helped me understand that deploying a container is only one part of operating a cloud application. The host server's resources still need to be monitored because containers share the underlying CPU, memory, and storage resources. Even if a container is running, limited RAM or disk space can cause slow responses, failed writes, or service interruptions. In my baseline check, the server had 1.9 GiB of RAM and a 19 GB root filesystem with 13 GB available, while `top` showed 100% CPU idle at the time of observation.

The `docker logs` command is useful when a user reports that they cannot log in or access a page. Logs can show requests, timestamps, errors, and HTTP status codes that help an administrator investigate what happened. In this activity, I requested a nonexistent page so I could identify the HTTP 404 entry in the Nginx logs. A 404 indicates that the requested resource was not found, although it does not automatically explain every possible login failure.

Logs and metrics provide different kinds of information. Logs describe individual events, requests, and errors, while metrics summarize measurements such as CPU usage, memory consumption, network traffic, and process counts. The `docker stats` output showed that `client-website` was using 0.00% CPU and 2.723 MiB of memory when I checked it. This was a useful snapshot, but it does not prove how the container would perform under heavy traffic.

Large companies can use monitoring platforms such as Prometheus to collect metrics from many services and containers and Grafana to display dashboards and trends. Alerts can notify operations teams when resource usage or service health crosses defined thresholds, allowing them to investigate potential problems.

Overall, this activity gave me practical experience using Linux commands and Docker to gather evidence instead of relying on guesses. I also practiced connecting terminal output to technical documentation. I learned that effective troubleshooting involves checking the host, inspecting logs, reviewing metrics, and using those findings together before deciding what to investigate next.
