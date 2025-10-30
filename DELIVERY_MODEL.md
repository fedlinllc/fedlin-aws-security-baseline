# Delivery Model — AWS Security Baseline

1. **Access prep** — customer creates an AWS role that trusts GitHub OIDC.
2. **Baseline run** — Fedlin runs/guides baseline to enable logging, Config, and IAM hygiene.
3. **Evidence capture** — evidence is stored in the **customer** AWS account (e.g. S3).
4. **Handoff** — customer/MSP receives scope + evidence model.
5. **(Optional)** customer schedules periodic GitHub Action re-runs.

**Why OIDC?**
- No long-lived AWS credentials in CI
- Easy to rotate/revoke from AWS side
- Cleaner story for auditors
