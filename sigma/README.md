# 🔍 Sigma - Universal SIEM Detection Rules

**Generic signature format for log-based threat detection across all SIEM platforms**

[![Rules](https://img.shields.io/badge/Rules-3000%2B-blue.svg)](#)
[![SIEM](https://img.shields.io/badge/SIEM-Universal-green.svg)](#)
[![Format](https://img.shields.io/badge/Format-YAML-orange.svg)](#)
[![License](https://img.shields.io/badge/License-DRL%201.1-red.svg)](LICENSE)

## 🎯 Overview

Sigma is the **industry-standard generic signature format** that allows security professionals to describe relevant log events in a straightforward, vendor-agnostic manner. Think of Sigma as **"what Snort is for network traffic and YARA is for files"** - but specifically designed for log analysis and SIEM integration.

This repository contains **over 3,000 peer-reviewed detection rules** covering everything from generic behavioral detections to emerging threat campaigns, making it an essential resource for SOC operations and threat hunting.

### 🚀 **Key Capabilities**
- **Universal SIEM Support**: Convert rules to Splunk, Elastic, QRadar, Sentinel, and 20+ other platforms
- **3,000+ Detection Rules**: Comprehensive coverage of MITRE ATT&CK techniques
- **Community-Driven**: Peer-reviewed by professional detection engineers
- **Industry Standard**: Adopted by major security vendors and organizations worldwide
- **Threat Intelligence Integration**: Rules for emerging threats and APT campaigns

## 📋 **Rule Categories**

### **🔍 Generic Detection Rules**
- **Threat-agnostic behavioral detections**
- **MITRE ATT&CK technique coverage**
- **Cross-platform compatibility**
- **Persistent threat detection**

### **🎯 Threat Hunting Rules**
- **Broad-scope suspicious activity detection**
- **Investigation starting points**
- **Anomaly identification**
- **Advanced persistent threat indicators**

### **⚡ Emerging Threat Rules**
- **Zero-day exploitation detection**
- **APT campaign indicators**
- **Timely threat intelligence**
- **Specific malware families**

## 🛠️ **Implementation Examples**

### **Basic Rule Structure**
```yaml
title: Suspicious PowerShell Download
id: 65531a13-5a43-4745-8e36-f95675e2e373
status: test
description: Detects suspicious PowerShell download activity
references:
    - https://attack.mitre.org/techniques/T1059/001/
tags:
    - attack.execution
    - attack.t1059.001
logsource:
    category: process_creation
    product: windows
detection:
    selection:
        Image|endswith: '\powershell.exe'
        CommandLine|contains:
            - 'DownloadString'
            - 'WebClient'
    condition: selection
fields:
    - Image
    - CommandLine
falsepositives:
    - Administrative scripts
level: medium
```

### **SIEM Integration Commands**
```bash
# Convert to Splunk
sigma convert --target splunk --output rules.conf sigma_rule.yml

# Convert to Elastic
sigma convert --target elasticsearch --output elastic_rules.json sigma_rule.yml

# Convert to Microsoft Sentinel
sigma convert --target sentinel --output sentinel_rules.yaml sigma_rule.yml

# Batch conversion
sigma convert --target splunk --recurse --output-dir splunk_rules/ rules/
```

## 🎮 **Available Rule Sets**

### **Core Detection Categories**
- **Windows Security**: Process creation, registry, network activity
- **Linux Security**: System calls, authentication, privilege escalation  
- **Network Security**: DNS, proxy, firewall, intrusion detection
- **Cloud Security**: AWS, Azure, GCP activity monitoring
- **Application Security**: Web applications, databases, email security

### **Specialized Collections**
- **MITRE ATT&CK Mapping**: Complete technique coverage
- **Compliance Rules**: SOC 2, PCI-DSS, HIPAA requirements
- **DFIR Collections**: Digital forensics and incident response
- **Threat Intelligence**: IOC-based detection rules

## 🔧 **Professional Implementation**

### **Enterprise Deployment**
```bash
# Install Sigma CLI
pip install pysigma

# Validate rule syntax
sigma check rules/

# Convert entire ruleset for Splunk deployment
sigma convert \
    --target splunk \
    --config splunk_enterprise.yml \
    --output-dir /opt/splunk/etc/apps/sigma_rules/default/savedsearches/ \
    --recurse rules/

# Generate MITRE ATT&CK coverage report
sigma coverage --technique-mapping rules/
```

### **Quality Assurance Workflow**
```bash
# Rule validation pipeline
sigma check --strict rules/
sigma test --target elasticsearch rules/
sigma benchmark --performance-test rules/
```

## 📊 **SOC Integration Use Cases**

### **Detection Engineering**
- **Rule Development**: Standardized format for sharing detections
- **SIEM Migration**: Portable rules across different platforms
- **Quality Assurance**: Peer-reviewed community validation
- **Coverage Analysis**: MITRE ATT&CK mapping and gap identification

### **Threat Hunting**
- **Hypothesis-Driven Hunting**: Pre-built hunting queries
- **Baseline Establishment**: Normal vs. suspicious behavior patterns
- **Incident Investigation**: Focused detection during active investigations
- **Threat Intelligence**: Converting IOCs to detection logic

### **Compliance & Governance**
- **Audit Documentation**: Standardized rule documentation
- **Control Validation**: Ensure detection capabilities meet requirements
- **Risk Assessment**: Quantify detection coverage across attack vectors
- **Reporting**: Standardized metrics for security posture

## 🏗️ **Advanced Features**

### **Rule Development Workflow**
```yaml
# Rule template structure
title: [Descriptive Name]
id: [UUID4]
status: [test|experimental|stable]
description: [Detailed description]
author: [Author name]
date: [YYYY/MM/DD]
modified: [YYYY/MM/DD]
references:
    - [External references]
tags:
    - attack.[tactic]
    - attack.[technique_id]
logsource:
    category: [Log category]
    product: [Product name]
detection:
    selection:
        [Field]: [Value]
    condition: selection
falsepositives:
    - [Known false positive scenarios]
level: [informational|low|medium|high|critical]
```

### **Multi-Platform Support**
- **Splunk**: Advanced SPL query generation
- **Elastic Stack**: Elasticsearch Query DSL and EQL
- **Microsoft Sentinel**: KQL (Kusto Query Language)
- **IBM QRadar**: AQL (Ariel Query Language)
- **Chronicle**: YARA-L 2.0 rules

## 🎯 **Training & Certification Value**

### **Professional Development**
- **SANS SEC555**: SIEM Implementation and Advanced Analytics
- **SANS FOR572**: Advanced Network Forensics and Analysis
- **Detection Engineering**: Industry-standard rule format knowledge
- **Threat Hunting**: Community-validated hunting hypotheses

### **Career Applications**
- **SOC Analyst**: Understanding detection logic and rule tuning
- **Detection Engineer**: Rule development and SIEM integration
- **Threat Hunter**: Advanced hunting techniques and methodologies
- **Security Architect**: Enterprise detection strategy and implementation

## 🔒 **Security Considerations**

### **Implementation Best Practices**
- **Rule Validation**: Always test rules in dev environments first
- **Performance Impact**: Monitor SIEM performance after rule deployment
- **False Positive Management**: Establish tuning processes for production rules
- **Version Control**: Track rule changes and performance metrics

### **Enterprise Guidelines**
- Use staged deployment processes for new rules
- Implement automated testing pipelines for rule validation
- Maintain documentation for custom rule modifications
- Regular review and update cycles for emerging threats

## 📧 **Professional Contact**

**Tope Adekeye**  
📧 adekeyetopeaiexpert@gmail.com  
🏢 **Specialization**: Governance • Risk • Compliance • AI Ethics • Cloud Security  
🔗 [LinkedIn](https://www.linkedin.com/in/temitope-adekeye-001a04359/) | [GitHub](https://github.com/Tope-Adekeye)

---

> **Professional Note**: This Sigma rule collection represents industry best practices for SIEM-based threat detection. Rules should be validated and tuned for specific environments before production deployment. Regular updates ensure coverage of emerging threats and attack techniques.

*Part of the [Cyber-Security-Projects](https://github.com/Tope-Adekeye/Cyber-Security-Projects) collection*
