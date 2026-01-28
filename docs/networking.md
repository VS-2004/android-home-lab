# Networking Notes

This document outlines basic networking concepts used in the Android Home Lab project.

## Local Network Only
The server is designed to operate only within a trusted local network.

## Client–Server Model
- macOS acts as the client
- Android tablet acts as the server

## SSH Access
Secure Shell (SSH) is used to remotely access the tablet.

## IP Addressing
The server is accessed using its local IP address assigned by the router.

## Security Considerations
- No public port exposure
- Key-based SSH authentication
- Minimal services running

## Network Constraints Observed

While testing, mobile hotspot connections were found to block device-to-device communication. SSH and HTTP services were only reachable when both devices were connected to the same local network or via USB tethering.

This highlighted practical limitations of hotspot-based networking and the importance of LAN access for home-lab setups.
