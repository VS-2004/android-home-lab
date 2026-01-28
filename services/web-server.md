# Lightweight Web Server

This service demonstrates hosting a simple HTTP server on an Android-based headless system using Termux.

## Technology Used
- Python built-in HTTP server
- Termux (Linux user space on Android)

## Port
- 8080

## Setup Steps
1. Install Python in Termux
2. Create a simple HTML file
3. Start the server using:
   ```sh
   python -m http.server 8080
   ```
4. Access the service from another device on the same network

## Purpose
- Validate client–server communication
- Confirm inbound network access to the tablet
- Demonstrate service hosting on constrained hardware

## Access Example
```text
http://<tablet-ip>:8080
```

## Notes
- Service is intended for local network testing only
- Server runs in the foreground and stops with Ctrl + C
- No production hardening applied
