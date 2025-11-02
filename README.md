# FEDLIN – AWS Security Baseline

[![Terraform](https://img.shields.io/badge/IaC-Terraform_5.0+-623CE4?logo=terraform)](https://www.terraform.io/)
[![AWS](https://img.shields.io/badge/Cloud-AWS-FF9900?logo=amazon-aws)](https://aws.amazon.com/)
[![ISO 27001](https://img.shields.io/badge/ISO%2027001-Mapped-1f77b4)](#compliance-coverage)
[![SOC 2](https://img.shields.io/badge/SOC%202-Mapped-d62728)](#compliance-coverage)
[![NIST 800-53](https://img.shields.io/badge/NIST%20800--53-Mapped-2ca02c)](#compliance-coverage)
[![HIPAA](https://img.shields.io/badge/HIPAA-Mapped-9467bd)](#compliance-coverage)
[![Maintained](https://img.shields.io/badge/Maintained-Yes-green)](#)

**Customer-tenant-first AWS security hardening without taking ownership of your cloud**

Deploy enterprise-grade AWS security controls in 3-5 business days with 100% customer-retained evidence.

[📧 Contact](mailto:info@fedlin.com) · [📞 Book Consultation](https://calendar.app.google/7z8eAZPvrW82jtxk6) · [🌐 fedlin.com](https://www.fedlin.com)

---

## 🎯 What This Delivers

A comprehensive security baseline for AWS environments preparing for compliance audits or requiring repeatable security hardening.

**Designed for:**
- **Compliance teams** preparing for SOC 2, ISO 27001, HIPAA, or NIST assessments
- **Organizations** needing automated security controls with audit-ready evidence
- **MSPs/MSSPs** requiring standardized security deployment across client accounts
- **Security teams** implementing AWS security best practices at scale

**Key capabilities:**
- Core AWS security services enabled (GuardDuty, Security Hub, Config, CloudTrail)
- 40-60 automated compliance checks mapped to regulatory frameworks
- Multi-region security coverage
- OIDC-only deployment (zero long-lived credentials)
- Customer-retained evidence and logs

---

## 🏗️ Security Services Configured

### AWS Security Services

| Service | Purpose | Evidence Output |
|---------|---------|-----------------|
| **AWS CloudTrail** | API audit logging (all regions) | Encrypted S3 logs, validation digests |
| **AWS Config** | Resource compliance tracking | Config snapshots, rule evaluations, compliance timelines |
| **Amazon GuardDuty** | Threat detection | Finding exports, threat intelligence |
| **AWS Security Hub** | Centralized security findings | Compliance scores, CIS benchmarks |
| **IAM Access Analyzer** | Unused access detection | External access findings, policy validation |
| **AWS KMS** | Encryption key management | Key policies, rotation status |
| **VPC Flow Logs** | Network traffic monitoring (optional) | Flow records, traffic analysis |
| **CloudWatch Logs** | Centralized log aggregation | Log groups, metric filters, retention policies |

### Modular Terraform Architecture
```
terraform/
├── modules/
│   ├── logging/       # Centralized logging infrastructure
│   ├── cloudtrail/    # Multi-region CloudTrail with KMS
│   ├── config/        # AWS Config with compliance rules
│   ├── guardduty/     # Threat detection service
│   ├── securityhub/   # Security findings aggregation
│   ├── iam/           # IAM password policy, access analyzer
│   └── kms/           # Encryption key management
└── main.tf            # Orchestration
```

**Configuration-driven deployment:**
- JSON-based account configuration
- Enable/disable modules per environment
- Customizable compliance rule sets
- Support for AWS Organizations

---

## 📊 Compliance Framework Coverage

### Automated Config Rules (40-60 checks)

**ISO 27001 Controls:**
- A.9 (Access Control): IAM password policy, MFA enforcement, access analyzer
- A.12 (Operations Security): CloudTrail logging, Config monitoring
- A.13 (Communications Security): VPC security groups, network ACLs
- A.14 (System Acquisition): Secure deployment practices

**SOC 2 Trust Services:**
- CC6.1: Logical and physical access controls
- CC6.6: Data access restrictions
- CC7.2: System monitoring and logging
- CC7.4: Security incident detection

**NIST 800-53 (Rev 5):**
- AC Family: Access Control (AC-2, AC-3, AC-6)
- AU Family: Audit and Accountability (AU-2, AU-3, AU-6, AU-9)
- CM Family: Configuration Management (CM-6, CM-8)
- IA Family: Identification and Authentication (IA-2, IA-5)
- SC Family: System and Communications Protection (SC-7, SC-12, SC-13)

**HIPAA Security Rule:**
- §164.308(a)(1)(ii)(D): Information system activity review
- §164.308(a)(5)(ii)(C): Log-in monitoring
- §164.312(a)(2)(i): Unique user identification
- §164.312(b): Audit controls

---

## 🔒 Customer-Tenant-First Architecture

All security controls and evidence remain in your AWS account:

**Evidence stays with you:**
- CloudTrail logs in your S3 buckets (encrypted, versioned)
- Config snapshots and evaluations in your account
- GuardDuty findings in your Security Hub
- CloudWatch logs under your control
- Complete data sovereignty

**FEDLIN deployment approach:**
- Infrastructure deployed via Terraform in your AWS account
- GitHub Actions with OIDC (no long-lived credentials stored)
- One-time setup, you maintain ongoing access
- Can be removed cleanly with standard Terraform destroy

**Benefits for regulated environments:**
- Satisfies data residency requirements
- Simplifies vendor risk assessments
- Supports SOC 2 / ISO 27001 / HIPAA / NIST evidence expectations
- No ongoing data processing agreements beyond initial deployment

---

## 🎯 Use Cases

### Healthcare SaaS SOC 2 Preparation

**Challenge:** First SOC 2 Type II audit, 8-week timeline, limited security team  
**Solution:** Deployed security baseline across 4 AWS accounts in 4 days  
**Outcome:** Passed audit with zero security findings, automated evidence collection

### MSP Multi-Tenant Standardization

**Challenge:** Inconsistent security posture across 15 client AWS accounts  
**Solution:** Standardized baseline with OIDC automation, per-customer evidence isolation  
**Outcome:** Deployment time reduced from 2 weeks to 1 day per customer

### Federal Subcontractor Engagement

**Challenge:** Prime contractor needed AWS hardening, customer must own all data  
**Solution:** Customer-tenant-first model deployed in AWS GovCloud  
**Outcome:** Clean subcontractor relationship, customer passed FedRAMP-equivalent assessment

---

## 💻 Infrastructure Efficiency

**Typical AWS costs:**
- Small accounts (< 50 resources): $30-80/month
- Medium accounts (50-500 resources): $80-200/month  
- Large accounts (500+ resources): $200-500/month
- Cost varies based on CloudTrail volume, Config rules, GuardDuty findings

**Deployment metrics:**
- Terraform resources: 80-120 (depends on modules enabled)
- Deployment time: 3-5 business days post-access
- Config rules: 40-60 automated checks
- Evidence retention: 7 years (configurable)
- Multi-region: All commercially available AWS regions

---

## 🤝 Engagement Models

**Direct Deployment**  
Complete security baseline setup in your AWS account with documentation and training.

**MSP Partnership**  
Standardized baseline deployment across your managed client accounts.

**Consulting Business Services**  
FEDLIN operates as an independent consulting firm, open to contract and C2C engagements for AWS security architecture and compliance automation projects.

---

## 📞 Get Started

**Primary Contact:** [info@fedlin.com](mailto:info@fedlin.com)  
**Book Consultation:** [Google Calendar](https://calendar.app.google/7z8eAZPvrW82jtxk6) or [Arrangr](https://arrangr.com/fedlin)  
**Demo:** Available upon request

### Related FEDLIN Services

- **[AWS VistaSec/CMC](https://github.com/fedlinllc/fedlin-aws-vistasec-cmc)** - Continuous monitoring for this baseline
- **[M365 Security Baseline](https://github.com/fedlinllc/fedlin-m365-security-baseline)** - Microsoft 365 hardening
- **[Google Workspace HIPAA](https://github.com/fedlinllc/fedlin-gws-hipaa-baseline)** - GWS compliance
- **[DMARC/SPF/DKIM](https://github.com/fedlinllc/fedlin-dmarc-spf-dkim)** - Email authentication

---

## 📋 Repository Note

This repository describes the AWS Security Baseline service and architecture approach. Deployment assets (Terraform modules, configuration templates, automation workflows) are provided as part of paid engagements.

**FEDLIN LLC**  
Security Solutions Architecture · Vulnerability Management · Compliance Automation  
Independent · Contract/C2C · Customer-tenant-first
