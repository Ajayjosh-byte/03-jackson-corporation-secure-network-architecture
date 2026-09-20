# 03-jackson-corporation-secure-network-architecture
# Jackson Corporation — Secure Network Architecture

## Project Overview

This project demonstrates the design of a secure network architecture
for Jackson Corporation following an assessment of identified
cybersecurity weaknesses.

The project was completed as part of the Cybersecurity Architecture
course on Coursera, delivered in partnership with IBM and sponsored by
Digital Training Academy.

The architecture was designed to address identified security
challenges through network segmentation, layered security controls,
secure remote access, web application protection, threat detection,
centralized monitoring, and protection of sensitive information.

> **Note:** Jackson Corporation is presented as a project scenario for
> educational and portfolio purposes.


## My Role

I analyzed the identified security challenges and developed the
security recommendations used as the basis for the architecture.

I then translated those recommendations into a secure network
architecture using Draw.io.

The project demonstrates my ability to move from:

**Security Problem → Security Recommendation → Security Architecture**

## Project Objectives

The architecture was designed to:

- Separate untrusted, semi-trusted, and trusted network environments
- Protect internet-facing services from the internal network
- Implement layered firewall protection
- Protect web applications against common attacks
- Provide secure remote access
- Detect and respond to suspicious network activity
- Centralize security logging and monitoring
- Protect sensitive information
- Apply least-privilege principles
- Improve network visibility and security resilience

# Security Architecture

The network is divided into three primary security zones:

### 1. Internet Zone — Untrusted

Contains external users and internet-facing traffic.

Traffic entering the organization passes through perimeter
security controls before reaching protected resources.

### 2. DMZ Zone — Semi-Trusted

The DMZ contains services that need to communicate with external
users while remaining isolated from the internal network.

The web server was relocated to the DMZ as part of the security
architecture.

### 3. Internal Zone — Trusted

Contains internal business systems and sensitive resources,
including:

- Application servers
- Database servers
- Employee workstations
- Protected internal services
- Monitoring and security infrastructure

# Security Controls

## External Firewall

The external firewall provides perimeter protection between the
Internet and DMZ.

It filters incoming and outgoing traffic according to defined
security rules.

## Internal Firewall

The internal firewall separates the DMZ from the trusted internal
network.

Only authorized traffic is permitted between the DMZ and internal
systems.

This provides an additional security layer if an internet-facing
system is compromised.

## Web Application Firewall (WAF)

A WAF protects the web application from malicious HTTP/HTTPS
requests and supports protection against common web application
threats.

The architecture also considers application-level protections such
as:

- Input validation
- Input sanitization
- Parameterized queries
- Secure error handling
- Protection against common OWASP risks

## IDS/IPS

The IDS/IPS provides network threat detection and monitoring.

It can identify suspicious activity and generate security alerts,
while IPS capabilities can support automated blocking of recognized
malicious traffic.

## VPN Gateway

Remote employees access internal resources through an encrypted VPN
connection.

The architecture incorporates:

- Encrypted remote access
- Multi-factor authentication
- Role-based access control
- Restricted access to authorized resources

# Core Infrastructure

### Web Server

The web server is located in the DMZ rather than directly inside the
internal network.

This limits the potential impact of a compromise of the
internet-facing server.

### Application Servers

Application servers are placed inside the trusted internal zone.

They communicate with the web layer through controlled and
authorized internal connections.

### Database Servers

Database servers are located within the internal trusted zone.

Sensitive information is protected through network segmentation,
restricted access, encryption, and controlled application-to-database
communication.

### Employee Workstations

Employee workstations remain within the trusted internal environment
and communicate with authorized internal applications.

### Monitoring / SIEM

A centralized SIEM collects and correlates security logs from
multiple infrastructure components.

The architecture provides centralized visibility across:

- Firewalls
- WAF
- IDS/IPS
- VPN Gateway
- Web Server
- Application Servers
- Database Servers
- Employee Workstations

# Traffic Flow

A typical external customer request follows the security path:

Internet

↓

External Firewall

↓

WAF

↓

Web Server in DMZ

↓

Internal Firewall

↓

Application Server

↓

Encrypted database connection

↓

Database Server

This architecture prevents external users from directly accessing
the internal network.

# Secure Remote Access Flow

Remote Employee

↓

Encrypted VPN Connection

↓

VPN Gateway

↓

Internal Firewall

↓

Authorized Internal Resources

Remote access is controlled through authentication, authorization,
encryption, and access restrictions.

# Data Protection

Sensitive information should be protected both:
- In transit
- At rest

The architecture therefore incorporates encrypted communication,
protected database infrastructure, access restrictions, least
privilege, and protected backups.


# Security Principles Applied

The architecture applies several important cybersecurity principles:

### Defense in Depth

Multiple security controls are implemented rather than relying on a
single security mechanism.

### Network Segmentation

Security zones limit unnecessary communication between systems with
different trust levels.

### Least Privilege

Users and systems should receive only the access required for their
authorized responsibilities.

### Secure Remote Access

Remote users access protected resources through an encrypted and
controlled VPN connection.

### Centralized Monitoring

Security events are collected and analyzed through centralized
monitoring and SIEM capabilities.

### Data Protection

Sensitive information is protected through encryption, access
controls, segmentation, and backup measures.


# Key Architecture Decisions
| Security Challenge | Architecture Response |
| Web server exposed to internal network | Relocated web server to DMZ |
| Single firewall | Added external and internal firewall layers |
| Web application threats | Added WAF |
| Limited threat detection | Added IDS/IPS |
| Unsecured remote access | Added VPN Gateway |
| Limited security visibility | Added centralized SIEM |
| Sensitive database exposure | Protected database in Internal Zone |
| Uncontrolled internal access | Applied segmentation and least privilege |
| Unencrypted sensitive traffic | Specified encrypted connections |
| Recovery requirements | Added protected backup infrastructure |


# Architecture Diagram
The main architecture diagram was created using Draw.io.

![Jackson Corporation Secure Network Architecture](Jackson_Corporation_Secure_Network_Architecture.png)


# Project Deliverables
- Secure network architecture diagram
- Editable Draw.io architecture file
- Network security-zone design
- Security control placement
- Traffic-flow mapping
- Security annotations
- Architecture legend

# Skills Demonstrated
- Cybersecurity Architecture
- Network Security
- Network Segmentation
- Security Zone Design
- Firewall Architecture
- DMZ Design
- WAF
- IDS/IPS
- SIEM
- VPN Architecture
- Secure Remote Access
- Data Protection
- Security Controls
- Defense in Depth
- Least Privilege
- Security Documentation
- Draw.io Network Diagramming
- Security Architecture Analysis


# Tools & Training

**Diagramming Tool**
- Draw.io

**Training**
- Cybersecurity Architecture — Coursera
- IBM-linked cybersecurity training
- Digital Training Academy sponsorship

## Disclaimer
This project was completed as an educational cybersecurity
architecture exercise based on a fictional organizational scenario.
The architecture is intended to demonstrate security analysis,
design, and documentation skills and does not represent an actual
production deployment.
