# AWS Security, IAM & Organizations | AWS Cloud Practitioner Notes

## Overview
This document summarizes my understanding of **AWS Security, Identity & Access Management (IAM), Organizations, Compliance, and Security Services**.

The goal of this document is to demonstrate **strong foundational knowledge, structured thinking, and practical understanding of securing cloud environments using AWS**.

---

# AWS Shared Responsibility Model

## Concept
AWS follows a **Shared Responsibility Model**, where security responsibilities are divided between AWS and the customer.

- **AWS → Security OF the Cloud**
- **Customer → Security IN the Cloud**

---

## AWS Responsibilities
- Physical data centers
- Hardware and infrastructure
- Global networking
- Managed services security

---

## Customer Responsibilities
- Data protection and encryption
- Application security
- IAM configuration (users, groups, roles, permissions)
- OS and software updates (for IaaS)

---

## Service Model Comparison

| Service Type | Responsibility |
|-------------|--------------|
| IaaS        | Customer manages OS and applications |
| PaaS        | Customer manages application code |
| SaaS        | Customer manages data and access |

---

# Security and Compliance

## What is Compliance?
Compliance refers to following **industry standards and legal regulations**.

### Examples:
- **PCI-DSS** → Payment data security
- **HIPAA** → Healthcare data protection

---

## AWS Compliance Support
- Regular audits and certifications
- Global compliance standards
- Audit reports available on demand

---

## Key Services

### AWS Artifact
- Provides access to compliance reports and certifications

### AWS Customer Compliance Center
- Helps understand regulatory requirements

### AWS Audit Manager
- Automates compliance checks
- Generates audit-ready reports

### AWS Config
- Tracks and records configuration changes

---

# AWS Identity and Access Management (IAM)

## Root User
- Has full administrative access
- Should not be used for daily tasks

---

## IAM Components

### IAM Users
- Individual identities (users/applications)
- No permissions by default

---

### IAM Groups
- Collection of IAM users
- Used to assign permissions to multiple users at once
- Simplifies access management

**Example:**  
A "Developers" group can have S3 and EC2 access, and all users in that group inherit those permissions.

---

### IAM Policies
- Define permissions using JSON
- Control what actions are allowed or denied

Example:
```json
{
  "Effect": "Allow",
  "Action": "s3:GetObject",
  "Resource": "*"
}

# AWS IAM, Organizations & Security Services – Notes

---

## IAM Roles
- Provide temporary permissions  
- Used for secure access and delegation  
- Common in cross-account access or AWS services  

---

## Principle of Least Privilege
Grant only the minimum permissions required to perform tasks.

---

## Multi-Factor Authentication (MFA)
- Adds an extra security layer  
- Requires password + OTP  

---

## IAM Practical Workflow
1. Create IAM user  
2. User has no permissions initially  
3. Attempted actions fail  
4. Attach policy to grant access  
5. Add user to group for easier management  
6. Use roles for temporary elevated access  

---

# AWS Organizations

## Purpose
AWS Organizations helps manage multiple AWS accounts centrally.

---

## Benefits
- Centralized billing  
- Simplified account management  
- Improved security governance  

---

## Key Components

### Organizational Units (OUs)
- Group accounts based on function (Dev, Prod)

### Service Control Policies (SCPs)
- Define maximum permissions at account level  
- Restrict actions across accounts  

---

---

# AWS Security Services

AWS security services are categorized into three types:

---

## 1. Preventative Services

| Service | Purpose |
|--------|--------|
| AWS WAF | Protects web applications from attacks |
| AWS Shield | Protects against DDoS attacks |
| AWS Network Firewall | Controls VPC network traffic |

---

## 2. Detection Services

| Service | Purpose |
|--------|--------|
| GuardDuty | Detects suspicious activity |
| Inspector | Identifies vulnerabilities |
| CloudTrail | Logs API and user activity |
| AWS Config | Tracks configuration changes |
| Detective | Investigates security issues |
| Security Hub | Centralized security alerts |
| Security Lake | Aggregates security logs |
| Macie | Detects sensitive data in S3 |

---

## 3. Management Services

| Service | Purpose |
|--------|--------|
| IAM | Access control management |
| IAM Identity Center | Multi-account access management |
| Secrets Manager | Secure storage of credentials |
| Certificate Manager | SSL/TLS certificate management |
| KMS | Encryption key management |
| CloudHSM | Hardware-based key security |
| Cognito | User authentication for applications |
| Firewall Manager | Centralized firewall management |
| Resource Access Manager | Secure resource sharing |

---

# Cryptographic Security

## AWS Key Management Service (KMS)
- Create and manage encryption keys  
- Supports automatic key rotation  

---

## AWS CloudHSM
- Provides hardware security modules  
- Secure storage for cryptographic keys  

---

# Key Takeaways
- AWS follows a Shared Responsibility Model  
- IAM manages users, groups, roles, and permissions  
- Organizations simplify multi-account management  
- Security services help prevent, detect, and manage threats  
- Always follow the principle of least privilege  

---

# Learning Outcome

Through this study, I have developed:

- Understanding of AWS security fundamentals  
- Knowledge of IAM and access control mechanisms  
- Awareness of compliance and governance  
- Familiarity with AWS security services  

---

# Future Learning Goals
- Hands-on IAM and security configurations  
- Implement real-world AWS security architectures  
- Learn advanced monitoring and threat detection  
- Integrate security in DevOps workflows (DevSecOps)  

---

> This document reflects my understanding of AWS security concepts and my commitment to building secure, scalable cloud solutions.