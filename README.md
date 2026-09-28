# cowrie-honeypot-lab
A cybersecurity lab project focused on deploying, testing, and analyzing an isolated Cowrie SSH honeypot.

## Project Status

**Phase 1 complete:** Cowrie has been installed and validated locally using simulated SSH activity from the host system.

## Technologies

- VMware Workstation Pro
- Ubuntu Server
- Cowrie
- Python
- Linux command line
- JSON logging

## Project Goals

- Safely simulate and monitor SSH activity
- Analyze authentication attempts and shell commands
- Practice security monitoring and incident investigation
- Create a documented blue-team portfolio project

## Documentation

- [Setup Notes](docs/setup-notes.md)
- [Security Decisions](docs/security-decisions.md)
- [Sanitized Log Samples](sample-logs/README.md)
- [Screenshots](screenshots/README.md)

## Current Architecture

Cowrie runs as a dedicated non-root user inside an Ubuntu Server VM using VMware NAT networking. The legitimate SSH service remains on port 22, while Cowrie listens on port 2222.

## Next Steps

- Build a separate testing VM
- Generate controlled reconnaissance and authentication activity
- Analyze Cowrie’s JSON logs
- Map findings to MITRE ATT&CK
- Create a findings report

> This project is currently limited to a controlled virtual lab. Sensitive data, raw credentials, captured files, and unsanitized logs are not published.
