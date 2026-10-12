# Mission Reflection

Checking the host server's resources is important even when containers are running
perfectly because containers share the host's CPU, memory, disk, and network. A
container may look healthy, but if the host runs out of RAM or disk space, every
container on it is affected at once. By establishing a baseline with `free`, `df`,
and `top`, I learned what "normal" looks like so I can detect abnormalities before
they escalate into outages during a traffic surge.

If a user complains that they cannot log into a web application, `docker logs`
would help me investigate by showing the exact requests the container received. I
could look for status codes such as 401 Unauthorized, 403 Forbidden, or 500
Internal Server Error, and check the timestamps of failed login attempts. This
would tell me whether the issue is wrong credentials, a backend service that is
down, or an application bug, turning a vague complaint into a specific diagnosis.

The difference between logs and metrics is that logs capture discrete events,
while metrics capture numeric measurements over time. In Checkpoint 4, `docker
logs` showed me what happened, such as the 404 error when I requested
`hidden-admin-page`. In Checkpoint 5, `docker stats` showed me how much CPU and
memory the container was using. Logs answer "what happened?" while metrics answer
"how is it performing?".

Large enterprises monitor thousands of containers using platforms like Prometheus
for collecting metrics and Grafana for visualizing them in dashboards and alerts.
Instead of manually running `docker stats`, they use agents that automatically
scrape metrics from every container, store them in a time-series database, and
trigger alerts when thresholds are crossed.

My ability to troubleshoot Linux environments has improved. I now gather
evidence before making conclusions, starting from the host baseline, moving to
container logs and metrics, and finally documenting findings in a structured
Markdown report. This workflow is what a Site Reliability Engineer does in
production.
