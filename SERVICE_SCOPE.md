# Service Scope — AWS Security Baseline

## In scope
- CloudTrail: enable / verify multi-region logging
- AWS Config: enable recorder + required rules
- IAM hygiene: root account checks, MFA expectation, password policy
- Logging/evidence: S3 bucket in customer account
- Example GitHub Action (OIDC) to re-run baseline checks
- Handoff notes

## Out of scope
- GuardDuty / Security Hub tuning (covered by VistaSec CMC)
- Multi-account landing zone design
- 24/7 monitoring / MDR
- Non-OIDC CI/CD patterns
