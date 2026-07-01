Penetration Testing & Vulnerability Assessment Report (VAPT)

👤 Author Deepika P

B.E. Computer Science and Design


Project Overview

This project presents a structured Vulnerability Assessment and Penetration Testing (VAPT) exercise conducted on a controlled virtual machine environment. The objective was to analyze system security, identify vulnerabilities across network and application layers, and document findings with remediation strategies.

Objectives
Perform reconnaissance and network-level analysis of the target system

Identify exposed services and potential vulnerabilities

Evaluate web application security weaknesses

Document findings with evidence and structured reporting

Recommend mitigation strategies based on security best practices

Environment Details

Target VM: ElavaIT Enterprise Security Lab VM

Target IP Address: 192.168.56.101

Attacker Machine IP: 192.168.56.103

Platform: VirtualBox

Network Mode: Host-only Adapter (isolated environment)

Methodology


1. Reconnaissance & Network Discovery
Performed ICMP connectivity checks using ping

Conducted ARP scanning to identify active hosts

Executed full port scanning using Nmap to identify open services and versions

3. Service & Vulnerability Identification
Identified open services:

HTTP (Port 80) – Web application

IRC Service (Port 6667) – UnrealIRCd 3.2.8.1 (vulnerable version)

Performed version analysis to map services with known vulnerabilities (CVEs)

5. Exploitation (Controlled Lab Environment)
Verified known vulnerability in outdated IRC service (CVE-based exposure)

Demonstrated remote code execution in a controlled lab environment

Achieved system-level access for validation of vulnerability impact

7. Web Application Security Testing (DVWA – Low Security Level)
SQL Injection (SQLi):

Unsanitized input allowed SQL query manipulation

Risk: Unauthorized database access

Cross-Site Scripting (XSS):

Reflected input executed in browser context

Risk: Session hijacking and client-side attacks

Command Injection:

Unsafe system command execution via input fields

Risk: Remote command execution on server

Key Findings

Outdated vulnerable service exposed at network layer

Weak input validation in web application

Missing parameterized queries in backend database logic

Lack of output encoding leading to XSS vulnerabilities

Unsafe system command execution handling in application layer

Recommended Fixes

Upgrade or disable vulnerable services (UnrealIRCd)


Implement parameterized queries to prevent SQL Injection

Apply strict output encoding for all user inputs

Enforce strong input validation and sanitization

Restrict system command execution using allow-lists

Project Structure

Deepika_VAPT_Report/

│

├── Deepika_VAPT_Report.docx

├── Deepika_VAPT_Report.pdf

├── scans/

├── screenshots/

└── README.md

Skills Demonstrated

Network Reconnaissance & Port Scanning

Vulnerability Assessment & Analysis

Web Application Security Testing

Secure Coding Awareness (SQLi, XSS, Command Injection)

Security Documentation & Reporting

Disclaimer

This project was conducted in a controlled virtual lab environment for educational purposes only. No production systems or external networks were targeted.
