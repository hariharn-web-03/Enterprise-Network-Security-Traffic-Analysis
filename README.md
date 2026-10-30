# Ethical Hacking & Security Testing Lab 🛡️

A comprehensive repository documenting hands-on vulnerability assessments, penetration testing engagements, web application security evaluations, and post-exploitation techniques conducted within a controlled laboratory environment.

---

## 📋 Table of Contents
- [About the Lab](#-about-the-lab)
- [Key Assessment Areas](#-key-assessment-areas)
- [Tools & Technologies](#-tools--technologies)
- [Methodology & Execution](#-methodology--execution)
- [Key Findings & Exploitations](#-key-findings--exploitations)
- [Remediation & Hardening](#-remediation--hardening)

---

## 🎯 About the Lab
This project simulates real-world offensive security engagements across diverse targets, including Windows Active Directory domains, vulnerable Linux web stacks, and enterprise network segments. All activities were performed strictly within authorized, isolated lab networks for educational and defensive validation purposes.

---

## 🔬 Key Assessment Areas
1. **Network Services & Credential Testing**:
   - Automated brute-forcing and credential auditing using `Hydra` against RDP, FTP, and SMB services[cite: 31, 175].
   - Name resolution poisoning (`Responder`) and session analysis[cite: 20].
2. **Web Application Penetration Testing (DVWA / Mutillidae / Joomla)**:
   - SQL Injection (Boolean-based, Error-based, Time-based, and UNION attacks via `sqlmap` and manual payloads)[cite: 67, 116].
   - Cross-Site Scripting (Reflected & Stored XSS) and command injection vectors[cite: 57, 113, 120].
   - CMS vulnerabilities and administrative exploitation (e.g., Joomla CVE-2017-8917 template editing and reverse shell deployment)[cite: 134].
3. **Exploitation & Privilege Escalation**:
   - Exploitation of vulnerable FTP/SSH services (e.g., `vsftpd 2.3.4` backdoor)[cite: 110, 147].
   - Windows local privilege escalation via UAC bypass and named-pipe impersonation (`NT AUTHORITY\SYSTEM`)[cite: 51, 92].
   - Kernel-level privilege escalation (`eBPF doubleput` exploits on Linux)[cite: 142].

---

## 🛠️ Tools & Technologies
* **Attack Frameworks**: Metasploit Framework, SQLmap, Burp Suite
* **Reconnaissance & Scanning**: Nmap, Dirb, Gobuster
* **Exploitation & Auditing**: Hydra, John the Ripper, Aircrack-ng
* **Operating Systems**: Kali Linux, Windows 7/10, Ubuntu (Metasploitable)

---

## 🚀 Execution Highlights
* **Web App Exploitation**: Automated database enumeration using `sqlmap` to extract user credentials and table structures[cite: 67, 116].
* **System Compromise**: Gained initial footholds via vulnerable services and successfully escalated privileges to root/SYSTEM authority[cite: 51, 110, 142].

---

## 🛡️ Remediation & Defense
* Enforce strict input validation and parameterization to neutralize SQL and command injection flaws.
* Implement Multi-Factor Authentication (MFA) and robust account lockout policies to defeat credential brute-forcing.
* Maintain rigorous patch management workflows to eliminate outdated software stacks and known remote code execution vulnerabilities.

# Security Testing & Defensive Engineering Lab 🔒

An enterprise-focused security engineering and defensive lab repository centered around SIEM monitoring, vulnerability management, host-based firewall hardening, and digital forensics & incident response (DFIR).

---

## 📋 Table of Contents
- [Overview](#-overview)
- [Core Engineering Modules](#-core-engineering-modules)
- [SIEM & Threat Detection (Wazuh)](#-siem--threat-detection-wazuh)
- [Vulnerability Assessment & Hardening](#-vulnerability-assessment--hardening)
- [Digital Forensics & Incident Response (DFIR)](#-digital-forensics--incident-response-dfir)

---

## 🏢 Overview
This repository showcases the implementation of proactive security controls, continuous monitoring pipelines, and incident investigation methodologies. It bridges offensive discovery with rigorous defensive engineering.

---

## ⚙️ Core Engineering Modules
1. **SIEM Deployment & Configuration**:
   - Setting up Wazuh Managers and deploying cross-platform agents (`Ubuntu`, `Windows Server`, `Windows 10`)[cite: 82, 177, 191].
   - Writing custom detection rules (`local_rules.xml`) to alert on suspicious authentication failures and brute-force attempts[cite: 196].
2. **Vulnerability Assessment & Scanning**:
   - Executing network and host scans using `Nessus` and `Nmap` to identify End-of-Life (EOL) operating systems and unpatched services[cite: 178, 206].
   - Validating critical exposures such as MS17-010 (EternalBlue)[cite: 209].
3. **Host-Based Firewalls & Access Controls**:
   - Configuring advanced Windows Firewall rules via `netsh` and Group Policy to restrict high-risk ports (e.g., blocking SMB port 445)[cite: 174, 219].
4. **Memory Forensics (DFIR)**:
   - Analyzing memory dumps (`.vmem`) using the **Volatility Framework** (`windows.netscan`, `windows.envars`, `windows.pslist`) to uncover hidden network connections and process anomalies[cite: 198, 199, 200].

---

## 📊 Monitoring & Detection Example
* **Audit Policy Tuning**: Configured advanced audit policies (`auditpol`) and linked them with Wazuh security events to capture real-time logon failures, privilege use, and process tracking[cite: 32, 188].
* **Malware Analysis Artifacts**: Inspected suspicious binaries against threat intelligence platforms (VirusTotal hashing/indicators)[cite: 185].

---

## 🛠️ Tech Stack
* **SIEM / Monitoring**: Wazuh, Splunk
* **Scanning & Analysis**: Nessus, Volatility 3, Nmap
* **OS & Environment**: Windows 7/10/Server, Ubuntu, Red Hat Enterprise Linux (RHEL)

---

## 💡 Key Takeaways
Implementing robust endpoint detection combined with principle-of-least-privilege firewall segmentation significantly reduces lateral movement capability and enhances organizational resilience against sophisticated attacks.
