# Log-Analysis-Network-Traffic-Investigation-using-Wireshark-in-Linux-Kali-
This project demonstrates hands-on log analysis and network traffic investigation techniques used in a Security Operations Center (SOC) environment. The objective is to identify suspicious activities such as brute-force attacks, privilege escalation, and anomalous network behavior using Linux system logs and packet analysis tools.

The analysis aligns with industry-standard security frameworks including NIST, MITRE ATT&CK, ISO/IEC 27001, and OWASP Top 10.

## Objectives
- Detect brute-force login attempts and unauthorized access
- Identify privilege escalation and suspicious user activity
- Analyze DNS and HTTP traffic for anomalies
- Correlate host-based logs with network-level evidence
- Map findings to standard security frameworks

## Tools & Environment
- Operating System: Kali Linux / Ubuntu
- Log Sources:
  - auth.log
  - syslog
  - SSH logs
- Network Analysis:
  - Wireshark
  - tcpdump
- Protocols Analyzed:
  - DNS
  - HTTP

## Methodology

### 1. Log Collection & Review
- Collected authentication and system logs from Linux hosts
- Filtered logs for failed login attempts, sudo usage, and user account changes

### 2. Threat Detection
- Identified brute-force attempts through repeated failed SSH logins
- Detected privilege escalation via abnormal sudo activity
- Investigated suspicious account behavior such as logins at unusual times

### 3. Network Traffic Analysis
- Captured network traffic using Wireshark and tcpdump
- Inspected DNS queries for suspicious domains
- Analyzed HTTP sessions for abnormal request patterns

### 4. Evidence Correlation
- Correlated log events with network traffic to validate potential security incidents

## MITRE ATT&CK Mapping

| Technique ID | Technique Name | Evidence |
|-------------|----------------|----------|
| T1110 | Brute Force | Repeated failed SSH login attempts |
| T1078 | Valid Accounts | Suspicious successful logins |
| T1548 | Abuse Elevation Control Mechanism | Unauthorized sudo usage |
| T1046 | Network Service Discovery | Abnormal DNS activity |

## NIST Cybersecurity Framework Alignment

- Identify: Review of system and authentication logs
- Detect: Detection of brute-force and anomalous network traffic
- Respond: Incident investigation using log correlation
- Recover: Recommendations for access hardening and monitoring

## ISO/IEC 27001 Mapping
- A.12.4 – Logging and Monitoring
- A.9 – Access Control
- A.13 – Network Security Management

## OWASP Top 10 Relevance
- A2: Broken Authentication – Brute-force detection
- A5: Security Misconfiguration – Excessive SSH exposure
- A10: Insufficient Logging & Monitoring – Importance of log analysis

## Findings & Analysis
- Evidence of brute-force SSH attempts from external IP addresses
- Multiple failed authentication attempts followed by a successful login
- Suspicious DNS queries indicating possible reconnaissance activity

/'Detailed analysis and screenshots are provided in the `/screenshots` directory.'

## Security Recommendations
- Enforce SSH key-based authentication
- Implement fail2ban for brute-force mitigation
- Restrict sudo privileges using least-privilege principles
- Enable centralized log monitoring and alerting

## Lab Environment
- The analysis was conducted in a controlled virtual lab environment.
- Virtual Machine: Kali Linux / Ubuntu (hosted on VirtualBox / VMware)
- Purpose: Safe simulation of attack and investigation scenarios
- Logs and network traffic were generated within the VM to replicate real-world SOC investigations.


## Disclaimer
This project is for educational and demonstration purposes only. All logs and traffic captures were generated in a controlled lab environment.

