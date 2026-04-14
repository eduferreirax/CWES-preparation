# CWES Preparation – Day 25

## Study Time
- **Bug Bounty**: 04:11:29
- **Web Practice**: 03:36:14
- **Lab Practice (HackingClub)**: 03:25:45
- **Total Study Time**: 11:13:28

# Topics Covered
Today was an intensive, 11+ hour marathon focused entirely on practical web exploitation. The session spanned across Bug Bounty hunting, structured Web Practice, and HackingClub labs. Core vulnerabilities explored included advanced Cross-Site Scripting (XSS), Insecure Direct Object Reference (IDOR) for privilege escalation, and deep-dive SQL Injection (SQLi) techniques covering both enumeration and authentication bypass.

# HTB Academy Study (CWES Path)
## Module Progress
- N/A (Dedicated entirely to practical application and live targets today).

## Key Concepts Studied
- N/A

# Web Practice & Lab Practice (HackingClub & PortSwigger)
## Vulnerabilities Exploited & Key Skills Practiced

### Cross-Site Scripting (XSS)
- Injected malicious payloads into standard page content and page titles.
- Exploited HTML attributes utilizing the `onmouseover` event handler.
- **Filter Bypass**: Successfully bypassed strict input filters using alternative HTML tags such as `<svg>`, `<img>`, and `<details>`.

### Insecure Direct Object Reference (IDOR)
- Achieved unauthenticated access to protected administrative pages (e.g., bypassing access controls to reach `/page/edit/4`).
- Manipulated object IDs to unauthorizedly access private posts belonging to other users.
- **Session Hijacking/Impersonation**: Identified and manipulated MD5-hashed cookies to impersonate other users and escalate privileges.

### SQL Injection (SQLi)
- Executed Boolean-based blind SQLi targeting the `username` authentication field.
- Fingerprinted the backend database engine, successfully identifying MySQL/MariaDB.
- Extracted complete database tables (Data Dump) utilizing automated tools.
- Performed authentication bypass using the `UNION SELECT` method (executing the "more perfect union" technique).
- **User Enumeration**: Leveraged verbose application responses—differentiating between "Unknown user" and "Invalid password" errors—to enumerate valid usernames on the system.

# Bug Bounty Practice
- Dedicated over 4 hours to applying these web exploitation techniques against live Bug Bounty targets. Utilized automated fuzzing and manual proxy manipulation to map target attack surfaces, specifically hunting for XSS, IDOR, and SQLi vectors.

# Tools Used
- **Burp Suite / Caido**: For manual HTTP request interception, modification, and analysis.
- **FFUF**: For rapid fuzzing of API endpoints, hidden directories, and predictable object IDs.
- **SQLMap**: For automated exploitation and dumping of vulnerable SQL databases.
- **cURL**: For rapid, manual command-line HTTP request testing.
- **Wappalyzer**: For initial technology stack fingerprinting and reconnaissance.

# Challenges Faced
- Bypassing modern XSS filters that actively stripped or blocked standard `<script>` tags.
- Identifying the exact hashing mechanism used for session cookies to successfully forge them for IDOR/Impersonation.
- Confirming precise boolean-based blind SQLi queries manually before passing them to automated tools.

# How I Solved Them
- Researched and applied alternative HTML event handlers (`onmouseover`) and tags to execute JavaScript without relying on standard vectors.
- Analyzed the cookie structure in Burp/Caido, recognized the 32-character hexadecimal string as an MD5 hash, and generated valid hashes corresponding to target user IDs.
- Used systematic boolean payloads (e.g., `AND 1=1` vs `AND 1=2`) to observe application behavior and confirm the blind SQLi vulnerability before utilizing `sqlmap` for the heavy lifting.

# Progress Update
- Completed an exceptional 11-hour training block, demonstrating high stamina.
- Solidified practical