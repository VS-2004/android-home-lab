# SSH Security

This document describes how SSH access is secured for the Android Home Lab server.

---

## Default SSH Behavior

Initially, SSH access was configured using password-based authentication.
While acceptable for learning, password authentication is weaker than key-based access.

---

## SSH Key-Based Authentication

To improve security, SSH key-based authentication is used.

This approach:
- Eliminates password transmission
- Protects against brute-force attacks
- Is the standard practice for server administration

---

## Key Generation (Client Side)

SSH keys are generated on the macOS client:

```sh
ssh-keygen
```

Default options are used for simplicity.

---

## Key Deployment (Server Side)

The public key is copied to the Android tablet over SSH:

```sh
ssh-copy-id -p 8022 u0_aXXX@<tablet-ip>
```

After this step, SSH access no longer requires a password.

---

## Security Scope

This setup improves security while keeping the system beginner-friendly.
Advanced hardening techniques (firewalls, intrusion detection) are intentionally out of scope.

---

## Design Decision

The project prioritizes clarity and learning over maximum security.
The chosen SSH configuration reflects real-world best practices without unnecessary complexity.
