# Laboratory 07 — Cloud Operations Engineer

## Mission Overview

In this mission, I stepped into the role of a Cloud Operations Engineer (Site
Reliability Engineer) at CloudNova Technologies. Using the KillerCoda Ubuntu
Playground, I established a performance baseline for a Linux host server,
deployed a containerized Nginx web server, generated artificial web traffic,
and analyzed both application logs and real-time container metrics to prove
the infrastructure is healthy and ready for a traffic surge.

## Objectives

- Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity.
- Deploy a web container and track its real-time performance using Docker metrics.
- Generate web traffic and extract application access logs for analysis.
- Translate raw performance data into a readable technical report using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio.

## Monitoring Commands Executed

### Host System Baseline

    free -h        # Check total, used, and available RAM
    df -h /        # Check root filesystem disk capacity
    top            # View running processes and CPU load (press q to exit)

### Container Deployment

    docker run -d --name client-website2 -p 8080:80 nginx
    docker ps

### Traffic Simulation

    curl http://localhost:8080
    curl http://localhost:8080
    curl http://localhost:8080
    curl http://localhost:8080/hidden-admin-page

### Logs and Metrics

    docker logs client-website2      # View application access and error logs
    docker stats                     # View live container CPU, memory, and I/O

## Key Metrics Captured

| Metric | Value |
|---|---|
| Total RAM | 1.9Gi |
| Available RAM | 1.5Gi |
| Root Filesystem Size | 19G |
| Root Filesystem Used | 5.5G (30%) |
| Host CPU Idle | 99.7% |
| Container CPU % | 0.00% |
| Container Memory Usage | 2.824MiB / 1.859GiB (0.15%) |

## Skills Learned

- Established a baseline health check of a Linux server using `free`, `df`, and `top`.
- Deployed and managed a containerized web server using Docker CLI.
- Simulated user traffic and intentionally triggered HTTP errors with `curl`.
- Extracted and interpreted Nginx access and error logs via `docker logs`.
- Monitored live container resource consumption using `docker stats`.
- Documented observability findings in Markdown for a professional GitHub portfolio.
