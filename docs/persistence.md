# Service Persistence

By default, services started in Termux run only while the terminal session is active.
If the SSH session disconnects or the command is stopped, the service also stops.

This document explains how basic persistence is handled in this project.

---

## Current Behavior

- Web server is started manually using Python
- Service runs in the foreground
- Stopping the process stops the service

This behavior is acceptable for learning and testing.

---

## Background Execution

To allow a service to continue running after disconnecting from SSH, the project uses background execution.

Example:

```sh
nohup python -m http.server 8080 > server.log 2>&1 &
```

This allows the service to:
- Continue running after logout
- Write output to a log file
- Be stopped manually when needed

---

## Stopping the Service

To stop the running web server:

```sh
pkill -f http.server
```

---

## Design Decision

Advanced persistence options (system services, auto-start on boot) are intentionally avoided at this stage to keep the project simple and beginner-friendly.

Future improvements may include automated startup using Termux add-ons.
