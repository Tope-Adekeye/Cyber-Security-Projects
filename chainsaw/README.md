# ⛓️ Chainsaw - Fast Event Log Hunting

**"Lightning-fast Windows forensic artefact analysis and threat hunting platform"**

[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-blue.svg)](#)
[![Forensics](https://img.shields.io/badge/Focus-Digital%20Forensics-green.svg)](#)
[![Detection](https://img.shields.io/badge/Rules-Sigma%20%7C%20Custom-orange.svg)](#)
[![License](https://img.shields.io/badge/License-MIT-red.svg)](LICENCE)

## 🎯 Overview

Chainsaw is a powerful **"first-response"** digital forensics and incident response tool that provides lightning-fast analysis of Windows forensic artefacts. Developed by WithSecure Labs, this tool enables security professionals to rapidly identify threats within Event Logs, MFT files, registry hives, and other critical Windows artefacts through advanced search capabilities and built-in threat detection logic.

### 🚀 **Key Features**
- **Sigma Rule Support**: Hunt for threats using Sigma detection rules and custom Chainsaw detection rules
- **Multi-Format Search**: Search and extract forensic artefacts by string matching and regex patterns
- **Timeline Analysis**: Create execution timelines by analysing Shimcache artefacts and enriching with Amcache data
- **SRUM Analysis**: Analyse the System Resource Usage Monitor database with detailed insights
- **Forensic Dumping**: Dump raw content of forensic artefacts (MFT, registry hives, ESE databases)
- **Cross-Platform**: Runs on Windows, Linux, and macOS with consistent performance
- **Multiple Output Formats**: ASCII tables, CSV, and JSON output for flexible integration

## 🛠️ **Detection Capabilities**

### **Supported Artefact Types**
- **Windows Event Logs (EVTX)**: Comprehensive analysis of security, system, and application logs
- **Master File Table (MFT)**: File system forensics and timeline reconstruction
- **Registry Hives**: System configuration and persistence analysis
- **Shimcache**: Program execution timeline analysis
- **SRUM Database**: System resource usage monitoring and analysis
- **Amcache**: Application execution evidence and enrichment

### **Built-in Detection Rules**
- **Account Tampering**: User creation, group modifications, privilege escalation
- **Antivirus Alerts**: Multi-vendor AV detection parsing (Defender, Kaspersky, Sophos, F-Secure)
- **AppLocker Events**: Application control and bypass detection
- **Credential Access**: Kerberoasting, ticket manipulation, credential dumping
- **Defense Evasion**: Sysmon tampering, service modifications, log clearing
- **Lateral Movement**: RDP, SSH, network logons, service installations
- **Persistence**: Scheduled tasks, registry modifications, service creation
- **PowerShell Activity**: Script block analysis and suspicious execution patterns

## 📋 **Professional Use Cases**

### **Incident Response Operations**
- **Rapid Triage**: Quick identification of compromise indicators across large log volumes
- **Timeline Analysis**: Reconstruct attack sequences and establish incident scope
- **Evidence Collection**: Extract and correlate forensic evidence from multiple sources
- **Threat Hunting**: Proactive search for advanced persistent threats and lateral movement

### **Digital Forensics Investigations**
- **Forensic Analysis**: Deep examination of Windows systems for evidence preservation
- **Malware Analysis**: Identify and track malicious software execution patterns
- **Data Exfiltration**: Detect unauthorized data access and transfer activities
- **System Compromise**: Determine attack vectors and assess damage scope

### **Security Operations Center (SOC)**
- **Log Analysis**: Efficient processing of high-volume Windows event streams
- **Detection Engineering**: Custom rule development and Sigma rule deployment
- **Threat Intelligence**: IOC matching and threat actor technique identification
- **Compliance Monitoring**: Audit trail analysis and regulatory compliance support

## 🎮 **Usage Examples**

### **Threat Hunting with Sigma Rules**
```bash
# Hunt through event logs using Sigma detection rules
./chainsaw hunt /path/to/logs/ -s sigma/ --mapping mappings/sigma-event-logs-all.yml

# Combined Sigma and Chainsaw rules with CSV output
./chainsaw hunt /path/to/logs/ -s sigma/ -r rules/ --csv --output results/
```

### **Targeted Search Operations**
```bash
# Search for specific IOCs across all log files
./chainsaw search "mimikatz" -i /path/to/logs/

# PowerShell script block analysis
./chainsaw search -t 'Event.System.EventID: =4104' /path/to/logs/

# Regex pattern matching with JSON output
./chainsaw search -e "DC[0-9].domain.local" /path/to/logs/ --json
```

### **Forensic Timeline Analysis**
```bash
# Shimcache analysis with Amcache enrichment
./chainsaw analyse shimcache ./SYSTEM --regexfile analysis/shimcache_patterns.txt --amcache ./Amcache.hve --output timeline.csv

# SRUM database analysis
./chainsaw analyse srum --software ./SOFTWARE ./SRUDB.dat --output srum_analysis.json
```

## 🔧 **Detection Rule Repository**

### **EVTX Detection Rules**
- **Account Tampering**: New user creation, group membership changes
- **Antivirus Events**: Multi-vendor security product alert parsing
- **Credential Access**: Kerberos attacks and credential dumping
- **Lateral Movement**: Remote access and privilege escalation detection
- **Log Tampering**: Security audit log manipulation and clearing
- **Service Attacks**: Malicious service installation and modification

### **MFT Analysis Rules**
- **Tool Detection**: Common penetration testing and attack tool identification
- **Data Exfiltration**: File access patterns indicating data theft
- **Persistence Mechanisms**: File system-based persistence detection
- **Malware Artifacts**: Suspicious file creation and modification patterns

## 🔒 **Enterprise Security Integration**

### **SIEM Platform Integration**
- **ELK Stack**: JSON output format for Elasticsearch ingestion
- **Splunk**: Structured logging format for universal forwarder integration
- **QRadar**: Custom DSM development support with detailed field mapping
- **Sentinel**: Azure cloud-native SIEM integration capabilities

### **Workflow Automation**
- **API Integration**: Programmatic access for automated threat response
- **Batch Processing**: Large-scale forensic analysis automation
- **Custom Pipelines**: Integration with existing security orchestration platforms
- **Reporting**: Automated report generation and distribution

## 📧 **Professional Contact**

**Tope Adekeye**  
📧 adekeyetopeaiexpert@gmail.com  
🏢 **Specialization**: Governance • Risk • Compliance • AI Ethics • Cloud Security  
🔗 [LinkedIn](https://www.linkedin.com/in/temitope-adekeye-001a04359/) | [GitHub](https://github.com/Tope-Adekeye)

---

> **Note**: Chainsaw is designed for authorized security operations only. Ensure proper legal authorization and organizational approval before analyzing systems. Users are responsible for compliance with applicable laws, regulations, and organizational policies.

*Part of the [Cyber-Security-Projects](https://github.com/Tope-Adekeye/Cyber-Security-Projects) collection*
