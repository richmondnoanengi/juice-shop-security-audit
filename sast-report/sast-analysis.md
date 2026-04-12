Title: Static Application Security Testing (SAST) using CodeQL

Aim:
To identify security vulnerabilities in the project using CodeQL.

Tools Used:
- GitHub CodeQL

Procedure:
- CodeQL was enabled in the GitHub repository
- The default configuration was selected
- The analysis was executed automatically on the main branch

Findings:

1. Vulnerability: Template Object Injection
   Severity: Critical
   File: routes/dataErasure.ts (Line 87)
   Description:
   This vulnerability allows attackers to inject malicious templates which may lead to code execution.

2. Vulnerability: Polynomial regular expression used on uncontrolled data
   Severity: High
   File: routes/profileImageUrlUpload.ts (Line 20)
   Description:
 Certain regular expressions can take excessive time to process specific inputs, leading to performance issues or potential Denial of Service (DoS) attacks.

3. Vulnerability: Information exposure through a stack trace
   Severity: Medium
   File: routes/likeProductReviews.ts (Line 56)
   Description:
Stack traces in error messages can reveal internal application details, which may help attackers understand system behavior.

Conclusion:
The CodeQL scan identified multiple vulnerabilities, including critical issues that could compromise application security. Proper validation and secure coding practices are required to mitigate these risks.