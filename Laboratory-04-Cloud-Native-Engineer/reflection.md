# Mission Reflection

Working with Docker in this laboratory activity gave me a clear understanding of how containerization differs from traditional virtualization. When it comes to boot time and setup, a Docker container is dramatically faster than installing an operating system on a Virtual Machine. A VM requires installing a full guest OS, which can take 15 to 30 minutes, plus configuration time. A container, on the other hand, starts in seconds because it shares the host OS kernel and only packages the application with its dependencies. During this lab, pulling the Nginx image and running the container took less than a minute in total.

Port mapping is also an important concept I learned. When running a web server inside a container, the Nginx server listens on port 80 inside the container, but this port is not accessible from the host by default because containers have their own isolated network namespace. The `-p 8080:80` flag maps port 8080 on the host machine to port 80 inside the container, allowing external access to the web server through `http://localhost:8080`.

I also learned what happens when a container is removed. Using the `docker rm` command permanently deletes the container and its writable layer, meaning any data stored inside the container's filesystem is lost. This is why best practices recommend using volumes or bind mounts for persistent data that needs to survive container removal.

Containerization also changes how developers and IT operations teams work together. It provides consistent environments from development to production, eliminating "it works on my machine" problems since containers run identically anywhere. This shared toolset bridges the gap between development and operations, enabling faster release cycles and more reliable deployments.

Finally, my GitHub portfolio continues to evolve into a comprehensive showcase of my cloud computing skills. Starting from basic cloud concepts in Laboratory 01, progressing through infrastructure blueprints and multi-cloud exploration, and now demonstrating containerization expertise, each laboratory adds practical, hands-on evidence of my growing capabilities as a cloud-native engineer.
