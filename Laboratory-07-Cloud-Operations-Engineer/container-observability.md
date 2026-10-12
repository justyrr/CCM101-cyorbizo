## Application Logs

Retrieved the application logs from the container:

    docker logs client-website2

### 404 Error Log Line

The following log entry shows the intentional 404 error from the earlier simulation:

    2026/10/12 01:11:49 [error] 29#29: *4 open() "/usr/share/nginx/html/hidden-admin-page" failed (2: No such file or directory), client: 172.17.0.1, server: localhost, request: "GET /hidden-admin-page HTTP/1.1", host: "localhost:8080"
    172.17.0.1 - - [12/Oct/2026:01:11:49 +0000] "GET /hidden-admin-page HTTP/1.1" 404 153 "-" "curl/8.5.0" "-"

### Why Application Logs Are Vital for Troubleshooting

Application logs are vital for troubleshooting because they provide a chronological
record of every request, error, and event that the application processes, allowing
engineers to pinpoint exactly what went wrong, when it happened, and which request
triggered the failure. Without logs, diagnosing issues would rely on guesswork,
making it nearly impossible to trace the root cause of a problem in a live
production system.

## Real-Time Container Metrics

Command used to view live resource consumption:

    docker stats

Observed metrics for the `client-website2` container:

- **CPU %:** 0.00%
- **Memory Usage:** 2.824MiB / 1.859GiB (0.15%)
- **Network I/O:** 3.84kB / 5.29kB
- **Block I/O:** 69.6kB / 12.3kB
- **PIDs:** 2

### Analysis

The container is consuming only 2.824MiB of memory and 0.00% CPU while idle,
which is an extremely small footprint for a running web server. This confirms
that the Nginx container is running efficiently, and the host still has more
than 1.8GiB of RAM free to handle a sudden surge in user traffic.
