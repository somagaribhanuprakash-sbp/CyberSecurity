# CyberSecurity
Hands-on cybersecurity lab reports — VAPT, network scanning, and web app testing
# Cybersecurity — S Bhanu Prakash

Cybersecurity enthusiast focused on ethical hacking, vulnerability assessment, and penetration testing. This repo documents hands-on lab work performed in isolated, personal virtual environments as part of independent skill-building and internship coursework.

**All testing was conducted against intentionally vulnerable practice systems (Metasploitable2, bWAPP/bee-box) in isolated lab networks. No production systems, third-party assets, or real organizations were involved.**

## Certifications & Credentials
- Fortinet Certified Fundamentals in Cybersecurity — Fortinet Training Institute
- Ethical Hacking Virtual Internship (8 weeks) — AICTE EduSkills Academy
- Cybersecurity Job Simulation — Deloitte (via Forage)
- Cybersecurity Job Simulation — Mastercard (via Forage)
- Currently in progress: Web Exploit Hunting & Bug Bounty Virtual Internship (EduSkills), Ethical Hacking (Cisco)

## Projects

| # | Project | Tools | Key Finding |
|---|---------|-------|--------------|
| 01 | [Nmap Scan — Metasploitable2](./01-nmap-scan-metasploitable2) | Nmap | 23 open ports/services enumerated, incl. planted bindshell backdoor |
| 02 | [Nessus Vulnerability Assessment](./02-nessus-vulnerability-assessment) | Nessus Essentials | 49 findings triaged; UnrealIRCd backdoor (CVE-2010-2075, CVSS 10.0) |
| 03 | [Burp Suite Web Crawling](./03-burp-suite-web-crawling) | Burp Suite CE | Full Site Map of bWAPP app built via manual proxy crawling |
| 04 | [Black-Box VAPT — bWAPP bee-box](./04-bwapp-beebox-vapt) | Nuclei, snmpwalk, enum4linux | Unauthenticated DistCC RCE (CVE-2004-2687); SNMP full system disclosure |
| 05 | [Web App Recon & Content Discovery](./05-web-app-recon-ffuf) | ffuf, curl | 300,000+ requests fuzzed; exposed phpMyAdmin, EOL software stack |

## About Me
Building toward a career in SOC analysis / VAPT. Open to internship opportunities — feel free to connect on [LinkedIn](#).
