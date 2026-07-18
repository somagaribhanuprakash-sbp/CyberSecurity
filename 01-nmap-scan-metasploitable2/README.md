# Nmap Scan — Metasploitable2

**Tools:** Nmap 7.99
**Target:** Metasploitable2 (isolated lab VM), 192.168.44.132
**Date:** July 2026

## Objective
Perform active network reconnaissance and service enumeration against a lab VM using Nmap, practicing host discovery, port scanning, version detection, OS fingerprinting, and NSE scripting.

## Summary
Ran `nmap -A` against the target, identifying **23 open ports** out of 1000 scanned, with OS fingerprinting placing the host on the Linux 2.6.x kernel line.

## Key Findings
- **Pre-configured bindshell** (port 1524) — Nmap explicitly fingerprinted this as a "Metasploitable root shell," a deliberately planted backdoor
- **Anonymous FTP** (port 21) — vsftpd 2.3.4, a version historically associated with a known backdoor
- **Plaintext protocols** — Telnet, rlogin, rexec all transmit credentials unencrypted
- **Outdated service stack** — Apache 2.2.8, Samba 3.0.20, MySQL 5.0.51a, and more, all predating 2011

## What I Practiced
- Structuring and interpreting an aggressive Nmap scan (-A) covering OS/version/script detection
- Reading service banners to identify outdated or vulnerable software versions
- Recognizing indicators of deliberately planted backdoors vs. genuine misconfigurations
- Prioritizing findings by exploitability to plan a logical next testing phase

📄 [Full Report (PDF)](./report.pdf)

---
*This assessment was carried out in an isolated personal lab environment against an intentionally vulnerable practice system. No production systems or real organizations were involved.*

