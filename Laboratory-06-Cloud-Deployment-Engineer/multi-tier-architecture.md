# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A two-tier architecture is a software architecture pattern where an application is divided into two main layers: the **Web/Application Tier** (frontend) and the **Database Tier** (backend). Each tier runs independently and communicates with the other over a network. In a containerized environment, each tier is typically deployed as its own container, allowing them to be managed, scaled, and updated separately.

## The Web/Application Tier

The Web/Application Tier is the layer that users interact with directly. Its role includes:

- Serving the user interface (HTML, CSS, JavaScript) to the browser
- Handling HTTP/HTTPS requests from clients
- Processing application logic and business rules
- Communicating with the database tier to fetch or store data
- Managing user sessions and authentication

In our deployment, **Nextcloud** acts as the Web/Application Tier. It provides the private cloud storage interface that users see in their browser.

## The Database Tier

The Database Tier is the layer responsible for storing and managing data. Its role includes:

- Storing persistent data such as user accounts, passwords, and file metadata
- Providing structured query capabilities (SQL)
- Ensuring data integrity, consistency, and security
- Handling backups and recovery operations

In our deployment, **MariaDB** acts as the Database Tier. It stores all the information Nextcloud needs to function, such as user credentials and file records.

## Why Separate Them?

It is better to have the web server and the database in two separate containers rather than packing them both into one because:

1. **Isolation and Security** — If one tier is compromised, the other remains protected. A vulnerability in the web server does not automatically expose the database.
2. **Scalability** — Each tier can be scaled independently based on demand. For example, you can run multiple web containers while keeping a single database container.
3. **Maintainability** — Updates, patches, and configuration changes can be applied to one tier without affecting the other, reducing downtime and risk.
