# Black-Box VAPT — bWAPP bee-box

**Tools:** Nuclei v3.11.0, snmpwalk, smbclient, enum4linux
**Target:** bWAPP bee-box (isolated lab VM), 192.168.1.17
**Date:** July 2026

## Objective
Perform a black-box vulnerability assessment and penetration test simulating an unauthenticated attacker with network access, combining automated scanning with manual enumeration.

## Summary
Combined Nuclei's full template scan (10,447 templates) with SNMP and SMB/NetBIOS enumeration. Confirmed **48 distinct findings**, including two Critical issues. Overall risk rated **Critical**.

## Key Findings
- **Unauthenticated DistCC RCE** (CVE-2004-2687, CVSS 9.8 est.) — arbitrary code execution as root
- **SNMP Community String Disclosure** — default "public" string exposed the full process table, confirming DistCC and VNC run as root
- **Samba 3.0.28a with anonymous SMB access** — unauthenticated share and user enumeration via RID cycling
- **Outdated Apache/PHP/OpenSSL stack**, weak SSH crypto configuration, exposed SQLite web manager

## What I Practiced
- Running and interpreting large-scale template-based scanning with Nuclei
- Using snmpwalk and enum4linux/smbclient for protocol-specific enumeration
- Correlating findings across tools to build a fuller picture of impact
- Structuring a full VAPT report: executive summary, methodology, risk-rated findings, remediation

📄 [Full Report (PDF)](./report.pdf)

---
*This assessment was carried out in an isolated personal lab environment against an intentionally vulnerable practice system. No production systems or real organizations were involved.*
