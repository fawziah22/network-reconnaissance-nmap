# Network Reconnaissance with Nmap

## Project Overview

This project demonstrates network reconnaissance techniques using Nmap in a controlled cybersecurity training lab environment. The objective was to identify exposed network services, perform service enumeration, and analyze potential security risks associated with publicly accessible ports.

Network reconnaissance is a critical step in security assessments because it helps identify a system’s attack surface before deeper vulnerability analysis.

---

## Lab Environment

| Component | Description |
|-----------|-------------|
| Environment | Controlled cybersecurity training lab |
| Target | Authorized training host |
| Sanitized IP | 203.0.113.100 |
| Tool Used | Nmap |
| Scanning System | Kali Linux |

**Note:** The IP address is sanitized for documentation purposes.

---

## Objectives

The goals of this project were to:

- Identify exposed network services  
- Enumerate service versions  
- Analyze potential attack vectors  
- Understand the system's attack surface  
- Provide security recommendations  

---

## Tools Used

- **Nmap** – Network reconnaissance and scanning tool  
- **Kali Linux Terminal** – Used to execute scanning commands  

---

## Methodology

The reconnaissance process was conducted in three stages to progressively gather information about the target system.

### 1. Basic Network Scan

A basic Nmap scan was performed to identify open ports and exposed network services on the target system.

Command used:

```bash
nmap 203.0.113.100
2. Service and Script Enumeration
Service version detection and default script scanning were conducted to gather additional information about exposed services.
Command used:
nmap -sC -sV 203.0.113.100
This scan identifies:
service versions
server configuration details
additional information about network services
3. Advanced Reconnaissance Scan
An advanced Nmap scan was performed to gather deeper intelligence about the target system.
Command used:
nmap -A 203.0.113.100
This scan enables:
OS detection
advanced service detection
script scanning
traceroute analysis
Key Findings
The scan identified multiple exposed services running on the host.
Port	Service	Description
21	FTP	File transfer service
23	Telnet	Remote login protocol
25	SMTP	Mail transfer service
80	HTTP	Web server
110	POP3	Email retrieval service
443	HTTPS	Secure web service
1099	RMI Registry	Java remote service
3306	MySQL	Database service
3389	RDP	Remote desktop service
5432	PostgreSQL	Database service
8180	Application Service	Web application port
These services increase the potential attack surface of the system.
Attack Surface Analysis
The reconnaissance process identified multiple exposed services on the target host. Each open port represents a potential entry point that could be leveraged by an attacker if the service is misconfigured, outdated, or improperly secured.
Examples of potential attack vectors include:
Telnet (Port 23)
Telnet is a legacy remote administration protocol that transmits authentication data in plaintext. Attackers may intercept credentials using packet sniffing or man-in-the-middle attacks.
Remote Desktop Protocol (Port 3389)
Publicly exposed RDP services are frequently targeted by brute-force attacks. If weak credentials are used, attackers may gain full remote access to the system.
Database Services (Ports 3306 and 5432)
Database services are typically intended for internal network access only. Public exposure increases the risk of unauthorized access or data exfiltration.
Security Recommendations
Based on the findings, the following security improvements are recommended:
Disable insecure legacy protocols such as Telnet and FTP
Restrict database services to internal networks
Limit RDP access using firewall rules or VPN access
Regularly update and patch all exposed services
Monitor network activity for suspicious behavior
Reconnaissance Workflow
Target Identification
        ↓
Basic Nmap Scan
        ↓
Service & Script Enumeration
        ↓
Advanced Reconnaissance
        ↓
Attack Surface Analysis
Ethical Use Notice
All scans performed in this project were conducted in a controlled and authorized cybersecurity training environment for educational purposes only.
