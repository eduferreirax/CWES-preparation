# CPTS Preparation – Day 08

Date: March 19, 2026

## Study Time

HTB Academy Study: 1h 21m  
Web Practice (PortSwigger Labs): 2h 36m  
Lab Practice: 14m  

Total Study Time: ~4h 12m

---

# Topics Covered

Today I focused on **username enumeration techniques in web applications** and continued studying **shell concepts in HTB Academy**.

The day combined web exploitation practice with foundational knowledge about shell types.

---

# Web Practice – PortSwigger Labs

Today I completed several labs related to **username enumeration techniques**.

---

## Labs Completed

- Username enumeration based on response differences  
- Username enumeration via subtly different responses  
- Timing-based username enumeration  

---

## Key Skills Practiced

During these labs I worked on:

- analyzing HTTP responses for subtle differences  
- identifying discrepancies in status codes, messages, and behavior  
- performing timing-based attacks to detect valid usernames  
- using Burp Suite to compare and manipulate requests  
- understanding how authentication mechanisms can leak information  

---

## Key Learnings

These labs demonstrated how small differences in application responses can lead to **information disclosure vulnerabilities**.

Important takeaways:

- even minor response variations can reveal valid usernames  
- timing differences can be exploited when responses are normalized  
- enumeration is a critical step before brute force or further attacks  

---

# HTB Academy Study

Today I studied the **Types of Shells** module.

---

## Topics Studied

- Reverse Shell  
- Bind Shell  
- Web Shell  

---

## Key Concepts

Understanding shell types is essential for exploitation:

- **Reverse Shell**: target connects back to attacker  
- **Bind Shell**: attacker connects to a listening port on target  
- **Web Shell**: command execution through a web interface  

This knowledge directly applies to real-world exploitation scenarios.

---

# Lab Practice Attempt

I attempted to practice **reverse shell exploitation** on a HackingClub lab.

However, the lab environment had issues:

- unstable IP / connection problems  
- inability to establish a reliable session  

As a result, I could not complete the practical exercise.

---

## Important Note

This situation highlights a real-world factor:

- lab environments can be unstable  
- troubleshooting infrastructure issues is part of the process  

---

# Progress Update

CPTS Path Progress: **~5%**

---

# Reflection

Today was a balanced study day combining:

- web enumeration techniques  
- theoretical knowledge about shells  
- attempted hands-on exploitation  

The username enumeration labs reinforced how **small implementation flaws can lead to critical vulnerabilities**.

Even though the reverse shell lab could not be completed due to technical issues, reviewing shell concepts helped strengthen my understanding for future practice.

Consistency remains strong, and the connection between **web attacks and system-level exploitation** is becoming clearer.