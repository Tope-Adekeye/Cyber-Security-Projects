# 🛡️ Cybersecurity Projects

This repository is a **curated collection of hands-on security labs, tools, and playbooks** that I use for
research, skills maintenance, and client demonstrations.  
Everything here is open-source and brought together under one roof for convenience.

| Folder | What it is | Key Skills |
| -------------------------------- | ---------------------------------------------------- | ----------------------------------------------- |
| **[incident-response-playbooks/](incident-response-playbooks/)** | **Enterprise SOC playbooks for NIST-compliant IR** | **IR process design • NIST 800-61 • SOC Operations** |
| **[pacu/](pacu/)** | **AWS exploitation framework for cloud pentesting** | **Cloud security • IAM privilege escalation • AWS enumeration** |
| **[cloudgoat/](cloudgoat/)** | **Vulnerable AWS environments for security training** | **CTF scenarios • Cloud pentesting labs • Terraform IaC** |
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
python3 cli.py
```
