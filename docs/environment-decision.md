# Linux Environment Decision

## Problem
Android does not natively behave like a Linux server. To run services such as SSH, monitoring scripts, and a web server, a Linux-like environment is required.

## Options Considered

### Termux
- No root required
- Easy to install and reset
- Large package ecosystem
- Strong community support

### proot-distro
- Provides a full Linux distribution
- More realistic environment
- Slight performance and complexity overhead

### Root / chroot-based setups
- High risk
- Requires rooting the device
- Not suitable for a learning-focused project

## Decision
The project will use **Termux** as the primary Linux environment.

## Reasoning
Termux offers the best balance between simplicity, stability, and learning value. It allows experimentation without risking the device and aligns well with the educational goals of this project.

## Future Considerations
A proot-based Linux distribution may be explored later as an extension of this project.
