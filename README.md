# 🛡️ Cybersecurity Projects

This repository is a **curated collection of hands-on security labs, tools, and playbooks** that I use for
research, skills maintenance, and client demonstrations.  
Everything here is open-source and brought together under one roof for convenience.

| Folder | What it is | Key Skills |
| -------------------------------- | ---------------------------------------------------- | ----------------------------------------------- |
| **[incident-response-playbooks/](incident-response-playbooks/)** | **Enterprise SOC playbooks for NIST-compliant IR** | **IR process design • NIST 800-61 • SOC Operations** |
| **[pacu/](pacu/)** | **AWS exploitation framework for cloud pentesting** | **Cloud security • IAM privilege escalation • AWS enumeration** |
| **[cloudgoat/](cloudgoat/)** | **Vulnerable AWS environments for security training** | **CTF scenarios • Cloud pentesting labs • Terraform IaC** |
| **[sigma/](sigma/)** | **Universal SIEM detection rules (3000+ rules)** | **Cross-platform detection • MITRE ATT&CK coverage • SOC operations** |
| **[chainsaw/](chainsaw/)** | **Fast Windows forensic artefact analysis and threat hunting** | **Event log analysis • DFIR timeline reconstruction • Multi-platform EVTX parsing** |
| **[osquery/](osquery/)** | **SQL-powered endpoint monitoring and analytics framework** | **System instrumentation • SQL querying • Cross-platform monitoring • DFIR** |
| **[MemProcFS/](MemProcFS/)** | **Advanced memory forensics framework** | **Virtual file system • Live analysis • DFIR • Malware detection** |
| **[sysmon-config/](sysmon-config/)** | **Enterprise Windows monitoring template (5.1k stars)** | **Sysmon configuration • Threat hunting • SOC operations** |
| **[opencanary/](opencanary/)** | **Enterprise deception technology platform (2.5k stars)** | **Honeypot services • Early threat detection • SOC integration** |
| **[tpotce/](tpotce/)** | **All-in-one multi honeypot platform with ELK (8k stars)** | **20+ honeypots • Threat intelligence • Enterprise analytics** |
| **[testmynids/](testmynids/)** | **NIDS effectiveness validation framework (264 stars)** | **15+ attack simulations • SOC validation • Multi-protocol testing** |

## Quick start (example: Pacu)

```bash
cd pacu
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt
python3 cli.py
```
