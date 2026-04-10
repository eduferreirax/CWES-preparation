# CWES Preparation – Day 24

## Study Time
- **Bug Bounty Practice**: 04:59:10
- **University Study (UoPeople)**: 00:26:21
- **Total Study Time**: 05:25:31

# Topics Covered
Today was a massive milestone day entirely dedicated to practical, real-world Bug Bounty hunting. I successfully built and deployed a V1 automated reconnaissance bot and, most importantly, submitted my very first official vulnerability report. Additionally, the University of the People semester officially began, and I conducted an initial review of the academic scope.

# HTB Academy Study (CWES Path)
## Module Progress
- N/A (Focus shifted entirely to live Bug Bounty and automation today).

## Key Concepts Studied
- N/A

# Web Practice – PortSwigger Labs
## Labs Completed
- N/A

## Key Skills Practiced
- N/A

## Key Learnings
- N/A

# Bug Bounty Practice
## Automation & Tooling
- **Recon Bot V1 (`recon_hunterV1`)**: Developed an automated reconnaissance pipeline integrating the ProjectDiscovery toolchain. The script utilizes `nuclei` for vulnerability scanning, `anew` to append only new discoveries (delta checking), and `notify` to send real-time alerts directly to a Telegram bot. 
- **Infrastructure**: Currently running the automation locally on Kali Linux to test the logic and stability, with concrete plans to migrate the pipeline to a 24/7 VPS in the near future.

## Live Targets & Reporting
- **First Official Report Submitted!** - **Target**: `1win` (`1w.run`)
- **Vulnerability**: Information Disclosure (Medium Severity - 6.9)
- **Details**: Discovered internal backend service URLs and third-party API keys exposed in the publicly rendered HTML source. The sensitive information was leaking via Nuxt.js SSR (Server-Side Rendering) hydration data embedded within the `NUXT_DATA` script tag.

# Tools Used
- Kali Linux
- ProjectDiscovery Tools (`nuclei`, `anew`, `notify`)
- Telegram API (for custom bot alerts)
- Browser DevTools (Source Code Inspection)

# Challenges Faced
- Managing the continuous output of automated recon tools and filtering out the noise to identify actual infrastructure changes or vulnerabilities.
- Understanding how modern JavaScript frameworks (like Nuxt.js) handle data hydration and where they might unintentionally expose backend secrets to the client.

# How I Solved Them
- Chained `anew` into the bash workflow to ensure the Telegram bot only triggers when a *new* endpoint or state change is detected, significantly reducing alert fatigue.
- Carefully inspected the raw HTML source code (Ctrl+U) rather than just relying on the rendered DOM, successfully identifying the exposed `NUXT_DATA` JSON object containing the leaked API keys.

# Progress Update
- **Milestone Reached**: Submitted my first real-world Bug Bounty report!
- **Automation**: Recon V1 pipeline is live and successfully monitoring targets.
- **Academic**: UoPeople semester officially started; reviewed the initial syllabus and scope, setting the stage for tomorrow's study session.

# Reflection
Today represents a huge shift from learning to executing. Submitting that first report is an incredible confidence booster and proves that the methodology (SuperHunterV6) and theoretical concepts I've been studying are directly applicable to live, hardened targets. Finding API keys leaking in Nuxt.js SSR data highlights the importance of manual source code review alongside automation. Building the Telegram recon bot also sets a strong foundation for continuous monitoring. Balancing this high-level offensive practice with the start of my Computer Science degree is challenging, but the momentum is exactly where it needs to be.