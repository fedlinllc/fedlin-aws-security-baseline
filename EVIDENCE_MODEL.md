# Evidence Model (Public-Safe)

| Area          | Evidence Source     | Lives in        | Notes                             |
|---------------|---------------------|-----------------|-----------------------------------|
| CloudTrail    | CloudTrail console  | Customer AWS     | Proves audit logging enabled      |
| AWS Config    | Config console      | Customer AWS     | Proves resource/config tracking   |
| IAM hygiene   | IAM settings export | Customer AWS     | Proves root/MFA/policy reviewed   |
| CI baseline   | GitHub Actions run  | Customer GitHub  | Proves OIDC-only delivery         |

> Fedlin does **not** store customer AWS exports in this public repo.
