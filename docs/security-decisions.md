# Security Decisions

## NAT Networking

The honeypot VM uses VMware NAT networking. This allows the VM to receive controlled test traffic from the host and other VMware guests without directly exposing it to the public internet or physical local network.

## Dedicated Service Account

Cowrie runs under a dedicated `cowrie` account rather than `root`. This follows the principle of least privilege and limits the permissions available to the honeypot process.

## Python Virtual Environment

Cowrie was installed inside a Python virtual environment. This isolates Cowrie's packages from Ubuntu's system-level Python packages and reduces dependency conflicts.

## Separate SSH Ports

The legitimate Ubuntu SSH service remains on TCP port 22, while Cowrie listens on TCP port 2222. This prevents the honeypot from interfering with administrative access during development.

## Controlled Testing

Initial tests were performed locally and from the Windows host using fake usernames, passwords, and commands. The honeypot has not yet been exposed to public internet traffic.

## VMware Snapshot

A clean snapshot was created before Cowrie was installed. This provides a recovery point if the installation or configuration becomes damaged.

## Data Sanitization

Raw Cowrie logs may contain passwords, IP addresses, session identifiers, and captured files. Only selected and sanitized examples will be published.

## Current Limitations

The current deployment is a controlled local lab. Its results demonstrate successful installation, event capture, and log analysis, but do not represent genuine internet attack activity.
