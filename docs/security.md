Open-source software development (SEN 406) 
Topic: Security Auditing & Vulnerability Management
By Group 9
211212115 Ibanga NoaNengi Richmond(Team lead)
211212013 Uchemefuna Chiwete Uchemefuna
210001029 Okafor klinsman sonikechukwu
211212039 Adinigwe Onyedikachi Chinaza
211212087 Charles-Eigbedion Eromosele
211212045 Abubakar Kamaludeen Barde
211212043 Huzaifa jamilu Adamu
201500032 Ezugwu Nnamdi
211212154 Elvis Sibigem

 
1.	 Aim of Project
•	To identify, assess, and remediate security vulnerabilities in an open-source project using various security tools.
2.	 Tools used 
•	Git & GitHub
•	VS Code
•	npm audit
•	TruffleHog
•	GitHub CodeQL
3.	Procedure
	Step 1: Project Setup
•	Cloned Juice Shop repository
•	Set up GitHub repository
•	Installed dependencies
	Step 2: Static Application Security Testing (SAST)
•	Enabled CodeQL in GitHub
•	Ran automated scan
•	Identified vulnerabilities
	Step 3: Dependency Scanning\
•	-Ran npm audit
•	Identified vulnerable packages and CVEs


	Step 4: Secret Detection
•	- Used TruffleHog to scan repository
•	- Identified exposed secrets (JWT, private key)
4.	Observations 
•	CodeQL detected multiple vulnerabilities (84 alerts)
•	npm audit revealed dependency vulnerabilities
•	TruffleHog detected JWT tokens and a private key
•	Some vulnerabilities were critical and required attention
5.	Challenges Encountered
•	Initial Git errors (merge conflicts, push issues)
•	Tool installation issues (npm, trufflehog)
•	Understanding scan outputs
6.	Solutions Applied
•	Resolved Git conflicts using pull and merge
•	 Missing tools installed (Node.js, TruffleHog)
•	Followed proper folder structure for organization
7.	Conclusion 
•	The practical successfully demonstrated how security tools can be used to identify vulnerabilities in open-source projects. Proper security practices are essential to prevent exploitation.
8.	Repository link and screenshots 
•	Github repository link: https://github.com/richmondnoanengi/juice-shop-security-audit
 Images 
   
Dependency scan images 1-3


   
Sast-Report File images 1-3





    
Secret- scan images1-4
