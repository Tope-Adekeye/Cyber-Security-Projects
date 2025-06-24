# ☁️ Pacu - AWS Exploitation Framework

**Advanced cloud penetration testing tool for AWS security assessments**

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/downloads/)
[![AWS](https://img.shields.io/badge/Cloud-AWS-orange.svg)](#)
[![License](https://img.shields.io/badge/License-BSD--3--Clause-green.svg)](LICENSE)

## 🎯 Overview

Pacu is a comprehensive **AWS exploitation framework** designed for offensive security testing against cloud environments. This tool enables security professionals to identify and exploit configuration flaws within AWS accounts through a modular architecture that supports diverse attack vectors.

### 🚀 **Key Capabilities**
- **IAM Privilege Escalation**: Exploit weak permission policies
- **User Backdooring**: Maintain persistent access mechanisms  
- **Lambda Function Exploitation**: Attack serverless vulnerabilities
- **S3 Bucket Enumeration**: Discover exposed storage resources
- **EC2 Instance Exploitation**: Compromise virtual machines
- **CloudTrail Log Analysis**: Understand security monitoring gaps

## 🛠️ **Installation & Setup**

### **Prerequisites**
- Python 3.7+ and pip3
- AWS CLI configured (optional but recommended)
- Valid AWS credentials for testing

### **Quick Installation**
```bash
# Install dependencies
pip3 install -U pip
pip3 install -r requirements.txt

# Launch Pacu
python3 cli.py
```

### **Docker Installation**
```bash
# Run with default entrypoint
docker run -it -v ~/.aws:/root/.aws pacu:latest

# Alternative: Run without entrypoint
docker run -it --entrypoint /bin/sh pacu:latest
```

### **Development Setup**
```bash
# Clone and install
git clone <repository-url>
cd pacu
pip3 install -e .

# Or install with pipx
pipx install .
```

## 📋 **Getting Started**

### **Session Management**
Pacu uses sessions to store AWS credentials and attack data:

1. **Start New Session**: `pacu` (first launch)
2. **Set AWS Keys**: `set_keys` command
3. **Resume Session**: Launch with existing session name

### **Basic Commands**
```bash
# List available modules
list

# Get help for specific module
help <module_name>

# Run module with default parameters
run <module_name>

# Run module against specific regions
run <module_name> --regions us-east-1,eu-west-1

# Check current user permissions
whoami
```

## 🔧 **Core Modules**

### **Reconnaissance**
- \`iam__enum_users_roles_policies_groups\`: IAM enumeration
- \`s3__bucket_finder\`: S3 bucket discovery
- \`ec2__enum\`: EC2 instance enumeration
- \`lambda__enum\`: Lambda function discovery

### **Privilege Escalation**
- \`iam__privesc_scan\`: Automated privilege escalation detection
- \`iam__backdoor_users\`: Create persistent access backdoors
- \`iam__create_user\`: Generate new IAM users

### **Data Exfiltration**
- \`s3__download_bucket\`: Mass S3 data extraction
- \`rds__explore_snapshots\`: RDS snapshot analysis
- \`ebs__explore_snapshots\`: EBS snapshot exploration

### **Persistence & Evasion**
- \`lambda__backdoor_new_users\`: Serverless persistence
- \`cloudtrail__download_event_history\`: Log analysis and evasion

## 🎯 **Attack Scenarios**

### **Cloud Security Assessment Workflow**
1. **Initial Access**: Obtain AWS credentials through various vectors
2. **Reconnaissance**: Enumerate cloud resources and permissions
3. **Privilege Escalation**: Exploit misconfigurations for elevated access
4. **Lateral Movement**: Expand access across AWS services
5. **Data Exfiltration**: Extract sensitive information
6. **Persistence**: Establish backdoors for continued access
7. **Log Evasion**: Understand and evade detection mechanisms

### **Common Use Cases**
- **Red Team Assessments**: Simulated adversary cloud attacks
- **Penetration Testing**: Comprehensive AWS security evaluations
- **Security Research**: Cloud vulnerability discovery and analysis
- **Training & Education**: Hands-on cloud security learning

## 📊 **Professional Applications**

### **Security Consulting**
- Client AWS environment assessments
- Cloud security posture evaluations
- Compliance testing (SOC 2, FedRAMP, etc.)
- Executive risk reporting

### **Training & Certification**
- **AWS Security Specialty** preparation
- **CISSP Domain 3** (Security Engineering)
- **CCSP** (Certified Cloud Security Professional)
- **GCCC** (GIAC Certified Cloud Security)

## 🔒 **Responsible Use & Compliance**

### **Legal & Ethical Guidelines**
- ✅ **Authorized Testing Only**: Use only on systems you own or have explicit permission to test
- ✅ **AWS Acceptable Use Policy**: Ensure compliance with AWS terms of service
- ✅ **Penetration Testing Guidelines**: Follow AWS Customer Support Policy for Penetration Testing
- ✅ **Documentation**: Maintain detailed logs for client reporting

### **Professional Standards**
- Scope limitation and authorization letters
- Client notification and coordination
- Secure handling of discovered vulnerabilities
- Executive summary and technical reporting

## 📈 **Advanced Features**

### **CLI Integration**
```bash
# Session management
pacu --session <session_name>

# Module execution
pacu --module-name <module> --exec
pacu --module-args="<arguments>"

# Data querying
pacu --data <service_name>
pacu --data all

# Regional configuration
pacu --set-regions us-east-1,eu-west-1
```

### **Database Integration**
- Local SQLite database for attack data storage
- Comprehensive logging and timeline reconstruction
- Export capabilities for reporting and analysis

## 🤝 **Contributing to Cloud Security**

This tool represents the cutting edge of cloud security research and offensive security capabilities. Contributions, improvements, and responsible disclosure of cloud vulnerabilities help strengthen the entire cloud security ecosystem.

## 📧 **Professional Contact**

**Tope Adekeye**  
📧 adekeyetopeaiexpert@gmail.com  
🏢 **Specialization**: Governance • Risk • Compliance • AI Ethics • Cloud Security  
🔗 [LinkedIn](https://linkedin.com/in/tope-adekeye) | [GitHub](https://github.com/Tope-Adekeye)

---

> **Disclaimer**: This tool is for authorized security testing only. Users are responsible for ensuring compliance with all applicable laws, regulations, and organizational policies. Unauthorized access to cloud resources is illegal and unethical.

*Part of the [Cyber-Security-Projects](https://github.com/Tope-Adekeye/Cyber-Security-Projects) collection*
