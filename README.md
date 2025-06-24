# 🛡️ Cybersecurity Projects

This repository is a **curated collection of hands-on security labs, tools, and playbooks** that I use for
research, skills maintenance, and client demonstrations.  
Everything here is open-source and brought together under one roof for convenience.

| Folder | What it is | Key Skills |
|--------|------------|------------|
| **incident-response-playbooks/** | SOC run-books for containment, eradication, recovery | IR process design • NIST 800-61 |
| **pacu/** | AWS exploitation framework | Cloud pentesting • IAM misconfig enumeration |
| **cloudgoat/** | Deliberately vulnerable AWS scenarios | Attack-path mapping • Least-privilege hardening |
| **sigma/** | Cross-SIEM detection-rule format | Threat hunting • Event correlation |
| **memprocfs/** | Memory forensics virtual FS | Malware triage • DFIR |
| **sysmon-config/** | SwiftonSecurity Sysmon template | Windows telemetry • Endpoint logging |
| **opencanary/** | Lightweight network honeypot | Deception tech • Alert enrichment |
| **honeypot-elk/** | TPOT honeypot + ELK Stack | Threat intel • Log analysis |
| **testmynids/** | NIDS effectiveness test suite | Snort/Suricata tuning • PCAP crafting |

## Quick start (example: Pacu)

```bash
cd pacu
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt
./pacu.py
