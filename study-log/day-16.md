# CWES Preparation – Day 16

## Study Time
- **CWES Path**: 01:46:27
- **Web Practice**: 00:32:44
- **Lab Practice (Python)**: 00:31:22
- **Total Study Time**: 02:50:33

# Topics Covered
Today's session explored the fundamental differences between relational (SQL) and non-relational (NoSQL) databases. On the practical side, I focused on database enumeration using SQL Injection (SQLi) specifically tailored for Oracle databases, and further refined my Python scripting skills by implementing functions for better code modularity.

# HTB Academy Study (CWES Path)
## Module Progress
- **Back End Components** (3/4 Sections Completed)
  - Back End Servers (Completed)
  - Web Servers (Completed)
  - Databases (Completed)
  - Development Frameworks & APIs (Pending)

## Key Concepts Studied
- Architectural differences between relational and non-relational databases.
- Understanding how backend servers, web servers, and databases interact to process user requests.
- Theoretical foundations of SQL and NoSQL structures and their respective security implications.

# Web Practice – PortSwigger Labs
## Labs Completed
- SQL injection attack, listing the database contents on Oracle

## Key Skills Practiced
- Database enumeration via `UNION` based SQL Injection on Oracle architectures.
- Extracting hidden schema information (table and column names).
- Adapting payloads to meet Oracle's strict syntax requirements.

## Key Learnings
- Oracle databases handle queries differently than MySQL or PostgreSQL; for instance, every `SELECT` statement must include a `FROM` clause, often requiring the use of the built-in `DUAL` table.
- System tables such as `all_tables` and `all_tab_columns` are critical targets for enumerating the database schema in Oracle environments.

# Lab Practice
- **Python Scripting**: Focused on writing modular code by utilizing functions. This practice is essential for structuring reusable and maintainable code, which will be highly beneficial for developing complex exploit and automation scripts in the future.

# Tools Used
- PortSwigger Labs
- Python
- VScode

# Challenges Faced
- Adapting standard SQL injection payloads to match Oracle-specific syntax and database structures.

# How I Solved Them
- Researched Oracle's specific SQL dialect (like the requirement of `FROM DUAL` for simple `SELECT` statements) and targeted the correct default tables to successfully craft valid payloads and extract the necessary data.

# Progress Update
- Reached 75% completion of the "Back End Components" module on HTB Academy.
- Successfully demonstrated the ability to fingerprint and extract data from a secondary, distinct database engine (Oracle).

# Reflection
Today's session provided a solid theoretical background on modern database types while reinforcing the practical nuances of exploiting them. Experiencing firsthand how Oracle handles SQL queries differently from other databases heavily underscores the importance of precise enumeration and payload adaptation. Additionally, improving my Python fundamentals by working with functions is a necessary step toward building my own custom security tools.
