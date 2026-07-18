# Web Application Recon & Content Discovery

**Tools:** ffuf v2.1.0-dev, curl
**Target:** bWAPP training web server, 10.232.2.58
**Date:** July 2026

## Objective
Identify exposed directories, files, and service-fingerprint information on a lab web target using automated fuzzing and manual verification, following a black-box content-discovery methodology (OWASP WSTG-INFO series).

## Summary
Ran 300,000+ fuzzing requests across five ffuf sessions. Identified **8 findings** ranging from Informational to High severity. Overall risk rated **High**.

## Key Findings
- **End-of-life software stack** (High) — Apache 2.2.8, PHP 5.2.4, OpenSSL 0.9.8g, all unpatched since 2011
- **Exposed phpMyAdmin interface** (Medium) — publicly reachable database admin panel
- **Anomalous WebDAV endpoint** (Medium) — returned HTTP 200 for every path tested, a catch-all masking true content
- **No rate limiting observed** — sustained ~4,500 req/sec with zero throttling across 300,000+ requests

## What I Practiced
- Building and tuning ffuf fuzzing sessions (matcher configuration, multi-wordlist combinations)
- Distinguishing genuine findings from scanner noise by manually verifying with curl
- Recognizing anomalous server behavior as a signal worth deeper investigation
- Writing a full findings-based report with risk ratings and structured remediation

📄 [Full Report (PDF)](./report.pdf)

---
*This assessment was carried out in an isolated personal lab environment against an intentionally vulnerable practice system. No production systems or real organizations were involved.*
