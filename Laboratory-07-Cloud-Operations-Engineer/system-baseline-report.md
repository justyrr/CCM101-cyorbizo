## Host System Information

**Date of baseline:** October 12, 2026
**Environment:** KillerCoda Ubuntu 24.04 Playground

## Memory (RAM)

Command used: `free -h`

- **Total RAM:** 1.9Gi
- **Used:** 416Mi
- **Free:** 1.1Gi
- **Available:** 1.5Gi

## Disk Storage

Command used: `df -h /`

- **Total Storage (root filesystem):** 19G
- **Used:** 5.5G
- **Available:** 13G
- **Use%:** 30%

## Why Check Disk Space Before a Traffic Surge?

Checking disk space is important before a massive traffic surge because web servers
continuously write logs, cache, and temporary files, and running out of disk space
can cause the application to crash or fail to serve requests even when CPU and RAM
are still healthy.
