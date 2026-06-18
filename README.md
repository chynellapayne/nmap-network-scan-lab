# Nmap Network Scan Lab 🔍

## Overview
Performed network reconnaissance and port scanning using Nmap 
in a Kali Linux home lab environment running in VirtualBox.
This lab was completed as part of building hands-on cybersecurity 
skills for a SOC Analyst career path.

---

## Tools Used
- Nmap 7.98
- Kali Linux (VirtualBox)

---

## Commands Run

| Command | Purpose |
|---------|---------|
| `nmap --version` | Verified Nmap installation |
| `ip addr` | Identified Kali VM IP address |
| `nmap localhost` | Scanned local machine for open ports |
| `nmap -v localhost` | Verbose scan of localhost |
| `nmap <subnet>` | Subnet scan to discover active hosts |

---

## Results Summary

### Localhost Scan
- Scanned 1000 ports on localhost (127.0.0.1)
- All ports in ignored/closed state — expected result for a 
  clean Kali VM with no services running

### Subnet Scan
Discovered 3 active hosts with the following open ports:

| Port | Service | Notes |
|------|---------|-------|
| 53/tcp | DNS (domain) | Name resolution service |
| 135/tcp | MSRPC | Remote procedure call |
| 445/tcp | Microsoft-DS (SMB) | File sharing — high value target |
| 5357/tcp | WSDAPI | Web services discovery |
| 5432/tcp | PostgreSQL | Database service exposed |

---

## What I Learned
- How to verify and run Nmap from the Kali Linux terminal
- How to identify my VM's IP address using `ip addr`
- How to perform localhost and subnet scans
- How to interpret open ports and map them to services
- Why exposed services like SMB (445) and PostgreSQL (5432) 
  are critical findings in a real SOC environment

---

## Screenshots
See images below for documented lab evidence.

---

## References
- [Nmap Official Documentation](https://nmap.org/docs.html)
- [Kali Linux](https://www.kali.org)
