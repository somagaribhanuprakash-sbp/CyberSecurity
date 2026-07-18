# Burp Suite Web Crawling — bWAPP

**Tools:** Burp Suite Community Edition v2026.4.3
**Target:** bWAPP on bee-box VM
**Date:** July 2026

## Objective
Map the structure of a vulnerable web application (bWAPP) using Burp Suite as an intercepting proxy, ahead of vulnerability analysis.

## Summary
Configured Burp's proxy listener, routed browser traffic through it, and manually crawled the target application to build a complete, scoped Site Map — using Community Edition's manual workflow since automated crawling requires Burp Professional.

## Key Steps
- Configured proxy listener (127.0.0.1:8080) and confirmed traffic interception
- Manually browsed the app (login, portal, training, password reset, user management) to populate the Site Map
- Defined target scope and filtered out-of-scope traffic to keep the map clean
- Identified full directory structure: `/bWAPP/`, `/bWAPP/js/`, `/bWAPP/stylesheets/`, `/phpmyadmin/`

## What I Practiced
- Configuring Burp Suite as an intercepting proxy and routing browser traffic through it
- Defining and applying target scope to keep analysis focused
- Building a Site Map organically through manual crawling
- Reading captured requests/responses to understand an application's structure before testing it

📄 [Full Report (PDF)](./report.pdf)

---
*This assessment was carried out in an isolated personal lab environment against an intentionally vulnerable practice system. No production systems or real organizations were involved.*
