# Docker Compose Guide

## Overview

This guide explains the `docker-compose.yml` file used to deploy the Nextcloud + MariaDB multi-container stack. It breaks down each section so another engineer can understand the purpose and behavior of the configuration.

## The `services:` Block

The `services:` block is the core of a Docker Compose file. It defines each container that makes up the application stack. In our file, we have two services:

- **`database`** — runs the MariaDB 10.6 image, which serves as the backend database.
- **`app`** — runs the Nextcloud image, which serves as the frontend web application.

Each service specifies:

- **`image`** — the Docker image to pull from Docker Hub
- **`environment`** — environment variables passed into the container
- **`ports`** — port mappings between the host and the container

Docker Compose reads this block and automatically creates a private network so the services can communicate with each other by service name.

## How the Nextcloud Container Finds the Database

The Nextcloud container knows how to find the database container through the **`MYSQL_HOST`** environment variable:

```
environment:
  - MYSQL_HOST=database
```

The value `database` matches the **service name** defined in the `services:` block. Docker Compose automatically creates an internal DNS entry for each service, so the hostname `database` resolves to the MariaDB container's IP address on the shared network. This means the Nextcloud container can connect to the database without needing to know its actual IP address.

## `docker run` vs `docker-compose up -d`

| Aspect | `docker run` | `docker-compose up -d` |
|--------|--------------|------------------------|
| Scope | Deploys a single container | Deploys an entire multi-container stack |
| Configuration | Passed as command-line flags | Defined in a YAML file |
| Networking | Manual network setup required | Automatic shared network created |
| Reproducibility | Hard to reproduce exactly | Fully reproducible from the file |
| Management | Each container managed separately | All containers managed as one unit |
| Teardown | `docker stop` + `docker rm` per container | `docker-compose down` removes everything |

`docker run` is useful for quick, single-container tasks. `docker-compose up -d` is the standard approach for multi-tier applications because it treats the entire stack as a single, version-controlled unit — this is the essence of **Infrastructure as Code (IaC)**.
