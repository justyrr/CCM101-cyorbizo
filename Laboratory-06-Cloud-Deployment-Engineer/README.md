## Mission Overview

In this mission, I transitioned from manually deploying single containers to deploying a multi-tier application using **Docker Compose**. I defined a two-tier architecture consisting of a **Nextcloud** web/application container and a **MariaDB** database container, deployed the entire stack with a single command, accessed the Nextcloud web interface, and then tore down the infrastructure gracefully.

This mission demonstrated the power of **Infrastructure as Code (IaC)** — a core principle in modern cloud engineering.

## Objectives

- Explain the concept of a multi-tier application architecture
- Understand the purpose and structure of a `docker-compose.yml` file
- Use a Linux command-line text editor (`nano`) to create configuration files
- Deploy a multi-container application (Nextcloud + MariaDB) using Docker Compose
- Document deployment procedures and IaC principles using Markdown
- Continue expanding my professional GitHub Cloud Computing Portfolio

## Commands Executed

```
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Skills Learned

- Writing a valid YAML configuration file for Docker Compose
- Understanding service-to-service communication via Docker's internal DNS
- Using environment variables to configure containers without hardcoding values
- Deploying and tearing down multi-container stacks as a single unit
- Documenting infrastructure code for other engineers
- Applying Infrastructure as Code (IaC) principles in a real deployment scenario
