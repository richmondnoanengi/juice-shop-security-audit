# Dependency Scanning Report

## Overview
This report presents vulnerabilities identified using npm audit on the Juice Shop project.

---

## Vulnerabilities Found

### 1. lodash
- **CVE ID:** Multiple (Prototype Pollution, Command Injection)
- **Severity:** Critical
- **Affected Version:** <= 4.17.23
- **Issue:** Allows prototype pollution and command injection attacks
- **Fix:** Run `npm audit fix --force` or upgrade to latest version

---

### 2. crypto-js
- **CVE ID:** GHSA-xwcq-pm8m-c4vf
- **Severity:** Critical
- **Affected Version:** < 4.2.0
- **Issue:** Weak cryptographic implementation (PBKDF2 significantly weaker than standard)
- **Fix:** Upgrade to version 4.2.0 or later

---

### 3. vm2
- **CVE ID:** Multiple Sandbox Escape Vulnerabilities
- **Severity:** Critical
- **Affected Version:** <= 3.10.1
- **Issue:** Attackers can escape sandbox environment and execute malicious code
- **Fix:** Upgrade dependency or replace with safer alternative

---

## Summary
A total of **58 vulnerabilities** were identified:
- 6 Low
- 11 Moderate
- 34 High
- 7 Critical

Most vulnerabilities are due to outdated and insecure dependencies. Updating packages and reviewing transitive dependencies is recommended.