# Firewall Configuration

## 1. Allowing SSH Connections

The first step was to create a firewall rule for SSH. This allows remote access to the server through TCP port 22 when needed.

```bash
sudo ufw allow 22/tcp
```

## 2. Configuring Default Firewall Rules

I set UFW to block incoming connections by default while permitting outgoing traffic. After configuring the policies, I enabled the firewall and reviewed its current settings.

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose
```

These settings help limit unwanted access while allowing the server to communicate with other systems.

## 3. Allowing Access to the Web Server

The Nginx application was mapped to port 8080. I added a firewall rule to permit TCP traffic on this port so the web application could be accessed when the network and other security settings allow it.

```bash
sudo ufw allow 8080/tcp
sudo ufw status numbered
```

The numbered status output helps identify the active firewall rules and makes them easier to review.

## 4. Why SSH Must Be Allowed

SSH is important for managing a server remotely. Allowing port 22 before activating UFW helps prevent losing remote access when the firewall starts blocking incoming connections.

However, SSH should only be accessible from trusted networks when possible. Firewall rules must be reviewed carefully to maintain access without exposing unnecessary services.

## Conclusion

Through this configuration, I learned how to manage network access using UFW. Setting default policies, allowing specific ports, and checking active rules are important steps in protecting a server. This activity also helped me understand the balance between server security and accessibility.

