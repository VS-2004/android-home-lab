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

## System Status Page

In addition to serving static HTML content, the web server exposes a lightweight system status page.

The status page displays:
- System uptime
- Disk usage
- Memory usage

The page is generated using standard Linux commands and served as static HTML.  
It automatically refreshes at regular intervals to reflect current system state.

### Access Example
```
http://<tablet-ip>:8080/status.html
```

### Design Note
The built-in Python HTTP server is used in static file mode.  
Dynamic script execution is intentionally avoided to keep the setup simple and secure.

