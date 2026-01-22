# Secrets & Tokens

## Token Strategy

Omkraft uses **fine-grained Personal Access Tokens (PATs)**.

### Why
- GitHub does NOT allow `GITHUB_TOKEN` to create releases across reusable workflows
- Fine-grained tokens provide least-privilege access

---

## Token Ownership

- Resource owner: **Omkraft organization**
- Scope: All repositories (or explicitly selected)

---

## Required Permissions

| Permission | Access |
|----------|-------|
| Contents | Read & Write |
| Pull Requests | Read |
| Metadata | Read (required) |

❗ There is NO separate "Releases" permission  
Releases are covered under **Contents**

---

## Secret Storage

Token is stored as:
```sql
ORG_SECRET: RELEASE_TOKEN
```
Used **only in release** workflows.