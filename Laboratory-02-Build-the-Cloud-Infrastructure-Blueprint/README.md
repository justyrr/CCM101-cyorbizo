
# Laboratory Activity 2: Build the Cloud Infrastructure Blueprint

## Student Information
- **Name**: [Your Name]
- **Course**: CCM101 - Cloud Computing
- **Section**: [Your Section]
- **Date**: [Current Date]
- **Instructor**: [Instructor's Name]

---

## Mission Overview

This laboratory activity simulates the planning phase of a cloud deployment. As a cloud engineer at **CloudNova Technologies**, I was tasked with investigating cloud infrastructure components using a Linux environment, documenting my findings, and creating professional technical documentation for a client.

The mission involved investigating a live Linux server in the **KillerCoda Playground**, identifying compute, storage, networking, and operating system components, and preparing a **Cloud Infrastructure Assessment Report** before any servers are deployed. This exercise mirrors real-world cloud engineering practices where understanding infrastructure is critical before deployment.

---

## Objectives

At the end of this laboratory activity, I was able to:

- [x] Investigate a Linux server in a cloud environment
- [x] Identify and explain the major components of cloud infrastructure
- [x] Compare equivalent cloud services from AWS, Microsoft Azure, and Google Cloud Platform
- [x] Create a simple cloud infrastructure diagram
- [x] Produce organized technical documentation using Markdown
- [x] Maintain a professional GitHub Cloud Computing Portfolio

---

## Cloud Infrastructure Components Identified

Based on the investigation of the Linux environment, the following cloud infrastructure components were identified:

| Component | Description | KillerCoda Example | Cloud Equivalent |
|-----------|-------------|-------------------|------------------|
| **Compute** | Processing power (CPU) and memory (RAM) for running applications | 1 vCPU @ 2.0GHz, 1.9GB RAM | AWS EC2, Azure VM, GCP Compute Engine |
| **Storage** | Persistent data storage for files and applications | 19GB root disk, tmpfs, swap | AWS EBS/S3, Azure Disk/Blob, GCP Persistent Disk/Cloud Storage |
| **Networking** | Connectivity and communication between resources | IP: 172.30.1.2, enp1s0 interface | AWS VPC, Azure VNet, GCP VPC |
| **Operating System** | Manages hardware and provides platform for applications | Ubuntu 24.04.4 LTS (Kernel 6.8.0) | AWS AMI, Azure Image, GCP Image |

---

## Tools Used

| Tool | Purpose |
|------|---------|
| **KillerCoda Playground** | Linux terminal environment for system investigation |
| **GitHub** | Version control and portfolio hosting |
| **Draw.io** | Cloud infrastructure diagram creation |
| **Linux Commands** | System investigation and resource identification |
| **Markdown** | Technical documentation formatting |
| **AWS Documentation** | Researching AWS cloud services |
| **Azure Documentation** | Researching Azure cloud services |
| **GCP Documentation** | Researching Google Cloud services |

---

## Linux Commands Executed

### System Information Commands

```bash
# Operating System Information
uname -a                    # Complete system information
uname -r                    # Kernel version only
cat /etc/os-release        # OS distribution details

# Hardware Information
lscpu                      # CPU specifications
free -h                    # RAM usage in human-readable format
df -h                      # Disk usage and mounted filesystems

# Network Information
hostname                   # Server hostname
hostname -I               # IP addresses only
ip a                       # All network interfaces and IPs
