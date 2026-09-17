# Docker Deployment

## Container Lifecycle

### 1. List running containers
```bash
docker ps
```
Shows all currently running containers with their IDs, names, ports, and status.

### 2. Stop the running container
```bash
docker stop my-nginx
```
Gracefully stops the running Nginx container by sending a SIGTERM signal.

### 3. Verify it is stopped
```bash
docker ps -a
```
Lists all containers including stopped ones, confirming the container is no longer running.

### 4. Remove the container completely
```bash
docker rm my-nginx
```
Permanently deletes the stopped container and its writable layer from the system.
