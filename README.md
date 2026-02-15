# Cybersecurity Incident Response Portfolio

This repository contains hands-on security labs and real-world attack simulations performed in a controlled SOC environment.

Each project demonstrates:

- Lab architecture design
- Attack simulation
- Log analysis
- SIEM-based detection
- Incident response documentation

---

## Lab Environment

- Attacker: Kali Linux
- Victim: Windows 11
- SIEM: Ubuntu Server + Wazuh
- Network: Internal segmented lab (192.168.100.0/24)

---

## Projects

### 1. Windows Brute Force Detection using Wazuh SIEM
Simulated brute-force authentication attack and detected it using Wazuh SIEM.

- Event ID: 4625
- MITRE: T1110 – Brute Force
- Includes SOC-style incident report

Folder: `01-bruteforce-detection`

---

More projects coming soon:
- Malware Detection & Analysis
- Network Intrusion Detection
- Cloud Account Breach Detection
- Web Attack Detection via SIEM

