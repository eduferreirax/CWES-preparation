# CWES Preparation – Day 26

## Study Time
- **CWES Path**: 01:37:15
- **Bug Bounty Practice**: 02:31:34
- **University Study (UoPeople)**: 01:43:15
- **Total Study Time**: 05:52:04

# Topics Covered
Today's session involved completing a major module on HTB Academy, actively hunting on live Bug Bounty programs via HackerOne, and balancing academic responsibilities. The theoretical and practical focus was on mastering web proxies (Burp Suite and ZAP), alongside deep-diving into infrastructure reconnaissance (Supabase), Server-Side Request Forgery (SSRF) bypasses, and low-level privilege escalation.

# HTB Academy Study (CWES Path)
## Module Progress
- Using Web Proxies (Completed)

## Key Concepts Studied
- Established a firm grasp of both the Burp Suite and OWASP ZAP platforms.
- Mastered intercepting and manipulating web requests made by different applications.
- Utilized Burp/ZAP to debug other security tools and proxy their traffic.
- Applied fuzzing techniques to various web functions to identify potential vulnerabilities.
- Leveraged Passive and Active scanning features to automate vulnerability discovery.
- Explored extending Burp and ZAP functionalities using plugins and extra features (e.g., Burp Sequencer, ZAP Scripting Engine).

# Web Practice – PortSwigger Labs
## Labs Completed
- N/A (Focus shifted to live Bug Bounty targets and HTB Academy completion today).

## Key Skills Practiced
- N/A

## Key Learnings
- N/A

# Bug Bounty Practice
## Live Targets
- Transitioned theoretical knowledge directly into practice by actively hunting on HackerOne programs, utilizing the newly mastered proxy configurations.

## Reconnaissance & Exploitation Notes
- [cite_start]**Supabase Infrastructure**: In environments utilizing Supabase, standard ports 54321 (REST API/PostgREST) and 54323 (Dashboard/Studio) are critical vectors if exposed[cite: 1]. [cite_start]The standard endpoint for querying tables via API is `/rest/v1/[table_name]`[cite: 2]. [cite_start]Table names can be discovered via the administrative Schema Visualizer or through directory brute-forcing on the API[cite: 3].
- [cite_start]**Row Level Security (RLS)**: Row Level Security (RLS) is a PostgreSQL security layer that filters row visibility and editability based on defined policies[cite: 4]. [cite_start]If RLS is disabled, any REST API request can return the entire table contents, leading to a full data dump[cite: 5]. [cite_start]"RLS not enabled" alerts in database dashboards indicate a critical risk, often rated P1/P2 in Bug Bounty programs[cite: 6].
- [cite_start]**SSRF Bypasses**: Server-Side Request Forgery (SSRF) involves forcing the server to make internal requests to unexposed services, such as a local Grafana instance on port 3000[cite: 7]. [cite_start]String filters blocking `127.0.0.1` or `localhost` can be bypassed by converting the IP to its decimal format, such as `2130706433`[cite: 8]. [cite_start]After confirming an SSRF vulnerability, the focus shifts to internal management endpoints (e.g., `/api/search`, `/api/dashboards`) to find cleartext credentials or secrets[cite: 9].
- [cite_start]**Privilege Escalation (C/Rust)**: In C applications, dynamic library loading is possible using `dlopen()` and `dlsym()` for Shared Objects (`.so`)[cite: 10]. [cite_start]Writing to a plugin directory allows an attacker to achieve Remote Code Execution (RCE) by creating a `.so` file with an initialization function like `plugin_init`[cite: 11]. The Rust package manager, `cargo`, can be used for privilege escalation if the user has `sudo` permissions over it[cite: 12]. By creating a new project (`cargo new`) and modifying `main.rs` to change system binary permissions (e.g., `/bin/bash`), effective privilege escalation is achieved[cite: 13].

# University Study (UoPeople)
- Successfully completed all required academic assignments for the week, ensuring my Computer Science coursework remains on track without disrupting my offensive security studies.

# Tools Used
- Burp Suite
- OWASP ZAP
- HackerOne Platform
- API Clients (for Supabase testing)

# Challenges Faced
- Managing the dense theoretical concepts of advanced web proxy usage while simultaneously performing live bug hunting and completing university assignments.

# How I Solved Them
- Strictly adhered to my time-tracking methodology, dedicating focused blocks to complete the HTB Academy module early, which freed up mental bandwidth for unscripted Bug Bounty hunting and academic tasks later in the day.

# Progress Update
- **Milestone**: 100% completion of the "Using Web Proxies" module on the CWES path.
- UoPeople assignments are fully up to date.

# Reflection
Completing the "Using Web Proxies" module solidifies the absolute core of my web exploitation methodology. Understanding how to not just intercept traffic, but actively manipulate, fuzz, and debug requests is the dividing line between automated scanning and professional penetration testing. Applying these exact skills directly to HackerOne targets on the same day reinforced the material perfectly. Integrating my infrastructure recon notes (specifically around Supabase and SSRF) into my active hunting strategy continues to mature my Bug Bounty approach (SuperHunterV5).