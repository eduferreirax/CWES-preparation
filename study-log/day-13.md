# CWES Preparation – Day 13

Date: Month Day, Year

## Study Time

CWES Preparation (HTB Academy): ~45m  
Web Practice (PortSwigger Labs): ~2h 20m  
Lab Practice (HackingClub): ~1h 20m  
Python Practice: ~35m  

Total Study Time: ~4h 55m

---

# Topics Covered

Focused on understanding the difference between web applications and websites, practicing SQL Injection attacks, and exploring WAF bypass techniques. Also worked on a competitive lab machine without a write-up, reinforcing independent problem-solving and real-world security concepts.

---

# HTB Academy Study (CWES Path)

## Module Progress

- Web Fundamentals (Web Applications vs Websites) – In Progress

---

## Key Concepts Studied

- Difference between static websites and dynamic web applications  
- Backend interaction with databases  
- Authentication logic and request flow  
- Security boundaries in web architectures  

---

# Web Practice – PortSwigger Labs

## Labs Completed

- SQL Injection authentication bypass lab  
- WAF-protected lab (first exposure)  

---

## Key Skills Practiced

- Crafting SQL Injection payloads  
- Authentication bypass techniques  
- Understanding query logic manipulation  
- Using Burp Suite extensions for payload encoding/obfuscation  

---

## Key Learnings

- SQL Injection payload like `' OR '1'='1` works because the condition is always true, allowing authentication bypass  
- Applications may return the first valid user (often admin) when login checks are bypassed  
- WAFs introduce additional filtering layers, requiring payload obfuscation techniques  
- Hackvertor extension can help encode and mutate payloads to bypass filters  

---

# Bug Bounty Practice

- No direct bug bounty activity, but concepts learned are highly applicable to real-world targets  

---

# Lab Practice

## HackingClub – Machine: Anomaly (Competition)

- Worked on a machine without a write-up  
- Required independent enumeration and exploitation  
- Simulated real-world scenario with no guidance  

---

## Key Learnings

- Importance of structured methodology during unknown environments  
- Reinforced enumeration and hypothesis testing  

---

# Tools Used

- Burp Suite  
- Hackvertor (Burp Extension)  
- Browser DevTools  
- SQL payloads  
- Linux CLI tools  

---

# Challenges Faced

- First interaction with WAF protections  
- No write-up available for lab machine  
- Need to understand SQL query behavior deeply  

---

# How I Solved Them

- Used Hackvertor to encode and modify payloads for WAF bypass  
- Applied logical reasoning to understand SQL conditions  
- Relied on methodology instead of guides for lab machine  

---

# Progress Update

CWES Path Progress: ~XX%

---

# Reflection

This was a highly valuable day, especially for understanding real-world attack scenarios. The transition from basic SQL Injection to dealing with WAF protections marked a significant step forward. Working on a machine without a write-up reinforced independence and practical problem-solving skills, which are critical for both certifications and bug bounty hunting.

---

# Security Learnings & Mitigations

- **Supabase & RLS**  
  Never rely on hiding API calls in the frontend. Always enforce proper Row Level Security (RLS) to restrict unauthorized access.

- **Passwords in Logs**  
  Avoid using tools like `sshpass` with plaintext passwords, as they can be exposed via `.bash_history`, process lists, and logs. Prefer SSH key-based authentication.

- **Principle of Least Privilege (Capabilities)**  
  Granting capabilities like `cap_dac_override` to interactive binaries (e.g., `gdb`) is extremely dangerous, as it can lead to full filesystem access. Avoid assigning elevated capabilities to interpreters or command-execution tools.