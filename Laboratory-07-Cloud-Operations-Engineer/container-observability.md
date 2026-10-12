## Application Logs

The application logs were retrieved using the `docker logs client-website` command.

### HTTP 404 Log Entry

172.17.0.1 - - [12/Oct/2026:04:31:55 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"
2026/10/12 04:31:55 [error] 29#29: *4 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"

### Why Application Logs Matter

Application logs help troubleshoot problems by recording HTTP requests, response status codes, and other useful event details. By examining these records, an administrator can identify failed requests, investigate possible causes, and determine whether an issue comes from the application or the requested resource.
