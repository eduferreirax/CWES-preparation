# CPTS Preparation – Day 04

Date: March 15, 2026

## Study Time

HTB Academy Study: 1h 06m  
Lab Practice: 2h 35m  

Total Study Time: ~3h 42m

---

## Topics Covered

Today I focused mainly on **lab practice and reinforcement of previously solved machines**, along with starting a new HTB Academy module.

The main goal today was to **deeply understand the exploitation process instead of only completing the machine**.

---

# Lab Practice

## Machine Review – Locker

Today I revisited the **Locker** machine to improve my understanding of the exploitation steps and the reasoning behind each command.

### First Session

During the first session I carefully reviewed the entire machine again, analyzing:

- each command executed
- the vulnerability being exploited
- why each step worked

After reviewing the full exploitation chain, I completed the machine again successfully.

---

### Second Session

In the second session I repeated the machine once more.

This time I was able to **complete it in under 30 minutes**, because I already fully understood the exploitation path.

However, I intentionally took extra time to:

- study the commands used in the attack
- better understand the technical concepts behind the vulnerability
- refine my understanding of the exploitation process

During this session I also **refined my original write-up**, improving the clarity and ensuring that all steps were **fully reproducible and functional**.

---

## Write-up Review – DocFlow

Later in the evening, I read the write-up of another machine that I had already **successfully compromised** called **DocFlow**.

My goal was not only to review the solution but also to better understand the **technical concepts and terminology** involved.

Since my understanding is improving, I noticed that the concepts are starting to **connect more clearly**, which makes it easier to follow the exploitation logic.

Tomorrow I plan to revisit this machine again and reproduce the full attack chain.

---

# HTB Academy Study

Today I started the **Offensive – Getting Started** module.

This module introduces fundamental tools and concepts used during penetration testing.

---

## Common Pentesting Tools

Some tools introduced in this section include:

- **Nmap** – used for network scanning and service discovery  
- **Netcat** – a networking utility often used for creating shells and interacting with network services

Interestingly, these tools were also used in today's lab practice, which helped reinforce their practical usage.

---

## Common Network Ports

The module also covered several commonly used ports:

- **22 – SSH**
- **80 – HTTP**
- **443 – HTTPS**

Understanding these ports is essential during **reconnaissance and service enumeration**.

---

## VPN Usage

HTB Academy also discussed the importance of using **VPN connections** to access lab environments securely.

Many penetration testing labs require connecting through a VPN to interact with the target network.

---

## Organization for Pentesters

Another important concept discussed was **organization and operational hygiene**.

A professional penetration tester should always maintain a **clean and controlled working environment**.

For example:

- using a **fresh virtual machine (VM)** for each new engagement
- separating client environments
- avoiding contamination of tools or collected data between different engagements

Good organization helps prevent mistakes and protects both the tester and the client.

---

## Shell Types

The module introduced different types of shells commonly used during exploitation.

### Reverse Shell

A **reverse shell** occurs when the target machine initiates a connection back to the attacker's system.

This type of shell is often used to bypass firewall restrictions.

Example scenario:

The attacker opens a listener and the compromised machine connects back to it.

Today’s lab machine also used a **reverse shell** during exploitation.

---

### Bind Shell

A **bind shell** occurs when the compromised machine opens a port and waits for the attacker to connect.

The attacker then connects directly to that port to gain shell access.

---

### Web Shell

A **web shell** is a malicious script uploaded to a web server that allows attackers to execute commands remotely through a web interface.

---

## OWASP Top 10

The module also introduced the **OWASP Top 10**, which is a list of the most critical web application security risks.

This list helps developers and security professionals understand the most common types of web vulnerabilities.

---

# Progress Update

At the end of today’s study session, my CPTS path progress reached:

**4% completion (+1% today).**

---

# Reflection

Today’s focus on **repeating and analyzing lab machines** helped reinforce my understanding of exploitation techniques.

Instead of simply solving machines, I focused on:

- understanding each command
- reviewing vulnerabilities in depth
- refining write-ups
- improving technical comprehension

I can also feel that the technical concepts are starting to **connect more naturally**, making it easier to understand the attack flow during exploitation.

This deeper approach should help build a stronger foundation for more advanced machines in the future.