# Enterprise Network Security & Traffic Analysis 📊🔍

An advanced defensive and offensive networking repository focusing on packet analysis, Man-in-the-Middle (MitM) simulation, wireless security auditing, memory forensics, and honeypot deployment.

---

## 📋 Table of Contents
- [Overview](#-overview)
- [Traffic Analysis & Packet Sniffing](#-traffic-analysis--packet-sniffing)
- [Layer-2 Attacks & MitM](#-layer-2-attacks--mitm)
- [Wireless Security Auditing](#-wireless-security-auditing)
- [Memory Forensics & Incident Response](#-memory-forensics--incident-response)

---

## 🔎 Overview
This lab investigates enterprise network traffic anomalies, protocol vulnerabilities, and host memory artifacts to understand attacker movement and improve defensive detection capabilities.

---

## 🌐 Traffic Analysis & Packet Sniffing
* **Wireshark & Tcpdump**: Captured and dissected network traffic across various protocols (HTTP, DHCP, Kerberos) to extract sensitive headers, user metadata, and connection states[cite: 201, 202, 203].

---

## ⚡ Layer-2 Attacks & MitM
* **ARP Cache Poisoning**: Executed ARP spoofing (`arpspoof` / Bettercap) with IP forwarding enabled to intercept and inspect local network traffic transparently[cite: 40, 151, 162].
* **Honeypot Deployment**: Configured `PentBox` honeypots on network ports to trap and log unauthorized scanning and intrusion attempts[cite: 170].

---

## 📡 Wireless Security Auditing
* **Wi-Fi Handshake Capture**: Collected 4-way WPA/WPA2 handshakes from wireless capture files (`.cap` / `.pcap`)[cite: 168, 169].
* **Key Cracking**: Performed dictionary and brute-force key recovery using `Aircrack-ng` to test pre-shared key (PSK) robustness[cite: 168, 169].

---

## 🧠 Memory Forensics & Incident Response
* **Volatility Framework**: Analyzed memory dump files (`.vmem`) using plugins like `windows.netscan`, `windows.envars`, and `windows.pslist` to identify active malware sockets, hidden processes, and system environment variables[cite: 198, 199, 200].
