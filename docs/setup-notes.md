# Setup Notes

## Environment

- VMware Workstation Pro
- Ubuntu Server 26.04.1 LTS
- VMware NAT networking
- Cowrie SSH honeypot
- Administrative SSH: TCP port 22
- Cowrie SSH: TCP port 2222

## Completed Work

1. Created and updated the Ubuntu Server VM.
2. Created a clean VMware snapshot.
3. Installed Cowrie dependencies.
4. Created a dedicated non-root Cowrie account.
5. Installed Cowrie in a Python virtual environment.
6. Started Cowrie and verified port 2222.
7. Tested the honeypot locally.
8. Tested it remotely from the Windows host.
9. Confirmed that authentication attempts and commands were logged.

## Validation Commands

```bash
cowrie status
ss -ltn | grep 2222
hostname -I
tail -n 30 ~/my-honeypot/var/log/cowrie/cowrie.log
