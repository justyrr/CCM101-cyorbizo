# Laboratory 04 - Cloud-Native Engineer

## Mission Overview

This laboratory activity focuses on understanding the shift from traditional virtualization to containerization. Using the KillerCoda Playground, I stepped into the shoes of a Cloud-Native Engineer by researching the differences between VMs and containers, executing Docker commands, and deploying a live containerized Nginx web server.

## Objectives

- Differentiate between traditional Virtual Machines (VMs) and Containers
- Access a Docker-enabled cloud environment using KillerCoda
- Execute fundamental Docker CLI commands
- Pull, run, manage, and terminate a containerized application (Nginx)
- Create professional technical documentation of container operations using Markdown
- Continue developing a well-organized GitHub Cloud Computing Portfolio

## Docker Commands Executed

### Checkpoint 3 - Verify Docker Installation
```bash
docker --version
docker info
systemctl status docker
```

### Checkpoint 4 - Deploy Nginx Container
```bash
docker pull nginx
docker run -d -p 8080:80 --name my-nginx nginx
curl http://localhost:8080
```

### Checkpoint 5 - Container Lifecycle
```bash
docker ps
docker stop my-nginx
docker ps -a
docker rm my-nginx
```

## Skills Learned

- Understanding the architectural differences between VMs and containers
- Using the Docker CLI to manage images and containers
- Pulling images from Docker Hub
- Running containers in detached mode with port mapping
- Managing the container lifecycle (list, stop, verify, remove)
- Writing technical documentation in Markdown
- Maintaining a structured GitHub portfolio

## Challenges Encountered

- Understanding how port mapping works between host and container
- Remembering the different Docker CLI flags and their purposes
- Adjusting to the concept of ephemeral containers versus persistent VMs
