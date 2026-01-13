# cyart-red-teaming

This repository contains practical cybersecurity tasks completed as part of the CYART Red Teaming / Cybersecurity Internship program.

## Structure

## Week 2
  - Consolidated practical report covering Tasks 1–8
  - Workflow and incident response diagrams
  - Screenshots and documentation

## Key Topics Covered

- Threat Hunting with Sigma Rules
- Malware Analysis (Static & Dynamic)
- Vulnerability Assessment (OpenVAS)
- Incident Response (SANS Framework)
- Network Defense (Suricata)
- Risk Assessment (ALE & Risk Matrix)
- Capstone Incident Response Project

All work was conducted in a controlled lab environment for educational purposes.


## Week 3
# Red Team Practical Application & Capstone Project

## Overview
This repository contains a **hands-on Red Team Practical Application and Capstone Project** focused on simulating real-world offensive security operations in a **controlled and authorized lab environment**. The project demonstrates the complete red team attack lifecycle, aligned with the **MITRE ATT&CK framework**, using open-source security tools.

All activities were performed ethically using **intentionally vulnerable virtual machines, test accounts, and simulated data**.

---

## Objectives
- Perform end-to-end red team operations
- Understand attacker techniques across the cyber kill chain
- Gain hands-on experience with offensive security tools
- Map techniques to the MITRE ATT&CK framework
- Document findings in professional red team reports

---

## Lab Environment
- **Attacker:** Kali Linux VM  
- **Victims:** Windows VM, Metasploitable2/3  
- **Network:** Isolated lab (NAT / Host-only)  
- **Tools:** Open-source offensive security tools  

---

## Practical Application (Tasks 1–7)

### Task 1: OSINT & Reconnaissance
- Recon-ng, Shodan, Maltego  
- Identified public assets and exposed services

### Task 2: Phishing Simulation
- Gophish, Evilginx2  
- Simulated credential harvesting via phishing

### Task 3: Vulnerability Exploitation
- Nmap, OWASP ZAP, Metasploit  
- Exploited a vulnerable web application

### Task 4: Lateral Movement & Persistence
- Impacket (PsExec)  
- Established persistence using scheduled tasks

### Task 5: Social Engineering (Vishing)
- PhoneInfoga, Maltego  
- Simulated phone-based social engineering

### Task 6: Exploit Development Basics
- GDB, radare2  
- Identified and tested a buffer overflow vulnerability

### Task 7: Post-Exploitation & Exfiltration
- Mimikatz  
- Simulated DNS-based data exfiltration

---

## Capstone Project
The capstone project combines all practical tasks into a **single end-to-end red team engagement**, covering:

1. Reconnaissance & OSINT  
2. Initial Access  
3. Exploitation  
4. Lateral Movement  
5. Persistence  
6. Post-Exploitation  
7. Simulated Data Exfiltration  
8. Blue Team Detection Review  
9. Final Reporting & Recommendations  

---

## Attack Flow
Recon → Initial Access → Exploitation → Lateral Movement → Persistence → Post-Exploitation → Exfiltration → Reporting


# Week 4 – Full Adversary Simulation (Red Team Operations)

# Overview
This week focuses on a full-spectrum red team engagement conducted in a controlled laboratory environment. The objective was to simulate a realistic cyber attack lifecycle, evaluate attacker capabilities, and analyze defensive detection gaps across cloud, endpoint, identity, and network layers.

All activities were performed ethically and strictly for academic and educational purposes.

# Simulation Scope
The engagement followed a real-world adversary lifecycle, including reconnaissance, initial access, privilege escalation, command and control (C2), evasion, automation, and post-compromise impact analysis.

# Attack Lifecycle Workflow
Initial Access → Privilege Escalation → Command & Control →  
Evasion Techniques → Automated Attack Execution → Impact & Risk Analysis

# Tools and Technologies Used
- Kali Linux (Attacker platform)
- Metasploit Framework (Payload delivery and C2)
- MITRE Caldera (Adversary emulation and automation)
- Pacu (Cloud reconnaissance and IAM abuse)
- AWS CLI (Cloud interaction)
- ScoutSuite (Cloud security posture assessment)
- Wazuh SIEM (Blue team detection analysis)
- PowerShell and WMI (Living-Off-the-Land techniques)
- Tor and Proxychains (Network evasion)
- Virtualized lab environment (Isolated)

