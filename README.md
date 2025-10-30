# FEDLIN – AWS Security Baseline

**Security Solutions Architecture · Vulnerability Management · Compliance Automation**

A service-oriented baseline for securing an existing AWS tenant/account without taking ownership of the customer’s cloud. FEDLIN deploys and validates security controls, but all evidence, logs, and configuration stay in the customer’s AWS environment.

---

## Who this is for

- Security teams that need a repeatable AWS hardening baseline
- MSPs / MSSPs that want a customer-tenant-first delivery model
- Regulated or PHI-adjacent organizations mapping to SOC 2 / ISO 27001 / HIPAA
- Subcontract and C2C engagements that need clearly separated deployment assets

---

## What it delivers

- Core AWS security services enabled and standardized (e.g. GuardDuty, Security Hub, AWS Config, basic logging)
- Account/organization guardrails aligned to security best practices
- Optional monitoring hooks suitable for “VistaSec / CMC” style dashboards
- Evidence-oriented outputs so the customer can prove control operation
- GitHub Actions (OIDC-only) automation patterns for repeatable delivery

> **Public repo policy:** This repository describes the service and delivery pattern. It does **not** contain customer-specific values, account IDs, or Terraform state.

---

## Evidence model (customer-owned)

FEDLIN works on a **customer-tenant-first** basis:

1. Evidence (logs, exports, compliance artifacts) is generated **in the customer’s AWS**.
2. Evidence is stored **in the customer’s S3 / logging / security services**.
3. FEDLIN can push automation via GitHub Actions using **OIDC only** – no long-lived AWS keys.
4. When subcontracting, we maintain the same model so the prime keeps the customer data.

This supports SOC 2, ISO 27001, HIPAA-style “evidence stays with the processor/controller” expectations.

---

## Delivery method

- **Primary:** GitHub Actions with **OIDC-only** authentication into AWS
- **IaC options:** Terraform and/or policy-as-code definitions
- **Scripting:** bash / python for helper tasks
- **Engagement model:** Independent / C2C, subcontract-ready, MSP-friendly

CI/CD is designed so you can show the public org to recruiters without leaking secrets.

---

## Deployment assets

Deployment assets (Terraform/Bicep modules, per-tenant variables, policy bundles, workflow files, redacted runbooks) are kept in a **private FEDLIN deployment repository** and are provided only as part of an engagement.

This public repo tracks the service description, not the customer code.

---

## Related services

- FEDLIN – AWS VistaSec / CMC (`fedlin-aws-vistasec-cmc`)
- FEDLIN – Microsoft 365 Security Baseline (`fedlin-m365-security-baseline`)
- FEDLIN – Google Workspace HIPAA Baseline (`fedlin-gws-hipaa-baseline`)
- FEDLIN – DMARC / SPF / DKIM (`fedlin-dmarc-spf-dkim`)

---

## About FEDLIN

**FEDLIN** delivers:  
**Security Solutions Architecture · Vulnerability Management · Compliance Automation**

Independent / C2C · Subcontract-ready · Customer-tenant-first
