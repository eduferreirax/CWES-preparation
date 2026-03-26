# CWES Preparation – Day 14

## Study Time
- **CWES Path**: 00:22:55
- **Web Practice**: 00:40:13
- **Lab Practice (Python Scripting)**: 00:11:41
- **Total Study Time**: 01:14:49

# Topics Covered
Today's session involved theoretical study on web application architectures, practical reinforcement of username enumeration vulnerabilities, and developing custom Python scripts to generate targeted payloads for bypassing IP-based rate limiting in Burp Suite. Additionally, I achieved a major personal milestone by securing a scholarship for a Computer Science degree.

# HTB Academy Study (CWES Path)
## Module Progress
- Web Application Architecture & Layout

## Key Concepts Studied
- Understanding the structural components and layout of modern web applications to identify potential attack surfaces.

# Web Practice – PortSwigger Labs
## Labs Completed
- Username enumeration via subtly different responses (Revisited)
- Username enumeration via different responses (Revisited)
- Password brute-force via IP block bypass (Custom payload strategy)

## Key Skills Practiced
- Analyzing HTTP response lengths and rendering times to enumerate valid users.
- Configuring Burp Suite Intruder with the Pitchfork attack type.
- Bypassing rate limiting by interspersing valid login attempts with invalid ones.

## Key Learnings
- Subtle differences in server responses are critical for enumeration when standard error messages are generic. 
- Automation and custom wordlist generation are essential for bypassing sophisticated defensive mechanisms like IP blocking.

# Lab Practice
- **Python Scripting for Payload Generation**: Developed a Python script to create custom username and password wordlists. The script interleaves a known valid credential (e.g., `wiener`/`peter`) every third attempt to reset the application's failed login counter, allowing a continuous brute-force attack (e.g., against user `carlos`) without triggering the IP block.

# Tools Used
- Burp Suite (Intruder - Pitchfork)
- Python (Scripting/Automation)

# Challenges Faced
- Bypassing a strict IP-based rate-limiting mechanism that blocks the attacker's IP address after 3 consecutive incorrect login attempts.

# How I Solved Them
- I wrote a Python script to dynamically generate custom payload lists for a Pitchfork attack. By sending two brute-force attempts followed by one successful login with my own valid credentials, the server's error counter resets, successfully evading the IP ban.

# Progress Update
- Solidified my understanding of enumeration techniques by revisiting core labs. 
- **Major Milestone**: Officially accepted with a scholarship into the Computer Science program at the University of the People! This academic journey will deeply enhance my foundational technical knowledge, heavily supporting my long-term offensive security goals.

# Reflection
- Writing custom Python scripts to manipulate Burp Suite attacks bridges the gap between basic tool usage and advanced, adaptable exploitation. Understanding how the target's logic works (like the error counter) allows for creative bypasses. Furthermore, starting the Computer Science degree is a massive step forward; building a strong theoretical foundation in computing will undoubtedly make me a sharper and more analytical penetration tester.