# FEDLIN — AWS Security Baseline

**Brand:** Security Architecture · Vulnerability Management · Compliance Automation  
**Delivery stance:** GitHub Actions (OIDC-only) · Evidence stays in the customer AWS account

This is Fedlin’s public service brief for establishing a **security baseline** in AWS — the step that usually comes **before** our `fedlin-aws-vistasec-cmc` monitoring service.

## What this service does
- Enables and standardizes AWS logging and configuration (CloudTrail, Config)
- Applies basic IAM/account hygiene checks
- Aligns the baseline to SOC 2 / ISO 27001 style controls
- Leaves evidence in **your** AWS account
- Shows how to re-run checks via GitHub Actions (OIDC-only)

## Who it’s for
- Teams starting in AWS that need a secure starting point
- MSPs onboarding customers into AWS
- Customers planning to adopt `fedlin-aws-vistasec-cmc` for ongoing monitoring

## What’s in this repo
- `SERVICE_SCOPE.md`
- `EVIDENCE_MODEL.md`
- `DELIVERY_MODEL.md`
- `.github/workflows/` (OIDC example)
- `SECURITY.md`

## What’s **not** in this repo
- Customer ARNs / account IDs
- Real AWS exports
- Full internal runbooks

---

Need this baseline applied?

📬 info@fedlin.com  
🌐 https://www.fedlin.com
