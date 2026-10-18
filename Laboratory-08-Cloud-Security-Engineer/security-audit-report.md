# Security Audit Report

## 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege means providing users and services with only the permissions they need to perform their tasks. Applying this practice helps reduce the chances of unauthorized access and protects sensitive information. It is important to review permissions regularly to ensure that unnecessary access is removed.

## 2. Attack Surface Analysis

The attack surface refers to the different points where a server may be exposed to security threats. Examples include open network ports, running services, and applications accessible through a network. Reducing the attack surface by disabling unused services and restricting unnecessary ports can help minimize possible vulnerabilities.

## 3. Default Deny Firewall Policy

The Default Deny policy prevents incoming network connections unless specific firewall rules permit them. This approach provides better control over which services can communicate with the server. By allowing only required connections through UFW, unnecessary network access can be restricted and the server's overall security can be improved.

## Conclusion

The security audit helped me understand the importance of limiting access, reducing potential entry points, and applying proper firewall policies. These practices work together to protect servers from unnecessary exposure and unauthorized connections. Regularly reviewing firewall rules and running services is also important to maintain a more secure system.

