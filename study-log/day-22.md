# CWES Preparation – Day 22

## Study Time
- **CWES Path**: 01:15:36
- **Lab Practice (HackingClub)**: 01:32:15
- **Total Study Time**: 02:47:51

# Topics Covered
Today's session was divided between mastering essential web proxies (Burp Suite and OWASP ZAP) via the CWES path and applying theoretical and practical knowledge on a HackingClub target. The hands-on practice focused heavily on exploiting client-side vulnerabilities (Stored and DOM XSS) and utilizing automated fuzzing tools for reconnaissance.

# HTB Academy Study (CWES Path)
## Module Progress
- Intercepting Web Traffic (Burp Suite & OWASP ZAP)

## Key Concepts Studied
- Core functionalities of web proxies for traffic interception, modification, and analysis.
- Configuration and setup of Burp Suite and OWASP ZAP (skipped introductory setup sections as my local environment is already fully configured and optimized).
- Methodologies for mapping applications and manipulating HTTP requests in real-time.

# Web Practice – PortSwigger Labs
## Labs Completed
- N/A (Focus shifted to HackingClub platform today).

## Key Skills Practiced
- N/A

## Key Learnings
- N/A

# Lab Practice
## Platform: HackingClub
- **Vulnerability Exploitation**: Studied and practically applied payloads for Stored Cross-Site Scripting (XSS) and DOM-based XSS. Analyzed how stored payloads persist in the backend and how DOM XSS specifically targets and manipulates the client-side JavaScript environment.
- **Reconnaissance**: Utilized FFUF (Fuzz Faster U Fool) for rapid web fuzzing, focusing on directory and endpoint discovery to map out the target application's attack surface.

# Tools Used
- Burp Suite
- OWASP ZAP
- FFUF
- HackingClub Platform

# Challenges Faced
- Differentiating the precise execution contexts between Stored XSS and complex DOM-based XSS scenarios.
- Tuning FFUF parameters (like wordlists and filtering mechanisms) to avoid false positives during reconnaissance.

# How I Solved Them
- Carefully traced the data flow from the input vectors to the execution sinks in the browser to better understand DOM manipulation.
- Adjusted FFUF flags (such as filtering by status code or response size) to ensure clean and actionable fuzzing results.

# Progress Update
- Reinforced my foundational proxy skills and successfully bridged the gap between manual traffic interception and automated web fuzzing. 

# Reflection
Skipping the basic Burp Suite setup sections was a good decision, allowing me to maximize active learning time and focus on deeper proxy features. Transitioning to HackingClub to practice XSS and FFUF provided an excellent mix of manual exploitation and automated recon. Understanding how to seamlessly switch between tools like Burp Suite for precision attacks and FFUF for rapid discovery is a critical workflow for real-world penetration testing and bug bounty hunting.