# 🔍 TestMyNIDS - Network Intrusion Detection System Testing Framework

**Comprehensive NIDS effectiveness validation tool for enterprise security operations**

[![Stars](https://img.shields.io/badge/GitHub-264%20stars-yellow.svg)](https://github.com/Tope-Adekeye/Cyber-Security-Projects/tree/main/testmynids)
[![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20macOS-blue.svg)](#)
[![NIDS](https://img.shields.io/badge/NIDS-Snort%20%7C%20Suricata-green.svg)](#)
[![License](https://img.shields.io/badge/License-Open%20Source-red.svg)](#)

## 🎯 Overview

TestMyNIDS is a **specialized framework for testing Network Intrusion Detection Systems (NIDS) effectiveness**, developed by **3CORESec**. This essential tool validates that enterprise NIDS deployments like Snort, Suricata, and other network security monitoring systems are properly detecting malicious activities and policy violations.

**Critical for SOC operations** - TestMyNIDS provides a standardized methodology to verify detection coverage across multiple attack vectors, ensuring your network security monitoring infrastructure is functioning optimally.

### 🚀 **Key Capabilities**

- **15+ Attack Simulation Tests**: Comprehensive coverage of common attack patterns
- **Multi-Protocol Testing**: HTTP, HTTPS, DNS, SSH, TLS validation
- **Ruleset Validation**: Tests against ET Open and commercial rulesets
- **Portable Framework**: Minimal dependencies with curl and nc
- **Immediate Results**: Quick validation of NIDS detection capabilities
- **SOC Integration**: Perfect for security operations center validation workflows

## 📋 **Comprehensive Test Coverage**

### **🌐 Web-Based Attacks**
- **HTTP Policy Violations**: Gaming, adware, and inappropriate content detection
- **Malicious User Agents**: Known malware and bot user agent strings
- **Command & Control**: C2 beacon simulation and communication patterns
- **File Downloads**: Malicious executables and embedded file detection

### **🔐 Cryptographic & Certificate Tests**
- **Bad Certificates**: Known malicious Certificate Authorities
- **TLS Anomalies**: Certificate validation and trust issues
- **Encrypted Traffic**: Suspicious encrypted communication patterns

### **🌍 DNS & Network Tests**
- **Malicious Domains**: Sinkhole, DGA, and known bad domains
- **Tor Detection**: .onion domains and Tor node connections
- **DNS Tunneling**: Suspicious DNS query patterns
- **URL Shorteners**: Potentially malicious redirect services

### **🔧 Protocol-Specific Tests**
- **SSH Scanning**: Outbound SSH port scanning simulation
- **Authentication**: Clear-text credential transmission
- **Anonymous Services**: File sharing and privacy service detection

## 🛠️ **Enterprise Implementation**

### **Quick Deployment**
```bash
# One-liner installation and interactive mode
curl -sSL https://github.com/Tope-Adekeye/Cyber-Security-Projects/raw/main/testmynids/tmNIDS -o /tmp/tmNIDS && chmod +x /tmp/tmNIDS && /tmp/tmNIDS

# Script mode with help
curl -sSL https://github.com/Tope-Adekeye/Cyber-Security-Projects/raw/main/testmynids/tmNIDS -o /tmp/tmNIDS && chmod +x /tmp/tmNIDS && /tmp/tmNIDS -h
```

### **Manual Installation**
```bash
# Clone from Tope Adekeye's cybersecurity portfolio
git clone https://github.com/Tope-Adekeye/Cyber-Security-Projects.git
cd Cyber-Security-Projects/testmynids
chmod +x tmNIDS

# Interactive mode
./tmNIDS

# Script mode - run specific test
./tmNIDS -5  # Run Tor detection test
```

### **System Requirements**
- **Linux/macOS**: Any modern distribution
- **Dependencies**: curl and nc (pre-installed on most systems)
- **Network Access**: Internet connectivity for external test validation
- **Privileges**: Standard user permissions (no root required)

## 🎯 **Detailed Test Matrix**

| **Test ID** | **Attack Simulation** | **Detection Focus** | **Protocols** |
|-------------|----------------------|-------------------|---------------|
| **1** | Linux UID Enumeration | System reconnaissance | HTTP |
| **2** | Basic Auth Clear Text | Credential exposure | HTTP |
| **3** | Malware User Agents | Known malware signatures | HTTP |
| **4** | Bad Certificates | Certificate validation | TLS, DNS, TCP |
| **5** | Tor Networks | Anonymity service usage | DNS, TLS |
| **6** | EXE Downloads | Malicious file download | HTTP |
| **7** | PDF w/ Embedded Files | Document-based attacks | HTTP |
| **8** | SSH Port Scanning | Network reconnaissance | SSH |
| **9** | Miscellaneous Domains | Various malicious domains | DNS |
| **10** | Anonymous File Sharing | Data exfiltration services | DNS, TLS |
| **11** | IP Lookup Services | Reconnaissance activities | HTTP, DNS, TLS |
| **12** | URL Shorteners | Redirect-based attacks | DNS |
| **13** | Gaming Policy Violation | Workplace policy enforcement | HTTP |
| **14** | Adware PUP | Potentially unwanted programs | HTTP |
| **15** | C2 Beacon | Command & control communication | HTTP |
| **99** | **CHAOS Mode** | **All tests simultaneously** | **ALL** |

## 🏗️ **SOC Integration Workflows**

### **NIDS Validation Process**
```bash
# Daily NIDS health check
./tmNIDS -99  # Run all tests for comprehensive validation

# Specific threat validation
./tmNIDS -4   # Test certificate validation
./tmNIDS -5   # Test Tor detection
./tmNIDS -15  # Test C2 beacon detection
```

### **Incident Response Testing**
```bash
# Validate detection during incident response
./tmNIDS -8   # Test SSH scanning detection
./tmNIDS -6   # Test malware download detection
./tmNIDS -10  # Test data exfiltration detection
```

### **Compliance Validation**
```bash
# Regular compliance testing schedule
./tmNIDS -2   # Clear-text authentication
./tmNIDS -13  # Policy violation detection
./tmNIDS -11  # Reconnaissance detection
```

## 📊 **Enterprise Use Cases**

### **Security Operations Center (SOC)**
- **Daily Health Checks**: Automated NIDS functionality validation
- **Shift Handover**: Quick verification of detection capabilities
- **Incident Response**: Validate detection during active investigations
- **New Analyst Training**: Hands-on NIDS testing and understanding

### **Security Engineering**
- **Ruleset Tuning**: Validate custom rule effectiveness
- **Platform Migration**: Test detection consistency across NIDS platforms
- **Performance Testing**: Measure detection impact on network performance
- **Vendor Evaluation**: Compare NIDS solution effectiveness

### **Compliance & Audit**
- **Regulatory Requirements**: Demonstrate network monitoring effectiveness
- **Security Control Validation**: Prove detection capability compliance
- **Risk Assessment**: Quantify network security monitoring coverage
- **Audit Evidence**: Document security monitoring effectiveness

## 🔧 **Advanced Configuration**

### **Custom Test Development**
The framework supports custom test development for organization-specific threats:

```bash
# Example: Custom domain testing
echo "malicious-domain.com" >> custom_domains.txt
./tmNIDS --custom-domains custom_domains.txt
```

### **SIEM Integration**
```bash
# Log output for SIEM ingestion
./tmNIDS -99 2>&1 | logger -t "testmynids"

# JSON output for structured logging
./tmNIDS --json-output -15
```

### **Automated Testing**
```bash
# Cron job for regular testing
0 */6 * * * /opt/testmynids/tmNIDS -99 >> /var/log/nids-testing.log 2>&1
```

## 🎓 **Professional Development Value**

### **Skill Enhancement**
- **NIDS Technology**: Deep understanding of network intrusion detection
- **Threat Simulation**: Practical attack pattern knowledge
- **Security Validation**: Systematic security control testing
- **SOC Operations**: Essential SOC analyst and engineer skills

### **Certification Alignment**
- **GIAC GCIA**: GIAC Certified Intrusion Analyst techniques
- **SANS SEC503**: Intrusion Detection In-Depth methodology
- **GCIH**: GIAC Certified Incident Handler validation processes
- **CCNA Security**: Network security monitoring best practices

### **Career Applications**
- **SOC Analyst**: Daily validation and monitoring procedures
- **Security Engineer**: NIDS deployment and optimization
- **Incident Responder**: Detection validation during investigations
- **Security Architect**: Network security monitoring design

## 🔒 **Security Considerations**

### **Testing Best Practices**
- **Controlled Environment**: Use dedicated test networks when possible
- **Authorization**: Ensure proper approval for testing activities
- **Documentation**: Log all testing activities for audit purposes
- **Coordination**: Notify SOC teams before comprehensive testing

### **Enterprise Guidelines**
- Test during maintenance windows for initial deployment validation
- Establish baseline detection rates for ongoing monitoring
- Document any detection gaps for remediation planning
- Regular testing schedule aligned with security operations

## 🤝 **Integration with Security Stack**

### **NIDS Platforms**
- **Snort**: Open source and commercial rule validation
- **Suricata**: IDS/IPS effectiveness testing
- **Zeek (Bro)**: Network analysis platform validation
- **Commercial Solutions**: Vendor-specific detection testing

### **Ruleset Compatibility**
- **Emerging Threats Open**: Community ruleset validation
- **Snort VRT**: Official Snort rules effectiveness
- **Custom Rules**: Organization-specific detection validation
- **Threat Intelligence**: IOC-based rule testing

### **SIEM Integration**
- **Splunk**: NIDS alert validation and correlation
- **Elastic Security**: Network security monitoring validation
- **IBM QRadar**: Network event correlation testing
- **Microsoft Sentinel**: Cloud-native NIDS integration

## 📈 **Business Value & ROI**

### **Cost Savings**
- **Preventive Validation**: Catch detection gaps before incidents
- **Reduced False Negatives**: Ensure critical threats are detected
- **Optimized Performance**: Balance detection and network performance
- **Vendor Accountability**: Validate commercial NIDS effectiveness

### **Risk Reduction**
- **Detection Assurance**: Confirm security monitoring effectiveness
- **Compliance Confidence**: Meet regulatory monitoring requirements
- **Incident Preparedness**: Validate detection during critical events
- **Security Maturity**: Demonstrate proactive security testing

## 🏆 **Framework Advantages**

### **Technical Benefits**
- **Lightweight**: Minimal system resource requirements
- **Portable**: Single script deployment across environments
- **Comprehensive**: Multi-protocol and multi-vector testing
- **Immediate**: Instant validation results

### **Operational Benefits**
- **Standardized**: Consistent testing methodology
- **Repeatable**: Automated and scheduled testing capability
- **Documented**: Clear test descriptions and expected outcomes
- **Community-Driven**: Open source with active development

## 📧 **Professional Contact**

**Tope Adekeye**  
📧 adekeyetopeaiexpert@gmail.com  
🏢 **Specialization**: Governance • Risk • Compliance • AI Ethics • Cloud Security  
🔗 [LinkedIn](https://www.linkedin.com/in/temitope-adekeye-001a04359/) | [GitHub](https://github.com/Tope-Adekeye)

---

> **Professional Note**: TestMyNIDS provides essential validation capabilities for enterprise network security monitoring. Regular testing ensures detection systems maintain effectiveness against evolving threats. This framework should be integrated into standard SOC operations and security engineering workflows.

*Part of the [Cyber-Security-Projects](https://github.com/Tope-Adekeye/Cyber-Security-Projects) collection*

**Security Impact**: Validates NIDS effectiveness and ensures network security monitoring systems detect malicious activities, providing confidence in enterprise threat detection capabilities.

**Professional Value**: Demonstrates expertise in network security monitoring, NIDS technologies, and security validation methodologies - essential skills for SOC operations and security engineering roles.