# Task 1 – Advanced Command and Control (C2) Simulation
This task demonstrated how attackers establish and maintain persistent command-and-control access to compromised systems. A Metasploit multi-handler listener was configured to receive reverse connections from a Windows target system.

Encrypted and reverse TCP communication methods were tested, validating session establishment and remote command execution capability. The task highlighted how C2 traffic can blend into normal network activity and evade perimeter-based detection.

# Task 2 – Cloud Environment Attack Simulation
Cloud infrastructure attacks were simulated using Pacu and AWS CLI within a vulnerable lab environment. Cloud reconnaissance focused on identifying exposed assets and misconfigured permissions rather than traditional network scanning.

IAM misconfigurations enabled unauthorized access and controlled data exfiltration using legitimate cloud APIs, demonstrating how cloud-native attacks can appear benign while causing severe security impact.

# Task 3 – Adversary Emulation and Detection Analysis
This task emulated real-world APT-style behavior using MITRE Caldera. Phishing-based initial access, persistence mechanisms, and post-compromise command execution were simulated.

Blue team detection analysis using Wazuh SIEM revealed limited visibility during early attack stages, with improved detection occurring during later post-exploitation activities.

# Task 4 – Advanced Evasion Techniques
Advanced evasion techniques were tested to bypass traditional security controls. Payloads were obfuscated using polymorphic encoding to evade signature-based antivirus detection.

Network-level evasion was achieved by routing command-and-control traffic through Tor using proxychains, concealing attacker infrastructure and bypassing IP-based detection mechanisms.

# Task 5 – Cloud Privilege Abuse Simulation
This task demonstrated how overprivileged IAM roles can lead to full administrative compromise in cloud environments. A low-privileged IAM identity was able to escalate access by abusing misconfigured role permissions.

ScoutSuite validated the presence of critical IAM misconfigurations, reinforcing the importance of least-privilege enforcement and continuous permission auditing.

# Task 6 – Automated Attack Orchestration
Automated attack execution was performed using MITRE Caldera deployed via Docker. A multi-stage attack scenario was executed using an adversary profile aligned with the MITRE ATT&CK framework.

Automation enabled rapid, repeatable execution of exploitation techniques, significantly reducing attacker effort while increasing operational speed and impact.

# Task 7 – Living-Off-the-Land (LOLBAS) Techniques
This task focused on abusing native Windows tools such as PowerShell and WMI to perform malicious actions without deploying external malware.

Fileless execution and credential-related access were simulated, demonstrating how native tool abuse closely resembles legitimate administrative activity and complicates detection efforts.

# MITRE ATT&CK Technique Mapping
- T1566.001 – Phishing: Spearphishing Attachment
- T1071 – Application Layer Protocol (C2)
- T1027 – Obfuscated / Encrypted Payload
- T1090 – Proxy and Anonymization
- T1580 – Cloud Infrastructure Discovery
- T1078.004 – Valid Accounts: Cloud Accounts
- T1190 – Exploit Public-Facing Application
- T1059 – Command and Scripting Interpreter
- T1047 – Windows Management Instrumentation
- T1537 – Transfer Data to Cloud Account

# Blue Team Detection Observations
- Early-stage reconnaissance and phishing generated minimal alerts
- Detection improved during privilege escalation and post-exploitation
- Encrypted C2 traffic blended with normal network behavior
- Native tool abuse produced limited endpoint alerts
- Behavioral and correlation-based detection proved more effective than signature-based controls

# Business and Security Impact
The simulated attack demonstrated how an adversary could gain access, escalate privileges, and maintain persistence before detection. Delayed visibility significantly increases the risk of data breaches, operational disruption, and prolonged attacker dwell time.

# Key Findings
- Cloud misconfigurations present a high-risk attack surface
- Identity security weaknesses enable silent privilege escalation
- Signature-based defenses are insufficient against obfuscation and LOLBAS techniques
- Automation increases attack speed and reduces defender response time

# Recommendations
- Enforce least-privilege IAM policies and continuous permission reviews
- Strengthen phishing detection and MFA enforcement
- Deploy behavior-based endpoint detection and response (EDR)
- Improve correlation across cloud, endpoint, and network logs
- Conduct regular adversary emulation and red team exercises

# Ethical Disclaimer
All simulations were conducted in an isolated laboratory environment for educational purposes only. No production systems or real-world targets were involved.


## Author
Utkarsh Kumar
