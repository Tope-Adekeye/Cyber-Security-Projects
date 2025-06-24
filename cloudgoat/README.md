# ☁️ CloudGoat - Vulnerable AWS Environment Lab

**"Vulnerable by Design" cloud deployment tool for hands-on AWS security training**

[![Python](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/downloads/)
[![AWS](https://img.shields.io/badge/Cloud-AWS-orange.svg)](#)
[![Terraform](https://img.shields.io/badge/IaC-Terraform-purple.svg)](#)
[![License](https://img.shields.io/badge/License-BSD--3--Clause-green.svg)](LICENSE)

## 🎯 Overview

CloudGoat is a powerful **"Vulnerable by Design"** cloud deployment tool that creates intentionally vulnerable AWS environments for cybersecurity training and penetration testing practice. This tool allows security professionals to develop and hone their cloud security skills through structured capture-the-flag style scenarios.

### 🚀 **Key Features**
- **Multi-Scenario Learning**: 20+ diverse cloud security scenarios
- **Capture-the-Flag Style**: Structured learning with clear objectives
- **Real AWS Resources**: Hands-on experience with actual cloud infrastructure
- **Multiple Attack Paths**: Various routes to achieve scenario goals
- **Terraform-Based**: Infrastructure as Code for consistent deployments
- **Easy Management**: Simple deployment, reset, and cleanup commands

## 🛠️ **Installation & Setup**

### **Prerequisites**
- Python 3.7+ and pip3
- AWS CLI configured with appropriate permissions
- Terraform installed (0.12+ recommended)
- Valid AWS account with billing enabled

### **Quick Installation**
```bash
# Install dependencies
pip3 install -r core/python/requirements.txt

# Configure AWS profile
aws configure --profile cloudgoat

# Initialize CloudGoat
python3 cloudgoat.py config profile cloudgoat
python3 cloudgoat.py config whitelist --auto
```

### **Docker Installation**
```bash
# Build the Docker image
docker build -t cloudgoat .

# Run with AWS credentials
docker run -it -v ~/.aws:/root/.aws cloudgoat
```

## 📋 **Getting Started**

### **Basic Commands**
```bash
# List available scenarios
python3 cloudgoat.py list

# Create a scenario
python3 cloudgoat.py create [scenario-name]

# Get scenario information
python3 cloudgoat.py [scenario-name] help

# Destroy scenario resources
python3 cloudgoat.py destroy [scenario-name]

# Configuration management
python3 cloudgoat.py config [option]
```

## 🎮 **Available Scenarios**

### **Beginner Level**
- **cloud_breach_s3**: S3 bucket enumeration and data exfiltration
- **vulnerable_lambda**: Serverless function exploitation
- **ec2_ssrf**: Server-Side Request Forgery in EC2 environments

### **Intermediate Level**
- **privilege_escalation_via_iam**: IAM permission escalation
- **codebuild_secrets**: CI/CD pipeline secret extraction
- **rce_web_app**: Remote code execution through web applications

### **Advanced Level**
- **cloud_breach_s3_advanced**: Complex multi-service attack chains
- **iam_privesc_by_rollback**: Advanced IAM privilege escalation
- **lambda_privesc**: Complex serverless privilege escalation

## 🎯 **Learning Objectives**

### **Cloud Security Skills**
- **AWS Service Exploitation**: S3, Lambda, EC2, IAM, RDS
- **Privilege Escalation**: Various IAM and service-based techniques
- **Data Exfiltration**: Multiple methods for extracting sensitive data
- **Lateral Movement**: Moving between AWS services and accounts
- **Defense Evasion**: Avoiding detection mechanisms

### **Professional Applications**
- **Red Team Training**: Realistic cloud attack scenarios
- **Blue Team Education**: Understanding attack vectors for defense
- **Penetration Testing**: Hands-on cloud security assessment skills
- **Security Research**: Safe environment for testing new techniques

## 🔒 **Responsible Use & Safety**

### **Important Security Notes**
- ⚠️ **Isolated Environment**: Always use dedicated AWS accounts
- ⚠️ **Cost Management**: Monitor AWS billing during exercises
- ⚠️ **Resource Cleanup**: Always destroy scenarios when finished
- ⚠️ **Network Security**: Proper IP whitelisting is critical

### **Best Practices**
- Use separate AWS accounts for CloudGoat training
- Implement billing alerts and spending limits
- Regular cleanup of unused resources
- Document findings and learning outcomes

## 📧 **Professional Contact**

**Tope Adekeye**  
📧 adekeyetopeaiexpert@gmail.com  
🏢 **Specialization**: Governance • Risk • Compliance • AI Ethics • Cloud Security  
🔗 [LinkedIn](https://www.linkedin.com/in/temitope-adekeye-001a04359/) | [GitHub](https://github.com/Tope-Adekeye)

---

> **Disclaimer**: CloudGoat creates intentionally vulnerable cloud resources. Use only in isolated environments with proper authorization. Users are responsible for all AWS costs and ensuring compliance with applicable laws and organizational policies.

*Part of the [Cyber-Security-Projects](https://github.com/Tope-Adekeye/Cyber-Security-Projects) collection*
