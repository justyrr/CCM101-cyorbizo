# Laboratory 08: Cloud Security Engineer

## Mission Overview

In this laboratory, I explored how to secure a server using a firewall. I used Docker to run an Nginx web server and tested its accessibility through a local port. I also configured UFW (Uncomplicated Firewall) to control incoming and outgoing network traffic.

## Objectives

- Understand the role of firewalls in server security.
- Deploy a web server using Docker.
- Test web server connectivity using a local port.
- Configure default firewall policies.
- Allow specific ports for required services.
- Verify firewall rules and network access.

## Commands Used

```bash
docker run -d -p 8080:80 --name secure-web-app nginx
```

```bash
curl http://localhost:8080
```

```bash
sudo ufw allow 22/tcp
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
```

```bash
sudo ufw status verbose
sudo ufw allow 8080/tcp
sudo ufw status numbered
```

## Skills Learned

- Running an Nginx container using Docker.
- Checking web server connectivity through `curl`.
- Configuring firewall rules with UFW.
- Managing incoming and outgoing network traffic.
- Allowing specific ports for network services.
- Checking firewall status and configured rules.

## Conclusion

This laboratory helped me understand how firewalls improve server security by controlling network connections. I learned how to configure UFW rules, allow necessary ports, and check firewall settings. It also showed me the importance of securing services while keeping required applications accessible.

