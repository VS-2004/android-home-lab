# Architecture Overview

This document describes the high-level architecture of the Android Home Lab project.

## Components

### Control Machine (macOS)
- Used to manage the server remotely
- SSH client
- GitHub for documentation and version control

### Server Device (Android Tablet)
- Runs a Linux-like environment
- Operates in headless mode
- Hosts lightweight services

## Network Design
- Local network only
- No public internet exposure
- Access restricted to trusted devices

## Design Philosophy
- Simplicity over performance
- Learning over production-readiness
- Minimal services, clearly documented
