# CWES Preparation – Day 15

## Study Time
- **CWES Path**: ~2h 10m
- **Web Practice**: ~2h 15m
- **Lab Practice (Python)**: ~1h 05m
- **Total Study Time**: ~5h 30m

# Topics Covered
Today's session focused on SQL Injection techniques for database enumeration and fingerprinting, along with continued Python scripting practice to support automation and exploitation workflows.

# HTB Academy Study (CWES Path)
## Module Progress
- Back End Components

## Key Concepts Studied
- Role of backend servers in handling HTTP requests.
- Interaction between web applications and underlying databases.
- How backend logic flaws can introduce critical vulnerabilities.
- The importance of secure, parameterized database queries.

# Web Practice – PortSwigger Labs
## Labs Completed
- SQL Injection: Listing database contents (Non-Oracle)
- SQL Injection: Querying database type and version (MySQL/Microsoft)

## Key Skills Practiced
- Database enumeration via SQL Injection (SQLi).
- Fingerprinting database types and versions.
- Extracting schema information (tables, columns) using `UNION` based attacks.
- Adapting SQL payloads based on the specific database technology in use.

## Key Learnings
- Different database engines (MySQL, PostgreSQL, Oracle, MSSQL) require distinct SQL syntax for enumeration and string concatenation.
- Fingerprinting the database type is a critical first step in targeted SQLi exploitation.
- System tables (such as `information_schema.tables` and `information_schema.columns`) are primary targets during database enumeration.
- SQL Injection extends far beyond simple authentication bypass; it enables comprehensive database interaction and data exfiltration.

# Lab Practice
- **Python Scripting Focus**: Practiced scripting for automation and custom payload generation.
- **Key Concepts Practiced**: Handled input/output in Python scripts, structured reusable code blocks, and prepared scripts for seamless integration with offensive security tools.

# Tools Used
- Burp Suite
- PortSwigger Labs
- Python
- Browser DevTools

# Challenges Faced
- Adapting SQL payloads dynamically for different database types.
- Memorizing and applying database-specific syntax and functions.
- Maintaining a consistent and structured methodology during deep enumeration.

# How I Solved Them
- Systematically tested different payload variations and referenced SQLi cheat sheets.
- Followed a highly structured enumeration approach (Identify -> Fingerprint -> Extract Schema -> Extract Data).
- Reinforced complex concepts through repetition and hands-on lab practice.

# Progress Update
- CWES Path Progress: ~7%

# Reflection
Today was a strong technical day focused on advancing my SQL Injection skills beyond basic authentication bypasses. I significantly improved my ability to fingerprint databases and extract hidden schemas, which deepened my understanding of how different database management systems behave under malicious input. The combination of web exploitation labs and Python scripting continues to strengthen my workflow and efficiency, bringing me closer to handling real-world pentesting scenarios effectively.