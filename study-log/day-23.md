# CWES Preparation – Day 23

## Study Time
- **CWES Path**: 00:54:47
- **Lab Practice (HackingClub & Local DB)**: 01:17:24
- **Web Practice (PortSwigger)**: 00:32:09
- **Total Study Time**: 02:44:20

# Topics Covered
Today's session was highly practical, covering a mix of Server-Side Request Forgery (SSRF) fundamentals, proxy-based file enumeration, and deep-dive SQL Injection (SQLi) practice. I also set up a local database environment to better visualize backend query execution.

# HTB Academy Study (CWES Path)
## Module Progress
- Intercepting Web Traffic (Burp Suite & OWASP ZAP)

## Key Concepts Studied
- Advanced usage of Burp Suite Intruder and FFUF (Fuzz Faster U Fool) for forced browsing and resource discovery.
- Configuring payloads and wordlists specifically to identify hidden files with `.html` extensions.

# Web Practice – PortSwigger Labs
## Labs Completed
- Basic SSRF against the local server
- Basic SSRF against another back-end system

## Key Skills Practiced
- Identifying and exploiting basic SSRF vulnerabilities.
- Manipulating URL parameters to force the server to access internal loopback addresses (`127.0.0.1` / `localhost`) and external back-end systems.

## Key Learnings
- Understanding how applications fetch remote resources is critical. SSRF effectively turns the vulnerable server into a proxy for the attacker, allowing access to internal management interfaces that are otherwise firewalled.

# Lab Practice
## Platform: HackingClub & Local Environment
- **SQL Injection (SQLi)**: Practiced SQLi exploitation on HackingClub targets.
- **Local Database Setup**: Downloaded and configured XAMPP to run a local MariaDB instance. Integrated the database directly into VSCode.
- **Backend Visualization**: Created and manipulated tables locally to simulate how SQL queries behave on the backend. This "white-box" approach significantly improves my ability to craft complex SQLi payloads in "black-box" scenarios.

# Tools Used
- Burp Suite (Intruder)
- FFUF
- OWASP ZAP
- XAMPP (MariaDB) & VSCode
- PortSwigger Labs
- HackingClub

# Challenges Faced
- Transitioning from theoretical SQLi payloads to understanding the exact execution flow within the database engine.
- Accurately configuring fuzzing tools to target specific file extensions without generating excessive noise.

# How I Solved Them
- Setting up the local MariaDB environment in VSCode bridged the gap between theory and practice, allowing me to instantly test and debug SQL syntax before weaponizing it.
- Tuned FFUF and Burp Intruder configurations by applying appropriate status code filters to cleanly identify valid `.html` files.

# Progress Update
- Solidified proxy enumeration techniques and successfully completed the foundational SSRF labs. I am fully prepped to tackle the Practitioner-level SSRF labs tomorrow.

# Reflection
Building a local environment (XAMPP/MariaDB) to test SQL queries was one of the best decisions for my SQLi study. Seeing exactly how the database engine handles tables and data makes crafting injection payloads much more intuitive. Furthermore, starting the PortSwigger SSRF track highlighted how a simple URL manipulation can compromise an entire internal network. The synergy between manual proxy use and automated fuzzing is becoming a core part of my methodology.