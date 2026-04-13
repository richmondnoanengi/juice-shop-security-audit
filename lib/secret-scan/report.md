# Secret Detection Report

# Aim
To identify sensitive information such as API keys, tokens, and private keys exposed in the repository using secret scanning tools.



# Tool Used
- TruffleHog


## Procedure
- The repository was scanned using TruffleHog.
- Command used:

- The tool analyzed commit history and files for exposed secrets.

---

## Findings

### 1. JWT Token Exposure
- **Type:** JSON Web Token (JWT)
- **Severity:** Medium
- **File:** `test/api/userApiSpec.ts` (Line 302)
- **Description:**  
A JWT token was found in the codebase, which may expose authentication data if misused.

---

### 2. JWT Token Exposure
- **Type:** JSON Web Token (JWT)
- **Severity:** Medium
- **File:** `test/server/currentUserSpec.ts` (Line 33)
- **Description:**  
Another JWT token was detected, indicating potential exposure of sensitive authentication information.

---

### 3. Private Key Exposure
- **Type:** RSA Private Key
- **Severity:** Critical
- **File:** `lib/insecurity.ts` (Line 23)
- **Description:**  
A private key was found in the repository. Exposure of private keys can allow attackers to decrypt sensitive data or impersonate the system.

---

## Remediation
- Remove sensitive data from the repository
- Rotate or revoke exposed keys immediately
- Store secrets securely using environment variables (.env files)
- Use secret management tools

---

## Conclusion
The scan revealed multiple sensitive items, including JWT tokens and a private key. These findings highlight the importance of secure handling of secrets in software development.

---