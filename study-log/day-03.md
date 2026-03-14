# CPTS Preparation – Day 03

Date: March 14, 2026

## Study Time

HTB Academy Study: 2h 33m  
Lab Practice: 2h 11m  

Total Study Time: ~4h 44m

## Module Completed

Penetration Testing Process (HTB Academy)

Difficulty: Fundamental  
Exercises Completed: 5 / 5

Today I completed the first module of the CPTS learning path.

In addition to the theoretical content, I also practiced on a lab machine on the **Hacking Club platform**, which I successfully compromised.

---

# Topics Covered

Today I studied the later stages of the **penetration testing lifecycle**, focusing on what happens after initial access and how the engagement is concluded.

---

# Making the Network Unusable

One potential impact of a security breach is making a company's network unusable.

A common example is **ransomware attacks**, where malware encrypts systems or files across the network.

If ransomware spreads successfully, the entire infrastructure may become inaccessible until a **decryption key** is provided, often after paying a ransom.

This demonstrates how serious a vulnerability can become if it is successfully exploited.

---

# Proof of Concept (PoC)

A **Proof of Concept (PoC)** demonstrates that a vulnerability is real and exploitable.

It is often helpful to include:

- scripts
- commands
- screenshots
- reproducible steps

Providing a PoC allows developers and security teams to **clearly understand the issue**.

However, the goal is not only to block the specific exploit script.  
Instead, the report should help the organization understand the **root cause of the vulnerability** and how to properly remediate it.

---

# Detection of Commands

Some defensive systems, such as **EDR (Endpoint Detection and Response)** solutions, can detect suspicious activity.

For example, commands such as:

```
whoami
net user
```

may be flagged as anomalous behavior when executed in certain contexts.

Because of this, penetration testers must be aware that **their actions can be detected and monitored** during engagements.

---

# Penetration Testing Phases

Later stages of a penetration test include:

- Vulnerability Assessment
- Exploitation
- Post-Exploitation
- Privilege Escalation
- Lateral Movement
- Pillaging

These phases simulate what a real attacker might do after gaining initial access.

---

# Exploitation

During the **exploitation phase**, the pentester attempts to leverage identified vulnerabilities to gain access to systems or networks.

At this stage, the goal is to successfully penetrate the target environment.

---

# Privilege Escalation

After gaining initial access, attackers often attempt to escalate their privileges.

Common targets include:

### Linux

```
root
```

### Windows

```
Administrator
SYSTEM
Local Administrator
```

Privilege escalation allows an attacker to gain greater control over a system.

---

# Post-Exploitation

The **post-exploitation phase** focuses on understanding the impact of the compromise.

Common objectives include:

- collecting sensitive data
- escalating privileges
- identifying additional attack paths
- maintaining access

---

# Lateral Movement

Lateral movement involves moving from one compromised system to another within the network.

The goal is to determine how far an attacker could potentially spread through the environment.

This phase helps identify weaknesses in:

- network segmentation
- identity management
- internal security controls

---

# Pillaging

Pillaging refers to collecting valuable data from compromised systems, such as:

- credentials
- configuration files
- databases
- sensitive documents

This step helps determine what information an attacker could realistically steal.

---

# Post-Engagement Activities

After the testing phase is complete, several activities take place.

These include:

- cleanup of test artifacts
- documentation
- preparation of the final report
- post-remediation testing
- meetings with stakeholders to review findings

These activities are typically included in the scope of the engagement.

---

# Close-Out Phase

At the end of the engagement, the penetration testing team must properly close the project.

This includes:

- disconnecting from client systems
- removing any testing artifacts
- securely deleting collected data when appropriate
- delivering the final report

After everything is completed and the client has reviewed the results, the engagement can officially be closed.

---

# Role of the Pentester in Remediation

The role of the penetration tester is **not to directly fix vulnerabilities**.

Instead, the pentester should:

- explain the vulnerability
- describe the impact
- provide general remediation guidance

For example, if a **SQL Injection** vulnerability is discovered, the pentester might recommend:

```
Sanitize and validate user input.
```

However, the pentester should not rewrite the application's code.

Their role is closer to that of an **auditor or security advisor**.

---

# Data Retention

Evidence collected during the engagement must be handled securely.

Collected data should be:

- stored in secure locations
- encrypted at rest
- accessible only to authorized personnel

Evidence is usually retained for some time after the engagement in case:

- questions arise about specific findings
- additional verification is required
- the client requests follow-up testing

---

# Reflection

Today I completed the **first module of the CPTS learning path**.

This module helped me understand that penetration testing is not only about exploiting vulnerabilities, but also about:

- understanding the full attack lifecycle
- properly documenting findings
- communicating risks to organizations
- acting responsibly and ethically during engagements.

I also practiced on a lab machine today and successfully compromised it, reinforcing the concepts learned during my study session.
